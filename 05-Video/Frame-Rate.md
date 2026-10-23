---
title: Frame Rate
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-22
---
# Frame Rate

> [!summary] In one line
> Frame rate is how many still pictures a video records each second. It decides how
> motion looks, which shutter speeds make sense, and how far you can slow a clip down.

## What it is

Video is a quick series of still photos. Each one is a **frame**. The frame rate is how
many frames the camera records per second, written as fps (frames per second). Played
back fast enough, the frames blend into smooth movement.

| Frame rate | Where it comes from | How it looks |
|---|---|---|
| 24 fps | Cinema | The "film look". A slight stutter on fast pans |
| 25 fps | TV in 50 Hz countries (PAL) | The same as 24 to almost everyone |
| 30 fps | TV in 60 Hz countries (NTSC); much web video | A touch smoother than 24 or 25 |
| 50 fps | Sport and live TV in 50 Hz countries | Very smooth, a "live TV" look; or 2× slow motion |
| 60 fps | Sport, live TV and games in 60 Hz countries | Very smooth; or slow motion |
| 120 fps | Slow motion | Rarely watched at real speed; about 5× slower on a 25 fps timeline |

Many cameras label 24 fps as 23.98 and 30 fps as 29.97. These odd numbers are a
leftover from colour TV in 60 Hz countries. Treat 23.98 as 24 and 29.97 as 30.

## How it works

### Two TV traditions

Early TV matched its timing to the mains electricity: 25 and 50 fps (PAL) in 50 Hz
countries such as Singapore, 30 and 60 fps (NTSC) in 60 Hz countries such as the US.
Cinema had settled on 24 fps in the late 1920s, when films gained sound. The internet
plays all of these, but in Singapore the tradition still matters because of the lights.

### Why 50 Hz lights push you to 25 or 50 fps

Singapore's mains runs at 50 Hz. Many lights, such as fluorescent tubes and cheap LEDs,
pulse brighter and dimmer 100 times a second. Your eyes don't notice. The camera does.

In video, the frame rate usually sets the shutter speed: about 1/(2 × frame rate), the
180° rule from [[Shutter-Angle]]. Compare those shutters with the 1/100 s pulse:

| Frame rate | Usual shutter | Pulses caught per frame | Under 50 Hz lights |
|---|---|---|---|
| 25 fps | 1/50 s | Exactly 2 | Steady |
| 50 fps | 1/100 s | Exactly 1 | Steady |
| 30 fps | 1/60 s | About 1.7 | Flicker or rolling bands |
| 60 fps | 1/120 s | About 0.8 | Flicker or rolling bands |

When every frame catches a whole number of pulses, every frame gets the same light. When
it catches a fraction, some frames get more light than others. Your devices also read
the sensor row by row (a rolling shutter), so different rows catch different parts of a
pulse. That shows as dark bands across the picture.

### Slow motion: record fast, play at normal speed

Real slow motion comes from recording more frames than you play back. Record at 50 fps,
put the clip on a 25 fps timeline, and slow it to 50%. The editor now shows every
recorded frame, so one second of action lasts two seconds. Every frame is real, so the
motion stays smooth.

| Recorded at | Speed on a 25 fps timeline | How much slower |
|---|---|---|
| 50 fps | 50% | 2× |
| 60 fps | About 42% | 2.4× |
| 100 fps | 25% | 4× |
| 120 fps | About 21% | 4.8× |

Slowing normal footage is different. A 25 fps clip slowed to 50% has only half the
frames it needs. The editor either shows each frame twice, which stutters, or invents
in-between frames by blending or "optical flow". Optical flow can look smooth, but
edges, hands and anything complicated tend to warp. Speeding up is easy: to play a clip
twice as fast, the editor just skips every second frame.

### Mixing frame rates in one project

Set the timeline's frame rate before you edit, usually 25 fps here. A 50 fps clip then
plays at normal speed by skipping every second frame, or slows to 50% cleanly. But 24,
30 and 60 fps don't divide evenly into 25, so the editor repeats or drops a frame at
regular intervals. You see it as a small hitch in pans and steady movement; static
shots hide it.

## How to use it

| You want | Record at | Shutter | Timeline |
|---|---|---|---|
| Normal footage | 25 fps | 1/50 s | 25 fps |
| Smooth action, or the option of 2× slow motion | 50 fps | 1/100 s | 25 fps |
| Strong slow motion | 100 or 120 fps | 1/200 or 1/250 s | 25 fps |

1. **Make 25 fps your default.** It's steady under Singapore's lights and looks like
   cinema to almost everyone.
2. **Use 50 fps when slow motion might help later.** You keep the choice for the edit.
3. **Save 100 or 120 fps for real slow motion** in bright light: a splash, a jump, hair
   turning. The shutter must be about 1/200–1/250 s, two stops or more less light than
   1/50 s, so dim scenes get noisy.
4. **Set every device to the same rate before a shoot.** Check the frame rate, not just
   the resolution. A5.5 depends on it.
5. **Use 30 or 60 fps only on purpose.** Daylight doesn't flicker, so outdoors it's
   fine. Under mains lights, keep the shutter at 1/50 s or 1/100 s, even at 30 fps.

## On your kit

- **All four devices:** set the frame rate in each device's video settings before you
  roll. Check which resolutions offer 50 fps and above. High frame rates often come
  with a lower resolution or a tighter crop.
- **iPhone 15 Pro Max:** 25 fps stays hidden until you turn on Show PAL Formats
  (Settings → Camera → Record Video). Apple's Camera app picks the shutter for you, so
  for a fixed 1/50 s use a video app such as Blackmagic Camera. Internal ProRes stops
  at 4K 30 fps; 4K 60 fps in ProRes needs an external USB-C SSD.
- **Pocket 3 and Action 5 Pro:** set the shutter yourself in Pro / PRO mode. Otherwise
  the camera chooses it.
- **Action 5 Pro:** HorizonSteady (horizon levelling) works only at 1080p or 2.7K 16:9,
  up to 60 fps. Above 60 fps, for slow motion, you lose it.

## Common mistakes

- **Mixing devices set to different rates.** One phone left at 30 fps puts a hitch in
  every pan it filmed. Check every device before you roll.
- **Slowing 25 fps footage and calling it slow motion.** It stutters or warps. Decide
  before you shoot, and record at 50 fps or more.
- **Changing the frame rate but not the shutter.** At 50 fps, 1/50 s gives twice the
  usual blur. Move the shutter to 1/100 s.
- **Shooting 120 fps in dim light.** The fast shutter starves each frame, so ISO climbs
  and noise follows. Keep high frame rates for bright scenes.

## Try it

Fifteen minutes, on any device that records 50 fps and lets you set the shutter:

1. Film the same short action twice, such as pouring water into a glass. First at
   25 fps with 1/50 s, then at 50 fps with 1/100 s.
2. Put both clips on a 25 fps timeline and slow each one to 50%.
3. Compare them full screen. The 50 fps clip stays smooth. The 25 fps clip stutters, or
   warps if the editor invents frames.

A warm-up for **A5.1**, which is shot at 25 fps, and **A5.5**, which needs every camera
at the same frame rate.

## Check yourself

> [!question]- You record at 50 fps and drop the clip on a 25 fps timeline at 100% speed. Is it slow motion?
> No. The editor skips every second frame and plays the clip at normal speed. It
> becomes slow motion only when you slow it to 50%, so that every recorded frame shows.

> [!question]- Why does 1/50 s stay steady under Singapore's indoor lights when 1/60 s flickers?
> The lights pulse 100 times a second. A 1/50 s exposure always holds exactly two
> pulses, so every frame, and every row, gets the same light. A 1/60 s exposure holds
> about 1.7 pulses, so each frame catches a different slice of the cycle.

> [!question]- A friend's phone clips are 30 fps and yours are 25 fps. What happens on a 25 fps timeline?
> The editor drops one frame in every six from the phone clips to fit 25 fps. The drops
> come at regular intervals, so pans and smooth movement in those clips hitch. Ask for
> 25 fps next time, or use their clips only for static shots.

> [!question]- You want 4× slow motion in a 25 fps film. What do you record, and what's the catch?
> Record at 100 fps with a shutter of about 1/200 s, or at 120 fps with 1/250 s for
> 4.8×. The catch is light: the shutter is two stops or more faster than 1/50 s, so you
> need a bright scene or the footage gets noisy.

## Related
[[Shutter-Angle]] · [[Shutter-Speed]] · [[ND-Filters]] · [[Codecs-and-Bitrate]] ·
[[Timeline-and-Trimming]] · [[Video-Export-Settings]] · [[Video-Index]]
