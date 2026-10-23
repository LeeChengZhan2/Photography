---
title: Local Adjustments
type: concept
module: 4
tags:
  - post/local
created: 2026-10-22
---
# Local Adjustments

> [!summary] In one line
> A local adjustment changes only part of the photo: a mask says where, and the sliders
> say what. Use them after the global edit is right, to guide the eye.

## What it is

Global sliders change every pixel. A local adjustment changes only the pixels inside a
**mask**: a greyscale map laid over the photo. White means the full effect, black means
none, and grey means part of the effect.

| Mask | How you make it | Good for |
|---|---|---|
| **Brush** | Paint it on | Odd shapes: a face, a doorway |
| **Linear gradient** | Drag a line; the effect fades from full to none | Skies and foregrounds, like a graduated filter |
| **Radial** | Draw an ellipse; affect the inside or the outside | Lifting a subject; a custom vignette |
| **Colour range** | Click a colour, then set how close a match counts | All the blue sky showing through branches |
| **Luminance range** | Choose a band of brightness | Only the highlights, or only the shadows |
| **AI subject, sky or person** | The software finds it for you | Quick selections of people, skies and backgrounds |

Masks can be combined. Add one to another, subtract one from another, or keep only the
part where two overlap: for example, a sky mask minus a tall building.

Lightroom groups all of these under Masking, and Capture One builds them as layers. The
ideas are the same everywhere.

## How it works

### A blend, controlled by the mask

Think of a local adjustment as two versions of the photo: the one you have, and one with
the new slider settings applied everywhere. The mask decides how much of each you see at
every pixel. Where it's white you see the new version, where it's black the old one,
and at 50% grey an even mix.

### Feathering

Feathering is the width of a mask's soft edge: the strip where the effect fades from
full to nothing. A hard edge looks cut out and pasted on. A very soft edge spills past
the subject, so a brightened face makes the wall behind it glow too. A gradient is just
a very wide feather.

### Range masks follow the picture

Colour and luminance ranges select by pixel values, not by where you paint. So they
follow complicated edges for free: every patch of sky between the leaves, every
highlight on a wet road. How strict you make the match sets how soft their edges are.

Tutorials, especially for Photoshop, often use the term **luminosity mask**. It means a
mask built from the photo's own brightness: the brighter a pixel, the more of the
effect it gets (or the darker, for a "darks" mask). It's the same idea as a luminance
range mask. In a layer editor you build it from the image itself; in a raw editor the
luminance range tool makes it for you.

### AI masks are a guess

An AI mask uses a trained model to guess which pixels are "sky" or "person". It's fast
and often very good. But it can miss fine hair, thin branches, glass and anything the
model didn't expect, so check its edges at 100% zoom.

### Why halos appear

A halo is a band of wrong brightness along an edge. It appears when the mask edge
doesn't match the real edge, so the strip between them gets the wrong amount of the
effect. Darken a sky strongly with a soft mask, and the edges of the trees turn into
bright outlines. The stronger the move, the more any mismatch shows.

### Global first, local second

A local adjustment is a correction on top of the global edit. If you change the global
sliders later, the base under every mask moves, and the local moves are no longer
right. → [[Basic-Panel-Order]]

## How to use it

### Typical local edits

| Problem | Mask | Move |
|---|---|---|
| Sky too bright | Linear gradient or AI sky | Exposure −0.3 to −1, Highlights down |
| Face too dark | AI person or brush | Exposure +0.2 to +0.5, Shadows up |
| Busy background | AI subject, inverted | Exposure −0.3; Texture, Clarity and Saturation down a little |
| The eye doesn't land on the subject | Radial around the subject, inverted | Exposure −0.2 to −0.5 outside it |
| Flat foreground | Linear gradient from the bottom | Texture or Clarity up a little |

The numbers are only a starting point. Small moves of about a third of a stop add up.
Viewers rarely notice them as edits, but they change where the eye goes. Brightening and
darkening areas on purpose is a skill of its own. → [[Dodge-and-Burn]]

### Habits that keep masks honest

- **Show the mask overlay** to see exactly what is covered.
- **Toggle the adjustment on and off** to judge the effect, not your memory of it.
- **Zoom to 100% on the edges** before you move on.
- **Name your masks** ("sky −0.5", "face +0.3"), so you can find and copy them later.
- **For a set,** AI masks can usually be copied to similar frames and recalculated for
  each one. That helps in A4.5.

## On your kit

- **The iPhone has already done some local work.** Apple's tone mapping lifts shadows
  and holds back skies before you start, and ProRAW carries it too. You may need fewer
  local moves, or moves that put some contrast back.
- **Small sensors show noise sooner.** Brighten a dark area by a stop and its noise
  rises with it. Files from the Action 5 Pro's 1/1.3-inch sensor show this before the
  L10's Four Thirds files do. → [[Noise-Reduction]]

## Common mistakes

- **Going local before global.** Every later global change knocks the masks off. Finish
  the global edit first.
- **Strong moves on soft masks.** You get halos and glowing edges. Make smaller moves,
  or tighten the mask.
- **Trusting an AI mask without checking.** Check hair, branches and glass at 100%.
- **A dozen masks on one photo.** If a frame needs that many, the light or the framing
  was the real problem. Note it in the shoot log.
- **A sky darker than the ground in daylight.** In daylight the sky is usually brighter
  than the land. Reverse that, and the edit shows.

## Try it

Twenty minutes, a warm-up for **A4.4**. On one finished frame, use three masks at most:
a gradient on the sky, an AI mask on the subject, and an inverted radial that darkens
the edges a little. Keep every move to 0.5 stop or less. Compare before and after, and
write down where your eye lands first in each.

## Check yourself

> [!question]- What does grey mean in a mask?
> Part of the effect. White gets the full adjustment, black gets none, and 50% grey gets
> half.

> [!question]- You darken the sky with a linear gradient, and the tops of the buildings go dark too. Why, and how do you fix it?
> A gradient knows nothing about what's in the photo; it darkens everything in its path.
> Subtract the buildings from the mask, or use an AI sky or a luminance range mask.

> [!question]- Why finish the global edit before the local ones?
> A local move is a correction on top of the global result. Change the global sliders
> later and every masked area shifts with them, so the local moves are no longer right.

> [!question]- You brighten a dark face by 1.5 stops with a mask, and it looks grainy. Why?
> The face got little light, so its signal was weak and its noise strong. Brightening it
> raises the noise along with the face. Make a smaller move, add noise reduction, or
> give the face more light next time.

> [!question]- When is a colour range mask better than a brush?
> When the area has a complicated edge but one colour, such as sky through branches. The
> range follows the colour into every gap, which no brush can do quickly.

## Related
[[Basic-Panel-Order]] · [[Dodge-and-Burn]] · [[HSL-and-Colour-Mixer]] · [[Retouching]] ·
[[Noise-Reduction]] · [[Tonal-Composition]] · [[Post-Processing-Index]]
