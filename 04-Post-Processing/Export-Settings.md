---
title: Export Settings
type: concept
module: 4
tags:
  - post/output
created: 2026-10-22
---
# Export Settings

> [!summary] In one line
> Exporting makes a new file for one purpose: the web, a print or the archive. Choose
> the format, quality, colour space, size, sharpening, metadata and name for that
> purpose, and save each set of choices as a preset.

## What it is

Your edits live with the raw file, which never changes. → [[Non-Destructive-Editing]]
Exporting renders a new file from the raw plus your edits: a copy made for one
destination. You can export again at any time, with different settings.

Every export makes seven decisions:

| Decision | The question it answers |
|---|---|
| Format | Which file type will the destination open? |
| Quality | How much compression is acceptable? |
| Colour space | Which colours will the viewer's screen or printer expect? |
| Size | How many pixels does the destination need? |
| Output sharpening | Which medium will it be seen on? |
| Metadata | What information travels with the file? |
| File name | Will you find it again? |

## How it works

### Format

| Format | What it is | Use it for | Watch out for |
|---|---|---|---|
| JPEG | 8-bit, lossy compression | Web, social, most print labs | Re-saving loses quality each time |
| HEIC / HEIF | 8- or 10-bit, lossy, smaller than JPEG at the same quality | Apple devices, phones | Not every app or website opens it |
| PNG | Lossless, 8- or 16-bit | Screenshots, graphics, text | Huge files for photos |
| TIFF | Lossless, 8- or 16-bit | Print masters, layer editors, archive | Very large files |

Newer web formats such as AVIF and WebP exist. JPEG is still the safe default.

### Quality

Lossy compression throws away the detail your eye is least likely to miss. On a 0–100
quality scale, around 80–90 usually looks almost the same as 100 in a much smaller
file. Go too low and smooth skies turn blocky and fine texture smears. Every time a
JPEG is opened and saved again, it's compressed again, so always export from the
master.

### Size

Size is set as the **long edge in pixels**. The L10's 3:2 frame is 5408 px wide. A web
export at 2048 px keeps about a seventh of the pixels, which is plenty for any screen.
Social platforms resize large uploads with their own settings, so a full-size upload
gains nothing. Check each platform's current recommended size, because they change.

For print, the pixels you need are the print size in inches times the resolution: an
A4 print at 300 ppi needs about 2480 × 3508 px. → [[Printing]]

### Colour space

sRGB for the web, whatever the lab asks for when printing, and a wide space in 16-bit
for archive masters. Always embed the profile. → [[Colour-Spaces]]

### Output sharpening

Resizing and printing soften the image, so exporters sharpen after resizing. Lightroom,
for example, sharpens for screen, matte paper or glossy paper, at low, standard or high
strength. → [[Sharpening]]

### Metadata

A photo carries hidden information: camera settings, your copyright and contact
details, keywords, and often the **GPS location** where it was taken.

- **Copyright:** add your name to every export. Set it once in a preset.
- **Location:** phones usually record where each photo was taken. A photo taken at
  home tells anyone where you live. Remove location from anything public. Some
  platforms strip metadata themselves; don't rely on it.

→ [[Copyright-and-Consent]]

### File names

Use one pattern: date, subject, number, then the purpose. For example,
`2027-02-10-tiong-bahru-012-web.jpg`. Dates first sort in time order, and hyphens
instead of spaces keep names safe for every system.

## How to use it

Make three presets once, then use them every time:

| Preset | Format | Colour space | Size | Sharpening | Metadata |
|---|---|---|---|---|---|
| Web and social | JPEG, quality 80–90 | sRGB | 2048 px long edge, or the platform's size | Screen, standard | Copyright; location removed |
| Print (lab) | JPEG at quality 100, or 16-bit TIFF if accepted | What the lab asks for, often sRGB | Print size × 300 ppi | Matte or glossy, to match the paper | Copyright |
| Archive master | 16-bit TIFF | Adobe RGB or ProPhoto RGB | Full size | None | All |

1. **Export into a folder named for the purpose,** such as `exports/web`, so versions
   don't mix.
2. **Check one export on the device it's for.** Look at the web version on your phone.
3. **Never edit an export.** Change the master and export again.

Video exports follow different rules. → [[Video-Export-Settings]]

## On your kit

- **Lumix L10:** RW2 masters with lots of pixels, so every preset has headroom.
- **iPhone 15 Pro Max:** HEIC files don't open everywhere. Export JPEG when you share
  beyond Apple devices. Its photos are in Display P3: convert to sRGB for the web, and
  remove the location. Its HDR photos look HDR only on HDR screens; for most sharing,
  export a normal JPEG.
- **Pocket 3:** stills are 3072 × 3072 (1:1) or 3840 × 2160 (16:9). A 2048 px web
  export is no problem; large prints are where pixels run short.
- **Action 5 Pro:** wide 40 MP frames, often of water and sport. Use the web preset for
  sharing; crop first if the fisheye edges distract.

## Common mistakes

- **Uploading full size at quality 100 to social media.** The platform shrinks and
  recompresses it anyway. Export at its size yourself.
- **Editing and re-saving a JPEG export.** It loses quality each time. Go back to the
  master.
- **Leaving the location in.** It can reveal where you live. Remove it in the preset.
- **Exporting Adobe RGB or ProPhoto for the web.** Many viewers show it dull. Use sRGB.
- **Sharpening before resizing, or not at all.** Use the exporter's output sharpening,
  which runs after the resize.
- **Random file names.** You'll never find the print version again. Use one pattern.

## Try it

Twenty minutes:

1. Build the three presets above in your editor.
2. Export one finished photo through each. Compare the file sizes.
3. Look at the web version on your phone. Is it sharp enough? Too sharp?
4. Open the web file's info or properties and confirm there's no GPS position.

In **A0.2** you exported one JPEG. These presets are the grown-up version, ready for the
**A4.5** set and the **A4.6** print.

## Check yourself

> [!question]- Why export 2048 px instead of full size for social media?
> The platform resizes and recompresses large uploads with its own settings. Exporting
> at the right size yourself keeps control of the resize and the sharpening.

> [!question]- Why export from the master each time, instead of resizing an old JPEG?
> Each JPEG save compresses again and loses more. The master holds all the data, and
> each purpose needs its own size, colour space and sharpening.

> [!question]- You post a photo taken in your flat. What should you strip from the file, and why?
> The GPS location. Phones usually record it, and it shows anyone where the photo was
> taken: in this case, where you live.

> [!question]- How many pixels does an A4 print at 300 ppi need?
> A4 is about 8.3 × 11.7 inches. Times 300 ppi, that's about 2480 × 3508 px.

## Related
[[Sharpening]] · [[Colour-Spaces]] · [[Printing]] · [[Non-Destructive-Editing]] ·
[[Archive-Strategy]] · [[Copyright-and-Consent]] · [[Post-Processing-Index]]
