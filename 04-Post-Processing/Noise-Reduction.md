---
title: Noise Reduction
type: concept
module: 4
tags:
  - post/detail
created: 2026-10-22
---
# Noise Reduction

> [!summary] In one line
> Noise reduction smooths away the speckle that comes from too little light. Classic
> tools trade fine detail for smoothness; AI denoise on the raw file loses far less,
> which makes high-ISO frames much more usable.

## What it is

Noise is random variation that wasn't in the scene: speckle in what should be a smooth
area. It comes mostly from too little light reaching the sensor, then gets amplified by
high [[ISO]]. It shows most in shadows and flat areas such as skies and walls.

There are two kinds, and they are treated separately:

| Kind | What it looks like | How hard it is to remove |
|---|---|---|
| Luminance noise | Grain-like speckle in brightness | Hard. Smoothing it also smooths real texture |
| Colour (chroma) noise | Red, green and blue blotches, often in dark areas | Easy. It can be smoothed with little visible loss |

## How it works

Classic noise reduction averages each pixel with its neighbours. Random speckle
averages out; a smooth area becomes smooth. The problem is that fine real detail looks
like speckle too: skin pores, leaves, fabric, hair. Smooth enough to kill the noise and
those go with it. Pushed too far, faces look like plastic and foliage looks like a
watercolour painting.

Colour noise is cheap to remove because your eyes see detail mostly in brightness, not
in colour. The software can blur the colour information a lot while leaving brightness
alone, and you rarely notice. Luminance noise has no such shortcut: every step costs
some texture.

### Why AI denoise is a big step forward

AI denoise uses a model trained on huge numbers of noisy and clean images. Instead of
averaging blindly, it has learned what real textures look like, so it can remove
speckle while keeping edges and fine detail. In practice it often makes a frame look
like one shot a stop or two lower in ISO.

It works best on the **raw** file. The raw holds the sensor's original values, before
demosaicing (building full colour from single-colour pixels), sharpening and
compression have mixed the noise into the picture. Once noise has been sharpened and
baked into a JPEG, it is much harder to tell apart from detail. Some apps' AI denoise
accepts only raw files, and some save the result as a new, larger file.

## How to use it

1. **Get light at capture first.** Noise comes from too little light, so exposing well
   beats any slider. → [[Expose-to-the-Right]]
2. **Apply AI denoise early, on the raw,** before other edits. It rewrites the base
   image that everything else builds on. Use it only on frames that need it: it's slow.
3. **With classic sliders, start with colour noise.** Raise it until the blotches go,
   and no further. Defaults are often already enough.
4. **Then luminance noise, gently.** Stop while some fine grain remains. A little grain
   looks natural; smeared skin doesn't.
5. **Check at 100%, then at viewing size.** Noise that shows at 100% often disappears
   in a 2000 px export or an A4 print.
6. **Set [[Sharpening]] together with it.** Sharpening boosts noise, so use its Masking
   control to keep it off smooth areas.

| Situation | Typical approach |
|---|---|
| Base ISO, good light | Leave the defaults alone |
| Medium ISO, about 800–3200 | Light colour and luminance noise reduction |
| ISO 6400 and up, or shadows pushed hard | AI denoise on the raw, then light sharpening |
| Phone JPEG or HEIC | Little or none: it was already denoised |

## On your kit

- **Lumix L10 (RW2):** your best raw file, and the one where AI denoise does the most.
  Its ISO runs to 25600. V-Log stills start at ISO 500, so V-Log frames carry more
  noise than an ISO 100 frame of the same scene.
- **iPhone 15 Pro Max:** ProRAW and HEIC have already been through Apple's multi-frame
  noise reduction. That's why [[My-Kit]] says to shoot Halide's single-frame RAW for the
  ISO ladder: otherwise you are measuring Apple's processing, not the sensor.
- **Pocket 3 and Action 5 Pro (DNG):** true raw files, so AI denoise helps. Both
  sensors are smaller than the L10's, so they collect less light at the same exposure
  and show noise sooner. The Action 5 Pro's ISO 25600 is a last resort.

## Common mistakes

- **Smoothing until the noise is gone.** Texture goes with it and faces turn to
  plastic. Stop while a fine grain remains.
- **Pushing colour noise reduction too far.** Small colourful details, such as a red
  sign far away, bleed and lose colour. Use the lowest value that removes the blotches.
- **Denoising a JPEG heavily.** The noise is already sharpened and compressed into the
  picture. Denoise the raw instead.
- **Judging noise only at 200%.** Nobody views your photo that way. Check at the size it
  will be seen.
- **Underexposing to be safe, then lifting the shadows three stops.** That creates the
  noise you then fight. Expose brighter at capture.

## Try it

Thirty minutes, with your ISO ladder from the L10:

1. Open the base ISO frame and the two highest ISO frames. Push the shadows +2 stops on
   each, as in the assignment.
2. On the highest ISO frame, apply colour noise reduction only. Then add luminance
   noise reduction until the skin or texture starts to smear. Note the value.
3. Make a copy of that frame and run AI denoise on the raw instead, if your app has it.
4. Compare the two copies at 100% and at 2000 px. Which ISO would you now trust in the
   dark?

This revisits **A1.3**: your usable ISO ceiling may move up once denoise is part of
your workflow.

## Check yourself

> [!question]- Why can colour noise be removed with little visible loss, but luminance noise can't?
> Your eyes see fine detail mostly in brightness, not in colour. The software can blur
> colour heavily and you won't notice. Smoothing brightness removes real texture along
> with the noise.

> [!question]- Why does AI denoise work better on a raw file than on a JPEG?
> The raw holds the sensor's original values. In a JPEG the noise has already been
> demosaiced, sharpened and compressed into the picture, so it's harder to tell apart
> from real detail.

> [!question]- Two frames look equally bright: one at ISO 200, one at ISO 6400. Which needs more noise reduction, and why?
> The ISO 6400 frame. It was made with far less light, and noise comes mainly from too
> little light. The higher ISO brightened that weak signal and its noise together.

> [!question]- Your portrait's skin looks waxy after noise reduction. What went wrong, and what do you change?
> Luminance noise reduction was set too high, so it smoothed real skin texture along
> with the noise. Lower it until some fine grain returns, or use AI denoise on the raw.

## Related
[[ISO]] · [[Sharpening]] · [[Expose-to-the-Right]] · [[RAW-vs-JPEG]] ·
[[Computational-Photography]] · [[Dynamic-Range]] · [[Post-Processing-Index]]
