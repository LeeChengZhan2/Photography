---
title: Exposure Triangle
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Exposure Triangle

> [!summary] In one line
> Three settings decide how bright a photo is: aperture, shutter speed and ISO. Each one
> also changes something else in the picture, so choosing an exposure means choosing
> which side effects you want.

## What it is

A photo's brightness depends on two things: how much light reaches the sensor, and how
much the camera amplifies the signal afterwards. You control that with three settings:

| Setting | What it does to brightness | What else it changes |
|---|---|---|
| [[Aperture]] | How wide the lens opening is | How much is sharp front to back ([[Depth-of-Field]]) |
| [[Shutter-Speed]] | How long the sensor collects light | Whether movement freezes or blurs |
| [[ISO]] | How much the signal is amplified | How much noise (grain) you see |

People call it a "triangle" because the three are linked: change one, and you must
change another to keep the same brightness.

## How it works

Only two of the three let light in. Aperture sets *how much light per second* gets
through the lens. Shutter speed sets *for how long*. Together they decide the total
amount of light that reaches the sensor. That total is the **exposure**.

ISO does not add light. It brightens the signal after the light has been collected,
like turning up the volume on a quiet recording. That is why high ISO looks noisy: you
are amplifying a weak signal, and the noise that comes from having too little light
gets amplified with it. → [[ISO]]

All three are measured in **stops**. One stop means double or half the light.
→ [[Stops-and-EV]]

- Aperture: f/2.8 → f/4 is one stop less light.
- Shutter: 1/125 s → 1/250 s is one stop less light.
- ISO: 400 → 200 is one stop darker.

Because they share the same unit, you can trade one against another. These three
combinations give the same brightness:

| Aperture | Shutter | ISO | What the photo looks like |
|---|---|---|---|
| f/2.8 | 1/500 s | 400 | Shallow depth of field, motion frozen |
| f/5.6 | 1/125 s | 400 | More in focus, fast movement may blur |
| f/5.6 | 1/500 s | 1600 | More in focus, motion frozen, more noise |

The brightness is identical. The *photo* is not. That is the whole point of the
triangle.

## How to use it

Decide what matters most in the picture. Set that first, then let the others follow.

1. **Is something moving?** Set the shutter speed first: fast (1/500 s or faster) to
   freeze it, slow to show the movement.
2. **Does depth of field matter?** Set the aperture first: wide (small f-number, like
   f/1.7) to blur the background, narrower (like f/8) to keep more sharp.
3. **Then ISO.** Use the lowest ISO that gives the brightness you need. Raise it only
   when the other two can't move any further.

A worked example, from the Gate 1 test: *"moving kid, indoors, want them sharp and the
background soft."*

- Sharp moving kid → shutter about 1/500 s.
- Soft background → the widest aperture: f/1.7 on the L10 at 24 mm.
- Indoors is dark → raise ISO until the exposure is right, maybe ISO 1600–6400.
- Accept the noise. A slightly noisy sharp photo beats a clean blurry one.

## On your kit

- **Lumix L10:** the only device where you control all three. The aperture ring sets
  the aperture. The widest aperture shrinks from f/1.7 to f/2.8 as you zoom to 75 mm, so
  zooming in can make the photo darker. Use the L10 for Module 1.
- **iPhone 15 Pro Max:** every lens has a fixed aperture, so only shutter speed and ISO
  can change, and only in an app such as Halide or Lightroom. Apple's Camera app picks
  both for you.
- **Pocket 3 and Action 5 Pro:** fixed apertures too (f/2.0 and f/2.8). In Pro / PRO
  mode you set the shutter speed and ISO yourself.

With a fixed aperture, the "triangle" becomes a straight line: brightness is a trade
between shutter speed and ISO only.

## Common mistakes

- **Thinking ISO makes the sensor more sensitive.** It doesn't. It brightens the signal
  after the light is collected. Too little light causes the noise; high ISO only makes
  it visible.
- **Changing two settings at once while learning.** You won't know which one caused the
  result. Change one setting, and fix the brightness with one other.
- **Chasing a "correct" exposure.** A dark, moody photo can be the right exposure. The
  meter only makes a suggestion. → [[Histogram]]
- **Keeping ISO at 100 at all costs.** A blurry photo at ISO 100 is worse than a sharp
  one at ISO 3200.

## Try it

Ten minutes, on the L10, in Manual (M) mode:

1. Find a correct exposure for any still scene, for example f/4, 1/125 s, ISO 400.
2. Close the aperture by one stop to f/5.6. The photo gets darker. Fix it by making the
   shutter one stop slower: 1/60 s. Same brightness.
3. Go back to 1/125 s and fix it with ISO instead: ISO 800. Same brightness again.
4. Compare the three photos at 100% zoom. Look at the depth of field, any motion blur,
   and the noise.

This is a small version of assignments **A1.1–A1.3**.

## Check yourself

> [!question]- Which two settings change the amount of light, and which one doesn't?
> Aperture and shutter speed change how much light reaches the sensor. ISO doesn't add
> any light. It amplifies the signal after the light has been collected.

> [!question]- You go from f/4 to f/8. How many stops is that, and how do you fix it with the shutter?
> f/4 → f/5.6 → f/8 is two stops less light. Make the shutter two stops slower to
> match: for example 1/250 s → 1/125 s → 1/60 s.

> [!question]- Why is a photo at ISO 6400 usually noisier than one at ISO 100, even if both look equally bright?
> Because the ISO 6400 photo was made with far less light. Noise comes mainly from
> having too little light. High ISO amplifies that weak signal, and its noise with it.

> [!question]- On the Pocket 3, which settings can you trade against each other?
> Only shutter speed and ISO. The aperture is fixed at f/2.0, so you can't change how
> much light comes through per second or how deep the depth of field is.

## Related
[[Stops-and-EV]] · [[Aperture]] · [[Shutter-Speed]] · [[ISO]] · [[Histogram]] ·
[[Shooting-Modes]] · [[Exposure-Compensation]] · [[Fundamentals-Index]]
