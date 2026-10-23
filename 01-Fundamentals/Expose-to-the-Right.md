---
title: Expose to the Right
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Expose to the Right

> [!summary] In one line
> Expose to the right (ETTR) means making a raw exposure as bright as you can without
> clipping important highlights, then darkening it in editing. More light in means
> cleaner shadows out.

## What it is

The name comes from the [[Histogram]]: you push the graph as far right as it will go
without piling up against the right edge. On the camera the photo looks too bright. In
editing you bring it back down to the brightness you want.

ETTR is a raw technique. You accept a brighter-looking capture in exchange for less
noise in the finished photo, especially in the shadows.

## How it works

Noise comes mostly from too little light (→ [[ISO]]). One extra stop of exposure
doubles the light the sensor collects, while the random noise grows only about 1.4
times (the square root of 2). So the signal-to-noise ratio, how far the signal stands
above the noise, improves. Darkening the file later scales the signal and the noise
down together, so the better ratio stays.

A worked example on an overcast day. The meter suggests f/5.6, 1/250 s, ISO 400, and
the histogram stops about 1.3 stops short of the right edge. You slow the shutter to
1/100 s, and the histogram now just reaches the edge. In editing you lower the
exposure by 1.3 stops. The photo looks like the metered one, but it was recorded with
about 2.5 times the light, so its shadows are visibly cleaner.

You may read that "half the raw data sits in the brightest stop". That's true of the
raw numbers, but it isn't the main reason ETTR works. The extra light is.

### ETTR and ISO-invariance

ETTR means **more light**: a slower shutter or a wider aperture. Raising ISO to push the
histogram right is not the same. On an ISO-invariant camera (one where raising ISO in
the camera or brightening later gives about the same noise), extra ISO adds no light.
It only makes the file clip sooner, which costs highlight room for nothing.

So once aperture and shutter are set for the picture, leave ISO where it is, or even a
little lower, and brighten in editing. On a camera that isn't invariant, a little more
ISO can still help the deepest shadows. The invariance test in the ISO note tells you
which kind you have.

### When not to use it

- **JPEG-only shooting.** The bright version is baked into the JPEG. Darkening it later
  costs quality and can't restore clipped colour. Expose JPEGs to look right.
- **When you need a fast shutter.** Never slow the shutter into blur for ETTR. A sharp,
  slightly noisy photo beats a clean blurred one. The same goes for depth of field:
  don't open the aperture beyond what the picture needs.
- **Specular highlights.** The sun, lamps and sparkles on water will clip anyway. Don't
  let them drag the whole exposure down. Ignore them.
- **When the brightest area must keep detail.** A white dress, an egret's feathers, a
  bright cloud. Stop short of the edge, because the camera's histogram is only an
  estimate.
- **High-contrast scenes.** If the histogram already touches both edges, there's no room
  to move right. ETTR becomes "expose for the highlights". → [[Dynamic-Range]]

### The JPEG-histogram caveat

The camera's histogram and highlight warning come from the JPEG preview, not from the
raw. The raw usually has a little more room, often a third of a stop to a stop, but it
varies with the camera, the picture style and the white balance. Find your margin by
testing (see Try it). Until then, treat the camera's right edge as the limit.

## How to use it

1. **Shoot raw**, at the lowest ISO the picture allows.
2. **Set aperture and shutter for the picture first**: depth of field, motion, steady
   hands. ETTR only works inside those choices.
3. **Turn on the live histogram and the highlight warning** (clipped areas flash in
   playback).
4. **Add exposure** until the histogram just reaches the right edge, ignoring specular
   highlights. In A or S, use positive exposure compensation; in M, a slower shutter or
   a wider aperture.
5. **Take a test shot and check playback.** If anything important blinks, take away
   1/3 stop.
6. **In editing, lower the exposure** (or the highlights) until the photo looks right.
   The shadows come out cleaner than in a metered shot.

## On your kit

- **Lumix L10:** your ETTR camera. It shoots RW2 raw and can show a live histogram as
  you frame. Find its margin with the Try it below.
- **iPhone 15 Pro Max:** Apple's Camera app and ProRAW merge several frames and process
  them heavily, so ETTR doesn't really apply. It does apply to a single-frame raw from
  Halide.
- **Pocket 3 and Action 5 Pro:** both save DNG raw. Their smaller sensors show noise
  sooner, so extra light helps them all the more, as long as nothing important clips.

## Common mistakes

- **Raising ISO to "expose right".** That adds brightness, not light. Use the shutter or
  aperture, or leave it.
- **Clipping a highlight that mattered.** Clipped is clipped. When in doubt, stop 1/3
  stop short.
- **Forgetting to darken in editing.** An ETTR file looks washed out until you do.
- **Using ETTR on JPEGs.** The bright look is baked in. Expose JPEGs for the final look.
- **Using it on every frame.** For fast street work, a normal exposure is fine. Use ETTR
  when noise or shadow detail matters.

## Try it

Twenty minutes on the L10, in raw, camera braced, in steady light:

1. Pick a scene with a bright area and some shadows. Meter it in A mode and shoot at
   0 EV.
2. Shoot again at +0.3, +0.7, +1, +1.3 and +1.7 EV. Note the first frame where the
   highlight warning blinks.
3. In editing, darken each frame to match the 0 EV one.
4. Find the brightest frame whose highlights still recover cleanly. The gap between it
   and the first blink is your raw margin.
5. Compare its shadows with the 0 EV frame at 100%.

This uses the push-the-shadows method from **A1.3**.

## Check yourself

> [!question]- If you darken the photo in editing anyway, why does ETTR give cleaner shadows?
> The sensor collected more light. The signal grows faster than shot noise, so the
> ratio improves. Darkening scales signal and noise down together, so the gain stays.

> [!question]- A child is running, you need 1/500 s, and ETTR would need 1/250 s. What do you do?
> Keep 1/500 s. A sharp photo with a little more noise beats a cleaner blurred one.
> ETTR only works inside the shutter and aperture the picture needs.

> [!question]- On an ISO-invariant camera, why is raising ISO a poor way to expose to the right?
> It adds no light, so the noise doesn't improve. It only makes the file clip sooner,
> so you lose highlight room.

> [!question]- The camera blinks on a white wall at +1 EV, but your edit recovers it. Why?
> The warning comes from the JPEG preview. The raw file had a little more highlight
> room than the preview showed.

> [!question]- Should you use ETTR for a JPEG you'll post straight from the camera?
> No. The JPEG keeps the bright look, and pulling it down later costs quality. ETTR
> only pays off with raw.

## Related
[[Histogram]] · [[Dynamic-Range]] · [[ISO]] · [[Exposure-Compensation]] ·
[[RAW-vs-JPEG]] · [[Noise-Reduction]] · [[Fundamentals-Index]]
