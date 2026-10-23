---
title: Sync Speed
type: concept
module: 2
tags:
  - light/flash
created: 2026-10-22
---
# Sync Speed

> [!summary] In one line
> The sync speed is the fastest shutter speed at which the whole sensor is uncovered at
> one moment, so a flash burst can light the entire frame. Above it, part of the frame
> stays dark, unless you use high-speed sync and accept a big loss of power.

## What it is

When you use flash, the shutter speed has a ceiling: the **flash sync speed**. On many
cameras with a focal-plane shutter it is somewhere around 1/160 s to 1/250 s. Panasonic
doesn't publish the L10's, so you find it yourself with the test below.

## How it works

### Two curtains

A focal-plane shutter sits just in front of the sensor and has two curtains. The
**first curtain** moves away to start the exposure. The **second curtain** follows to
end it. Each takes a short, fixed time to cross the sensor.

- **At a slow speed**, such as 1/60 s, the first curtain finishes opening before the
  second one starts. For a moment the whole sensor is uncovered. The flash fires then,
  and the whole frame gets its light.
- **At a fast speed**, such as 1/2000 s, the second curtain starts closing before the
  first has finished opening. The sensor is exposed through a moving slit, and is never
  uncovered all at once. The flash burst is far shorter than the slit's journey, so it
  lights only the strip that is open at that instant. The rest stays dark.

The sync speed is the fastest speed that still has that "fully open" moment.

Some cameras, especially fixed-lens compacts, use a *leaf shutter* inside the lens
instead, which can sync with flash at much faster speeds. [[My-Kit]] doesn't say which
type the L10 has, and the test below gives you the practical answer either way.

### High-speed sync (HSS)

With HSS, the flash fires a rapid series of small pulses for the whole time the slit
crosses the sensor, acting like a continuous light. Every part of the frame gets the
same light at any shutter speed.

The cost is power. Each part of the sensor receives only the pulses fired while the
slit passes over it; the rest of the light lands on the curtains. You often lose two
stops or more, and each faster shutter step costs about another stop. HSS needs a
flash and a camera that both support it, so check the L10's manual.

### Front and rear curtain sync

| Mode | When the flash fires | A moving subject at a slow shutter speed |
|---|---|---|
| Front (first) curtain | Just after the first curtain opens | The blur trail appears in front of the subject, so it looks like it's moving backwards |
| Rear (second) curtain | Just before the second curtain closes | The trail is behind the subject, which looks natural |

This only matters when the shutter is slow enough for the ambient light to record
movement.

### Why electronic shutter and flash don't mix

An electronic shutter reads the sensor row by row. That readout is slow compared with a
flash burst, so at most speeds only some rows would catch the flash. Many cameras don't
fire a flash with the electronic shutter, and the L10 is one of them. A few newer
cameras with very fast sensor readout can.

## How to use it

- **For normal flash work, stay at or below the sync speed**, and choose the shutter
  speed for the ambient light. → [[Balancing-Flash-and-Ambient]]
- **In bright sun at a wide aperture**, the shutter wants to go above the sync speed.
  Close the aperture, lower the ISO, use an ND filter (it darkens flash and ambient
  equally), or use HSS and accept the power loss.
- **For movement with flash at slow speeds**, choose rear-curtain sync.

## On your kit

The L10 fires a flash only with its mechanical shutter, which runs from 60 s to
1/2000 s. With the electronic shutter selected, the flash won't fire, and the manual
doesn't mention high-speed sync, so plan without it. The other three devices can't use
a flash at all.

## Common mistakes

- **Raising the shutter speed to darken a bright background.** Above the sync speed you
  get a dark band. Close the aperture, lower the ISO, or use HSS.
- **Expecting full power from HSS.** It can lose several stops. Move the flash closer.
- **Using front-curtain sync for moving subjects at slow speeds.** The trail ends up in
  front of the subject. Switch to rear curtain.
- **Leaving the electronic shutter on.** No flash at all.

## Try it

Fifteen minutes: find the L10's sync speed.

1. Put a flash on the hot shoe, in manual at about 1/8 power, with HSS off. Use the
   mechanical shutter, M mode, ISO 200, f/5.6.
2. In a dim room, point the camera at a plain light wall 1–2 m away, so the flash is
   nearly the only light.
3. Shoot at 1/60, 1/125, 1/160, 1/200, 1/250, 1/320, 1/400 and 1/500 s, then on up to
   1/2000 s.
4. Look for a dark band along one edge of the frame. The fastest speed that gives an
   evenly lit frame is your sync speed. If no band appears even at 1/2000 s, the camera
   syncs at every mechanical speed.
5. If the camera refuses to go above a certain speed with the flash on, that limit is
   probably its sync speed too. Write the answer down; you'll use it in every flash
   shot.

## Check yourself

> [!question]- Above the sync speed, why does part of the frame go dark with flash?
> The two curtains are never fully open at the same moment, so the sensor is exposed
> through a moving slit. The very short flash burst lights only the strip that is open
> when it fires.

> [!question]- Why does high-speed sync cost so much power?
> The flash spreads its light over many pulses while the slit crosses the sensor. Each
> part of the sensor gets only the pulses fired while it was uncovered; most of the
> light hits the curtains.

> [!question]- A cyclist rides past at 1/15 s with flash, and you want the blur trail behind them. Which sync mode?
> Rear-curtain sync. The ambient light records the trail first, and the flash freezes
> the cyclist at the end, so the trail sits behind them.

> [!question]- Suppose your test gives an even frame at 1/200 s and a dark edge at 1/250 s. What do you do with that?
> Your sync speed is 1/200 s. For normal flash, never set the shutter faster than that.
> To go faster you need HSS, if the camera and flash support it.

## Related
[[Flash-Fundamentals]] · [[Balancing-Flash-and-Ambient]] · [[Shutter-Speed]] ·
[[Off-Camera-Flash]] · [[My-Kit]] · [[Light-Index]]
