---
title: Video Stabilisation
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-22
---
# Video Stabilisation

> [!summary] In one line
> Stabilisation removes unwanted shake from video: mechanically, optically,
> electronically or in the editor. Each method fixes a different kind of movement and
> costs something different, so steady footage still starts with how you hold the
> camera and move.

## What it is

A shake you'd barely notice in a photo becomes obvious in video, because the whole
frame keeps jumping as it plays. There are four ways to fight it:

| Type | How it works | On your kit | What it costs |
|---|---|---|---|
| Mechanical gimbal | Motors turn the camera against your movement | Pocket 3 (3-axis) | Can't stop up-and-down bounce |
| Optical (OIS) | A lens element or the sensor shifts to cancel small shakes | L10 (lens, 2-axis); iPhone (sensor-shift on 1×/2× and 5×) | Small, fast shakes only |
| Electronic (EIS) | The camera crops in and moves the crop to cancel movement | Action 5 Pro (video only) | A tighter frame; smear in low light |
| In the editor | Software tracks the shake and shifts or warps each frame | Any clip | A crop, possible warping; blur stays |

And the simplest of all: a tripod, or anything solid to rest the camera on.

## How it works

### A shake has two parts

Your hands and body move the camera in two ways:

- **Rotation:** the camera turns, tilts or leans. A tiny turn moves the whole picture,
  and a [[Focal-Length-and-Perspective|longer lens]] magnifies it.
- **Translation:** the camera itself moves up, down, forwards or sideways, as when you
  walk. Each step adds a bounce.

A gimbal and OIS deal mainly with rotation. Electronic and editor stabilisation can
also shift the picture to hide some bounce, at the cost of a crop.

### Mechanical: the gimbal

The Pocket 3's gimbal has three motors. Sensors detect how the handle turns, and the
motors turn the camera the other way: left-right (pan), up-down (tilt) and leaning
(roll). The result is very smooth rotation.

But a gimbal can't cancel translation. When you walk, the whole gimbal bobs up and down
with you, and so does the picture. That's why walking technique still matters.

### Optical: OIS

Optical image stabilisation moves a lens element, or the sensor itself, to cancel small,
fast shakes from your hands. The L10's lens OIS works on two axes: small tilts up-down
and left-right. It doesn't correct a twist around the lens axis. The iPhone shifts the
sensor on its 1×/2× and 5× lenses; the 0.5× ultra-wide has no OIS.

OIS is excellent when you stand still and hold the camera. It can't smooth out walking.

### Electronic: EIS

EIS records a slightly larger area than the frame you get. For each frame, it moves the
crop to cancel the shake. It can hide bounce as well as rotation, which is why action
cameras can look smooth even when you run.

It has two costs:

- **A crop.** You lose some field of view and some resolution.
- **Smear in low light.** In dim light the shutter is slower, so each frame holds some
  blur from the shake. EIS moves the frame back into place, but it can't remove the blur
  inside it. You see a steady picture with blur that flickers in and out.

This is one reason action footage is often shot with a faster shutter than 180°: less
blur in each frame for EIS to reveal. → [[Shutter-Angle]]

### In the editor

Editing software can track points in the picture, work out the shake, then shift,
rotate or warp each frame to cancel it. It crops in to hide the moving edges. Premiere
Pro calls it Warp Stabilizer; DaVinci Resolve has a stabiliser too.

It works best on small leftover wobbles. Push it hard and you pay: a bigger crop, and
warping, where buildings bend and faces wobble like jelly. It can't remove motion blur,
for the same reason EIS can't.

## How to use it

Stabilise when you shoot, not in the edit, because every fix afterwards costs a crop and
can't remove blur.

| Shot | Best tool |
|---|---|
| Static shot | A tripod, or the camera resting on something solid |
| Walking, or following someone | The Pocket 3, plus good walking technique |
| Action, water, a bike mount | The Action 5 Pro with its stabilisation |
| Handheld, standing still | The L10 or iPhone with OIS, braced against your body |
| A small leftover wobble | The editor's stabiliser, at a low strength |

### Walking technique

- Bend your knees slightly and keep them soft. They're your suspension.
- Take short steps, and roll each foot from heel to toe.
- Keep your elbows tucked into your body, and hold the camera with both hands if you
  can.
- Breathe slowly, and move your whole body, not just your arms.
- Stay wide. The same wobble is far less visible at 20 mm than at 120 mm.
- Walk closer instead of zooming in.

### Without a tripod

A tripod is the steadiest support, but anything solid works: a wall, a railing, a
table, a ledge, a bag on the ground. Sit or kneel and rest your elbows on your knees.
Lean your shoulder against a pillar.

## On your kit

- **Pocket 3:** your steadiest moving camera. Follow mode for walking, Tilt Locked to
  hold the pitch steady, FPV to roll with your movement. → [[Camera-Movement]]
- **Lumix L10:** 2-axis lens OIS for handheld shots. At 75 mm every wobble looks about
  three times as big as at 24 mm, so brace yourself when you zoom in.
- **iPhone 15 Pro Max:** sensor-shift OIS on the 1×/2× and 5× lenses. The 5× (120 mm)
  magnifies shake the most, so rest it on something. The 0.5× has no OIS, but its wide
  view hides shake well.
- **Action 5 Pro:** electronic stabilisation, for video only. It crops, and it can smear
  in low light, so give it more light or a steady mount at night. HorizonSteady (which
  keeps the horizon level) works only at 1080p or 2.7K 16:9, up to 60 fps.

## Common mistakes

- **Expecting the gimbal to fix walking bounce.** It cancels rotation, not up-and-down
  movement. Walk with soft knees and short steps.
- **Stacking stabilisers.** Electronic stabilisation in the camera, then the editor's
  on top, means two crops and more warping. Pick one.
- **Using EIS at night and blaming the camera.** The smear is blur inside each frame.
  Add light, brace the camera, or accept it.
- **Over-fixing in the edit.** Buildings bend and faces wobble. Lower the strength, or
  keep a little natural shake.
- **Zooming in handheld.** A long focal length magnifies every wobble. Walk closer
  instead.

## Try it

Twenty minutes, along a 20 m corridor or void deck:

1. Walk the path with the Pocket 3 in Follow mode, at your normal pace.
2. Walk it again with soft knees and short, rolling steps.
3. Walk it a third time with the L10 or the iPhone (1×) handheld.
4. Put the three clips one after another on a timeline. Watch the bottom edge of the
   frame for bounce, and the horizon for tilt.
5. Try the editor's stabiliser on the worst clip. Note what it fixed, and what it cost.

Useful before **A5.3**, whose ten minutes of footage from one outing will include plenty
of walking.

## Check yourself

> [!question]- Your Pocket 3 footage still bounces when you walk normally. Why?
> The gimbal's motors cancel rotation: turning, tilting and leaning. They can't cancel
> the camera moving up and down with each step. Walking technique handles that.

> [!question]- Why can the Action 5 Pro's footage smear at night when it looks crisp in daylight?
> At night the shutter is slower, so each frame holds blur from the shake. Electronic
> stabilisation moves each frame back into place but can't remove the blur inside it.
> In daylight the shutter is fast, so there's little blur to show.

> [!question]- You fix a shaky L10 clip shot at 75 mm in the editor. What does it cost?
> A crop, so less resolution and a tighter frame. Possibly warping on straight lines and
> faces. And any motion blur stays, because the editor can only move frames, not
> sharpen them.

> [!question]- When would you choose a tripod over the Pocket 3 for a static shot?
> When you want the frame truly still. The gimbal cancels rotation, but your hand still
> drifts a little, so the frame floats. A tripod locks it in place.

## Related
[[Camera-Movement]] · [[Shutter-Angle]] · [[Focal-Length-and-Perspective]] ·
[[Shot-Sizes-and-Coverage]] · [[Video-Editing-Workflow]] · [[Video-Index]]
