---
title: Sensor Size and Crop Factor
type: concept
module: 0
tags:
  - fundamentals/sensor
created: 2026-10-22
---
# Sensor Size and Crop Factor

> [!summary] In one line
> A smaller sensor records a smaller part of the image the lens makes, so it frames
> tighter and gives deeper depth of field. The crop factor converts both into
> full-frame terms. It doesn't change exposure: f/2.8 is f/2.8 on any sensor.

## What it is

The sensor is the rectangle that records the picture. Sizes vary a lot, and size
explains many of the differences between your four devices.

| Name | Size, about (mm) | Crop factor | Area vs full frame |
|---|---|---|---|
| Full frame | 36 × 24 | 1× | 100% |
| APS-C | 23.5 × 15.6 | 1.5× (Canon: 1.6×) | About 42% |
| Four Thirds | 17.3 × 13 | 2× | About 26% |
| 1-inch type | 13.2 × 8.8 | About 2.7× | About 13% |
| 1/1.3-inch type (big phone and action-camera sensors) | 9.8 × 7.4 | About 3.5× | About 8% |

The **crop factor** is how many times smaller the sensor's diagonal is than full
frame's (43 mm). "Full frame" means the size of a 35 mm film frame, which is why focal
lengths are often quoted as "35 mm equivalent". The "inch" names are old labels from
video camera tubes, not measurements: a "1-inch" sensor is about 16 mm across the
diagonal, not 25 mm.

## How it works

### Crop factor and focal length

A lens projects a circle of image, and the sensor records a rectangle from the middle.
A smaller sensor records a smaller rectangle, so it sees a narrower view, as if the
lens were longer.

**Equivalent focal length = real focal length × crop factor.** A 25 mm lens on Four
Thirds frames like a 50 mm lens on full frame. Small cameras quote the equivalent: the
iPhone's "24 mm" main camera has a real focal length of about 7 mm (24 ÷ 3.5).

Cropping doesn't change perspective. From the same spot, a crop from a wide lens looks
exactly like the same view through a longer lens, because perspective comes from where
you stand. → [[Focal-Length-and-Perspective]]

### Equivalent aperture: depth of field and noise

For the same framing, a smaller sensor needs a shorter real focal length. At the same
f-number, a shorter lens has a smaller physical opening, because the f-number is focal
length ÷ opening. A smaller opening sends a narrower cone of light, so more of the
scene looks sharp, and less light arrives in total.

So, to compare [[Depth-of-Field|depth of field]] and noise with full frame, multiply the
f-number by the crop factor. On the L10, f/1.7 at 24 mm blurs a background about as
much as f/3.7 on a full-frame 24 mm, and f/2.8 at 75 mm behaves like about f/6.2.

Noise follows the total light collected. Four Thirds has about a quarter of full
frame's area, so at the same exposure it collects about a quarter of the light: two
stops less. At the same print size, ISO 800 on Four Thirds looks roughly as noisy as
ISO 3200 on a full-frame sensor of a similar age. → [[ISO]]

### What it does not change

- **Exposure.** f/2.8 at 1/250 s and ISO 400 gives the same brightness on every
  sensor. The f-number sets the light per square millimetre, and that's what decides
  brightness. A smaller sensor simply has fewer square millimetres.
- **Perspective,** which is set by distance, and **the lens itself**: a 25 mm lens is
  25 mm on any camera.

That's why a light meter, Sunny 16 and exposure tables work on any camera without
conversion. → [[Stops-and-EV]]

### Pixel size and diffraction

The same number of pixels on a smaller sensor means smaller pixels. The L10's 20.4 MP
Four Thirds sensor has pixels about 3.0 µm (micrometres) wide. The iPhone's main sensor
fits 48 MP into about a third of that area, so its pixels are about 1.2 µm wide.

Light spreads slightly as it passes through the lens opening. This **diffraction**
blurs every point into a small spot, which grows with the f-number: for green light,
about 7.5 µm across at f/5.6 and 11 µm at f/8. Once the spot covers two or three
pixels, the whole picture starts to soften. On the L10's pixels that happens between
f/5.6 and f/8. On the iPhone's, the spot is already about two pixels wide at f/1.78:
the main camera is at its limit wide open, and a smaller opening could only blur it.
More on choosing apertures with this in mind in [[Aperture]].

### Why phones lean on computational tricks

The iPhone's main sensor has about a third of the L10's area, so it collects roughly
1½ stops less light at the same exposure. Against full frame it has about a twelfth of
the area: about 3½ stops less. Less light means more noise, and less room between the
darkest and brightest tones in one frame. A tiny sensor also gives deep depth of field,
so there's little natural background blur. Phones make up for this in software: they
merge several frames to collect more light, and fake the blur.
→ [[Computational-Photography]]

## How to use it

- **Convert in your head.** Focal length × crop factor for framing. f-number × crop
  factor for depth of field and noise. The real f-number for exposure.
- **For more background blur on a small sensor,** move closer, use the longest focal
  length, open the aperture, and put distance between subject and background. On the
  L10 that means 75 mm, f/2.8 and a far-away background.
- **For deep depth of field, a small sensor helps.** The L10 at f/5.6 already gives
  about the depth of f/12 on full frame, so you rarely need to stop down further.
- **Judge ISO by your own camera, not full-frame advice.** Four Thirds at a given ISO
  is about as noisy as full frame two stops higher. Find your limit in **A1.3**.

## On your kit

| Device | Sensor | Crop factor | Lens (equiv.) | Aperture | Depth of field like full frame at |
|---|---|---|---|---|---|
| Lumix L10 | Four Thirds (uses part of it) | About 2.2× | 24–75 mm (10.9–34 mm real) | f/1.7–2.8 | About f/3.7–6.2 |
| iPhone 15 Pro Max, 1× | 1/1.28-inch | About 3.5× | 24 mm | f/1.78 | About f/6 |
| DJI Pocket 3 | 1-inch | About 2.7× | 20 mm | f/2.0 | About f/5.4 |
| DJI Osmo Action 5 Pro | 1/1.3-inch | About 3.5× | 155° view | f/2.8 | About f/10 |

The iPhone's 0.5× and 5× cameras have their own sensors, so its row covers the 1× only.

The L10 is a special case. Its sensor is Four Thirds size, but the camera records only
a central part of it — a slightly different rectangle for each aspect ratio — so 4:3,
3:2 and 16:9 all keep the same 24 mm view. Because it uses less than the full sensor,
its crop factor is about 2.2×, not the 2× of most Four Thirds cameras: the lens is
really 10.9–34 mm. → [[My-Kit]]

- **Same f-number, same exposure.** The L10 at 75 mm, the iPhone's 5× and the Action 5
  Pro are all f/2.8. In the same light, they need the same shutter speed and ISO.
- **Why the Action 5 Pro can be fixed-focus.** Its small sensor, very short lens and
  f/2.8 give depth of field like about f/10 on full frame. Everything from about 35 cm
  to the horizon is sharp enough, so it never needs to focus.

## Common mistakes

- **Multiplying the f-number for exposure.** f/2.8 on the L10 is f/2.8 for brightness.
  The crop factor applies only to depth of field and noise.
- **Thinking a smaller sensor changes perspective.** It only crops. Perspective comes
  from where you stand.
- **Reading a phone's f/1.78 as "shallow depth of field".** On a sensor that small it
  behaves like about f/6 on full frame.
- **Stopping a small sensor down "for sharpness".** Diffraction arrives early: between
  f/5.6 and f/8 on the L10.
- **Comparing noise at the same ISO across sensor sizes.** The smaller sensor collects
  less light in total, so it's noisier at the same ISO and print size.

## Try it

Fifteen minutes. Put a small object on a table about 1 m away, with a busy background a
few metres behind it.

1. Shoot it with the L10 at 24 mm and f/1.7.
2. Shoot the same framing with the iPhone at 1×, with Portrait mode off. Compare the
   backgrounds: the f-numbers almost match, but the blur doesn't.
3. Shoot it again on the L10 at 75 mm and f/2.8, stepping back to keep the framing. The
   background should be blurrier than at 24 mm, even at f/2.8, because the longer
   lens's opening is about twice as wide.

This prepares you for **A1.6**, where you predict depth of field before each shot.

## Check yourself

> [!question]- The L10 at f/2.8, 1/250 s, ISO 400 is well exposed. You switch to the Action 5 Pro at f/2.8. What shutter speed and ISO do you need?
> The same: 1/250 s at ISO 400. The f-number sets the light per area, and that's the
> same on any sensor. The crop factor changes depth of field and noise, not exposure.

> [!question]- The Pocket 3 is f/2.0 and the Action 5 Pro is f/2.8. Which gives shallower depth of field on the same subject, and why isn't the f-number the whole answer?
> The Pocket 3. Its f-number is wider, but it also has the bigger sensor (about 2.7×
> against about 3.5×) and a longer equivalent focal length (20 mm against a 155°
> ultra-wide). In full-frame terms that's about f/5.4 against about f/10.

> [!question]- Why would a smaller aperture make the iPhone's main camera less sharp, not sharper?
> Its pixels are about 1.2 µm wide, and at f/1.78 the diffraction spot already covers
> about two of them. Any smaller opening makes the spot bigger and softens everything.

> [!question]- Why do phones merge several frames for one photo?
> Their tiny sensors collect much less light per exposure, about 3½ stops less than
> full frame. Merging frames adds up more light, which lowers noise and widens the range
> of tones.

## Related
[[My-Kit]] · [[Aperture]] · [[Depth-of-Field]] · [[Focal-Length-and-Perspective]] ·
[[ISO]] · [[Stops-and-EV]] · [[Computational-Photography]] · [[Fundamentals-Index]]
