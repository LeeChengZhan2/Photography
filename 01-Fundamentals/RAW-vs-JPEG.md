---
title: RAW vs JPEG
type: concept
module: 0
tags:
  - fundamentals/files
created: 2026-10-22
---
# RAW vs JPEG

> [!summary] In one line
> A raw file is the sensor's data before it becomes a picture. A JPEG or HEIF is a
> finished picture with the camera's decisions baked in. Shoot raw when you want to make
> those decisions yourself.

## What it is

A sensor is a grid of millions of **photosites**: tiny cells that measure how much light
reached them. The camera can save that data in two ways.

- A **raw file** keeps the measurements almost untouched, plus **metadata**: your
  settings, the camera model, the white balance it chose and a small JPEG preview. It
  isn't a picture yet. A raw developer, such as Lightroom or darktable, turns it into
  one.
- A **JPEG** is a finished picture. The camera has already set the colour, white
  balance, contrast, sharpening and noise reduction, compressed the result and thrown
  the rest away. **HEIF** (`.heif` or `.heic`) does the same job with better
  compression, so its files are smaller.

| | Raw | JPEG | HEIF |
|---|---|---|---|
| What it holds | Sensor data + metadata | A finished picture | A finished picture |
| Bit depth | 12 or 14 bits | 8 bits | 8 or 10 bits |
| Tonal levels | 4,096 or 16,384 | 256 per colour | 256 or 1,024 per colour |
| White balance | A setting you can change later | Baked in | Baked in |
| Typical size, 20 MP | Roughly 20–30 MB | Roughly 5–10 MB | Often about half a JPEG |
| Opens in | A raw developer | Anything | Most modern software |

## How it works

### From sensor data to a picture

Each photosite sits under a red, green or blue filter, so it records only one colour.
Software estimates the two missing colours from the neighbours (**demosaicing**), then
applies white balance, a tone curve for contrast, colour, sharpening and noise
reduction. A JPEG gets all this once, in the camera, and the raw data is discarded. A
raw file gets it later, in your developer, as often as you like. The original data
never changes.

### Why the extra bits matter

Bit depth is the number of steps between black and white: 256 per colour in an 8-bit
JPEG, 16,384 in a 14-bit raw. → [[Bit-Depth]]

Editing stretches tones apart. Lift the shadows by two stops and a few dark levels must
fill a much wider range. With 256 steps you see **banding** (stripes across smooth
areas such as skies) and blotchy noise. With thousands of steps, the stretch stays
smooth.

### Latitude: what you can still fix

- **White balance:** in a raw file it's only a number in the metadata, so changing it
  costs nothing. A JPEG's colours were already shifted and rounded to 8 bits, so a big
  correction leaves odd, muddy colours.
- **Highlights:** the camera's JPEG turns the brightest tones white a little before the
  sensor fills up, so a raw file often holds some extra detail. But once the sensor
  **clipped** (a photosite collected all the light it can hold), nothing brings that
  detail back. → [[Dynamic-Range]]
- **Shadows:** raw shadows carry many levels and no baked-in noise reduction, so on a
  modern camera they lift cleanly by a stop or two. JPEG shadows band and smear.

Sharpening and noise reduction can't be undone either. A JPEG is the camera's opinion;
a raw file keeps the question open.

### Apple ProRAW is not a plain raw

A normal camera raw file holds one exposure, not yet demosaiced. Apple ProRAW is a raw
file too (a DNG), but much more has already happened to it:

| | Single-frame raw (the L10's RW2, Halide's single-frame RAW) | Apple ProRAW |
|---|---|---|
| Frames | One exposure | Several frames merged into one |
| Demosaiced | No | Yes, already |
| Noise reduction | None | Apple's, already applied |
| Tone mapping | None | Apple's, stored inside the file |
| White balance and exposure | Fully adjustable | Fully adjustable |

So ProRAW keeps raw's flexible white balance and exposure, but starts from Apple's
merged, cleaned-up picture. That's useful for everyday editing, and misleading when you
want to test the sensor itself. → [[Computational-Photography]]

### DNG and RW2

**RW2** is Panasonic's own raw format. **DNG** is a raw format that Adobe publishes
openly, used by the iPhone, both DJI cameras and many others. Most raw developers open
any DNG, but support for each new camera's RW2 files has to be added, so a camera from
2026 may need the newest version of your software. There's no need to convert RW2
files to DNG: keep the originals.

## How to use it

- **While learning, shoot RAW + JPEG (or HEIF).** The JPEG shows what the camera would
  have done; the raw is what you edit. Comparing the two is a lesson in itself.
- **Later, shoot raw alone** for anything you might edit. JPEG or HEIF alone is fine
  when you won't edit, need to share at once, are shooting hundreds of frames in easy
  light, or want the camera's look on purpose, such as an in-camera LUT.
- **Expose carefully anyway.** Clipped highlights are gone, and big shadow pushes add
  noise. → [[Histogram]]
- **Remember the preview is a JPEG.** The camera's screen, histogram and highlight
  warning all come from the processed preview, not the raw data. So they're slightly
  cautious, and they change with your Photo Style.

## On your kit

- **Lumix L10:** RAW (RW2), JPEG or HEIF, or RAW plus either. A Photo Style or
  [REAL TIME LUT] changes the JPEG/HEIF and the preview, not the raw data. One catch:
  the V-Log Photo Style starts at ISO 500, so the camera lets in less light than it
  would at ISO 100, and the raw pays for that too.
- **iPhone 15 Pro Max:** HEIF/JPEG, or ProRAW (DNG). ProRAW is 48 MP on the 1× lens
  only; the other lenses, Night mode, flash and macro shots save 12 MP. Photographic
  Styles can't be used with ProRAW. For A1.3, use Halide's single-frame RAW instead, or
  you'll be measuring Apple's noise reduction.
- **Pocket 3 and Action 5 Pro:** JPEG or raw DNG. The Pocket 3's stills are only about
  9.4 MP (1:1) or 8.3 MP (16:9).

## Common mistakes

- **Thinking raw can rescue anything.** Clipped highlights stay clipped, and pushed
  shadows still get noisy. Expose well, and treat the latitude as a safety margin.
- **Judging the raw by the camera's preview.** That's a processed JPEG. Open the raw in
  your developer before deciding a frame is ruined.
- **Expecting a raw file to look finished when it first opens.** The developer's
  starting rendering often looks flatter than the camera's JPEG. That's where editing
  starts, not a fault.
- **Deleting raws to save space.** The raw is your original. Delete the JPEG copies
  instead.

## Try it

Twenty minutes on the L10, set to RAW + JPEG:

1. Indoors under warm lamps, set white balance to daylight (sunny) and take a photo. It
   will look orange.
2. From inside a dim room, photograph a bright window, exposed for the room, so the
   window turns white.
3. In your raw developer, fix the first photo's white balance and pull back the window
   in the second. Do it on the raw, then on the JPEG, and compare at 100%. Note where
   the JPEG gives up first.

This previews **A1.3** (pushing shadows) and **A4.2** (recovery limits).

## Check yourself

> [!question]- Under warm lamps with white balance on daylight, why does the raw fix cleanly but the JPEG doesn't?
> In the raw file, white balance is only a number in the metadata, so the developer
> re-renders the colours from the original data. The JPEG's colours were already
> shifted and rounded to 8 bits, so correcting them stretches limited data.

> [!question]- The camera's highlight warning blinks on a cloud. Is the raw file definitely clipped?
> Not necessarily. The warning comes from the processed JPEG preview, which turns
> highlights white a little early, so the raw may hold some detail. If the sensor itself
> clipped, though, nothing will bring it back.

> [!question]- Why does lifting shadows by two stops cause banding in a JPEG but not in a 14-bit raw?
> The JPEG has only 256 levels per colour, and few of them sit in the shadows.
> Stretching them leaves visible steps. The raw has 16,384 levels, so there are enough
> in-between values to stay smooth.

> [!question]- Why is ProRAW a poor choice for A1.3's ISO ladder?
> ProRAW is merged from several frames and already noise-reduced, so its noise doesn't
> show what the sensor does at each ISO. A single-frame raw from Halide does.

## Related
[[Bit-Depth]] · [[Dynamic-Range]] · [[White-Balance]] · [[Histogram]] ·
[[Computational-Photography]] · [[Camera-Menu-Baseline]] ·
[[Non-Destructive-Editing]] · [[Fundamentals-Index]]
