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
> then **overwrite the top three sections in your own words** and answer the
> questions marked 🔸. Delete this callout when you do.

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

### Formats
`.cube` — plain text, most portable, the default choice. `.3dl`, `.look`, `.dat` — older
or vendor-specific. Camera **profiles** (DCP, ICC) sit earlier in the pipeline and do a
different job; an ICC profile describes a device, a LUT applies a transform.

## Where it sits in the pipeline

```
RAW → demosaic → WB → exposure → [technical LUT] → [creative LUT] → local work → output sharpening → export
```

Compare against [[Editing-Workflow]] and note what has to be settled *before* the
lookup. 🔸 **Why can't the creative LUT go first?** Answer it in your own words.

## How I set it in the field
<!-- Yours. What actually happens on your machine? -->
- **My tool:** ____________________
- **Do I shoot anything log?** ____________________ (if no, technical LUTs are not
  currently your problem — say so here and move on)
- **Loading a LUT in my editor:** ____________________
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

## Proof from my own frames
<!-- Don't write this from theory. Build a look on one frame, export it, apply it to
     five others from a different session, and log what broke. That is A4.5's problem
     in miniature. -->
- 

## Related
[[Tone-Curve]] · [[HSL-and-Colour-Mixer]] · [[Colour-Grading]] ·
[[Developing-a-Look]] · [[Colour-Spaces]] · [[Colour-Management]] ·
[[Non-Destructive-Editing]] · [[Export-Settings]]

## Source
- Claude draft, 2026-08-11 — **replace this line** with where you actually verified it
- 
