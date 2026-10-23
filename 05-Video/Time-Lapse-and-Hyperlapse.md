---
title: Time-Lapse and Hyperlapse
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-23
---
# Time-Lapse and Hyperlapse

> [!summary] In one line
> A time-lapse takes one frame every few seconds and plays them back at normal speed,
> so minutes become seconds. A hyperlapse does the same while the camera moves.

## What it is

Normal video records 25 frames every second and plays them back at 25 frames a second,
so time runs at its real speed. A **time-lapse** records far fewer frames — one every
1, 2 or 10 seconds — and still plays them back at 25 frames a second. Time speeds up:
clouds race, shadows sweep across a building, a hawker centre fills and empties.

A **hyperlapse** is a time-lapse where the camera also travels between frames: along a
street, across a bridge, round a building. The movement is stretched over a long
distance, so the clip feels like flying.

## How it works

Two numbers decide everything: the **interval** (the time between frames) and the
**playback frame rate** ([[Frame-Rate]]).

- **Speed-up** = interval × playback frame rate. One frame every 2 s, played at 25 fps,
  is 2 × 25 = 50 times faster than real life.
- **Clip length** = number of frames ÷ playback frame rate. A 10-second clip at 25 fps
  needs 250 frames. At a 2 s interval that is 500 s of shooting — just over 8 minutes.

| Subject | Interval to start with | Why |
|---|---|---|
| Fast clouds, busy traffic, crowds | 1–2 s | Things move a lot between frames |
| Slow clouds, sunset, shadows moving | 3–5 s | Change is slow; longer gaps keep it visible |
| Stars turning | 20–30 s (each frame a long exposure) | You need long exposures anyway |
| A plant opening, a building going up | Minutes to hours | The change itself is very slow |

**Smooth or jerky?** Each frame is a still. If the shutter is very fast, every frame is
crisp, and moving things seem to jump from place to place. A longer shutter adds motion
blur to each frame, which joins the jumps up — the same idea as the 180° rule in
[[Shutter-Angle]]. A common starting point is a shutter of about half the interval: at a
2 s interval, about 1 s. In daylight that needs a small aperture, a low ISO or an ND
filter ([[ND-Filters]]); at dusk it happens naturally, and car lights turn into trails.

**Flicker.** Played fast, tiny differences between frames become visible pulsing. Auto
exposure, auto white balance and autofocus all change a little from frame to frame.
That is why a time-lapse is shot with everything locked.

## How to use it

1. **Support the camera.** A tripod, a wall, a beanbag. It must not move at all between
   frames — unless you're making a hyperlapse.
2. **Lock everything:** manual exposure, a fixed white balance (not auto), manual or
   locked focus. → [[White-Balance]] · [[Manual-Focus]]
3. **Choose the interval** from the table, then work out how long to shoot. For a
   10-second clip: 250 frames × the interval.
4. **Set the shutter** to about half the interval for smooth motion, if the light allows.
5. **Check battery and card space.** A long time-lapse can run for an hour.
6. **Make the video.** Phones and the DJIs build the clip themselves. If you shoot a
   sequence of photos instead, import them into your editor as an image sequence at
   25 fps. → [[Video-Editing-Workflow]]

**Hyperlapse by hand:** pick a point far ahead to aim at. Take a frame, step forward the
same distance (say half a metre), aim at the same point, take the next frame, and so on.
Stabilisation in the editor smooths what's left. → [[Video-Stabilisation]]

**Day to night is the hardest case.** The light falls by many stops, so locked exposure
fails. Shooting it well (changing exposure in small, smooth steps, then removing flicker
in editing) is an advanced skill; start with scenes where the light stays steady.

## On your kit

- **iPhone 15 Pro Max:** Apple's Camera app has a Time-lapse mode. It chooses the
  interval and exposure for you. Use the AE/AF lock (press and hold) to stop exposure
  changes, and keep the phone on a support.
- **Pocket 3 and Action 5 Pro:** both have built-in time-lapse and hyperlapse modes;
  check each manual for the mode names and settings. Pro / PRO mode lets you lock
  exposure. The Pocket 3's gimbal keeps a handheld hyperlapse steady.
- **Lumix L10:** check the manual for an interval or time-lapse shooting setting. If it
  has one, it gives you raw files for every frame, which grade far better than a phone
  clip. Its 60 s mechanical shutter suits star time-lapses.

## Common mistakes

- **Leaving anything on auto.** Exposure, white balance or focus changes cause flicker.
  Lock all three.
- **An interval too long for the subject.** People and cars jump instead of flow. Use
  1–2 s for fast subjects.
- **A very fast shutter.** Every frame is frozen, so movement looks jerky. Aim for about
  half the interval.
- **Not shooting long enough.** Ten seconds of clip at a 3 s interval is 12½ minutes of
  shooting. Plan the time before you start.
- **Midday in Singapore.** The sun is almost overhead and nothing changes much. Late
  afternoon into dusk gives moving shadows and a sky that changes colour.

## Try it

Twenty minutes, at dusk:

1. Put the iPhone on a support facing a busy road or a cloudy sky, lock exposure, and
   record a 10-minute time-lapse.
2. Then set a DJI or the L10 to a 2 s interval with locked manual exposure and white
   balance, and shoot the same scene.
3. Compare: which is smoother, which flickers, and why?

A good time-lapse makes a strong opening or transition shot in your **A5.6** film.

## Check yourself

> [!question]- You shoot one frame every 3 s for 10 minutes and play it at 25 fps. How long is the clip, and how much faster than real life?
> 600 s ÷ 3 s = 200 frames. 200 ÷ 25 fps = 8 seconds of clip. It runs 3 × 25 = 75 times
> faster than real life.

> [!question]- Why does auto exposure make a time-lapse flicker?
> The camera sets a slightly different exposure for each frame. Played back fast, those
> small differences become a visible pulsing in brightness.

> [!question]- The clouds in your time-lapse look jerky. Give two fixes.
> Use a shorter interval, so the clouds move less between frames, and a longer shutter
> (about half the interval), so each frame carries some motion blur.

> [!question]- What makes a hyperlapse harder than a time-lapse?
> The camera moves between frames, so each frame must be aimed at the same point and
> taken the same distance apart, and the result usually needs stabilising.

## Related
[[Frame-Rate]] · [[Shutter-Angle]] · [[Long-Exposure]] · [[ND-Filters]] ·
[[Video-Stabilisation]] · [[Camera-Movement]] · [[Video-Editing-Workflow]] ·
[[Video-Index]]
