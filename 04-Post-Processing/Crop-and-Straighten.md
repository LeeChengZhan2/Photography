---
title: Crop and Straighten
type: concept
module: 4
tags:
  - post/geometry
created: 2026-10-22
---
# Crop and Straighten

> [!summary] In one line
> Cropping cuts away the edges of a photo to improve the composition or fit a shape.
> Straightening levels a tilted horizon or leaning lines. Both cost pixels, so get close
> in camera and use the crop to finish a frame, not to rescue it.

## What it is

- **Crop:** keep a smaller rectangle inside the photo and discard the rest. In a raw
  editor this is non-destructive, so you can change it later.
- **Straighten:** rotate the photo so a line that should be level is level. The editor
  then crops away the empty corners.
- **Aspect ratio:** the shape of the frame, width to height.
  → [[Frame-and-Aspect-Ratio]]

| Ratio | Where you meet it |
|---|---|
| 3:2 | 35 mm film, and most larger sensors |
| 4:3 | Four Thirds sensors and phone main cameras |
| 1:1 | Square |
| 4:5 | A common portrait shape for social media |
| 16:9 | Screens and video |

## How it works

### Composing after the fact

A crop can remove a distraction at the edge, move the subject off-centre, or tighten a
loose frame. Overlays help you see it:

- **Rule of thirds:** lines one-third and two-thirds of the way across and down.
  → [[Rule-of-Thirds]]
- **Golden ratio:** lines at about 38% and 62%, a little closer to the centre than
  thirds. They come from the ratio 1 : 1.618.
- **Golden spiral and diagonals:** guides for curves and diagonal lines.

What a crop can't do is change perspective. Perspective comes from where you stood. A
crop looks exactly like a longer lens used from the same spot: same compression, same
background, fewer pixels. → [[Focal-Length-and-Perspective]]

### The pixel cost

Pixels are counted over an area, so a crop costs more than it looks. Halve the width
and the height, and you keep only a quarter of the pixels.

| Starting file | Pixels | After halving width and height | Enough for |
|---|---|---|---|
| L10, 4:3 | 5200 px wide, about 20 MP | 2600 px wide, about 5 MP | Screens; A4 at about 220 ppi |
| iPhone 1× ProRAW | 48 MP | About 12 MP | Screens; A4 |
| Pocket 3, 16:9 | 3840 × 2160, about 8.3 MP | 1920 × 1080, about 2 MP | Screens only |

How many pixels do you need?

- **Screens:** about 2000 px on the long edge is plenty for a phone or a web page.
- **Print:** 300 ppi (pixels per inch) is the usual target for prints seen up close.
  An A4 print at 300 ppi needs about 3500 × 2500 px, nearly 9 MP. At 200 ppi it needs
  about 4 MP, which often looks fine at arm's length. → [[Printing]]

### Straightening costs pixels too

Rotating leaves empty triangles in the corners, and the crop that removes them shrinks
the frame. On a 3:2 frame, levelling a 1° tilt costs about 5% of the pixels, and 2°
costs about 10%.

Which line to level:

- **A sea horizon** must be level. A tilted sea looks as if it's draining away.
- **Verticals** matter more than the horizon in buildings and interiors. Walls that lean
  inwards because you tilted the camera up are called converging verticals. A
  perspective tool straightens them by stretching the top of the frame.
  → [[Perspective-Correction]]
- **Not a sloping road or a hillside,** because they aren't level in real life. Find a
  true horizontal or vertical: a door frame, a window, a lamp post.

Lens distortion bends straight lines, so turn on lens corrections before you
straighten. → [[Lens-Corrections]]

### Cropping or moving your feet

| | Move closer | Crop later |
|---|---|---|
| Perspective | Changes: the subject grows against the background | Stays as it was where you stood |
| Pixels | You keep all of them | You lose some |
| Background | You can pick a new one by changing your angle | Fixed |

Get as close as the picture needs, so the crop only refines. But leave a little room if
you'll need to straighten, or if you don't yet know the final shape.

## How to use it

Straighten and crop at the start of developing, right after lens corrections. Every
later judgement about tone and colour depends on what's inside the frame.

1. Turn on lens corrections.
2. Straighten: draw along a true horizontal or vertical with the level tool.
3. Lock the aspect ratio you want.
4. Drag the crop, with an overlay on.
5. Check the edges. Run your eye around all four sides for bright spots, cut-off limbs
   and stray objects.
6. Check the pixel size against what the photo is for.

Rules of thumb:

- **One ratio for a set.** Twelve photos in mixed shapes look like twelve separate
  photos, because the frame keeps changing. Choose one ratio for A4.5.
- **Don't crop through joints.** Cutting a person at the wrist, knee or ankle looks like
  an amputation. Crop between joints.
- **If you crop away more than half the frame, you were too far away.** Note it in the
  shoot log.

## On your kit

- **L10: choose the ratio in camera.** Its multi-aspect sensor makes 3:2 and 16:9
  frames wider than 4:3: 5408 and 5664 px against 5200. A 3:2 frame from the camera is
  wider than a 3:2 crop from a 4:3 file.
- **Pocket 3: very little room.** Stills come only as 3840 × 2160 (16:9) or 3072 × 3072
  (1:1). Even a 3:2 crop from 16:9 leaves 3240 × 2160, about 7 MP. Frame tightly.
- **iPhone: crop from 1× ProRAW.** Only the 1× lens saves 48 MP. The 2× setting is
  already a 12 MP crop of the main sensor, so cropping a 2× photo costs you twice.
- **Action 5 Pro: remove the bend before you straighten.** Its 155° view bends straight
  lines, except those that pass through the centre of the frame. Shoot in Standard
  (Dewarp) or correct the lens in your editor first. Otherwise, keep the horizon
  through the middle of the frame.

## Common mistakes

- **Cropping too tight.** The subject feels squeezed against the edges. Leave some
  breathing room.
- **Levelling the wrong line.** A road or a hillside slopes in reality. Level a true
  horizontal or vertical.
- **Cropping to rescue a distant subject.** You lose pixels and keep the far-away
  perspective. Next time, walk closer.
- **Forgetting the pixel cost.** Check the final pixel size before you print.
- **Mixing shapes in one set.** It breaks the set apart. Choose one ratio.

## Try it

Twenty minutes. Take five frames from **A3.1**. Straighten each one, then try three
crops on virtual copies: 3:2, 1:1 and 4:5. Write down the pixel size of each. Which crop
improved the frame, and which was a rescue? This is **A3.4**'s subtracting, done in the
editor.

## Check yourself

> [!question]- You crop a 20 MP photo to half its width and half its height. How many megapixels remain?
> About 5 MP, a quarter. Pixels are counted over the area, and half times half is a
> quarter.

> [!question]- Why doesn't cropping change perspective?
> Perspective depends on where the camera stood. A crop only removes edges, so it looks
> exactly like a longer lens used from the same spot.

> [!question]- The horizon is tilted by 2°. Why do you lose pixels when you level it?
> Rotating the photo leaves empty corners, and the crop that removes them makes the
> frame smaller: about 10% of the pixels on a 3:2 frame.

> [!question]- Why is "I'll crop it later" riskier on the Pocket 3 than on the iPhone's 1× ProRAW?
> The Pocket 3's stills are only about 8–9 MP, against 48 MP. Uncropped, they already
> print A4 at only about 260 ppi, so any crop takes them further below the 300 ppi that
> close viewing needs. The 48 MP file can lose three-quarters of its pixels and still
> print A4 at over 300 ppi.

> [!question]- Where do golden-ratio lines fall, compared with thirds?
> At about 38% and 62% of the way across, against 33% and 67%. They sit a little closer
> to the centre.

## Related
[[Frame-and-Aspect-Ratio]] · [[Rule-of-Thirds]] · [[Focal-Length-and-Perspective]] ·
[[Perspective-Correction]] · [[Lens-Corrections]] · [[Printing]] ·
[[Post-Processing-Index]]
