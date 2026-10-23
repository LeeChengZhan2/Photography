---
title: Shot Matching
type: concept
module: 5
tags:
  - video/colour
created: 2026-10-22
---
# Shot Matching

> [!summary] In one line
> Shot matching makes clips from different cameras, or different moments, look like one
> film. Correct each clip first (exposure, white balance, contrast), match them all to
> one reference clip, and only then grade the whole film.

## What it is

When you cut between two clips, the viewer compares them. If one is warmer, brighter or
more saturated, the cut "jumps", even when the framing is perfect. Matching removes
those differences. It happens in two passes:

| Pass | Works on | Goal | Example |
|---|---|---|---|
| **Correction** | Each clip on its own | Neutral and consistent | Remove a blue cast, brighten a dark clip |
| **Grade** | The whole film at once | A look | Warm, soft contrast for a morning film |

Correction makes the clips agree. The grade then gives them all the same personality.
→ [[Colour-Grading]]

## How it works

**A technical LUT converts the encoding, not the camera.** Log footage is recorded with
a flat curve so it can hold more dynamic range. A technical LUT (a table that converts
every colour to another) undoes one camera's log curve and colour space, and maps them
to **Rec.709**, the standard for normal screens. → [[LUTs]]

What the LUT leaves alone:

- **The sensor's colour response.** Each sensor's colour filters see colours slightly
  differently, especially greens, skin and saturated reds.
- **The maker's taste.** Each maker designs its own LUT to look right to them: its own
  contrast, saturation and skin rendering.
- **Your settings.** Differences in white balance and exposure pass straight through.
- **The lens and the sensor size:** contrast, flare, vignetting, noise and depth of
  field.

So a Pocket 3 clip and an iPhone clip, each through its own maker's LUT, both arrive in
Rec.709 and still don't match. The LUTs got them speaking the same language. They
didn't make them say the same thing.

**Correct before you grade, because a grade amplifies differences.** A look adds
warmth, contrast or a colour shift to whatever it's given. Two clips that differ a
little underneath come out of the same look differing more. So the clips must agree
first. With log footage, fix exposure and white balance *before* the technical LUT:
the LUT can only respond to the values it's handed.

**Scopes measure what your eyes adapt to.** After a minute of looking at a warm clip,
your eyes accept it as neutral. Scopes don't adapt. → [[Zebras-and-Waveform]]

| Scope | What it shows | Use it to match |
|---|---|---|
| **Waveform** | Brightness across the frame: black at the bottom, white at the top | Exposure and contrast |
| **RGB parade** | The waveform split into red, green and blue, side by side | White balance |
| **Vectorscope** | Colour as a circle: direction is hue, distance from the centre is saturation | Hue and saturation, especially of skin |

On the RGB parade, something white or grey should show the three channels at the same
height. If red sits higher than blue, the clip is warm. On the vectorscope, neutral
things sit in the centre. Skin of every colour tends to fall near one line between red
and yellow, often called the **skin-tone line**.

## How to use it

### Match at capture first

Grading can't fix what the cameras didn't record. For a scene you'll cut between
cameras:

- Use the same frame rate and shutter speed on every camera. → [[Frame-Rate]]
- Set white balance manually, to the same value, on every device that allows it. Auto
  white balance drifts during a shot and differs between cameras.
- Shoot all in log, or all in the normal profile. Not a mix.
- At the start, film a **reference frame** on every camera: the same scene with a sheet
  of white paper and your hand in it. The paper is a neutral; the hand is skin.

A **colour chart**, a card of printed patches with known colours, does the same job
more precisely. Resolve's Color Match can read some charts and correct a clip
automatically. Paper and a hand are a free start.

### Matching in the editor, step by step

1. **Put the clips on one timeline** in the order they'll cut.
2. **Choose a reference clip:** the camera with the most shots, or the best-looking
   one. Match everything to it.
3. **Convert the log clips.** Fix exposure and white balance first, then apply each
   camera's own technical LUT (or a colour-space transform).
4. **Match exposure** on the waveform: put the same thing, such as the paper or a face,
   at the same height in every clip.
5. **Match white balance** on the RGB parade: line up the three channels on the paper.
6. **Match contrast:** put the darkest and brightest parts at similar heights.
7. **Match saturation and hue** on the vectorscope: skin on the skin-tone line, at the
   same distance from the centre.
8. **Compare by eye.** Split the screen or wipe between the clip and the reference. In
   Resolve, grab a still of the reference and wipe across it.
9. **Grade once.** Apply one look to every clip together: an adjustment layer in most
   editors, or a timeline-level grade in Resolve. Then check each cut again.

## On your kit

| Device | Log for grading | Its technical LUT | Watch for |
|---|---|---|---|
| **Lumix L10** | V-Log | Panasonic's V-Log → V-709 LUT, or a colour-space transform | V-Log starts at ISO 500 |
| **iPhone 15 Pro Max** | Apple Log (ProRes only) | Apple's Log → Rec.709 LUT, or a colour-space transform | Normal video is HDR by default |
| **DJI Pocket 3** | 10-bit D-Log M | DJI's Pocket 3 LUT | Not the Action 5 Pro's LUT |
| **DJI Osmo Action 5 Pro** | 10-bit D-Log M | DJI's Action 5 Pro LUT | The fisheye bend in Ultra Wide |

- **Same log name, different LUTs.** Both DJIs shoot D-Log M, but DJI publishes a
  separate LUT for each. The wrong one looks plausible and is quietly wrong.
- **The iPhone's normal video is HDR.** In an SDR timeline it sits wrong next to the
  others, with flat highlights and shifted colours. Turn HDR off in the iPhone's camera
  settings before you shoot, or convert those clips to SDR Rec.709 first.
  → [[Video-Export-Settings]]
- **Use Standard (Dewarp) on the Action 5 Pro** next to the other cameras. Lines that
  bend in one camera and not the next make the cut jump, whatever the colour.
- **Four sensor sizes:** Four Thirds, 1-inch, 1/1.3-inch and the iPhone's 1/1.28-inch
  main camera. Noise and depth of field will differ, and grading can't change either.
  Get them closer at capture with light and distance, or accept them.

## Common mistakes

- **Expecting each maker's LUT to make the cameras match.** It only converts each one
  to Rec.709. Match them afterwards, by eye and with scopes.
- **Grading before correcting.** A look on top of mismatched clips makes the mismatch
  bigger. Correct and match first.
- **Matching by eye alone.** Your eyes adapt to whatever you've been staring at. Check
  with the RGB parade and the vectorscope.
- **Leaving white balance on auto.** It shifts mid-shot and differs between cameras.
  Set it manually, the same on every device.
- **Mixing HDR and SDR clips without converting.** The iPhone's HDR clips will never
  match the others until they're converted to SDR.

## Try it

Thirty minutes, a small version of **A5.5**:

1. Tape a sheet of white paper to a wall near a window. Film it, with your hand in
   front, for ten seconds on two devices, such as the Pocket 3 and the iPhone, at the
   same frame rate.
2. Put both clips on one timeline. Convert any log clip with its own technical LUT.
3. Match the second clip to the first: exposure on the waveform, white balance on the
   RGB parade, skin on the vectorscope.
4. Cut between them every two seconds. Keep adjusting until the cut stops jumping.
5. Write down what you couldn't match, and why.

## Check yourself

> [!question]- Your Pocket 3 and iPhone filmed the same scene in log, and each clip got its maker's Rec.709 LUT. Why don't they match?
> A technical LUT only undoes one camera's own log curve and colour space, so both end
> up in Rec.709. It doesn't change how each sensor saw colour, each maker's taste in
> contrast and skin, or your white balance and exposure. Those you match by hand.

> [!question]- Why correct and match the clips before you apply the film's look?
> A look builds on what it's given, so small differences between clips come out bigger.
> When the clips agree first, one look gives them all the same result.

> [!question]- On the RGB parade, a white wall shows the red channel higher than the blue. What's wrong, and which way do you adjust?
> The clip is too warm. Cool the white balance, towards blue, until the three channels
> sit at the same height on the wall.

> [!question]- The colours now match, but the cut between the Action 5 Pro and the L10 still jumps. What else could it be?
> Things grading can't change: the Action 5 Pro's fisheye bend in Ultra Wide, different
> depth of field or noise from the different sensor sizes, a different shutter speed
> changing the motion blur, or a different frame rate.

## Related
[[LUTs]] · [[Colour-Grading]] · [[Zebras-and-Waveform]] · [[Log-Profiles]] ·
[[White-Balance]] · [[Colour-Spaces]] · [[Video-Export-Settings]] · [[Video-Index]]
