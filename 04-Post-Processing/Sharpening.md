---
title: Sharpening
type: concept
module: 4
tags:
  - post/detail
created: 2026-10-22
---
# Sharpening

> [!summary] In one line
> Sharpening raises the contrast along edges so a photo looks crisper. It can't add
> detail the lens and sensor never recorded, so it polishes a sharp photo but can't
> rescue a blurred one.

## What it is

Sharpening makes edges look harder. Where a light area meets a dark one, it makes the
light side a little lighter and the dark side a little darker. Your eye reads that
extra edge contrast as sharpness.

It happens at three points in an edit, and each one has a different job:

| Stage | When | Why |
|---|---|---|
| Capture sharpening | Early, on the whole raw file | Raw files look soft straight from the sensor. This restores crispness |
| Creative sharpening | During the edit, on parts of the photo | To pull the eye to eyes, texture or a sign. Not to skin or sky |
| Output sharpening | At export, for one size and one medium | Resizing and printing soften the image again |

Raw files look soft because of the lens and because of demosaicing: the step that
builds full colour from the sensor's single-colour pixels by blending neighbours.

## How it works

Most sharpening tools use one idea, called **unsharp masking**. The software makes a
blurred copy of the photo and compares it with the original. Where the two differ,
there is an edge. It then adds that difference back, which boosts the contrast on both
sides of every edge.

Four controls decide how it behaves. The names below are Lightroom's; other raw
developers have the same controls under similar names.

| Control | What it does | Starting point |
|---|---|---|
| Amount | How strong the edge boost is | Moderate. Judge it at 100% zoom |
| Radius | How wide the boosted zone around each edge is, in pixels | 0.5–1.0 for fine detail, more for coarse edges |
| Detail | How much the finest textures get sharpened. Low values hold back halos | Low for portraits, higher for landscapes |
| Masking | Limits sharpening to strong edges and leaves smooth areas alone | 0 sharpens everything; 50–80 protects skin and sky |

Lightroom's default for raw files is Amount 40, Radius 1.0, Detail 25, Masking 0: a
gentle capture sharpening and a sensible place to start.

### Halos

Push Amount or Radius too far and the boosted zone becomes visible: a light outline
around dark objects and a dark outline around light ones. You see it most where a
building or a branch meets a bright sky. A halo means the sharpening has become
something the viewer notices.

### Why it can't fix blur

Sharpening only strengthens edges that are already in the file. When focus is missed,
each point of the subject spreads into a soft disc, so the fine edges never reach the
sensor. With motion blur, each point is smeared into a streak. There is nothing crisp
left to strengthen, so sharpening adds halos and noise instead. Some AI tools claim to
reverse blur. At best they rescue slight softness, and they do it by guessing detail.

Sharpening also boosts noise, because to the software a speck of noise looks like a
tiny edge. That's why Masking exists, and why sharpening and [[Noise-Reduction]] are
set together.

## How to use it

1. **Judge at 100% zoom.** At "fit to screen" you can't see what sharpening does.
2. **Capture sharpening first, lightly.** Raise Amount until fine detail looks crisp,
   then back off a little. Keep Radius around 1.0 for a 20 MP file.
3. **Set Masking.** In Lightroom, hold Alt (Option on a Mac) while dragging Masking to
   see the mask: white areas get sharpened, black areas don't. Raise it until skin and
   sky turn black.
4. **Add creative sharpening with a mask, only where it matters:** the eyes in a
   portrait, the texture of a wall. → [[Local-Adjustments]]
5. **Output sharpening last, at export,** after the image has been resized:

| Output | Why it needs sharpening | Typical setting |
|---|---|---|
| Screen | Shrinking 5000 px to 2000 px softens fine detail | Low to standard, for screen |
| Glossy print | Ink spreads a little into the paper | Standard, for glossy |
| Matte print | Ink spreads more into matte paper | Standard to high, for matte |

Lightroom's export dialog offers exactly these: sharpen for Screen, Matte Paper or
Glossy Paper, at Low, Standard or High. Print sharpening looks too strong on a monitor,
and that's correct: judge it on the print. → [[Export-Settings]] · [[Printing]]

## On your kit

- **Lumix L10 (RW2):** a raw file, so it arrives unsharpened and needs capture
  sharpening. Diffraction shows from about f/5.6–f/8, so frames at f/11–f/16 are softer
  all over. Sharpening hides a little of that. It can't give back what diffraction
  took. → [[Aperture]]
- **iPhone 15 Pro Max:** like any camera's JPEG, its HEIC and JPEG files are already
  sharpened. ProRAW has been through Apple's multi-frame pipeline too. Start with little
  or no extra sharpening, or phone files turn crunchy.
- **Pocket 3 and Action 5 Pro (DNG):** raw, so capture sharpening applies. The Pocket 3's
  stills are only about 8–9 MP, so don't over-sharpen to fake resolution. The Action
  5 Pro's focus is fixed from 35 cm; anything closer is soft and stays soft.

## Common mistakes

- **Sharpening a blurred photo.** It adds halos, not detail. Fix focus and shutter
  speed at capture instead. → [[Shutter-Speed]]
- **Judging at "fit to screen".** Zoom to 100% for capture and creative sharpening.
- **Sharpening everything equally.** Skin, sky and smooth walls only gain noise. Raise
  Masking, or sharpen with a local mask.
- **Sharpening twice over.** A camera JPEG plus heavy capture sharpening plus output
  sharpening looks crunchy. Sharpen each stage once, gently.
- **Turning down print sharpening because it looks harsh on screen.** Paper softens it.
  Judge a test print in your hand.

## Try it

Twenty minutes, with your L10 frames from the aperture ladder:

1. Open a frame from the middle of the ladder and the f/16 frame. Zoom to 100%.
2. Set Amount to 0, then to 150 with Radius 3. Find the halos along the edges.
3. Go back to Amount 40, Radius 1.0. Hold Alt and raise Masking until the sky goes
   black.
4. Sharpen the f/16 frame as far as it will go without halos. Does it match the
   unsharpened middle frame? Usually it doesn't, and that's the lesson.
5. Export one frame at 2048 px with and without screen sharpening. Compare on your
   phone.

This reuses your **A1.1** frames, and the habit carries into every **A4.1** edit.

## Check yourself

> [!question]- Why does sharpening make noise more visible?
> To the software, each speck of noise looks like a tiny edge, so it gets the same
> contrast boost as real detail. Masking limits sharpening to strong edges, which is
> why it protects smooth areas like skin and sky.

> [!question]- A portrait looks crisp, but the skin now looks rough. Which control fixes it, and why?
> Masking. It restricts sharpening to strong edges such as eyelashes and hair, and
> leaves smooth, low-contrast areas like skin alone.

> [!question]- A cyclist shot at 1/30 s is smeared. Why won't sharpening fix it?
> Motion blur smeared each point into a streak, so the sharp edges were never recorded.
> Sharpening can only strengthen edges that exist; here it adds halos and noise.

> [!question]- You sharpened the raw file already. Why sharpen again at export?
> Capture sharpening was for the full-size file. Resizing to 2000 px and printing on
> paper both soften the image again, so output sharpening is set for that one size and
> medium.

## Related
[[Noise-Reduction]] · [[Local-Adjustments]] · [[Export-Settings]] · [[Printing]] ·
[[RAW-vs-JPEG]] · [[Post-Processing-Index]]
