---
title: Dynamic Range
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Dynamic Range

> [!summary] In one line
> Dynamic range is the span from the darkest to the brightest tones, measured in stops.
> When a scene's range is wider than the camera's, you must choose what to lose, or
> find a way to fit it all in.

## What it is

There are two dynamic ranges, and much of exposure is the gap between them:

- **Scene dynamic range:** how much brighter the brightest part you care about is than
  the darkest part you care about.
- **Camera dynamic range:** how much brighter the brightest tone the sensor can record
  (just before it clips) is than the darkest one it can still separate from noise.

Both are measured in [[Stops-and-EV|stops]]. Ten stops means the brightest part is
2¹⁰, or about 1,000 times, brighter than the darkest. Your eyes adjust as you look
around, so you see detail in a bright sky *and* in deep shade. One exposure can't do
that.

## How it works

### Highlights clip suddenly; shadows fade slowly

Think of each pixel as a bucket collecting light. When the bucket is full, extra light
spills over and is lost. Every brighter tone records as the same pure white. That's
why highlight clipping is sudden and final.

At the dark end there is no wall. Fewer photons arrive, so their random variation
([[ISO|shot noise]]) gets larger compared with the signal, and the electronics' own
read noise starts to show. Shadows don't stop. They get noisier and noisier until the
detail drowns.

### Highlight and shadow latitude

**Latitude** is how far you can miss the exposure and still rescue the file in
editing.

| | Highlights | Shadows |
|---|---|---|
| How much latitude | Little: often a third of a stop to a stop past the camera's warning | A lot: several stops, at the cost of noise |
| What happens past it | Flat white, odd colours, no detail | Noise, then blotchy colour |
| What helps | Less exposure | More light, at base ISO |

The space is lopsided. A camera's meter places middle grey only about 3 stops below the
point where a typical sensor clips. Below middle grey there is far more room: at base
ISO, often 7 stops or more before noise takes over. That's why you protect highlights
first.

### Typical ranges

Rough figures, in stops. Real scenes and cameras vary.

| Scene or file | About |
|---|---|
| Overcast day, flat light | 5–8 |
| Sun and shade in the same frame | 10–14 |
| A room with a sunny window, or a sunset with the sun in frame | 15 or more |
| A modern camera's raw file at base ISO | 10–14, usually more for larger sensors |
| A JPEG from the same camera | 8–10 |

Dynamic range is largest at base ISO. Each stop of ISO above it costs up to about a
stop of range, because the highlights clip with less light while the noise floor (the
level where noise swamps detail) drops much less.

## How to use it

**Measure the gap.** With spot metering, read the brightest area that must keep detail,
then the darkest. Count the stops between the two readings. Up to about 5 stops fits
easily, even in a JPEG. Up to about 8–9 can work in raw if you protect the highlights
and lift the shadows later. Beyond that, something has to give. These numbers are
smaller than the table's because a file keeps clean detail only well inside its full
range; the last stops at each end are noise or near-white.

When the scene is too wide, you have five options:

1. **Expose for the highlights.** Keep the important bright areas just short of
   clipping, then lift the shadows in editing. This works best in raw at base ISO.
2. **Add fill light.** Lift the shadows so the range shrinks: a reflector, a white
   wall, a flash, or move your subject into open shade. → [[Light-Modifiers]]
3. **Bracket and merge.** Shoot the same frame at, say, −2, 0 and +2 EV, ideally on a
   support, then merge them into one HDR (high dynamic range) file. → [[Photo-Merges]]
4. **Use a graduated ND filter**, which is dark at the top and clear at the bottom. It
   darkens the sky and leaves the ground alone, and suits straight horizons.
   → [[Lens-Filters]]
5. **Accept clipping.** Let a sky go white for a bright, airy look, or let a subject go
   black for a silhouette. Choose it on purpose.

Or change the light. In Singapore the harshest, widest-range light runs from late
morning to mid-afternoon. Early morning, late afternoon or cloud shrinks the range for
free.

### Phones and log video

Phones stretch their range by **merging frames**: they capture several exposures and
blend them automatically. That's how a phone holds a bright sky and a shaded face that
would defeat a single frame. → [[Computational-Photography]]

In video, a **log profile** records a flat, grey-looking image that keeps more of the
sensor's range in the file, ready for grading. Log doesn't widen the sensor's range. It
stops the file throwing range away. → [[Log-Profiles]]

## On your kit

- **Lumix L10:** the largest sensor you own, so one raw frame holds the most range.
  Shoot RW2 at base ISO when the range is wide, and protect the highlights. It records
  V-Log video, and V-Log stills too, but for stills a raw file already keeps everything
  the sensor saw.
- **iPhone 15 Pro Max:** Apple's multi-frame processing shapes every file, ProRAW
  included, which is why it copes so well with high contrast. Its video is HDR (Dolby
  Vision) by default; Apple Log needs ProRes.
- **Pocket 3 and Action 5 Pro:** both record 10-bit D-Log M video. Their sensors are
  smaller than the L10's, so in stills, protect the highlights carefully.

## Common mistakes

- **Exposing for the shadows in a high-contrast scene.** The sky clips and can't come
  back. Expose for the highlights and lift the shadows later.
- **Lifting shadows in a high-ISO file.** Range is smallest at high ISO. Use the lowest
  ISO the shutter speed allows.
- **Bracketing a moving scene.** People and leaves move between frames and leave
  ghosts. Use one raw frame, or the phone's built-in merging.
- **Thinking log adds range.** It only keeps what the sensor captured, and it needs
  grading to look normal.
- **Fighting every bright sky.** Sometimes a white sky is the honest choice. Decide what
  matters and let the rest go.

## Try it

Twenty minutes around midday, on the L10 in raw, with the camera braced:

1. Stand in the shade of an HDB void deck, looking out at a sunlit street.
2. Spot meter the brightest area that should keep detail, then the darkest. Count the
   stops between them.
3. Shoot at −2, 0 and +2 EV.
4. In editing, try to rescue the shadows of the −2 frame and the highlights of the +2
   frame. Which recovers better?

This pairs with **A1.4**, which you shoot the same week, and previews **A4.2**.

## Check yourself

> [!question]- Why does a clipped sky look flat white, while a dark shadow still has some detail?
> A full pixel can't record more, so all the brighter tones become the same white.
> Shadow pixels still hold some light. Lifting them brings back detail, with noise.

> [!question]- Bright sky, friend in shade, about 12 stops apart. Name three ways to handle it.
> Add fill light with a reflector or flash; bracket and merge; or expose for the sky
> and lift your friend in editing, accepting noise, because 12 stops is past what one
> raw file holds cleanly. Or accept a silhouette, or a white sky, on purpose.

> [!question]- Why does dynamic range shrink as ISO rises?
> Gain makes the file clip with less light, so highlight room shrinks. The noise floor
> doesn't drop by as much, so the span between them gets shorter.

> [!question]- Does a log profile give your camera more dynamic range?
> No. The sensor's range is fixed. Log keeps more of it in the file instead of
> clipping it with a contrasty curve, and then it needs grading.

> [!question]- How can your iPhone hold a bright sunset and a face in one shot?
> It merges several frames at different exposures: darker ones for the sky, brighter
> ones for the face.

## Related
[[Histogram]] · [[Expose-to-the-Right]] · [[ISO]] · [[Photo-Merges]] ·
[[Lens-Filters]] · [[Computational-Photography]] · [[Log-Profiles]] ·
[[Fundamentals-Index]]
