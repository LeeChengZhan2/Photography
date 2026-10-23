---
title: Aperture
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-08-03
---
# Aperture

> [!summary] In one line
> The aperture is the opening in the lens that light passes through. Its size sets both
> how much light arrives and how much of the scene renders sharp from front to back.

## What it is

Inside the lens, a ring of thin blades (the iris) opens and closes to make a hole of
adjustable size. That hole is the aperture. You set it as an **f-number**, such as
f/1.7, f/4 or f/11.

A small f-number means a wide opening; a big f-number means a small one. **Opening up**
(f/8 → f/4) lets in more light and makes the zone of sharpness shallower. **Stopping
down** (f/4 → f/8) does the opposite.

## How it works

### The f-number is a ratio

**f-number = focal length ÷ diameter of the effective opening.** That's why it's
written f/2.8: it's literally a division. A 50 mm lens at f/2.8 has an opening of about
18 mm. A 200 mm lens at f/2.8 needs about 71 mm, which is why fast long lenses are
enormous.

The ratio is also why the same f-number gives the same brightness on any lens. A longer
lens magnifies the scene, spreading its light over a bigger image. It needs a
proportionally bigger opening to stay as bright, and the ratio builds that in.

### The ladder is built on √2

Light passes through the opening's area, and area grows with the square of the
diameter. To halve the area, the diameter shrinks by √2 (about 1.41). So each full
stop multiplies the f-number by 1.41:

**f/1.4 · f/2 · f/2.8 · f/4 · f/5.6 · f/8 · f/11 · f/16 · f/22**

Each step halves the light. Doubling the f-number quarters it: two stops. It's the one
sequence in photography worth learning by heart. → [[Stops-and-EV]]

### Depth of field

Light from each point in the scene enters the lens as a cone, and the lens focuses it
back to a point, but only for one distance. Points nearer or further land on the sensor
as small discs instead. A narrower opening admits a narrower cone of rays, so those
discs are smaller. When a disc is smaller than the detail you can see in the final
picture, that point reads as sharp. So stopping down widens the zone that looks sharp.
→ [[Depth-of-Field]]

### Diffraction: why smaller isn't always sharper

Light bends slightly as it passes the edge of the opening. This **diffraction** spreads
every point into a small spot, and the spot grows as the opening shrinks. Once the spot
covers two or three pixels, the whole picture softens, in focus or not.

Where that starts depends on pixel size: about f/11 on a 24 MP full-frame sensor, f/8
at 45 MP, and between f/5.6 and f/8 on the L10's 20 MP Four Thirds sensor. Past that
point, stopping down costs more resolution than the extra depth of field gains, so
**f/22 is not sharper than f/8**. If you need more depth, focus more carefully
([[Hyperfocal-Distance]]) or focus-stack: shoot several frames focused at different
distances and merge them in software.

### The trade-off

| | Wide open (f/1.4–f/2.8) | Stopped down (f/8–f/16) |
|---|---|---|
| Light | More: lower ISO or a faster shutter | Less: higher ISO or a slower shutter |
| Depth of field | Shallow: separates the subject | Deep: sharp from front to back |
| Lens flaws | Softer, darker corners (vignetting) and colour fringes (chromatic aberration) | Mostly gone, but diffraction softens *everything* past your sensor's limit |
| Focus errors | Unforgiving | Forgiving |
| Bright points of light | No sunstars | Sunstars |

Most lenses are sharpest about 2–3 stops down from wide open, between the two columns.

## How to use it

Choose the aperture for what must be sharp, then let shutter speed and ISO follow.
Starting values:

| Situation | Aperture | Because |
|---|---|---|
| Default | Aperture priority (A), f/4, Auto-ISO capped at your ceiling from A1.3 | Enough depth for most scenes, and plenty of light |
| Portrait, one person | f/2–f/2.8 (wide open at 75 mm on the L10) | Both eyes sharp at head-and-shoulders distance, background soft |
| Portrait, two people | f/4 or smaller | Two faces at different distances must both fit in the sharp zone |
| Street | f/5.6–f/8, focus preset at a fixed distance (zone focusing) | Deep enough that you stop thinking about focus |
| Landscape | f/8 on full frame; f/5.6 on the L10 | Deep depth of field, just before diffraction bites |
| Low light | Wide open | Every stop of aperture is a stop less ISO |

**Landscape focus:** focus at about twice the distance of the nearest thing that must
be sharp. With the right aperture, sharpness then runs from about half the focus
distance to the horizon, so it starts at your foreground. Don't focus "a third of the
way into the scene": that's right at only one distance. Go one stop smaller (f/11 on
full frame, f/8 on the L10) only if the foreground is genuinely close.

**Your lens's sharpest aperture:** measure it in **A1.1** rather than trusting reviews.

## On your kit

- **Lumix L10:** the only device you own with an iris, set with the aperture ring. The
  widest aperture is f/1.7 at 24 mm, shrinking to f/2.8 at 75 mm; the smallest is f/16.
  The zoom changes it because of the ratio: from 24 to 75 mm the focal length roughly
  triples, but the opening only roughly doubles, so the f-number rises. On Four Thirds,
  f/1.7–2.8 blurs a background about as much as f/3.7–6.2 would on full frame. In
  bright sun, f/1.7 needs a faster shutter than 1/2000 s at base ISO, so use the
  electronic shutter; there's no built-in ND filter.
- **iPhone 15 Pro Max:** each lens has a fixed aperture: f/2.2 (0.5×), f/1.78 (1×, and
  the 2× crop) and f/2.8 (5×). Portrait mode's blur is software, not aperture.
  → [[Computational-Photography]]
- **Pocket 3 and Action 5 Pro:** fixed at f/2.0 and f/2.8. On these two and the
  iPhone, you control brightness with shutter speed and ISO only, and depth of field
  with distance.

## Common mistakes

- **Thinking wide open makes a better photo.** Shallow depth of field is a tool for
  separation, not a mark of quality. The usual result is a soft ear and a beautifully
  blurred wall nobody cared about. Choose the aperture for what must be sharp.
- **Treating aperture as the only depth-of-field control.** Magnification matters as
  much: how big the subject is in the frame, set by distance and focal length together.
  Sensor size sets how much blur still reads as sharp. Halving your distance shrinks
  depth of field far more than opening one stop, mostly because it doubles the
  subject's size.
- **Assuming f/1.8 on a phone means shallow depth of field.** Sensor size and the real
  focal length set the blur; the f-number alone doesn't.
  → [[Sensor-Size-and-Crop-Factor]]
- **Stopping down to f/16 "for sharpness".** On the L10, diffraction softens everything
  past f/5.6–f/8. f/16 is the floor, not the goal.
- **Zooming in the middle of an aperture test on the L10.** The widest aperture changes
  from f/1.7 to f/2.8 as you zoom, so you change two things at once. Fix the focal
  length first.

## Try it

A small version of **A1.1**, 20 minutes on the L10. Choose a still subject with a clear
foreground, middle ground and background.

1. Zoom to 24 mm and leave it there. Set Manual (M) and a fixed ISO.
2. At f/2, find a shutter speed that exposes well.
3. Shoot every full stop down to f/16: f/2.8, f/4, f/5.6, f/8, f/11, f/16. Each time,
   make the shutter one stop slower (double the time), so the brightness stays the
   same. Brace the camera on a wall or table for the slow end.
4. Compare the frames at 100%. Where does the background turn sharp? At which f-number
   is the subject sharpest, and from where does everything start to soften?

## Check yourself

> [!question]- Why does a 200 mm f/2.8 lens need a far bigger front than a 50 mm f/2.8?
> The f-number is focal length ÷ opening. f/2.8 at 200 mm needs an opening of about
> 71 mm; at 50 mm it needs only about 18 mm. Same brightness, much bigger glass.

> [!question]- Why does f/8 let in a quarter of the light of f/4, not half?
> Doubling the f-number halves the opening's diameter. Light passes through the area,
> and halving the diameter quarters the area. A quarter is two stops.

> [!question]- For a landscape on the L10, why not shoot at f/16 for the most sharpness?
> Diffraction softens the L10's whole picture from about f/5.6–f/8. f/16 gains depth of
> field but loses detail everywhere. Use about f/5.6, focused at twice the distance of
> the nearest thing that must be sharp.

> [!question]- Why does the L10's widest aperture shrink from f/1.7 to f/2.8 as you zoom in?
> The f-number is focal length ÷ opening. Zooming from 24 to 75 mm roughly triples the
> focal length, but the opening only roughly doubles, so the ratio rises from 1.7 to
> 2.8.

> [!question]- A photo of two friends at f/1.7 has one sharp face and one soft. Why, and what do you change?
> They stood at different distances, and the depth of field at f/1.7 was too shallow
> to hold both. Stop down to about f/4, or ask them to stand side by side at the same
> distance from you.

## Related
[[Exposure-Triangle]] · [[Stops-and-EV]] · [[Shutter-Speed]] · [[ISO]] ·
[[Depth-of-Field]] · [[Hyperfocal-Distance]] · [[Sensor-Size-and-Crop-Factor]] ·
[[Fundamentals-Index]]
