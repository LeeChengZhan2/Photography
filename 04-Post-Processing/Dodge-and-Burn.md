---
title: Dodge and Burn
type: concept
module: 4
tags:
  - post/tone
created: 2026-10-22
---
# Dodge and Burn

> [!summary] In one line
> Dodging brightens an area and burning darkens it. Small, careful moves steer the
> viewer's eye through a photo without them noticing that you did anything.

## What it is

- **Dodge:** make an area lighter.
- **Burn:** make an area darker.

Nothing else changes: no colour, no sharpness, only brightness in places you choose.
It's the oldest kind of local adjustment. → [[Local-Adjustments]]

The names come from the darkroom. A print is made by shining light through the negative
onto photographic paper, and the more light a part of the paper gets, the darker it
turns. To **dodge**, the printer held a hand or a small card on a wire over part of the
print during the exposure. That part got less light and stayed lighter. To **burn**,
they gave one area extra light through a hole in a card, so it came out darker. Ansel
Adams's book *The Print* covers both as a normal part of printing, not a trick.

## How it works

### Why the eye follows light

The eye tends to go first to the brightest parts of a picture and to the places with
the most contrast. Dark, low-contrast areas recede. Dodge and burn uses that habit:

- **Brighten the subject** a little, and the eye goes there first.
- **Darken distractions and edges** a little, and they stop pulling the eye away.

So dodge and burn is composition, done after the shutter. It rearranges the light and
dark masses of the frame. → [[Tonal-Composition]]

### Two scales of work

| | Large and subtle | Detailed |
|---|---|---|
| Job | Shape the light across the whole frame | Shape form: a face, a rock, a fold of cloth |
| Brush | Big and very soft | Small, following the form |
| Strength | Low: 0.1–0.5 stop, built up slowly | Low, in many small strokes |
| Example | Darken a bright corner; lift the area around the subject | Brighten the lit side of a cheekbone; deepen its shadow side |

Both rely on the same idea: many small moves add up to a big change that nobody sees as
an edit. One strong move shows as a patch.

### Follow the light that's there

Dodge where light already falls, and burn where shadow already falls. That strengthens
what the light was doing. Dodge a shadow side and burn a lit side, and the light stops
making sense. The photo looks wrong, even if the viewer can't say why.

### Doing it digitally

- **In a raw editor:** make two brush masks, one at about +0.3 stop of Exposure
  ("dodge") and one at −0.3 ("burn"). Paint with a low flow setting, so each stroke adds
  a little more.
- **In a pixel editor:** a common method is a layer filled with 50% grey, set to the
  Soft Light blend mode. Paint on it with white at low opacity to dodge, and with black
  to burn. Two curves layers with masks also work.

Brightening can also change how strong colours look. If a dodged area starts to look
washed out, or a burned one too rich, adjust saturation slightly in the same mask.

## How to use it

For **A4.4** you use nothing but local brightness, so skip the global sliders:

1. **Squint, or look at a small, blurred version.** See the light and dark masses, not
   the details. It's **A3.7**'s squint test again.
2. **Decide where the eye should land first,** and which path it should take after
   that.
3. **Burn the distractions first:** bright patches near the edges, and bright objects
   that aren't the subject. Use a big, soft brush.
4. **Dodge the subject** and the path you want the eye to follow.
5. **Shape the detail** with small strokes on faces or forms, following the light.
6. **Check at a distance.** Dodge and burn works at viewing size. Zoom out to a small
   preview and see whether the eye goes where you planned.

Start at ±0.3 stop and build up. If you can see a stroke as a stroke, it's too strong.

## On your kit

- **Dodging shadows brings up noise.** A dark area holds little light and a lot of
  noise, and brightening it shows the noise. Files from the Action 5 Pro's small sensor
  show it first; the L10's RW2 files take the most.
- **The iPhone already brightens and darkens areas for you.** Apple's tone mapping lifts
  shadows and holds back skies, aiming for even brightness across the frame. Dodge and
  burn does the opposite: it makes brightness uneven on purpose, to lead the eye.

## Common mistakes

- **Visible patches and halos.** One strong stroke shows; ten weak ones don't. Use low
  flow and soft brushes.
- **Working against the light.** Dodging a shadow side makes the light look fake. Dodge
  the lit side instead.
- **Brightening noise.** Dodging deep shadows shows their noise. Dodge less, or add
  noise reduction in the same area.
- **Burning the edges into an obvious vignette.** Darken the corners so the viewer
  doesn't notice, not so they see a dark ring.
- **Judging only at 100%.** Dodge and burn is about the whole picture. Check it small.

## Try it

A short version of **A4.4**, twenty minutes. Take one portrait or street frame, and use
only two brush masks: +0.3 stop and −0.3 stop. Paint them in, then put the before and
after side by side. For each, write down where your eye lands first and where it goes
next.

## Check yourself

> [!question]- In the darkroom, why did holding a card over part of a print make that part lighter?
> Photographic paper darkens with light. The card blocked some of the light, so that
> part of the print got less exposure and stayed lighter.

> [!question]- In a documentary photo, a bright plastic bag near the edge pulls the eye. Why burn it rather than remove it?
> The eye goes to brightness, so darkening the bag takes away its pull without changing
> what was in the scene. Removing it would be retouching, which documentary work
> doesn't allow. → [[Retouching]]

> [!question]- Why dodge with many weak strokes instead of one strong one?
> Weak strokes build up smoothly and blend into the photo. One strong stroke leaves a
> visible patch with an edge.

> [!question]- How is dodging different from raising the Shadows slider?
> Shadows brightens every dark area in the frame. Dodging brightens only the areas you
> choose, and that choice is what leads the eye.

## Related
[[Local-Adjustments]] · [[Tonal-Composition]] · [[Visual-Weight-and-Balance]] ·
[[Basic-Panel-Order]] · [[Black-and-White-Conversion]] · [[Retouching]] ·
[[Post-Processing-Index]]
