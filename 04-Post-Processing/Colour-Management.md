---
title: Colour Management
type: concept
module: 4
tags:
  - post/colour
created: 2026-10-22
---
# Colour Management

> [!summary] In one line
> The same RGB numbers look different on every screen and printer. Colour management
> translates the numbers for each device, using profiles, so a photo looks as alike as
> possible everywhere. It only works if your own screen is described accurately.

## What it is

A pixel stored as red 200, green 120, blue 80 is just numbers. Each device turns
numbers into colour its own way. One screen is bluer, another brighter; a printer's
inks make different colours again. Send the same numbers to each and you get several
different photos.

Colour management is the system that translates. It needs four parts:

| Part | What it tells the system |
|---|---|
| The image's colour space (an embedded profile, such as sRGB) | What colour the numbers in the file mean |
| A display profile, made by calibrating your screen | How your screen turns numbers into colour |
| A printer profile, one per printer and paper | How that printer on that paper reproduces colour |
| A colour-managed app (raw developer, modern browser) | Does the translation, using the profiles above |

If any part is missing or wrong, the translation is wrong. → [[Colour-Spaces]]

## How it works

### ICC profiles in plain words

A profile is a dictionary between a device's numbers and real, measured colours. "ICC"
is the International Color Consortium, which set the standard file format, so most
software can read any profile.

A conversion is a translation through a shared language. The source profile says "these
numbers mean this real colour". The destination profile says "to show that real colour
here, send these numbers". The app looks up both and converts every pixel.

An app without colour management skips the translation and sends the file's numbers
straight to the screen. On a wide-gamut screen, that makes ordinary photos look
oversaturated.

### Monitor calibration

Calibration has two steps:

1. **Calibrate:** set the screen to known targets for white, brightness and contrast
   curve.
2. **Profile:** measure what the screen actually shows and save it as a profile, which
   the system then uses for every colour-managed app.

Both need a small measuring device, a **colorimeter**, that sits on the screen. Common
targets:

| Setting | Typical target | Why |
|---|---|---|
| White point | D65, about 6500 K | The standard white for sRGB and most screens |
| Tone curve | Gamma 2.2, or the sRGB curve | Matches how most images are encoded |
| Brightness | About 80–120 cd/m² for print work | Close to how bright a print looks under room light |

Brightness is measured in candelas per square metre (cd/m², also called nits). Many
screens ship far brighter than 120. That matters for printing: paper only reflects the
light in the room. Edit on a very bright screen and you'll make the photo too dark, and
the print comes out darker still. → [[Printing]]

Screens drift as they age, so re-measure every month or two.

> [!tip] No colorimeter?
> Windows and macOS both have a built-in visual calibration assistant. It adjusts by
> eye, so it's better than nothing but it isn't a measurement. A camera club may lend
> you a colorimeter. For print brightness, hold a sheet of white paper next to the
> screen under your usual light, and lower the screen until a white page on screen is
> about as bright as the paper.

### Soft proofing

Soft proofing makes the screen imitate a print. The app uses the printer-and-paper
profile to show what will change:

- Paper white is duller than screen white.
- Black becomes dark grey, especially on matte paper.
- Colours outside the printer's range are pulled in. A **gamut warning** can highlight
  them.

You then make a proof copy and adjust it, often a little brighter and with a touch more
contrast, until the simulation looks like your original.

Soft proofing also lets you compare **rendering intents**, the two common rules for
colours that don't fit:

- **Perceptual:** shrinks all colours a little, so out-of-range ones fit and the
  relationships between colours survive. Good for very saturated photos.
- **Relative colorimetric:** keeps every colour that fits exactly and moves only the
  ones that don't to the nearest printable colour. Good for most photos.

Try both on the proof and keep the one that looks closer.

### Viewing conditions

Your eyes adapt to the light around you. A bright window behind the screen makes the
screen look dim. Warm room light makes the screen look blue by comparison. So:

- Edit in steady, moderate light with no strong colour, and nothing bright reflected in
  the screen.
- Keep a neutral grey around the photo in your editor. Most editors use one by default.
- Judge prints under daylight-balanced light, about 5000 K, and near where they will
  hang.

### Phone screen features that shift colour

Phones change their screens on purpose, for comfort:

| Feature | What it does | Effect on judging photos |
|---|---|---|
| Auto-brightness | Follows the room's light | The same photo looks brighter or darker minute to minute |
| True Tone | Shifts the screen's white to match the room's light | Warmer under warm lamps, so your white balance judgement drifts |
| Night Shift | Makes the screen much warmer in the evening | Everything looks orange |

Turn them off in the display settings while you edit or judge colour on the phone, and
back on afterwards. Computers have similar night modes.

## How to use it

1. **Calibrate your main editing screen,** or at least adjust it visually, and set its
   brightness for the work: about 80–120 cd/m² before printing.
2. **Edit in a colour-managed app.** Raw developers are.
3. **Embed the profile on export,** and use sRGB for the web. → [[Export-Settings]]
4. **Soft proof before you print,** with your lab's or printer's profile for that paper.
5. **Judge the print under daylight-balanced light,** not under a warm lamp.
6. **On the phone,** turn off auto-brightness, True Tone and Night Shift while editing.

Aim for close, not identical. A glowing screen and a sheet of paper can never match
exactly; colour management makes the difference small and predictable.

## On your kit

- **iPhone 15 Pro Max:** auto-brightness, True Tone and Night Shift all apply. Its HDR
  photos carry a gain map, so on an HDR screen their highlights can glow brighter than
  the screen's white; on other screens they don't. Its video is HDR (Dolby Vision) by
  default, which also looks different on an SDR screen.
- **The cameras' screens and viewfinders** (L10, Pocket 3, Action 5 Pro) aren't
  calibrated. Use them to frame and read the [[Histogram]], not to judge colour.
- **Your computer screen** is the reference once it's calibrated. Use the phone to check
  how other people will see the photo.

## Common mistakes

- **Editing at full screen brightness.** Prints come out dark. Lower the brightness
  before print work.
- **Judging colour on the camera's screen.** It isn't calibrated. Check the histogram and
  judge colour on the calibrated screen.
- **Leaving True Tone or Night Shift on while editing.** Your white balance drifts with
  the room. Turn them off.
- **Exporting without an embedded profile.** Viewers guess, often wrongly. Embed it.
- **Expecting a perfect screen-to-print match.** Paper reflects; screens glow. Soft
  proof, and make a test print.

## Try it

Twenty minutes, before **A4.6**:

1. Open one photo on the phone. Toggle True Tone and Night Shift and watch the colours
   move. Then turn both off.
2. Do the paper test: white paper next to your computer screen, and lower the screen
   brightness until a white page roughly matches it. Look at your favourite edit again.
   Does it now look too dark?
3. If your print lab offers a profile for its paper, soft proof the photo you plan to
   print and note what changes.

## Check yourself

> [!question]- Two calibrated screens show the same iPhone P3 photo in colour-managed apps, yet one looks more saturated. How can that be?
> Colour management can't show colours a screen can't make. A wide-gamut screen shows
> the photo's most saturated colours; a screen that only covers sRGB has to pull them
> in.

> [!question]- Why do prints edited on a very bright screen come out too dark?
> You set the photo's brightness to look right on a glowing screen. Paper only reflects
> room light, so it looks dimmer. A screen near print brightness makes you brighten the
> edit to match.

> [!question]- What does an ICC profile do, in one sentence?
> It describes how one device's numbers map to real colours, so software can translate
> a photo from one device to another.

> [!question]- The soft proof turns your vivid red sign dull. Why, and what can you do?
> That red lies outside what the printer and paper can reproduce. Try the other
> rendering intent, adjust the proof copy, or try a paper with a wider range.

> [!question]- Why turn off True Tone before judging white balance on the phone?
> True Tone shifts the screen's white to match the room's light. Your judgement of
> white balance would shift with the room, not with the photo.

## Related
[[Colour-Spaces]] · [[Printing]] · [[Export-Settings]] · [[White-Balance]] ·
[[LUTs]] · [[Post-Processing-Index]]
