---
title: Bit Depth
type: concept
module: 4
tags:
  - post/file
created: 2026-10-22
---
# Bit Depth

> [!summary] In one line
> Bit depth is how many brightness steps each colour channel can store. More steps
> survive heavy edits without smooth skies breaking into bands, so edit in high bit
> depth and drop to 8-bit only at the final export.

## What it is

A digital image stores each pixel's red, green and blue as numbers. Bit depth is how
many different values each number can take: its number of **levels**. Each extra bit
doubles the levels.

| Bit depth | Levels per channel | Where you meet it |
|---|---|---|
| 8-bit | 256 | JPEG, most web images, most screens |
| 10-bit | 1,024 | Some HEIF files, log video, HDR video |
| 12-bit | 4,096 | Many raw files |
| 14-bit | 16,384 | Many raw files |
| 16-bit | 65,536 | TIFF and PSD working files |

Three 8-bit channels give 256 × 256 × 256, about 16.7 million colours. Three 10-bit
channels give about 1.07 billion.

A raw file isn't RGB yet: each pixel holds a single number from the sensor. "12-bit
raw" means that number has 4,096 possible levels. Once developed, your raw developer
works with far more precision internally.

## How it works

### Why levels matter: banding

A smooth gradient, such as a clear sky, uses only a narrow slice of the range. Say a
sky runs from darker to lighter blue across 30 levels of an 8-bit file. Neighbouring
steps are one level apart, too small to see.

Now edit it hard: triple the sky's contrast to make it dramatic. The 30 steps now
spread over 90 levels, but there are still only 30 different values, with gaps of three
levels between them. Each step is now a visible stripe. That's **banding**, also
called posterisation.

In a 16-bit file, the same sky has about 7,700 steps (30 × 256). Stretch it three times
and the steps are still far too small to see. Bit depth doesn't make the photo look
better on its own. It's headroom for editing.

### Shadows have the fewest levels

Raw data is linear: half of all the levels describe the brightest stop, half of the
rest describe the next stop, and so on. The darkest stops get very few. Lifting deep
shadows stretches those few levels, and noise comes with them. That's one more reason
to expose well at capture. → [[Expose-to-the-Right]]

### Why 8-bit is fine at the end

An unstretched gradient looks smooth in 256 levels on most screens. The damage happens
only when you stretch it after reducing to 8-bit. So the rule is: do all the stretching
in high bit depth, then reduce once, at export, when nothing will stretch it again.

### Bit depth and colour space

A wide colour space covers more colours with the same number of steps, so each step is
a bigger jump. ProPhoto RGB in 8-bit bands easily, which is why it's used with 16-bit.
→ [[Colour-Spaces]]

### What the LUTs note assumes

[[LUTs]] says to apply LUTs to "16-bit or float data and quantise to 8-bit last". In
plain words:

- **Quantise** means rounding values to fewer levels, for example from 65,536 down to
  256. It's the step that can't be undone.
- **Float** (32-bit floating point) stores values with decimals, so it has practically
  unlimited levels, and can even hold values brighter than white. Video and grading
  software often work this way internally.
- **Posterisation** is the visible banding when too few levels are stretched.

A LUT that adds contrast stretches levels just like a curve, so it needs the same
headroom.

### 10-bit HEIF and 10-bit video

JPEG can't go beyond 8-bit. HEIF, the format behind HEIC files, can store 10 bits.
Whether a given HEIF file is 8- or 10-bit depends on the device and mode, so check the
file's info.

Log video wants 10-bit for the same banding reason. Log squeezes a wide brightness
range into a flat file, and grading stretches it back out: exactly the heavy edit that
breaks 8-bit. → [[Log-Profiles]]

## How to use it

1. **Shoot raw** for anything you plan to edit hard.
2. **Make your big moves in the raw developer,** which works in high precision.
3. **Hand off in 16-bit.** If a photo moves to a layer editor or gets a LUT, export a
   16-bit TIFF, not a JPEG.
4. **Export 8-bit JPEG last,** for delivery only. → [[Export-Settings]]
5. **Keep masters in high bit depth.** Never edit an exported JPEG and export it again;
   go back to the raw.
6. **If you see banding,** check it at 100% on another screen first, since screens and
   previews can band too. Then reduce the move, or add a little grain: random grain
   breaks up the hard edges between steps.

## On your kit

- **Lumix L10:** shoot RW2 for editing. Its JPEGs are 8-bit; check the HEIF files' info
  for their bit depth. V-Log stills are flat files made to be stretched, so shoot RAW
  alongside, as [[My-Kit]] advises.
- **iPhone 15 Pro Max:** use ProRAW for heavy edits. For video, Apple Log needs ProRes,
  a high-quality 10-bit format.
- **Pocket 3 and Action 5 Pro:** DNG for stills. For footage you plan to grade, shoot
  10-bit D-Log M.

## Common mistakes

- **Heavy edits on an 8-bit JPEG.** Skies band. Edit the raw instead.
- **Re-editing an export.** Each 8-bit round trip loses levels. Go back to the master.
- **ProPhoto RGB in 8-bit.** The steps are too coarse for such a wide space. Use 16-bit.
- **Blaming the file for screen banding.** Check at 100% and on another screen.
- **Thinking more bits mean more dynamic range.** Bits divide the range more finely; the
  sensor sets how wide the range is.

## Try it

Fifteen minutes, with one raw file that has a clear sky:

1. Export it twice: an 8-bit JPEG at quality 100 and a 16-bit TIFF.
2. Open both in the same editor. Apply the same extreme curve to each: lots of contrast
   and saturation in the sky.
3. Compare the skies at 100%. Then add a little grain to the banded one.

This is a side experiment for **A4.2**, where you push files to find their limits.

## Check yourself

> [!question]- How many levels per channel does 10-bit have compared with 8-bit, and why?
> 1,024 against 256: four times as many. Each extra bit doubles the levels, and 10-bit
> has two more bits than 8-bit.

> [!question]- The same contrast boost bands the sky in a JPEG but not in the raw. Why?
> The stretch spreads the JPEG's few sky levels apart, leaving visible gaps. The raw is
> developed at far higher precision, so it has enough steps to fill the stretched range.

> [!question]- If 8-bit bands so easily, why is it fine for the final export?
> Banding comes from stretching. After the final export nothing stretches the levels
> again, and an unstretched gradient looks smooth in 256 levels.

> [!question]- Does a 14-bit raw file have more dynamic range than a 12-bit one?
> Not by itself. Bit depth divides the range more finely; the sensor and its noise set
> how wide the range is. Extra bits help only if the sensor is clean enough to fill them.

## Related
[[RAW-vs-JPEG]] · [[Colour-Spaces]] · [[LUTs]] · [[Log-Profiles]] ·
[[Export-Settings]] · [[Dynamic-Range]] · [[Post-Processing-Index]]
