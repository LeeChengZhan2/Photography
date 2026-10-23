---
title: Shutter Angle
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-22
---
# Shutter Angle

> [!summary] In one line
> Shutter angle describes the shutter speed as a share of each frame's time. The 180°
> rule, a shutter of about 1/(2 × frame rate), gives motion the amount of blur that
> looks natural, so in video the frame rate, not the light, sets the shutter.

## What it is

In stills you choose the [[Shutter-Speed]] to suit the light and the movement. In video
the [[Frame-Rate|frame rate]] makes most of that choice for you.

Shutter angle is a way of writing the shutter speed relative to the frame rate. The name
comes from film cameras. Their shutter was a spinning disc with a slice cut out. With a
half-disc opening (180°), each frame of film was exposed for half of its time.

The **180° rule**: set the shutter to one over twice the frame rate.

| Frame rate | 180° shutter |
|---|---|
| 24 fps | 1/48 s (most cameras offer 1/50 s) |
| 25 fps | 1/50 s |
| 30 fps | 1/60 s |
| 50 fps | 1/100 s |
| 60 fps | 1/120 s (or 1/125 s) |

## How it works

### The sum

Each frame at 25 fps lasts 1/25 s. A 180° shutter is open for half of that time:

- shutter time = (angle ÷ 360) × (1 ÷ frame rate)
- 180° at 25 fps = ½ × 1/25 = 1/50 s; 90° at 25 fps = ¼ × 1/25 = 1/100 s
- angle = 360 × frame rate × shutter time: at 25 fps and 1/500 s, 360 × 25 ÷ 500 = 18°

### Why 180° looks natural

Every frame holds a little motion blur. When the frames play, that blur bridges the jump
from one frame to the next, and your brain reads smooth movement. At 180° each frame
records the subject's movement for half the time between frames. Most films and TV are
shot this way, so it looks "normal" to us.

Here is the A5.1 ladder at 25 fps:

| Shutter | Angle | Blur in each frame | How the motion feels |
|---|---|---|---|
| 1/25 s | 360° | Long smears | Dreamy and smeary; can look like a mistake |
| 1/50 s | 180° | The usual amount | Smooth and natural |
| 1/100 s | 90° | Half as much | Slightly crisper; few people notice |
| 1/500 s | 18° | Almost none | Choppy: movement jumps from frame to frame |
| 1/2000 s | 4.5° | None | Very choppy: a string of frozen snapshots |

A fast shutter freezes every frame. Nothing bridges the gaps, so movement stutters. This
is often called strobing. Some war and action films use it on purpose for a tense,
jittery feel.

A slow shutter smears. Most cameras won't go slower than one over the frame rate in
video, because a frame can't be exposed for longer than it lasts.

### Angle or speed: two ways to write the same thing

Cinema cameras and some video apps show the shutter as an angle. Stills-style cameras
show it as a speed. The difference appears when you change the frame rate:

- **In angle notation**, 180° stays 180°. Switch from 25 to 50 fps and the shutter moves
  from 1/50 s to 1/100 s by itself. The motion looks the same, but each frame gets half
  the light: one stop darker.
- **In speed notation**, 1/50 s stays 1/50 s. The brightness stays the same, but at
  50 fps that's now a 360° shutter, with twice the usual blur.

So angle keeps the *look* of motion fixed; speed keeps the *exposure* fixed.

### Flicker under 50 Hz lights

Singapore's mains runs at 50 Hz, so many lights pulse 100 times a second. A shutter that
lasts a whole number of pulses gets the same light in every frame: 1/100 s, 1/50 s and
1/25 s are all safe. 1/60 s lasts about 1.7 pulses, so each frame gets a different
amount of light, and the video flickers.

Your devices also read the sensor row by row (a rolling shutter). With a short shutter,
each row catches a different part of a pulse, so dark bands appear across the frame.
The faster the shutter, the stronger the bands. That's what A5.1 asks you to notice at
1/500 s and 1/2000 s indoors.

## How to use it

1. **Set the frame rate first, then the shutter at 180°:** 1/50 s at 25 fps, 1/100 s at
   50 fps.
2. **Control brightness with everything else:** the aperture (on the L10), ISO, or an
   ND filter. → [[ND-Filters]]
3. **Break the rule on purpose, not by accident:**
   - **Faster (90° or narrower)** for a crisp, nervous feel in action or sport, or when
     you want sharp single frames to pull out as stills.
   - **1/50 s at 30 fps** (216°) under mains lights, when you must shoot 30 fps. A bit
     more blur than 180°, but no flicker.
   - **Slower (up to 360°)** for a dreamy look, or to gain one stop of light at night.
4. **If you can't hold 180° in daylight, choose a faster shutter knowingly.** Write it
   in the shoot log, with what it did to the motion.

## On your kit

- **iPhone 15 Pro Max:** Apple's Camera app sets the shutter for you. With fixed
  apertures and no ND, in daylight it can only use a fast shutter, so motion gets
  choppy. For a fixed 1/50 s, use a video app such as Blackmagic Camera.
- **Pocket 3 and Action 5 Pro:** fixed apertures too. Set the shutter in Pro / PRO mode.
  On auto they have to choose fast shutters in bright light, for the same reason.
- **Lumix L10:** the only device with an adjustable aperture, so it can hold 1/50 s in
  more light by stopping down. Diffraction softens the picture from about f/5.6–f/8, so
  stopping down only gets you so far.

## Common mistakes

- **Leaving exposure on auto in daylight.** The camera controls brightness with the
  shutter, often at 1/1000 s or faster, and the footage turns choppy. Lock the shutter
  at 180° and control brightness another way.
- **Changing the frame rate but not the shutter.** 50 fps at 1/50 s is a 360° shutter:
  smeary. Move to 1/100 s.
- **Using 1/60 s indoors in Singapore.** It flickers. Use 1/50 s or 1/100 s.
- **Thinking a fast shutter makes video sharper.** Each frame is sharper, but nobody
  watches one frame. The motion looks worse.

## Try it

Fifteen minutes, a small version of **A5.1**, on a device where you can set the shutter
(the Pocket 3 in Pro mode is easiest):

1. At dusk or indoors, set 25 fps. Film a fan or passing traffic for 10 seconds at
   1/50 s.
2. Film it again at 1/500 s, raising ISO to keep the same brightness.
3. Indoors under ceiling lights, film a plain wall at 1/60 s, then at 1/50 s.
4. Watch every clip full screen at full speed. Describe the motion of each in one word,
   and look for bands on the wall.

## Check yourself

> [!question]- You're filming at 50 fps. What shutter is 180°, and what angle is 1/50 s?
> 180° at 50 fps is 1/100 s. 1/50 s at 50 fps is 360 × 50 ÷ 50 = 360°: the shutter is
> open for the whole frame, so motion smears.

> [!question]- Why does footage at 1/2000 s look choppy when every single frame is sharp?
> Because there's no blur to bridge the gaps. Each frame is a frozen moment, and the
> subject jumps to a new position in the next one. Your eye sees the jumps instead of
> smooth movement.

> [!question]- Indoors, 30 fps footage at 1/60 s shows dark bands rolling through it. Name two fixes.
> Keep 30 fps but change the shutter to 1/50 s or 1/100 s, which hold a whole number of
> the lights' pulses. Or switch to 25 fps at 1/50 s, which fixes it and keeps 180°.

> [!question]- A camera shows the shutter as an angle. You switch from 25 to 50 fps at 180°. What happens to the brightness?
> It drops by one stop. At 180° the shutter moves from 1/50 s to 1/100 s, so each frame
> gets half the light. Fix it with ISO, the aperture or a weaker ND, not the shutter.

## Related
[[Shutter-Speed]] · [[Frame-Rate]] · [[ND-Filters]] · [[Exposure-Triangle]] ·
[[Zebras-and-Waveform]] · [[Video-Stabilisation]] · [[Video-Index]]
