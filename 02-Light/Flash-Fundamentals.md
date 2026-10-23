---
title: Flash Fundamentals
type: concept
module: 2
tags:
  - light/flash
created: 2026-10-22
---
# Flash Fundamentals

> [!summary] In one line
> A flash fires a very bright burst of light that lasts a tiny fraction of a second.
> You set its strength yourself or let the camera choose (TTL), and you treat the flash
> and the existing light as two separate exposures in one frame.

## What it is

A flash (often called a *speedlight*) stores energy and releases it in one short,
bright burst. It is the most portable way to add a lot of light. The words you'll meet:

| Term | Meaning |
|---|---|
| Guide number (GN) | The flash's power rating: distance × f-number for a correct exposure, at ISO 100 and a stated zoom setting |
| TTL | "Through the lens": the camera measures a test burst and sets the power for you |
| Manual power | You set the power yourself: 1/1 (full), 1/2, 1/4 and so on |
| Flash exposure compensation (FEC) | Tells TTL to give more or less flash, in stops |
| Recycle time | How long the flash needs to recharge between bursts |
| Ambient light | All the light that was already there: sun, lamps, windows |

## How it works

### A very short burst

Batteries charge a capacitor, a part that stores electrical energy. When you fire, it
empties through a gas-filled tube, which glows very brightly. For a typical small flash,
the burst lasts roughly 1/1000 s at full power, and much less at low power. The exact
numbers vary by model.

On most modern flashes, lower power works by cutting the burst short. So low power also
means a shorter burst, which freezes motion even better. This freezing works only where
the flash is the main light on the subject. If strong ambient light also reaches the
subject, that part of the exposure can still blur.

### Guide number

Guide number = distance × f-number. A flash with GN 36 (in metres, at ISO 100) at full
power:

| Aperture | Furthest correctly lit subject |
|---|---|
| f/2 | 18 m |
| f/4 | 9 m |
| f/8 | 4.5 m |

Raising ISO two stops (100 → 400) doubles every distance. Halving the power divides
them by about 1.4. Makers often quote the guide number at the flash head's longest zoom
setting, which makes it look bigger, so compare flashes at the same setting. Once you
bounce or diffuse the flash, the guide number no longer predicts distance: use test
shots.

### Power in stops

Manual power runs 1/1 → 1/2 → 1/4 → 1/8 → 1/16 → 1/32 → 1/64 → 1/128. Each step is
one stop, so that range is seven stops. Many flashes also offer third-stop steps
between them. → [[Stops-and-EV]]

### TTL or manual

With TTL, the flash fires a weak *pre-flash* when you press the shutter. The camera
measures how much bounces back through the lens, works out the power, and fires the
main burst, all in a split second.

| | TTL | Manual |
|---|---|---|
| Subject distance keeps changing (events, children) | Good: adjusts itself | Must reset for each distance |
| Fixed setup (portraits) | Can vary from shot to shot | Good: same every time |
| Very white or very dark subject | Fooled, like any meter; needs FEC | Unaffected |

TTL meters reflected light, just like the camera's normal meter. A white dress fools it
into giving too little flash, and a black suit into giving too much. FEC fixes that:
+1 doubles the flash, −1 halves it. Check the manual for whether the camera's normal
exposure compensation also changes the flash. The pre-flash can also make some people
blink just before the real burst.

**Recycle time** grows with power. After a full-power burst, a flash may need a few
seconds to recharge; at low power it is almost instant. Many full-power bursts in a row
can overheat it.

### Two exposures in one frame

The flash burst is far shorter than the shutter time. As long as the whole sensor is
uncovered when it fires, the shutter speed doesn't change how much flash is recorded.
Ambient light, though, keeps building up for as long as the shutter is open.

| Control | Ambient exposure | Flash exposure |
|---|---|---|
| Shutter speed | Yes | Almost none |
| Aperture | Yes | Yes |
| ISO | Yes | Yes |
| Flash power and distance | No | Yes |

That table is the key to every flash technique. The shutter has a limit, though: above
the [[Sync-Speed]], part of the frame misses the flash. Using it in practice:
[[Balancing-Flash-and-Ambient]].

## How to use it

- **Avoid bare flash pointing straight from the camera.** It flattens faces and gives
  red-eye. Bounce it instead. → [[Bounce-Flash]]
- **Events and moving people:** TTL, bounced, with the camera in manual mode at, for
  example, f/2.8, 1/60–1/100 s, ISO 800.
- **A fixed portrait setup:** manual power. Start at 1/8, take a test shot, and adjust
  in whole stops, then in thirds.
- **Fill flash outdoors:** TTL with FEC of about −1 to −2, so the flash lifts the
  shadows without looking like flash.
- **Fast sequences:** raise ISO one stop and halve the power. The flash recycles faster
  and its burst gets shorter.

## On your kit

- **Lumix L10:** a hot shoe for an external flash, no built-in flash. It fires a flash
  only with its **mechanical shutter** (60 s to 1/2000 s). If a flash won't fire, check
  that you haven't switched to the electronic shutter.
- **Sync speed:** Panasonic doesn't publish the L10's, so you find it with test shots.
  That is a ready-made Module 2 experiment.
- **Compatibility:** TTL needs a flash that works with the camera's flash system. A
  manual-only flash just fires at the power you set. Check the flash's documentation
  and the L10's manual.
- **iPhone 15 Pro Max:** its "flash" is an LED, a continuous light switched on briefly.
  It is much weaker, can't be aimed, bounced or moved, and isn't a flash in the sense
  of this note. It works well as a torch for A2.2 and A2.3.
- **Pocket 3 and Action 5 Pro:** no flash, and they can't sync one.

No flash yet? The Roadmap's substitute for week 8 is a continuous LED panel or a
window with a curtain. → [[Continuous-Light]]

## Common mistakes

- **Fixing flash brightness with the shutter.** The shutter mostly changes the ambient
  light. Change the flash power, its distance, the aperture or the ISO.
- **Trusting TTL with white or black subjects.** It is fooled like any meter. Use FEC.
- **Leaving the electronic shutter on.** The L10 won't fire the flash.
- **Firing full power for every shot.** It recycles slowly and overheats. Raise the ISO
  and lower the power.
- **Comparing guide numbers from spec sheets at face value.** Check the units and the
  zoom setting they were measured at.

## Try it

Twenty minutes with a flash on the L10, in a room with one lamp on. This is groundwork
for **A2.5** and **A2.6**:

1. Set M mode, mechanical shutter, ISO 400, f/4, 1/60 s. Set the flash to manual, 1/64
   power, pointing at a person or an object about 2 m away.
2. Shoot at 1/64, 1/32 and 1/16 power. The subject brightens one stop each time; the
   lamp-lit background doesn't change.
3. Back at 1/64, shoot at 1/30 s and 1/15 s. Now the background brightens and the
   flash-lit subject barely changes.
4. Finally change the aperture to f/5.6. Both get darker.

## Check yourself

> [!question]- Your flash at 1/4 power gives the right exposure. How do you make the subject one stop darker without changing the background?
> Drop the flash to 1/8 power, or move it about 1.4 times further away. Changing the
> aperture or ISO would darken the background as well.

> [!question]- A flash has GN 40 (metres, ISO 100). How far can it reach at f/5.6, and at ISO 400?
> 40 ÷ 5.6 ≈ 7 m at ISO 100. ISO 400 is two stops more, which doubles the distance to
> about 14 m.

> [!question]- Indoors with flash, the subject looks right but the room behind is too dark. What do you change?
> Make the shutter slower. That lets in more ambient light while the flash on the
> subject stays the same.

> [!question]- Why does a flash at low power freeze motion better than at full power?
> Most flashes lower their power by cutting the burst short. A shorter burst records
> less movement.

> [!question]- TTL makes a bride in a white dress look too dark. Why?
> TTL meters reflected light. The white dress reflects a lot, so the camera thinks
> there's plenty of light and cuts the power. Dial in positive FEC.

## Related
[[Sync-Speed]] · [[Bounce-Flash]] · [[Off-Camera-Flash]] ·
[[Balancing-Flash-and-Ambient]] · [[Inverse-Square-Law]] · [[Continuous-Light]] ·
[[Light-Index]]
