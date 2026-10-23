---
title: Lens Corrections
type: concept
module: 4
tags:
  - post/geometry
created: 2026-10-22
---
# Lens Corrections

> [!summary] In one line
> Every lens bends straight lines a little, darkens the corners and adds colour fringes.
> Lens corrections undo those faults in software, usually with one click, so start
> every edit with them.

## What it is

No lens is perfect. Three faults show up in almost every photo, more on wide and fast
lenses:

| Fault | What you see | Where |
|---|---|---|
| Distortion | Straight lines bow outwards (barrel) or inwards (pincushion) | Near the frame edges |
| Vignetting | Corners darker than the centre | Corners, most at the widest aperture |
| Chromatic aberration (CA) | Coloured fringes along high-contrast edges | Edges, or around out-of-focus highlights |

A raw developer fixes all three with a **lens profile**: a measured description of how
one lens model behaves at each focal length and aperture.

## How it works

### Distortion

Distortion happens when the lens magnifies the edges of the frame by a different amount
than the centre.

- **Barrel:** magnification falls towards the edges, so straight lines near the edges
  bow outwards, like the sides of a barrel. Common at the wide end of zooms.
- **Pincushion:** magnification rises towards the edges, so lines bow inwards. Common
  at the long end of zooms.

Correction stretches or squeezes the edges back into place. The stretch is uneven, so
afterwards the image's outline bends and no longer fills a neat rectangle. The software
crops the edges or leaves gaps to fill. That is why correcting distortion always costs
a little of the frame.

### Vignetting

Light reaching the corners arrives at an angle, so it spreads over more sensor area and
is dimmer. At wide apertures the lens barrel also blocks some of that angled light.
Stopping down reduces the second effect, which is why corners brighten from f/1.7 to
f/4. At the widest aperture, corners can be about a stop darker than the centre.

Correction brightens the corners. That's the same as raising exposure there, so corner
noise rises slightly. A creative vignette, added later to darken the edges on purpose,
is a separate step.

### Chromatic aberration

Glass bends each colour of light by a slightly different amount. That causes two
different faults:

| Type | Cause | What it looks like | Fix |
|---|---|---|---|
| Lateral CA | Each colour is magnified by a different amount | Red/cyan or blue/yellow fringes, growing towards the corners | Easy: the software scales the colour channels back into line |
| Axial CA | Each colour focuses at a different distance | Purple or green fringes around out-of-focus edges, anywhere in the frame | Harder: a defringe tool, or stop down at capture |

Axial CA is often purple in front of the focus point and green behind it. A defringe
tool removes those colours along edges, so used too strongly it also greys out real
purple or green edges.

## How to use it

1. **Turn on profile corrections first,** before any other edit. In Lightroom it's
   "Enable Profile Corrections"; most raw developers find the profile from the file's
   metadata automatically.
2. **Tick "remove chromatic aberration"** (or your app's equivalent). It fixes lateral
   CA with almost no risk.
3. **Look for leftover fringes at 100%,** on branches against a bright sky. Use the
   defringe tool only if purple or green edges remain, at the lowest amount that works.
4. **Adjust the distortion amount if you want.** A fully corrected wide shot can look
   stretched at the edges; some people leave a touch of barrel on purpose.
5. **Then fix perspective and crop.** Perspective tools assume lines are already
   straight. → [[Perspective-Correction]]

> [!note] Built-in corrections
> Many fixed-lens cameras and phones are designed to rely on software correction. The
> lens is made smaller and the camera corrects its distortion digitally. The
> correction data travels inside the raw file, and many raw developers apply it
> automatically, sometimes with no way to turn it off.

## On your kit

- **Lumix L10:** a fixed lens, the kind of camera that often carries built-in
  corrections. Open an RW2 and check your raw developer's lens panel: it shows whether a
  profile is applied and whether you can turn it off. Vignetting is strongest at f/1.7.
  → [[Aperture]]
- **iPhone 15 Pro Max:** phones correct their lenses in software before you ever see
  the file. The 13 mm ultra-wide needs the most correction.
- **Pocket 3 (DNG):** check whether your raw developer finds a profile. If it doesn't,
  use the manual Distortion and Vignetting sliders.
- **Action 5 Pro:** its 155° lens is a fisheye: it bends straight lines into curves,
  which is how it fits so much into the frame. The **Standard (Dewarp)** field of view
  removes the bend in camera; [[My-Kit]] suggests it for people and buildings.
  Straightening a fisheye always costs some of the edges. In Ultra Wide, keep the
  horizon through the centre of the frame, where lines stay straight.

## Common mistakes

- **Forgetting to turn corrections on.** It's one click, and most apps let you make it
  part of your import default.
- **Blaming the lens for stretched faces at the edge of a wide frame.** That's
  wide-angle perspective, not lens distortion, and no profile fixes it. Keep faces away
  from the corners. → [[Focal-Length-and-Perspective]]
- **Defringing hard everywhere.** It removes real purple and green detail too. Use it
  only where fringes remain.
- **Straightening and cropping before correcting.** The correction changes the geometry
  underneath your crop. Correct first.
- **Treating vignette removal and a creative vignette as the same thing.** Remove the
  lens's vignette first; add your own later, on purpose.

## Try it

Twenty minutes, around an HDB block or any building with straight edges:

1. On the L10 at 24 mm, f/1.7, frame a wall so straight lines run near the frame edges.
   Include a branch against bright sky. Repeat at 75 mm.
2. Open both RW2 files. Toggle profile corrections and CA removal, and watch the lines,
   the corners and the fringes.
3. On the Action 5 Pro, shoot the same building in Ultra Wide and in Standard (Dewarp).
   Compare what each keeps and what each bends.

Your **A1.1** aperture ladder also shows vignetting fading as you stop down: compare
the corners of the f/1.7 and f/5.6 frames.

## Check yourself

> [!question]- Which kind of chromatic aberration does a "remove CA" checkbox fix reliably, and why not the other?
> Lateral CA. Each colour is just magnified by a slightly different amount, so the
> software scales the channels back into line. Axial CA comes from colours focusing at
> different distances, which no rescaling can undo.

> [!question]- Why do the corners get brighter when you stop down from f/1.7 to f/4?
> At wide apertures the lens barrel blocks part of the light arriving at an angle, which
> is the light that reaches the corners. A smaller aperture uses only the central part
> of the beam, so the corners lose less.

> [!question]- Why does correcting barrel distortion always crop a little of the frame?
> Straightening the lines stretches the image unevenly, so its outline bends and no
> longer fills a rectangle. The software crops back to a rectangle or leaves gaps to
> fill.

> [!question]- A friend at the edge of your iPhone's 13 mm frame looks stretched, even with corrections on. Why?
> That's wide-angle perspective: a lens that keeps lines straight must stretch shapes
> near the edges. Lens corrections fix distortion, not perspective. Move them towards
> the centre.

## Related
[[Perspective-Correction]] · [[Focal-Length-and-Perspective]] · [[Crop-and-Straighten]] ·
[[Aperture]] · [[My-Kit]] · [[Post-Processing-Index]]
