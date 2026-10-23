---
title: ND Filters
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-22
---
# ND Filters

> [!summary] In one line
> An ND (neutral density) filter is dark glass that cuts light evenly across all
> colours. In video it lets you keep the 180° shutter in daylight, when the aperture is
> fixed and the ISO can't go any lower.

## What it is

ND stands for **neutral density**. "Density" because it blocks light. "Neutral" because
it should block every colour equally, so it darkens the picture without tinting it. It
works like sunglasses for the lens.

Strengths are written three ways. The factor (ND8) is what the light is divided by. The
[[Stops-and-EV|stops]] say how much darker the picture gets. The optical density (0.9)
goes up by 0.3 for every stop.

| Name | Optical density | Stops darker | Light let through |
|---|---|---|---|
| ND2 | 0.3 | 1 | 1/2 |
| ND4 | 0.6 | 2 | 1/4 |
| ND8 | 0.9 | 3 | 1/8 |
| ND16 | 1.2 | 4 | 1/16 |
| ND32 | 1.5 | 5 | 1/32 |
| ND64 | 1.8 | 6 | 1/64 |
| ND1000 | 3.0 | About 10 | 1/1000 |

Stacking two filters adds their stops: ND8 + ND8 = 3 + 3 = 6 stops, the same as ND64.

## How it works

### Why stills rarely need one and video often does

In stills, bright light is easy: you use a faster shutter. In video the shutter is
pinned by the 180° rule, at 1/50 s for 25 fps (see [[Shutter-Angle]]). That leaves the
aperture and ISO to control brightness. Three of your four devices have fixed
apertures, and ISO can't go below its base value. In bright sun, that isn't enough.

### A worked example

The "sunny 16" rule says that in bright sun with hard shadows, a correct exposure is
about f/16 at 1/ISO s. At ISO 100 that's f/16 at 1/100 s.

The Action 5 Pro is fixed at f/2.8. From f/16 to f/2.8 is five stops more light
(f/16 → 11 → 8 → 5.6 → 4 → 2.8). To keep the same exposure, the shutter must be five
stops faster: about 1/3200 s. From 1/3200 s to 1/50 s is six stops. So it needs a
six-stop filter: ND64.

| Device, ISO 100, bright sun | Aperture | Shutter for a correct exposure | ND to reach 1/50 s |
|---|---|---|---|
| Action 5 Pro | f/2.8 | About 1/3200 s | About 6 stops (ND64) |
| Pocket 3 | f/2.0 | About 1/6400 s | About 7 stops (ND128) |
| iPhone, 1× lens | f/1.78 | About 1/8000 s | About 7 stops |
| L10 | f/5.6 | About 1/800 s | About 4 stops (ND16) |
| L10 in V-Log (ISO 500) | f/5.6 | About 1/4000 s | About 6 stops (ND64) |

Real base ISOs differ a little between devices and profiles. The point is the size of
the gap: daylight video at 1/50 s needs roughly 4–7 stops of ND.

### Why not just stop down?

Only the L10 can. Even at f/16 in bright sun, ISO 100 gives 1/100 s, still one stop too
fast. And on Four Thirds, diffraction softens the picture from about f/5.6–f/8. An ND
lets you keep a sharper aperture, and a shallower [[Depth-of-Field|depth of field]] if
you want one.

### Variable ND and the X pattern

A variable ND is two polarising layers in one mount. Turning the front layer changes
how much light gets through, like turning one pair of polarised sunglasses against
another. One filter covers a range of strengths, so you can adjust exposure without
swapping glass.

The catch: the two layers cancel evenly only for light that comes straight through.
Light from the edges of a wide frame arrives at an angle and gets cut by a different
amount. Near the strongest setting this shows as a dark, blotchy X across the picture.
The wider the lens, the worse it gets. Because it's a polariser, it can also change
reflections and darken parts of a blue sky as you turn it.

### Colour casts

No filter is perfectly neutral. Many add a slight tint, warm, cool or magenta, and
cheap or very strong ones tint the most. Strong NDs can also let through infrared light,
which your eye can't see but the sensor can. Black fabric and dark leaves may then look
brownish or reddish.

## How to use it

1. **Set the frame rate and shutter first:** 25 fps at 1/50 s.
2. **Set the lowest ISO** for the profile you're using.
3. **On the L10, pick the aperture you want**, ideally f/5.6 or wider.
4. **Add ND until the exposure looks right** on the zebras or histogram.
   → [[Zebras-and-Waveform]]
5. **Set the [[White-Balance|white balance]] with the filter on**, and lock it, so the
   cast is corrected at the source.
6. **Use the same filter on cameras you'll cut together.** Different filters tint
   differently, which makes [[Shot-Matching|matching]] harder.

With a variable ND, stay away from the strongest end of its range. If you need more
than it can give cleanly, use a fixed ND instead.

### Without an ND filter

You can still film at 1/50 s; you just choose when and where. This is the plan the
[[Roadmap]] gives for A5.1 if you don't own ND filters.

- **Open shade:** under an HDB void deck, a tree or a building's shadow. Often 2–4
  stops darker than direct sun.
- **Dusk:** the half hour after sunset, which is around 19:00 in Singapore. The light
  drops fast, so be set up early.
- **Indoors:** usually dim enough without any filter.
- **A polariser** cuts about 1–2 stops, if you already have one. → [[Lens-Filters]]
- **Accept a faster shutter** in daylight, and note what it does to the motion.

## On your kit

- **Lumix L10:** no built-in ND. It's the only device with an aperture, so it needs the
  least ND: about 4 stops at f/5.6 in sun. V-Log starts at ISO 500, which adds over two
  stops more to block. Check whether the lens takes a screw-in filter before you plan
  around one.
- **Pocket 3 and Action 5 Pro:** fixed at f/2.0 and f/2.8, so ND is the only way to
  hold 1/50 s in daylight. Lock the shutter at 1/50 s in Pro / PRO mode, then add ND.
  On auto, the camera decides the shutter for you.
- **Action 5 Pro:** its 155° lens is extremely wide, so a variable ND is risky here. A
  fixed ND suits it better.
- **iPhone 15 Pro Max:** every lens has a fixed aperture. Apple's Camera app doesn't let
  you lock the shutter, so an ND only nudges its automatic shutter slower. For a true
  1/50 s, use a video app such as Blackmagic Camera.

## Common mistakes

- **Turning a variable ND to its strongest setting.** A dark X appears, worse on wide
  lenses. Stay in the middle of its range, or use a fixed ND.
- **Leaving white balance on auto with a filter on.** The cast stays, or drifts during
  the shot. Set white balance with the filter in place and lock it.
- **Stacking several filters on a wide lens.** Corners darken, and each layer adds
  reflections and softness. Use one filter of the right strength where you can.
- **Stopping the L10 down to f/16 instead.** Diffraction softens everything, and it's
  still too bright. Stay around f/5.6 or wider and add ND.
- **Assuming you can't film in daylight without ND.** You can: shade, dusk, indoors, or
  a faster shutter chosen on purpose.

## Try it

Fifteen minutes around midday, no filter needed. It measures the ND you would need.

1. Set the Pocket 3 (or the Action 5 Pro) to Pro / PRO mode at 25 fps and its lowest
   ISO.
2. In direct sun, set 1/50 s. The picture will be far too bright.
3. Raise the shutter speed one stop at a time (1/100, 1/200, 1/400 s, or the nearest
   settings) until the histogram or zebras look right. Count the stops. That's the ND
   strength you'd need.
4. Move into open shade, such as a void deck, and count again. Then try once more at
   dusk.

This tells you when and where **A5.1** works without a filter.

## Check yourself

> [!question]- Why does a stills photographer rarely need ND in daylight, when a video shooter often does?
> In stills you handle bright light with a fast shutter. In video the 180° rule pins the
> shutter near 1/50 s. With a fixed aperture and the ISO already at its lowest, the only
> control left is to cut the light before it reaches the sensor.

> [!question]- Your clip is four stops too bright at 1/50 s. Which filter do you need?
> ND16, also written as an optical density of 1.2. Each stop halves the light, so four
> stops let through 1/2 × 1/2 × 1/2 × 1/2 = 1/16.

> [!question]- You stack an ND8 and an ND8. How strong is the result?
> Six stops, the same as ND64. The stops add (3 + 3) and the factors multiply (8 × 8).
> Expect more reflections and softness than from a single ND64.

> [!question]- A variable ND shows a dark X across the Action 5 Pro's frame. Why, and what do you do?
> Its two polarising layers cancel evenly only for light coming straight through. The
> 155° lens takes in light at steep angles, so near full strength the cut becomes
> uneven. Back the filter off, or use a fixed ND.

> [!question]- A black T-shirt looks brown through a strong ND. What's going on?
> The filter lets through infrared light, which the sensor records but your eye can't
> see. Correct what you can in the edit. A filter that also blocks infrared avoids the
> problem.

## Related
[[Lens-Filters]] · [[Shutter-Angle]] · [[Stops-and-EV]] · [[Aperture]] ·
[[Exposure-Triangle]] · [[Frame-Rate]] · [[Video-Index]]
