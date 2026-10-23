---
title: Tone Curve
type: concept
module: 4
tags:
  - post/tone
created: 2026-10-22
---
# Tone Curve

> [!summary] In one line
> A tone curve maps every input brightness to an output brightness. Bending it is the
> most precise way to set contrast, the black point, and how highlights fade to white.

## What it is

The curve is a graph. The horizontal axis is the brightness going in, from black on the
left to white on the right. The vertical axis is the brightness coming out. It starts
as a straight diagonal line: every tone comes out exactly as it went in.

Drag a point on the line up, and tones at that brightness come out brighter. Drag it
down, and they come out darker. Nearby tones move too, because the curve bends smoothly.

| Shape | What it does | Looks like |
|---|---|---|
| Straight diagonal | Nothing | The original |
| Gentle S | Darker shadows, brighter highlights | More contrast, more punch |
| Inverted S | Lighter shadows, darker highlights | Flatter and softer |
| Bottom-left end raised | Nothing is pure black any more | A faded, matte look |
| Top bending over gently | Highlights ease into white | A soft, "filmic" finish |

Mechanically, a tone curve is a 1D [[LUTs|LUT]]: a table with one output value for each
input value.

## How it works

### Slope is contrast

The steepness of the curve is what matters. Where the curve is steeper than the
diagonal, tones in that range are pulled further apart: more contrast. Where it is
flatter, they are squeezed together: less contrast.

A worked example on a 0–255 scale. Make an S-curve by pulling input 64 down to 50 and
pushing input 192 up to 205. The middle, 128, stays where it is:

| Range | Input span | Output span | Result |
|---|---|---|---|
| Shadows | 0–64 (64 levels) | 0–50 (50 levels) | Squeezed: less shadow detail |
| Midtones | 64–192 (128 levels) | 50–205 (155 levels) | About 20% more contrast |
| Highlights | 192–255 (63 levels) | 205–255 (50 levels) | Squeezed: less highlight detail |

The output still runs from 0 to 255, so contrast is a budget. An S-curve gives the
midtones more contrast by taking it from the shadows and highlights. You can't add
contrast everywhere at once.

### Black point, white point and the filmic shoulder

**Lifting the black point:** drag the bottom-left end up, say from 0 to 20. The darkest
tone in the photo is now a dark grey, so shadows look soft and faded, like an old print.
**Lowering the white point** does the same at the top: whites turn a dull grey.

**A filmic shoulder:** let the top of the curve bend over gradually instead of running
straight into white. Bright tones are squeezed gently, so highlights fade into white
smoothly instead of stopping hard at a clipped edge. The name comes from film, whose
response curve has a soft "toe" at the bottom and a "shoulder" at the top.

### Per-channel curves

Most editors also offer a separate curve for red, green and blue. Each one moves a
colour against its opposite:

| Curve | Pull it up | Pull it down |
|---|---|---|
| Red | More red | More cyan |
| Green | More green | More magenta |
| Blue | More blue | More yellow |

You also choose which tones to change. Lift the blue curve in the shadows and lower it
in the highlights, and you get cool shadows with warm highlights: a split tone, built
from one curve. → [[Colour-Grading]]

### Point and parametric curves

- **Point curve:** you place points anywhere and drag them. Precise, but too many
  points make bumps.
- **Parametric curve:** sliders for regions of the tonal range (Lightroom's are
  Highlights, Lights, Darks and Shadows). Less precise, but always smooth.

### What a curve can't do

A curve treats every pixel of the same brightness the same way, wherever it is in the
frame. It doesn't know sky from skin. That is what makes it a 1D LUT, and it's how it
differs from the area-aware Highlights and Shadows sliders. → [[Basic-Panel-Order]]

A curve also can't change one colour on its own. To darken only the blues, you need the
[[HSL-and-Colour-Mixer|colour mixer]] or a 3D LUT.

A strong curve on the combined RGB channel also makes colours stronger, because it
pushes the three channels apart. Some editors, such as Capture One, offer a Luma curve
that changes brightness and leaves saturation alone.

## How to use it

1. **Do the basic sliders first,** then refine with the curve.
2. **Find the tone.** Many editors let you click a spot in the photo and drag up or
   down to move that part of the curve. It shows you where a face or a sky sits.
3. **Use two to four points,** and move them a little. On a 0–255 scale, 5–10 levels is
   often enough.
4. **Keep the curve rising from left to right.** Where it slopes down, brighter tones
   come out darker than darker ones, and the tones flip. This is called solarisation.
5. **Save curves you like as presets.** A curve is a big part of a consistent look.
   → [[Developing-a-Look]]

In black and white, the curve does most of the work: it sets how deep the blacks are
and how the greys step up to white. → [[Black-and-White-Conversion]]

## On your kit

- **Raw files take strong curves; JPEG and HEIC files don't.** A steep curve stretches
  tones apart. JPEG has only 256 levels per channel, and HEIC files are often 8-bit too,
  so a stretched sky can break into visible bands. The L10's RW2 and the DNGs from your
  other devices have far more levels. → [[Bit-Depth]]
- **Log files look flat because their curve is low-contrast on purpose.** For an L10
  V-Log file or a D-Log M frame, apply the technical LUT first, not a hand-drawn S-curve.

## Common mistakes

- **A strong S-curve on every photo.** Shadow and highlight detail disappear, because
  you spent the whole contrast budget on the middle. Keep it gentle.
- **Too many points.** Bumps make uneven tones and odd colour. Use two to four.
- **Wondering why the colours got louder.** An RGB curve adds saturation along with
  contrast. Lower saturation slightly, or use a luminance curve if your editor has one.
- **Lifting the black point to fix dark shadows.** A faded black is a style, not a fix.
  To see into shadows, use the Shadows slider and keep a true black.
- **Ignoring banding on JPEGs.** Zoom into skies after a strong curve.

## Try it

Twenty minutes, a small version of **A4.1**. Make three virtual copies of one raw. Give
the first a gentle S-curve, the second a lifted black point and a soft shoulder, and
the third cool shadows and warm highlights with the blue curve. Put all three side by
side and write one line on what each does to the mood.

## Check yourself

> [!question]- What does a part of the curve that is steeper than the diagonal do?
> It pulls the tones in that range apart, so that range gains contrast. A flatter part
> squeezes them together, and that range loses contrast.

> [!question]- Why does an S-curve make shadow detail harder to see?
> The curve must stay between 0 and 255. To be steeper in the middle, it has to be
> flatter at the ends, so the shadow tones are squeezed closer together.

> [!question]- You lower the blue curve in the highlights. What colour do they turn, and why?
> Yellow. Each channel moves against its opposite, and yellow is the opposite of blue.

> [!question]- Why is a tone curve called a 1D LUT, and what can't it do that a 3D LUT can?
> It gives one output value for each input value, per channel: a one-dimensional table.
> It can't change one hue on its own, such as darkening only the blues, because each
> channel never sees the other two.

> [!question]- You drag the curve point at input 200 below the point at input 180. What happens?
> The curve now slopes downwards there, so brighter tones come out darker than slightly
> darker ones. The tones flip, and that part of the photo looks strange and posterised.

## Related
[[Basic-Panel-Order]] · [[Histogram]] · [[LUTs]] · [[Bit-Depth]] · [[Colour-Grading]] ·
[[Black-and-White-Conversion]] · [[Developing-a-Look]] · [[Post-Processing-Index]]
