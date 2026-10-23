---
title: Perspective Correction
type: concept
module: 4
tags:
  - post/geometry
created: 2026-10-22
---
# Perspective Correction

> [!summary] In one line
> Tilt the camera up at a building and its sides lean in towards the top. Perspective
> correction straightens them in software, but it costs part of the frame, so the best
> fix is a level camera at capture.

## What it is

Point the camera up at a tall building and its vertical edges lean towards each other,
as if the building were falling backwards. This is called **converging verticals**, or
keystoning. The same thing happens sideways when you photograph a wall at an angle: its
horizontal lines converge towards one side.

Perspective correction is the set of tools that stretches the image so those lines
become parallel again. Most raw developers have them: Lightroom calls them Upright and
Transform, Capture One calls its tool Keystone.

## How it works

Things further away look smaller. That single fact causes all of it.

- **Camera level:** the sensor is parallel to the building's face. The top and the
  bottom of the building are the same distance from the sensor, so they are drawn at
  the same scale. Vertical lines stay parallel.
- **Camera tilted up:** the top of the building is now further from the sensor than the
  bottom. It's drawn smaller, so the sides lean in towards a point above the building.

This isn't a lens fault. Every lens does it, even a perfect one. A wide lens only
tempts you to tilt more, because it shows you so much sky.

### A worked example

You want a 60 m building in the frame, with the camera level, at 24 mm, held upright.
The top of that frame sees about 36° above level. To fit the top of the building
inside that angle, you must stand about 80 m away. The building then fills only the
top half of the frame. You crop away the empty bottom half later.

That crop costs half your pixels: about 10 MP left from the L10's 20.4 MP. Correcting a
tilted shot in software costs pixels too. It just hides the cost in stretched corners.

### What the software does

The correction stretches the top of the image outwards, or squeezes the bottom, until
the lines are parallel. That leaves empty wedges in the corners, which must be cropped
away. The stretch also makes the building look taller or squatter than it is, and
softens the stretched areas slightly.

## How to use it

1. **Apply lens corrections first.** Perspective tools need straight lines to work
   from. → [[Lens-Corrections]]
2. **Try the automatic modes.** These are Lightroom's Upright modes; other apps have
   similar ones:

| Mode | What it fixes |
|---|---|
| Auto | A balanced mix of level, verticals and horizontals |
| Level | Only tilts the horizon straight |
| Vertical | Level plus converging verticals |
| Full | Verticals and horizontals: for a wall shot face-on |
| Guided | You draw two to four lines along edges that should be straight |

3. **Use Guided when Auto guesses wrong.** Draw lines on two edges you know are
   vertical, such as the corners of the building.
4. **Fix the proportions.** If the building now looks stretched, use the Aspect slider
   (or your app's equivalent) until it looks right.
5. **Crop, and check the top.** If the spire or the roofline is cut off, the shot was
   framed too tight.

**Leave a little convergence on very tall buildings.** Perfectly parallel verticals on
a tower seen from below can look top-heavy, as if it were leaning out over you. Many
photographers correct most of the way, but not all of it.

**Or keep the lines converging on purpose.** A strong upward tilt reads as a choice:
the building towers over the viewer. A small tilt reads as a mistake. Commit to one or
the other. → [[Architecture]]

### Getting it right in camera

- **Keep the camera level.** Use a grid or level display if your camera has one
  (check the manual).
- **Step back, or go higher.** A footbridge, an upper floor or a car park roof puts you
  closer to the middle of the building, so you need less tilt.
- **Use the wide end and crop later.** Keep the camera level, let the building sit in
  the top part of the frame, and crop the foreground away.
- **Leave room around the building** if you plan to correct in post, because the
  correction will eat the edges.

## On your kit

- **Lumix L10:** the 24 mm end and 20.4 MP give the most room to crop. The vari-angle
  screen lets you hold the camera low or high while keeping it level.
- **iPhone 15 Pro Max:** the 13 mm ultra-wide fits a whole building from close up, which
  invites a steep tilt. Hold the phone level, step back, and crop.
- **Pocket 3:** in video, Tilt Locked holds the pitch steady, so set the camera level
  and verticals stay straight as you walk. Its stills are only about 8–9 MP, so there's
  little room to crop.
- **Action 5 Pro:** in Ultra Wide the fisheye curves straight lines, and perspective
  tools can't straighten curves. Use Standard (Dewarp) for buildings.

## Common mistakes

- **Tilting up "just a little".** Slight convergence looks accidental. Keep the camera
  level, or tilt boldly.
- **Framing tightly, then correcting.** The correction crops the edges and loses the
  top of the building. Leave space around it.
- **Correcting very tall buildings all the way.** They can look top-heavy. Leave a
  little convergence.
- **Ignoring the stretch.** A corrected building can look squat or stretched. Fix the
  proportions with the Aspect control.
- **Correcting a fisheye frame.** Straighten the curves first with lens corrections or
  Dewarp, then fix perspective.

## Try it

Twenty minutes, at one tall building:

1. Shoot it on the L10 at 24 mm, tilted up to fit the whole building.
2. Keep the camera level, step back until the building fits, and shoot again.
3. Shoot a third frame from close to the base, tilted up steeply, on purpose.
4. At home, correct frame 1 with the Vertical or Guided mode. Crop frame 2. Compare
   what each lost, and decide whether frame 3 needs correcting at all.

If you choose architecture in Module 6, this is the core skill for its **A6.2** set.

## Check yourself

> [!question]- Why do verticals converge when you tilt up, even with a perfect lens?
> Tilting puts the top of the building further from the sensor than the bottom.
> Further things are drawn smaller, so the top shrinks and the sides lean in. It's
> perspective, not a lens fault.

> [!question]- You corrected the verticals and the top of the spire got cut off. What should you have done at capture?
> Left more space around the building. The correction stretches the top outwards and
> the crop removes the edges, so the spire needed room above it.

> [!question]- Why can a fully corrected skyscraper look as if it's leaning out over you?
> When you look up at a tall building, you expect some convergence. Perfectly parallel
> sides look top-heavy, so many photographers leave a little lean.

> [!question]- Shooting level from 80 m away gives straight verticals with no software. What's the cost?
> Half the frame is empty foreground, so the crop leaves about half the pixels. In
> return there's no stretching, and the top of the building is never cut off.

## Related
[[Architecture]] · [[Lens-Corrections]] · [[Crop-and-Straighten]] ·
[[Focal-Length-and-Perspective]] · [[Point-of-View]] · [[Post-Processing-Index]]
