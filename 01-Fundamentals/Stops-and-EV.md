---
title: Stops and EV
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Stops and EV

> [!summary] In one line
> A stop is a doubling or halving of light. Aperture, shutter speed and ISO are all
> counted in stops, so you can trade one against another. EV puts a whole exposure
> setting into one number.

## What it is

A **stop** is a change in light by a factor of two. One stop more is twice the light;
one stop less is half. All three exposure controls are counted in stops, so they share
one unit, and you can add and subtract them.

Counting in doubles also matches how we see. Going from 1 to 2 units of light looks
like roughly the same step as going from 100 to 200.

**EV** (exposure value) is one number for an aperture and shutter speed together. It's
used in two ways, and mixing them up causes most of the confusion:

| Use | Example | Meaning |
|---|---|---|
| A setting, or a scene | "This scene is EV 15" | Which settings give a normal exposure at ISO 100 |
| A difference | "+1 EV", "−2 EV" | How many stops brighter or darker |

## How it works

### The three ladders

| Stops | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Aperture | f/1 | f/1.4 | f/2 | f/2.8 | f/4 | f/5.6 | f/8 | f/11 | f/16 | f/22 | |
| Shutter | 1 s | 1/2 s | 1/4 s | 1/8 s | 1/15 s | 1/30 s | 1/60 s | 1/125 s | 1/250 s | 1/500 s | 1/1000 s |
| ISO | 100 | 200 | 400 | 800 | 1600 | 3200 | 6400 | 12800 | 25600 | | |

Each step to the right on the aperture or shutter row halves the light that reaches the
sensor. Each step right on the ISO row doubles the brightness of the result. ISO adds
no light; it amplifies what the sensor collected. → [[ISO]]

- **Shutter:** each step halves the time. The marked numbers are rounded: 1/15 s is
  really 1/16 s, and 1/125 s is really 1/128 s.
- **Aperture:** the f-number is focal length ÷ opening diameter, and light passes
  through the opening's *area*. Area grows with the square of the diameter. To halve
  the area, the diameter shrinks by √2 (about 1.41), so each f-number is the last one
  × 1.41. Two steps double the f-number and let in a quarter of the light: f/4 → f/8 is
  two stops. → [[Aperture]]
- **ISO:** each doubling is one stop brighter.

### Thirds of a stop

Most cameras step in thirds of a stop, so between two full stops you'll see two extra
values. Three clicks make one stop.

| Full stop | + ⅓ stop | + ⅔ stop | Next full stop |
|---|---|---|---|
| 1/125 s | 1/160 s | 1/200 s | 1/250 s |
| f/4 | f/4.5 | f/5 | f/5.6 |
| ISO 400 | ISO 500 | ISO 640 | ISO 800 |

Lens makers quote the true widest aperture, which may sit between the marks. The L10's
f/1.7 is about half a stop wider than f/2, and the iPhone's main camera is f/1.78.

### EV: one number for a setting

**EV 0 is f/1 at 1 s.** Every stop less light adds 1 to the EV. To find the EV of any
setting, count its stops along the ladder from f/1 and from 1 s, then add them:

- f/8 (6 stops) at 1/125 s (7 stops) = **EV 13**
- f/16 (8 stops) at 1/125 s (7 stops) = **EV 15**

The formula is EV = log₂(N² ÷ t), where N is the f-number and t is the time in seconds.
Counting gives the same answer.

A higher EV setting lets in less light, which is what a brighter scene needs. So EV
also describes scenes: "bright sun is about EV 15" means a normal exposure at ISO 100
needs a setting of EV 15.

| Scene, at ISO 100 | About |
|---|---|
| Bright sun, clear sky | EV 15 |
| Open shade, or a heavily overcast day | EV 11–12 |
| A home interior at night | EV 5–7 |

### EV as a difference

"+1 EV" always means one stop *more* light in the photo, and "−1 EV" one stop less.
Exposure compensation is marked this way. → [[Exposure-Compensation]]

Watch the direction. A +1 EV *difference* makes the photo brighter, but a higher EV
*setting* lets in less light. One describes a change to the photo; the other labels a
setting.

### Reciprocity: many settings, one exposure

Because the units match, you can trade one control against another. Each of these
settings is EV 13, so each gives the same brightness:

| Aperture | Shutter | What else changes |
|---|---|---|
| f/4 | 1/500 s | Shallowest depth of field; motion frozen |
| f/5.6 | 1/250 s | |
| f/8 | 1/125 s | |
| f/11 | 1/60 s | |
| f/16 | 1/30 s | Deepest depth of field; movement may blur |

This trade is called **reciprocity**. Film stopped obeying it on very long exposures
and needed extra time. Digital sensors keep to it, although very long exposures get
noisier.

### Sunny 16

In direct sun, a normal exposure is **f/16 at 1/ISO seconds**. At ISO 100 that's f/16
at 1/100 s, or 1/125 s on a camera's scale: EV 15, as in the table above.

| Light | Aperture, at 1/ISO s |
|---|---|
| Direct sun, sharp shadows | f/16 |
| Hazy sun, soft shadows | f/11 |
| Overcast, faint shadows | f/8 |
| Heavy overcast, no shadows | f/5.6 |
| Open shade, or just after sunset | f/4 |

Use it as a sanity check, not a meter. In Singapore it fits direct sun for most of the
day. In the first and last hours of daylight the sun is lower and weaker, so open up a
stop or two. If your meter disagrees with Sunny 16 by two stops or more in direct sun,
find out why before you shoot. → [[Metering-Modes]]

## How to use it

1. **Learn the full-stop ladders by heart.** Shutter from 1 s to 1/1000 s, aperture
   from f/1.4 to f/22, ISO from 100 upwards. Everything else is counting.
2. **Say the change in stops before you make it.** "f/4 to f/8 is two stops darker, so
   the shutter goes from 1/250 s to 1/60 s."
3. **Count clicks for thirds.** Three clicks on any dial is one stop.
4. **Compare scenes in EV when you plan.** Bright sun (EV 15) against a home at night
   (about EV 5–7) is a difference of 8–10 stops.

### Practice

Keep the brightness the same. What's the missing setting?

| Start | Change | Fix it with |
|---|---|---|
| f/4, 1/250 s, ISO 200 | Aperture to f/8 | Shutter: ? |
| f/2.8, 1/500 s, ISO 400 | Shutter to 1/125 s | Aperture: ? |
| f/5.6, 1/60 s, ISO 100 | Shutter to 1/250 s | ISO: ? |
| f/8, 1/125 s, ISO 100 | Aperture to f/2.8 | Shutter: ? |
| f/11, 1/30 s, ISO 800 | Shutter to 1/250 s | ISO: ? |

> [!example]- Answers
> 1. 1/60 s. f/4 → f/8 is two stops less light, so slow the shutter by two stops.
> 2. f/5.6. The slower shutter adds two stops of light, so close down two stops.
> 3. ISO 400. The faster shutter cuts two stops, so raise ISO by two stops.
> 4. 1/1000 s. f/8 → f/2.8 is three stops more light, so speed up three stops.
> 5. ISO 6400. 1/30 → 1/60 → 1/125 → 1/250 s cuts three stops; 800 → 6400 adds three.

## On your kit

- **Lumix L10:** aperture f/1.7 to f/16 (about 6½ stops at 24 mm, 5 stops at 75 mm),
  shutter 60 s to 1/2000 s mechanical and to 1/32000 s electronic, ISO 100–25600
  (8 stops). Sunny 16 at f/1.7 and ISO 100 needs about 1/8000 s, four times faster
  than the mechanical shutter allows. That's why bright sun at f/1.7 needs the
  electronic shutter.
- **iPhone 15 Pro Max:** fixed apertures, so in Halide or Lightroom only shutter and
  ISO move. In Apple's Camera app, dragging the sun icon is exposure compensation: it
  brightens or darkens the photo.
- **DJI Pocket 3:** fixed f/2.0, shutter 1/8000–1 s, ISO 50–6400. In full sun at
  ISO 100, Sunny 16 at f/2.0 needs 1/8000 s, its fastest speed.
- **DJI Osmo Action 5 Pro:** fixed f/2.8, shutter 1/8000–30 s, ISO 100–25600. Full sun
  at ISO 100 needs about 1/4000 s.

## Common mistakes

- **Reading f-numbers as a straight scale.** f/8 isn't half the light of f/4; it's a
  quarter. Count the steps on the ladder, not the size of the number.
- **Counting thirds as full stops.** 1/125 s → 1/160 s is a third of a stop. Three
  clicks make one.
- **Mixing up the two meanings of EV.** +1 EV of compensation brightens the photo; a
  setting with a higher EV lets in less light.
- **Using Sunny 16 for a subject in shade.** It's for subjects lit by direct sun. A
  face in open shade needs about f/4 at 1/ISO s, or a meter reading.
- **Forgetting that scene EVs assume ISO 100.** At ISO 400 the same scene needs a
  setting two EV higher.

## Try it

Fifteen minutes on the L10, in bright sun, in Manual (M):

1. Set ISO 100, f/16 and 1/125 s: Sunny 16. Photograph a sunlit wall or street.
2. Shoot three equivalent exposures: f/8 at 1/500 s, f/5.6 at 1/1000 s, and f/2.8 at
   1/4000 s. The last one needs the electronic shutter.
3. Compare the four histograms. They should match to within about a third of a stop.
4. Note what the camera's meter suggested for the same scene, and how far it was from
   Sunny 16.

This is the arithmetic behind **A1.1** and **A1.2**.

## Check yourself

> [!question]- Why does going from f/4 to f/8 cost two stops, not one?
> The f-number is focal length ÷ opening diameter, so at f/8 the diameter is half what
> it is at f/4. Light passes through the area, and half the diameter means a quarter of
> the area. A quarter of the light is two stops.

> [!question]- Your dial goes 1/125, 1/160, 1/200, 1/250. How big is each click, and the whole move?
> Each click is a third of a stop. From 1/125 s to 1/250 s is three clicks: one stop,
> or half the light.

> [!question]- Is an EV 15 setting brighter or darker than an EV 12 setting?
> Darker: it lets in three stops less light. That's what a scene three stops brighter
> needs, such as full sun instead of shade.

> [!question]- In direct sun at ISO 100, your meter suggests f/5.6 at 1/250 s. What does Sunny 16 say, and what might be going on?
> Sunny 16 says f/16 at 1/125 s, which is EV 15. The meter's setting is EV 13, two
> stops more light. Either the subject isn't really in direct sun, or something dark
> fills the frame and the meter is trying to make it mid-grey.

> [!question]- You need 1/500 s instead of 1/125 s and can't open the aperture further. ISO is 200. What ISO now?
> 1/125 → 1/250 → 1/500 s is two stops less light. Raise ISO by two stops:
> 200 → 400 → 800.

## Related
[[Exposure-Triangle]] · [[Aperture]] · [[Shutter-Speed]] · [[ISO]] ·
[[Exposure-Compensation]] · [[Metering-Modes]] · [[Histogram]] · [[Fundamentals-Index]]
