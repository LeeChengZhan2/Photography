---
title: Zebras and Waveform
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-22
---
# Zebras and Waveform

> [!summary] In one line
> Zebras, the waveform, false colour and the histogram measure brightness as numbers,
> so you can expose video correctly whatever your screen shows. They're the video
> cousins of the stills histogram.

## What it is

Four exposure tools you'll meet in video cameras and apps:

| Tool | What it shows | Best for |
|---|---|---|
| Zebras | Stripes over every area brighter than a level you set | Clipping warnings and skin |
| Waveform | The brightness of every part of the frame, left to right | Seeing which part is how bright |
| False colour | The picture recoloured by brightness | A quick read of faces and highlights |
| Histogram | How many pixels sit at each brightness | The overall spread; clipping at either end |

Video tools measure brightness in percent, sometimes called IRE. 0% is black. 100% is
the top of the normal range: in a standard profile, the brightest white before detail
is lost.

## How it works

### Why video needs these more than stills

- **Most video isn't raw.** A highlight that clips at capture is gone. You can't pull it
  back later.
- **A clip has to work for its whole length.** You can't fix exposure frame by frame.
- **Screens lie.** In Singapore's midday sun a screen looks dim, so you brighten the
  picture until it looks right, and the file comes out overexposed. The numbers don't
  care how bright the screen is.

### Zebras

The camera draws moving diagonal stripes over every area brighter than the level you
set. Two levels do two different jobs:

- **About 95–100%: a clipping warning.** Stripes mean "this area is at or near pure
  white". Any detail there is gone, or nearly gone.
- **About 70%: a skin guide.** On a light-skinned face, stripes just appearing on the
  brightest parts (forehead, cheekbones, nose) usually mean a good exposure in a
  standard profile. Darker skin looks right lower down, often somewhere around 45–60%.

The exact number matters less than using the same one every time. Some cameras let you
set two zebra levels at once.

### Waveform

Imagine squashing the frame flat from top to bottom. The waveform keeps the frame's
left-to-right order, but plots each point's brightness upwards: 0% at the bottom, 100%
at the top.

An example. A person stands on the left third of the frame, against a bright window on
the right. The waveform shows:

- on its left third, a cluster around 60–70%: the face;
- on its right side, a band near 100%: the window;
- if that band is pressed flat against the top line, the window has clipped.

That is what a histogram can't tell you: *where* in the frame each brightness is.

### False colour

False colour replaces the picture with a colour code for brightness. A typical scheme
shows near-black as blue or purple, mid-grey as green, skin tones as pink, and areas
close to clipping as yellow, then red. The colours differ between makers, so check the
key before you trust it.

### Histogram

The same graph you know from stills: dark tones on the left, bright on the right, and
the height shows how many pixels sit at each level. A tall spike pressed against the
right edge means clipping. → [[Histogram]]

### In a log profile, the numbers change

A log profile records a flat image, so every tone reads lower and closer together. A
face that sits at 70% in a standard profile reads lower in log, and white may never
reach 100%. Use the maker's exposure guidance for log, or check whether the camera can
measure the picture after a viewing LUT. → [[Log-Profiles]]

## How to use it

1. **Default: zebras at about 95–100%.** Leave them on as a clipping alarm.
2. **For a face, switch to your skin level** (about 70% for light skin), or read the
   face on the waveform.
3. **Expose for what matters most, usually the face.** Then check the highlights. If a
   window or sky clips, choose: let it go, reframe, add light to the subject, or move
   them.
4. **Keep faces at the same level from shot to shot.** It's the simplest way to make
   shots cut together. Write the level in the shoot log, for example "face 65%".
5. **Lock exposure once it's set.** Auto exposure keeps adjusting: someone in a white
   shirt walks past and the whole picture dims.

The rule of thumb: let a bright background clip before you let a face go dark, because
viewers look at faces first.

## On your kit

Which of these tools each device shows, and where, depends on the device and the app.
Before week 17, look through each one's display or exposure-assist settings and note
what it offers. A few points hold whatever you find:

- **iPhone 15 Pro Max:** in Apple's Camera app, press and hold on the face to lock focus
  and exposure (AE/AF LOCK), then drag the sun icon to adjust. That stops the face's
  brightness drifting during a shot. If you want zebras or a waveform, look in a
  dedicated video app such as Blackmagic Camera.
- **Pocket 3 and Action 5 Pro:** in Pro / PRO mode you set the shutter and ISO yourself.
  Use whatever exposure tool the device shows to check the result before you roll.
- **Lumix L10:** if you shoot V-Log, the standard skin targets don't apply. Follow
  Panasonic's guidance for V-Log.
- **On any device without these tools,** film a short test and check it on your
  editor's scopes. Most video editors, including DaVinci Resolve and Premiere Pro, have
  a waveform.

## Common mistakes

- **Judging exposure on the screen in bright sun.** The screen looks dim, so you
  overexpose. Trust the zebras, waveform or histogram.
- **Forgetting which zebra level is set.** Stripes at 70% are a skin guide, not a
  clipping warning. Know which one you're looking at.
- **Exposing to save the sky and losing the face.** A dark face lifted later turns
  noisy. Expose for the face, then deal with the sky.
- **Using standard targets on log footage.** Log reads lower and flatter. Follow the
  maker's guidance.
- **Leaving auto exposure on during a shot.** The brightness pumps as things move
  through the frame. Lock it.

## Try it

Fifteen minutes, with a friend and a window:

1. Seat them side-on to a window. With zebras at your skin level (about 70% for light
   skin) or the waveform, expose so the stripes just touch the brightest part of the
   face. Note the level.
2. Film 10 seconds. Turn them to face the window and film again. Then turn them away
   from it and film once more.
3. Each time, bring the face back to the same level before you record.
4. Cut the three clips together. If you held the level, the face shouldn't jump in
   brightness at the cuts.

This is the habit **A5.5** depends on: the same face level on every camera.

## Check yourself

> [!question]- What does a waveform tell you that a histogram can't?
> Where each brightness is in the frame. A histogram counts pixels at each level but
> throws away their position. A waveform keeps the left-to-right position, so you can
> see that it's the window on the right that clips, not the face on the left.

> [!question]- Zebras at 100% show stripes on a white shirt but not on the face. Is that a problem?
> Only if the shirt's detail matters. Those areas are at or near pure white, so their
> texture is gone. If the face is right, you'd usually accept it. If the shirt matters,
> lower the exposure a little or add light to the face.

> [!question]- Two shots of the same person: the face sits at 70% in one and 50% in the other. What happens when you cut between them?
> The face jumps in brightness at the cut, and the viewer notices the edit. You can
> correct it in the edit, but that costs time and adds noise to the darker clip.
> Matching the level on location is cheaper.

> [!question]- Why are the standard skin targets wrong for log footage?
> Log records a flat curve, so every tone reads lower and closer together. A face that
> belongs at 70% in a standard profile reads lower in log. The maker's log guidance
> replaces the standard numbers.

## Related
[[Histogram]] · [[Expose-to-the-Right]] · [[Dynamic-Range]] · [[Log-Profiles]] ·
[[Shot-Matching]] · [[Exposure-Compensation]] · [[Video-Index]]
