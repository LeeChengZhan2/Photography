---
title: ISO
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# ISO

> [!summary] In one line
> ISO sets how much the camera brightens the signal after the light has been
> collected. It adds no light, so it can't fix the noise that too little light causes.
> Only more light can.

## What it is

ISO tells the camera how bright to make the photo from a given amount of light. Each
doubling (ISO 100 → 200 → 400) makes the photo one stop brighter. → [[Stops-and-EV]]

People call it "sensitivity", but the sensor's sensitivity never changes. At ISO 100
and at ISO 6400 the sensor collects light in exactly the same way. What changes is the
**gain**: how much the signal is amplified, mostly before it is turned into numbers.
It works like the volume knob on a quiet recording.

## How it works

### Where noise comes from

Light arrives as tiny packets called **photons**. They land at random, like raindrops
on a roof. If a pixel expects 100 photons, it may get 90 in one photo and 110 in the
next. This random spread is called **shot noise**. It belongs to light itself, not to
the camera.

The spread grows more slowly than the signal: it's about the square root of the photon
count. A pixel with 100 photons varies by about ±10, so its **signal-to-noise ratio**
(how far the signal stands above the noise) is 10 : 1, which looks grainy. A pixel with
10,000 photons varies by about ±100, a ratio of 100 : 1, which looks clean. So more
light always gives a cleaner photo. That is the main rule of noise.

The electronics add a little noise of their own every time the sensor is read. This
**read noise** is small, so it only shows in the deepest shadows, where the signal is
tiny too.

### Why high ISO looks noisy

You raise ISO because light is short: a fast shutter, a narrow aperture, a dim room.
Fewer photons reach each pixel, so the shot noise is larger compared with the signal.
ISO then brightens the weak signal and its noise together. The high ISO didn't create
the noise. The lack of light did.

Same scene, same final brightness, made-up round numbers for one mid-grey pixel:

| Settings | Photons collected | Signal-to-noise |
|---|---|---|
| f/4, 1/30 s, ISO 100 | 6,400 | 80 : 1 |
| f/4, 1/500 s, ISO 1600 | 400 | 20 : 1 |
| f/4, 1/2000 s, ISO 6400 | 100 | 10 : 1 |

### Base ISO

Every sensor has a **base ISO**: its lowest native setting, with the least gain. There
each pixel can fill to its full capacity before the file clips (hits pure white), so
you get the most [[Dynamic-Range|dynamic range]]: the widest span from dark to bright
that one frame can hold. Higher ISO makes the file clip with less light, so you lose
highlight room.

"Extended" settings below base, such as ISO 50 on the L10, usually work by
overexposing at base ISO and darkening the result. They cost some highlight room, so
use them only when bright light leaves no other way to get a slower shutter.

### Dual native ISO

Some sensors, often in video-focused cameras, have two base ISOs. Each pixel can switch
between two readout modes: one that holds the most light, for bright scenes, and one
with lower read noise, for dim scenes. Just above the second base ISO, shadows often
look *cleaner* than just below it. The specifications usually say if a camera has it.

### ISO-invariance

On many modern sensors, read noise is so low that it hardly matters *where* the
brightening happens. Raising ISO in the camera, or brightening the same frame in
editing later, gives almost the same noise. Such a sensor is called **ISO-invariant**,
at least above a certain ISO.

What that means for "shoot darker, brighten later":

- **It works for the ISO.** Keep aperture and shutter the same, set a lower ISO, and
  brighten later. The light is the same, so the noise is about the same. In return you
  keep more highlight room for street lamps and neon signs.
- **It does not work for the light.** Underexposing with a faster shutter or a smaller
  aperture collects fewer photons. That photo will be noisier, whatever you do later.
- **You need raw, and the preview looks dark.** Brightening a JPEG by several stops
  breaks it, and a dark preview is harder to judge. → [[RAW-vs-JPEG]]

Not every camera is invariant, and dual-ISO sensors aren't invariant across their
switch point. Test yours (see Try it).

## How to use it

### Auto ISO

With **Auto ISO**, the camera picks the ISO for you, within two limits you set:

- **Maximum ISO:** the highest it may use. Set it to your tested ceiling from A1.3.
- **Minimum shutter speed:** the slowest shutter it accepts before it raises ISO. Pick
  it for the subject: 1/125 s for people standing, 1/500 s for children running.

In A mode the camera then holds your minimum shutter speed by raising ISO as the light
falls. Once ISO hits the maximum, most cameras let the shutter slow down instead. Check
the manual for where to set both limits. → [[Shooting-Modes]]

### Find your usable ceiling (A1.3)

1. Shoot raw. Rest the camera on something steady and frame a scene with dark areas.
2. Shoot one frame at each full stop from base ISO to the maximum. Keep the brightness
   the same by changing the shutter speed.
3. In editing, lift the shadows by +2 stops on every frame.
4. View each at the size you really use: a phone screen, full screen, or a print.
5. Your ceiling is the highest ISO you would still happily share. Write it down and
   make it your Auto ISO maximum.

Past your ceiling, a slightly noisy sharp photo still beats a clean blurred one, and
[[Noise-Reduction]] in editing can buy you more.

## On your kit

- **Lumix L10:** ISO 100–25600, plus an extended ISO 50. Its Four Thirds sensor is the
  largest you own, so at the same settings it collects the most light in total and
  shows the least noise. Check its manual for whether it has dual native ISO.
- **iPhone 15 Pro Max:** Apple's Camera app sets ISO itself; Halide or Lightroom let
  you set it. For A1.3, use Halide's single-frame RAW, not ProRAW, which merges several
  frames and is noise-reduced by Apple (→ [[Computational-Photography]]).
- **Pocket 3:** ISO 50–6400 in Pro mode. It's your best low-light *video* camera; for
  low-light stills, the L10's bigger sensor wins.
- **Action 5 Pro:** ISO up to 25600 in PRO mode, but its smaller sensor gets noisy
  sooner. Expect a lower ceiling than on the L10.

## Common mistakes

- **Thinking high ISO causes noise.** Too little light causes it; high ISO makes it
  visible. Find more light first: a wider aperture, a slower shutter if nothing moves.
- **Keeping ISO low and underexposing "to avoid noise".** Brightened later, the file is
  at best as noisy, and often noisier. Expose properly.
- **Auto ISO with no ceiling.** The camera may climb all the way to its maximum. Set the
  limit to the number you tested.
- **Judging noise at 200%.** Nobody views your photos that way. Judge at the size you
  share or print.

## Try it

Fifteen minutes on the L10, in a dim room. Is your camera ISO-invariant?

1. Use M mode and raw. Frame something with shadows. Fix the aperture and shutter.
2. Shoot one frame at ISO 3200, correctly exposed.
3. Without touching aperture or shutter, shoot one at ISO 200. It's 4 stops too dark.
4. In editing, brighten the ISO 200 frame by +4 stops.
5. Compare both at 100%, especially the shadows. If they look alike, you can keep ISO
   lower at night and protect your highlights.

This is a side quest of **A1.3**.

## Check yourself

> [!question]- Two photos look equally bright: ISO 100 at 1/30 s, and ISO 6400 at 1/2000 s. Why is the second one noisier?
> It collected 64 times less light (six stops). With fewer photons, shot noise is
> larger compared with the signal. ISO 6400 only brightened that weaker signal.

> [!question]- Your camera is ISO-invariant. At night you shoot at ISO 800 instead of 3200, same aperture and shutter, then brighten by 2 stops. What did you gain and lose?
> You gained 2 stops of highlight room, so lamps and signs are less likely to clip.
> The noise is about the same. You lose a bright preview, and you must shoot raw.

> [!question]- Why use Halide's single-frame RAW instead of ProRAW for the ISO ladder?
> ProRAW merges several frames and applies Apple's noise reduction. You would be
> testing Apple's software, not how the sensor behaves at each ISO.

> [!question]- Auto ISO has a maximum of ISO 6400 and a minimum shutter of 1/250 s. In A mode the light keeps falling. What happens?
> First the ISO rises to hold 1/250 s. Once it reaches ISO 6400, most cameras let the
> shutter slow below 1/250 s, so moving subjects start to blur.

## Related
[[Exposure-Triangle]] · [[Stops-and-EV]] · [[Shutter-Speed]] · [[Dynamic-Range]] ·
[[Expose-to-the-Right]] · [[Noise-Reduction]] · [[RAW-vs-JPEG]] · [[Fundamentals-Index]]
