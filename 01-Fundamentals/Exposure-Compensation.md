---
title: Exposure Compensation
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Exposure Compensation

> [!summary] In one line
> Exposure compensation tells the camera to make the photo brighter or darker than its
> meter suggests. It's how you correct the meter when the scene isn't middle grey.

## What it is

Exposure compensation (EC) is a setting marked in **EV** (exposure value). One EV is
one stop, and most cameras move in 1/3-stop steps, shown as 0.3 and 0.7. +1 EV means
"one stop brighter than the meter wants"; −1 EV means one stop darker.
→ [[Stops-and-EV]]

EC doesn't change the light. It moves the meter's **target**. The camera still meters
the scene, then aims for a result brighter or darker than middle grey by the amount you
set. → [[Metering-Modes]]

## How it works

EC can only move a setting the camera controls. So what it changes depends on the
shooting mode:

| Mode | You set | +1 EV makes the camera… |
|---|---|---|
| P (Program) | ISO, or Auto ISO | Pick a slower shutter or a wider aperture |
| A (Aperture priority) | Aperture, ISO | Pick a slower shutter: 1/250 s → 1/125 s |
| S (Shutter priority) | Shutter, ISO | Open the aperture: f/5.6 → f/4 |
| M, fixed ISO | Aperture, shutter, ISO | Usually nothing to the photo |
| M with Auto ISO | Aperture, shutter | Raise the ISO: ISO 400 → 800 |

In M with a fixed ISO, nothing is left for the camera to change. On some cameras EC
then moves the zero point of the meter scale; on others it does nothing. Either way,
you change the exposure yourself.

With Auto ISO (the camera picks the ISO) on in P, A or S, EC may change the ISO as well
as, or instead of, the shutter or aperture. The brightness change is the same; the side
effect is different.

A worked example in A mode at f/4 and ISO 200. The meter picks 1/500 s for a white
wall, and the wall comes out grey. You set +1.7 EV. The camera now picks about
1/160 s, so 1.7 stops more light reaches the sensor, and the wall comes out white.

If the camera runs out of room, EC can't help. In S mode with the aperture already wide
open, or in A mode at the shutter's limit, the camera usually warns you, often by
blinking the setting.

## How to use it

Starting amounts with evaluative metering:

| Scene | EC | Because |
|---|---|---|
| White wall, white sand, a white dress filling the frame | +1 to +2 EV | The meter darkens white towards grey |
| A dull grey sky filling much of the frame | +1 EV | Same reason, milder |
| Black jacket, dark animal, dark wall | −1 to −2 EV | The meter brightens black towards grey |
| Backlit person, face wanted | +1 to +2 EV | The bright background fools the meter; the sky will clip |
| Backlit person, silhouette wanted | −1 to −2 EV | Keeps the sky rich and the person black |
| Spotlit performer on a dark stage | −1 to −2 EV | The dark stage fools the meter the other way |
| Night street with bright signs | −0.7 to −1 EV | Keeps the night dark and the signs from clipping |

A routine:

1. Shoot once at 0 EV.
2. Ask: is the scene mostly bright, mostly dark, or backlit?
3. Dial in a starting amount from the table.
4. Check the [[Histogram]] and the highlight warning (clipped areas flash in playback),
   then adjust in 1/3-stop steps.
5. **Reset to 0 when the scene changes.** Most cameras keep EC until you change it.

## On your kit

- **Lumix L10:** as on most cameras, EC works in P, A and S. In M, expect it to matter
  only with Auto ISO on, where it shifts the ISO. Check the manual for how the L10
  handles it.
- **iPhone 15 Pro Max:** press and hold on the subject for AE/AF LOCK, then drag the sun
  icon up or down. That fixes the exposure on your subject first, then shifts it. The
  Camera app also has its own exposure compensation control.
- **Pocket 3 and Action 5 Pro:** in their automatic modes the camera meters for you. In
  Pro / PRO mode you set shutter and ISO yourself, so brightness is your job, as in M.

## Common mistakes

- **Forgetting to reset it.** +2 EV from the beach ruins the next indoor shot. Glance at
  the EC value before each new scene.
- **Expecting it to work in M with a fixed ISO.** It usually does nothing. Change the
  shutter, aperture or ISO yourself.
- **Leaving it all to editing.** A clipped white dress can't be rescued later. EC at the
  time saves the highlights.
- **Using the same amount everywhere.** A white wall filling the frame needs more than a
  small white shirt. Judge how much of the frame is bright or dark.
- **Missing what Auto ISO did.** With Auto ISO on, EC may change the ISO instead of the
  shutter. Check which setting moved.

## Try it

Ten minutes on the L10, in A mode with evaluative metering:

1. Frame a white wall in shade. Shoot at 0, +1 and +2 EV.
2. Frame something black in the same light. Shoot at 0, −1 and −2 EV.
3. For each set, pick the frame that matches what your eyes saw. Note where its
   histogram sits.
4. If the L10 allows Auto ISO in M, repeat one set that way. Watch which setting EC
   moves now.

This is the fixing half of **A1.4**.

## Check yourself

> [!question]- In A mode at f/4 the meter picks 1/250 s. You set −1 EV. What changes, and to what?
> The shutter speed, to 1/500 s. In A mode the aperture is yours, so the camera can
> only change the shutter (or the ISO, if Auto ISO is on).

> [!question]- In M with ISO fixed at 400, you dial in +1 EV. Why does the photo look the same?
> You set every exposure control yourself, so the camera has nothing left to change.
> EC moves the meter's target, not your settings.

> [!question]- Why does a white wall need *plus* compensation when it's already bright?
> The meter wants it middle grey, so it darkens it. Plus compensation tells it the
> wall is brighter than grey, which brings it back to white.

> [!question]- Indoors in S mode at 1/1000 s, you add +1 EV and nothing changes. Why?
> The aperture is probably already wide open and the ISO is fixed, so the camera has
> no room left. Raise the ISO, turn on Auto ISO, or choose a slower shutter.

> [!question]- You give a backlit friend +1.7 EV and the sky goes white. Is that a mistake?
> Not if the face matters most. The scene's range is wider than one exposure holds,
> so something clips. To keep both, add light to the face; you'll try that in A2.5.

## Related
[[Metering-Modes]] · [[Histogram]] · [[Shooting-Modes]] · [[Stops-and-EV]] ·
[[Exposure-Triangle]] · [[Expose-to-the-Right]] · [[Dynamic-Range]] ·
[[Fundamentals-Index]]
