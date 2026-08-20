---
title: LUTs
type: concept
module: 4
status: drafted
confidence: 1
tags:
  - post/colour
created: 2026-08-11
---
# LUTs (Look-Up Tables)

> [!warning] Claude drafted this — it is not yours yet
> `confidence: 1` is deliberate: this is someone else's wording, so it counts for
> nothing until you rewrite it. Use it as reference while you learn the mechanism,
> then **rewrite every section above "How I set it in the field" in your own words**
> and answer the questions marked 🔸. Delete this callout when you do.

## In one sentence
A stored table that maps every input colour to an output colour, so an arbitrary
colour transform can be replayed identically anywhere without re-deriving it.

## What it actually does

A LUT is not a filter or an effect. It is a **precomputed answer key**. Instead of
running maths on each pixel, the software looks the pixel's value up in a table and
substitutes what it finds.

**1D LUT** — three independent tables, one per channel: `R_in → R_out`, `G_in → G_out`,
`B_in → B_out`. This is exactly a [[Tone-Curve]]. Because each channel only ever sees
its own value, a 1D LUT can change brightness and contrast, and can tint by pushing
channels apart — but it can never say "make *this* hue warmer and leave the rest
alone". The output for red doesn't know what green and blue were doing.

**3D LUT** — one table indexed by all three channels at once. Picture RGB space as a
cube, with black at one corner and white at the opposite one. The LUT samples that cube
on a lattice — commonly 17×17×17, 33×33×33, or 65×65×65 nodes — and stores an arbitrary
output triplet at each node. Input values that fall between nodes get **interpolated**
(trilinear, or the more accurate tetrahedral).

That single structural difference is the whole point:

- Because every node is independent, a 3D LUT can rotate one hue, desaturate only deep
  shadows, or split-tone highlights and shadows in opposite directions — cross-channel
  moves a curve cannot express.
- Because it's just a table, the transform is **deterministic and portable**. A `.cube`
  file produces the same result in Resolve, Premiere, Photoshop, or a camera's monitor
  output. Nobody has to reimplement your edit.
- Because it's a lookup, cost is fixed regardless of how complicated the grade was.
  This is why video lives on LUTs: a 90-second clip is ~2,700 frames, and you cannot
  re-run a 40-step slider stack on each one in real time.

### The two kinds are not interchangeable
| | Technical / transform LUT | Creative / look LUT |
|---|---|---|
| Job | Undo a log encoding or move between colour spaces (`S-Log3 → Rec.709`) | Impose an aesthetic |
| Correct answer? | Yes — use the manufacturer's | No, it's taste |
| Get it wrong | Image is objectively broken | Image is just not to your taste |

**Order matters and is the most common mistake.** Technical first, creative second. A
look LUT authored for Rec.709 footage, dropped onto raw log footage, produces a washed
grey mess — not because the LUT is bad but because it was handed input it was never
built to receive. → [[Colour-Spaces]]

## The trade-off

A LUT is **stateless and global**. It sees one pixel's input value and nothing else —
not where the pixel sits, not what surrounds it, not whether it's skin or sky. That
single limitation generates every practical constraint:

| A LUT can | A LUT cannot |
|---|---|
| Remap any colour to any other colour | Know *where* a pixel is → no masks, no local work |
| Reshape tonality globally | Do local contrast, sharpening, or noise reduction |
| Travel between applications unchanged | Be re-opened and adjusted — the maths is baked |
| Apply at fixed cost | Recover values that were already clipped |

Consequences worth remembering:

- **Apply late.** Exposure and [[White-Balance]] come *first*. The LUT can only respond
  to the values it's given, so a cast fed into a LUT comes out amplified, not fixed.
  Anything already pushed past white is gone before the lookup happens.
- **Coarse lattice + big move = banding.** A 17³ LUT asked to do something violent will
  show stepping in smooth gradients like skies. 33³ or 65³ with tetrahedral
  interpolation is the fix.
- **Opacity is a blunt instrument.** Dialling a LUT to 50% blends toward the original;
  it is not "half the look" in any perceptual sense, and it dilutes the technical part
  along with the creative part if they were baked together.
- **In stills, a preset usually beats a LUT.** A preset is a set of *parameters* you can
  reopen and argue with; a LUT is an endpoint. Prefer presets in a raw developer and
  keep LUTs for interchange, video, or a look you have genuinely finished designing.
  → [[Non-Destructive-Editing]] · [[Developing-a-Look]]

### Formats, and what is actually in the file
`.cube` (Adobe/Resolve) — plain text, most portable, the default choice. `.3dl`
(Lustre/Flame), `.look` (Sony), `.csp`, `.dat` — older or vendor-specific; convert to
`.cube` and stop thinking about them.

A `.cube` is small enough to open in a text editor, and doing that once removes most of
the mystery:

```
TITLE "Warm Fade"
LUT_3D_SIZE 33
DOMAIN_MIN 0.0 0.0 0.0
DOMAIN_MAX 1.0 1.0 1.0
0.000000 0.000000 0.000000
0.031250 0.000000 0.000000
...
```

- `LUT_3D_SIZE 33` means the lattice is 33×33×33, so 35,937 lines follow, each one an
  output RGB triplet. **No input values are stored** — position in the file *is* the
  input. Red varies fastest, then green, then blue.
- `DOMAIN_MIN`/`DOMAIN_MAX` declare the input range the table covers, normally 0–1.
  Values outside it are clamped *before* the lookup, which is how a 0–1 LUT quietly
  destroys the negative and super-white values that log and HDR material carries.
- **Nothing in the file says what colour space it expects.** The format cannot warn you
  that you fed it the wrong input. That absence is the entire reason naming discipline
  (`SLog3_to_Rec709_v2.cube`) does real work.

A 1D LUT in the same format is `LUT_1D_SIZE` plus one triplet per input level — a curve,
written down.

**Profiles are a different animal.** An ICC profile *describes a device* so a colour
manager can compute a conversion; a camera profile (DCP, or a raw developer's creative
profiles) sits at demosaic time and interprets sensor data. Both contain lookup tables
internally — a DCP's `HueSatMap` is a 3D table in HSV — but they are declared inputs to
a colour-managed pipeline, not a transform dropped on top. → [[Colour-Management]]

## Under the hood: interpolation, shapers, precision

**Trilinear vs tetrahedral.** Between nodes the software has to guess. Trilinear blends
the eight corners of the surrounding cube; tetrahedral splits that cube into six
tetrahedra and blends only the four corners of the one the pixel lands in. Tetrahedral
is both cheaper and more accurate along the neutral axis — grey runs corner-to-corner
through the cube as a straight diagonal, and tetrahedral keeps points on it while
trilinear drifts off it and tints your greys. Choose tetrahedral wherever it is offered.

**Lattice size is not the whole story.** 33³ is 35,937 nodes and 65³ is 274,625 — eight
times the file for one doubling per axis. But nodes are spaced evenly in *code value*,
not in perceived colour, so the lattice is only dense where the encoding is dense. This
is why a 3D LUT applied to **linear** data misbehaves: linear light spends nearly all
its code values on highlights, leaving the shadows — where the eye is most sensitive — a
handful of nodes to work with.

**Shaper LUTs.** A shaper is a 1D LUT applied *before* the 3D lookup that bends the data
into a roughly perceptual (log-ish) encoding so the lattice samples somewhere useful,
with its inverse applied afterwards if needed. A "shaper + 3D LUT" pair is not two
looks; it is one look plus the thing that makes the table spend its nodes usefully.

**Stacking multiplies error.** Every lookup is an approximation between nodes. Chain
three LUTs and you interpolate an interpolation of an interpolation, and rounding and
banding compound. Build the chain as live nodes or layers, then **bake once** to one
high-resolution LUT for delivery.

**Bit depth sits upstream of all of it.** A LUT that stretches contrast pulls the input
levels apart; if the input only had 256 levels per channel to start with (8-bit JPEG),
the gaps show as posterisation and no lattice size repairs it. Apply LUTs to 16-bit or
float data and quantise to 8-bit last. → [[Bit-Depth]]

**Most LUTs cannot be inverted.** If a table maps two different inputs to the same
output — which anything that clips or crushes does — no inverse exists in that region.
Manufacturer "inverse" LUTs work only across the range where the forward transform is
one-to-one.

## Where it sits in the pipeline

```
RAW → demosaic → WB → exposure → [technical LUT] → [creative LUT] → local work → output sharpening → export
```

Compare against [[Editing-Workflow]] and note what has to be settled *before* the
lookup. 🔸 **Why can't the creative LUT go first?** Answer it in your own words.

## Viewing LUT vs baked LUT

One file, two completely different uses:

- **Viewing (monitor) LUT** — applied to the *display path only*. The recording stays
  log; you simply stop staring at a flat grey image while you shoot or edit. On set it
  is how everyone sees the intent; in an editor it is a viewer or timeline LUT.
- **Baked LUT** — applied to the image data and rendered into the export. Permanent.

Confusing the two produces the two classic failures: grading against a viewing LUT and
then exporting without it (delivered flat and grey), or exporting *with* it after it was
already applied to the clip (crushed and oversaturated). Before delivery, check which of
the two your export path is actually doing.

A third case that should never travel with a file: the **calibration LUT** loaded into
the GPU or the display itself to correct that one panel to a standard. It describes your
monitor, not your picture.

## Making one

Two honest routes:

1. **Bake your own grade.** Build the look as a node graph or adjustment stack, then
   export it (Resolve: right-click the node → Generate LUT; most grading tools have an
   equivalent). Only the *global* part survives — masks, tracking, spatial operations
   and anything that depends on where a pixel is cannot be written into a table. When a
   baked LUT looks unlike the grade it came from, that is almost always why.
2. **Match a reference.** Photograph a colour chart under controlled light, process one
   copy to the target rendering, then solve for the transform between the two sets of
   patches. This is how camera-matching LUTs get made when two bodies have to cut
   together.

## Testing a LUT you were handed

A minute of this tells you more than any vendor preview:

1. Apply it to a **greyscale ramp**. Banding, crushed blacks and clipped whites are
   obvious here and invisible on a busy photograph.
2. Apply it to a **colour chart or hue sweep**. Watch where hues twist and where
   saturation runs out — that is the LUT's actual personality, as opposed to its name.
3. Apply it to a **frame with skin in it**. Skin is the least forgiving subject and the
   first place a look designed for something else gives itself away.
4. Read the **filename and any documentation** for the input space it expects. If nobody
   says, assume Rec.709 and confirm with step 1.

🔸 Run this on one LUT you own, and write here what it does that its name doesn't say.

## What kind of image can take a LUT

| Input | Can it take a LUT? | What to watch |
|---|---|---|
| **Raw — DNG, ProRAW, CR3…** | Not directly. A raw file has no RGB triplets until it's demosaiced, so there is nothing to look up. The LUT applies *after* the developer, or is wrapped as a profile *inside* it | WB and exposure decide the numbers the LUT will be handed. Settle them first |
| **16-bit TIFF / PSD** | Yes — the safe target for stills | Enough levels to survive a stretch. This is the case with no gotcha |
| **8-bit JPEG / HEIC** | Yes, and it's where most people actually do it | 256 levels per channel. A heavy LUT posterises skies and gradients — keep the move gentle |
| **Log video (D-Log M, Apple Log)** | Yes, and here it isn't optional — the technical LUT is the required first step | The LUT must match the exact log curve *and* the camera |
| **HLG / HDR stills and video** | Only with an HDR-aware LUT | An SDR Rec.709 LUT clamps everything above 1.0 — which is the entire point of the format |
| **An already-graded delivery file** | Don't | You'd be stacking a look on a look, on values that were already clipped |

The pattern: **log is the only case where a LUT is compulsory.** Everywhere else it is a
preference, and usually a preference a preset expresses better.

## My kit, and what it means for LUTs

Full specifications live in [[My-Kit]] — keep the numbers there, not here. This table is
only the LUT-relevant slice of it.

| Device | Stills | Log stills? | Video | Technical LUT |
|---|---|---|---|---|
| **iPhone 15 Pro Max** | HEIC/JPEG, or Apple ProRAW (DNG) | No | Apple Log (in ProRes), HDR/HLG by default | Apple publishes a Log → Rec.709 LUT. Video only |
| **DJI Osmo Action 5 Pro** | JPEG, or raw DNG | No | D-Log M (10-bit), HLG, Normal | DJI publishes a D-Log M → Rec.709 LUT. Video only |
| **DJI Pocket 3** | JPEG, or raw DNG | No | D-Log M (10-bit), HLG, Normal | Same DJI D-Log M LUT family |
| **Camera #4 (planned)** | ____________ | ____________ | ____________ | ____________ |

> [!important] The honest conclusion for this kit
> **Not one of these three shoots log stills** — no phone or compact does. Technical
> LUTs are therefore a *video* problem for you and not a photography one. For a
> photograph, a LUT can only ever be a creative look, and a preset in your raw developer
> beats it, because a preset can be reopened and argued with. → [[Developing-a-Look]]

When camera #4 arrives, three questions answer the whole row above: **does it record a
log curve, and which one exactly? does the maker publish a matching LUT? what raw format
and bit depth?** Nothing about LUTs should influence which one you buy.

### Four traps specific to this kit
- **`D-Log M` is not `D-Log`.** Different curves; DJI ships LUTs for both. The wrong one
  gives you wrong contrast and a colour cast, and it looks *plausible*, which is worse.
- **Photographic Styles on the iPhone bake at capture.** A style is a look applied
  *before* you ever see the file — the "apply late" rule broken by the phone itself, and
  on the 15 Pro it is not cleanly reversible afterwards. Shoot Standard, or ProRAW, if
  you intend to grade.
- **ProRAW is not a neutral raw.** Apple's tone mapping and Smart HDR are already
  described inside the DNG. Put a look LUT on top and you have a look on a look.
- **iPhone HDR stills carry a gain map.** An SDR LUT grades the base image while the
  gain map still describes the ungraded one, so it reads wrong in any HDR-aware viewer.
  Convert to SDR deliberately before grading, or keep the whole chain HDR.

## Applying a LUT to a photograph

**Route A — develop first, LUT after (use this one)**
1. Develop the DNG/ProRAW: white balance → exposure → highlights and shadows. No look
   yet. The LUT can only respond to what you hand it.
2. Export **16-bit TIFF**, ProPhoto or Adobe RGB. Not JPEG — not yet.
3. Apply the LUT. Photoshop: Layer → New Adjustment Layer → **Color Lookup** → Load 3D
   LUT. Affinity Photo: Adjustment → **LUT**. darktable: the **lut 3D** module. DaVinci
   Resolve grades stills too, is free, and is where your DJI footage will end up anyway.
4. Then local work, then output sharpening, then export 8-bit for delivery.

**Route B — LUT as a profile inside the raw developer**
Lightroom/ACR can carry a `.cube` as a *creative profile*, which applies inside the raw
pipeline with an amount slider and never leaves high bit depth. The `.cube` has to be
wrapped into an `.xmp` profile first — confirm the current method for your version
before trusting any tutorial, then write the steps here: ____________________

**On the phone.** LumaFusion and DJI's Mimo app accept `.cube` for *video*. For stills,
check whether your mobile editor imports `.cube` at all before planning around it — most
don't, and the ones that do often only take them at low resolution. ____________________

🔸 Your Pocket 3 and your iPhone film the same scene, each in its own log, and you apply
each maker's own Rec.709 LUT. The two clips still don't match. Why not — what does a
technical LUT normalise, and what does it leave untouched?

## How I set it in the field
<!-- Yours. What actually happens on your machine? -->
- **My raw developer:** ____________________
- **Where my LUT files live:** ____________________
- **Do I shoot anything log?** Video yes — D-Log M on both DJI bodies, Apple Log on the
  iPhone. Stills no. So: ____________________
- **LUT downloads I've actually verified:** DJI ____________ · Apple ____________
- **Where in my stack it goes:** ____________________

## What I got wrong
<!-- Replace with what YOU actually believed. Delete any of these you never thought. -->
- 🔸 Did you think a LUT and a preset were the same thing? What's the difference, in one
  sentence?
- 🔸 A "Kodak Portra" LUT cannot make a digital file into Portra. Name two things film
  does that a table of RGB values structurally cannot reproduce.
- 🔸 If a 3D LUT can remap any colour to any other colour, why does the order of
  operations still matter at all? (This is the question that tests whether you actually
  understood the section above.)
- 🔸 You export a LUT from a grade you liked and it comes back looking different.
  Give two reasons that are the LUT's fault and one that isn't.
- 🔸 Why does a 3D LUT waste most of its nodes when it is fed linear-light data?
- 🔸 Someone sends you `Teal_Orange.cube` with no documentation. What do you check
  first, and what are you actually looking for?

## Proof from my own frames
<!-- Don't write this from theory. Build a look on one frame, export it, apply it to
     five others from a different session, and log what broke. That is A4.5's problem
     in miniature. -->
- 

## Related
[[Tone-Curve]] · [[HSL-and-Colour-Mixer]] · [[Colour-Grading]] ·
[[Developing-a-Look]] · [[Colour-Spaces]] · [[Colour-Management]] ·
[[Non-Destructive-Editing]] · [[Export-Settings]] · [[Bit-Depth]] ·
[[Dynamic-Range]]

## Source
- Claude draft, 2026-08-11, expanded 2026-08-18 — **replace this line** with where you
  actually verified it
- 
