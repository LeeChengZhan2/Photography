---
title: Shutter Speed
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Shutter Speed

> [!summary] In one line
> Shutter speed is how long the sensor collects light for one photo. It sets the
> brightness, and it decides whether movement freezes or blurs.

## What it is

The shutter opens, lets light reach the sensor, then closes. The time in between is the
shutter speed, also called the exposure time. It's written in seconds: 1/1000 s is
very short, 1 s is long.

Double the time and the sensor collects twice the light, so the photo is one
[[Stops-and-EV|stop]] brighter. The full stops run like this (some are rounded):

1/1000 → 1/500 → 1/250 → 1/125 → 1/60 → 1/30 → 1/15 → 1/8 → 1/4 → 1/2 → 1 s

Shutter speed also controls movement. Anything that moves while the shutter is open
smears across the photo. So every shutter speed is two decisions: how bright, and how
much motion shows.

## How it works

### Why things blur

Blur happens when the image of something moves across the sensor during the exposure.
A person walking at about 5 km/h covers about 1.4 m every second. This is how far they
move while the shutter is open:

| Shutter speed | Distance moved | What you usually see |
|---|---|---|
| 1/500 s | about 3 mm | Frozen |
| 1/125 s | about 1 cm | Mostly frozen; hands and feet may blur |
| 1/30 s | about 5 cm | Blurred arms and legs: you can feel the movement |
| 1/4 s | about 35 cm | A blurred shape |
| 1 s | about 1.4 m | A faint, see-through streak |

Three things change how much blur you see: **speed** (a running child moves several
times faster than a walking adult), **direction** (movement across the frame blurs
most) and **size in the frame** (a close or zoomed-in subject crosses more pixels).

### Camera shake and stabilisation

Your hands move too, and a tiny wobble moves the whole image. A longer focal length
magnifies the image, so it magnifies the wobble as well. Hence the **handheld rule of
thumb: use a shutter speed of at least 1 ÷ the focal length**. At 24 mm that's about
1/25 s; at 75 mm, about 1/80 s. If you inspect photos at 100%, go twice as fast. Use
the full-frame equivalent focal length (the one that gives the same view on a
full-frame camera), because a smaller sensor's image is enlarged more, shake included.
→ [[Sensor-Size-and-Crop-Factor]]

**Stabilisation** moves a lens element, or the sensor, to cancel small shakes. It
usually buys a few stops, often 2–4: at 75 mm, 1/80 s becomes about 1/20 s with
2 stops, or 1/10 s with 3. But it only cancels *your* movement. A friend walking past
at 1/10 s still blurs, however steady the camera is.

### Mechanical and electronic shutters

A **mechanical shutter** uses physical blades or curtains. An **electronic shutter**
has no moving parts: the sensor starts and stops recording by itself, silently.

Most sensors are read one row at a time, top to bottom. That takes a small fraction of
a second, far longer than a 1/2000 s exposure, so the top of the photo is recorded
slightly before the bottom. This is called **rolling shutter**. It causes two kinds of
trouble:

- **Leaning and bending.** In a fast pan, buildings lean. A passing bus looks slanted.
  Fan blades bend into odd shapes.
- **Banding.** Many LED and fluorescent lights flicker at twice the mains frequency:
  100 times a second on Singapore's 50 Hz supply. Rows read while the light dips come
  out darker, so dark stripes cross the photo. At 1/100 s or 1/50 s, every row
  collects light over whole flicker cycles, so the rows match and the stripes go.

A mechanical shutter avoids most of this. It starts and ends the exposure across the
whole frame much faster than a row-by-row readout.

## How to use it

### Pick the speed for the subject

Starting points for movement across the frame, at a normal distance:

| Subject | To freeze it | To show movement |
|---|---|---|
| People walking | 1/250 s | 1/15–1/30 s |
| Children running | 1/500–1/1000 s | 1/30–1/60 s |
| Cars in town | 1/1000 s | 1/15–1/30 s, or pan |
| Birds in flight | 1/2000 s or faster | Slower than 1/250 s blurs the wings |
| Water from a tap | 1/1000 s | 1/4 s or slower turns it silky |

Motion blur is a choice, not a fault. A blurred crowd past a sharp wall says "busy"; a
frozen splash says "instant". Keep *something* sharp, so the blur looks deliberate.
Speeds of 1/15 s and slower have their own note: [[Long-Exposure]].

### Hold it steady

Tuck your elbows in and support the lens with your left hand. Use the viewfinder, so
your face becomes a third support; a camera held out at arm's length is much less
steady. Lean on a wall or pillar if you can. Breathe out, press the button gently, and
shoot a short burst (several frames in quick succession): one is often sharper.

### Panning

Panning means following a moving subject with the camera during the exposure. The
subject stays fairly sharp while the background streaks.

1. Start at 1/30 s for cyclists and cars in town, 1/15 s for runners.
2. Point your feet at the spot where you'll take the photo. Twist from the hips to pick
   up the subject early, and follow it smoothly.
3. Press the shutter as it passes you, and keep turning after the click.
4. Use continuous autofocus (focus that keeps tracking the subject) and a burst. Expect
   a low hit rate at first. → [[Autofocus-Modes]]

## On your kit

- **Lumix L10:** the only device with both shutters. Mechanical (60 s to 1/2000 s) is
  for flash, fast motion and LED-lit rooms. Electronic (to 1/32000 s) is silent, but
  flash won't fire with it. You need it for f/1.7 in bright sun, which calls for about
  1/8000 s at ISO 100; there's no built-in ND filter (dark glass that cuts light). Test
  how slow its 2-axis optical stabilisation lets you go at 24 mm and at 75 mm.
- **iPhone 15 Pro Max:** electronic only. Halide or Lightroom can set the shutter, up to
  about 1 s. The 0.5× (13 mm) lens has no stabilisation: brace yourself or switch to 1×.
- **Pocket 3:** electronic only, 1/8000–1 s in Pro mode. The gimbal holds the camera
  steady at slow speeds, but it can't stop the subject moving.
- **Action 5 Pro:** electronic only, 1/8000–30 s in PRO mode. Stills get no
  stabilisation, so rest or mount it for slow speeds.

## Common mistakes

- **Trusting stabilisation to freeze a subject.** It only steadies the camera. For
  movement, choose a faster shutter speed.
- **Using the handheld speed for people.** 1/30 s at 24 mm beats your shake, but a
  walking person still blurs. Set the speed for the fastest thing that must be sharp.
- **Using the electronic shutter under LED lights.** Expect bands. Switch to the
  mechanical shutter on the L10, or use 1/100 s or 1/50 s.
- **Stopping the pan at the click.** The subject smears. Keep turning after the shutter
  closes.

## Try it

Twenty minutes at dusk, beside a road where you can stand safely, on the L10:

1. Set S mode (shutter priority), Auto ISO (the camera picks the ISO) and the
   mechanical shutter.
2. Shoot the traffic at every full stop from 1/1000 s to 1 s. Brace the camera on a
   railing for the slow end.
3. Pick three frames: "frozen", "suggested motion" and "abstract". Note their speeds.
4. Bonus, indoors under LED lights: shoot one frame at 1/1000 s with the electronic
   shutter and one with the mechanical. Look for bands.

This is a small version of **A1.2**.

## Check yourself

> [!question]- At 1/30 s and 24 mm, the wall behind your walking friend is sharp but your friend is blurred. Why?
> 1/30 s beats your shake at 24 mm, so the wall is sharp. But your friend moved about
> 5 cm during the exposure, which stabilisation can't fix. Use about 1/250 s.

> [!question]- Why does the handheld rule ask for a faster shutter at 75 mm than at 24 mm?
> A longer focal length magnifies the image, and your shake with it. The same wobble
> moves the image about three times as far across the sensor at 75 mm.

> [!question]- Under LED lights, your electronic-shutter photos have dark bands. Give two fixes and say why they work.
> Use 1/100 s or 1/50 s, so every row collects whole flicker cycles. Or use the L10's
> mechanical shutter, which exposes the frame far faster than a row-by-row readout.

> [!question]- A heron takes off and you want 1/4000 s on the L10. Which shutter, and what could go wrong?
> The electronic shutter, because the mechanical one stops at 1/2000 s. The fast wing
> beats may lean or bend because of rolling shutter.

## Related
[[Exposure-Triangle]] · [[Stops-and-EV]] · [[Long-Exposure]] · [[ISO]] ·
[[Shooting-Modes]] · [[Shutter-Angle]] · [[Sports-and-Action]] · [[Fundamentals-Index]]
