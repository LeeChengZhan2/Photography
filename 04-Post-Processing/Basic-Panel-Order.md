---
title: Basic Panel Order
type: concept
module: 4
tags:
  - post/tone
created: 2026-10-22
---
# Basic Panel Order

> [!summary] In one line
> Work through the main sliders from top to bottom: white balance, exposure, contrast,
> highlights and shadows, whites and blacks, texture, clarity and dehaze, then vibrance
> and saturation. Each step changes what the next one sees, so this order stops you
> fixing the same thing twice.

## What it is

Every raw editor has a set of global sliders: controls that change the whole photo at
once. Lightroom Classic calls it the Basic panel. Lightroom, the app that also runs on
phones and iPads, splits the same sliders into its Light, Color and Effects panels.
Other editors spread them over several tools too, but the controls are the same.

| Step | Sliders | What they control |
|---|---|---|
| 1 | Temperature, Tint | The colour of things that should look neutral |
| 2 | Exposure | Overall brightness, in stops |
| 3 | Contrast | How far apart the light and dark tones are |
| 4 | Highlights, Shadows | The brightness of the bright areas and of the dark areas |
| 5 | Whites, Blacks | The very ends: where pure white and pure black begin |
| 6 | Texture, Clarity, Dehaze | Contrast at small, medium and large scales |
| 7 | Vibrance, Saturation | How strong the colours are |

Lightroom Classic groups steps 6 and 7 under the name "Presence".

## How it works

### Why this order

Each slider changes the image that the next slider works on. Go from top to bottom, and
you make each decision once.

1. **White balance first.** Every colour you judge later depends on it. Boost saturation
   on a photo with a blue cast and you get a stronger blue cast. → [[White-Balance]]
2. **Exposure next.** It sets the midtones, and every tone slider below works relative
   to them. Set Highlights first, then raise Exposure, and you must redo the highlights.
3. **Contrast.** It spreads the tones out from the middle. That often pushes the
   brightest and darkest areas too far, which the next two steps fix.
4. **Highlights and Shadows** pull back the ends that Contrast pushed.
5. **Whites and Blacks** set the end points last, because every slider above moved them.
6. **Texture, Clarity and Dehaze** work on edges and areas, so they need the tones
   underneath to be settled.
7. **Vibrance and Saturation** come last because tone changes colour. More contrast and
   more brightness both make colours look stronger, so set saturation once tones are
   final.

### What each slider does to the tones

Watch the histogram while you work. → [[Histogram]]

| Slider | What it does | On the histogram |
|---|---|---|
| Exposure | Brightens or darkens everything; in most editors +1 means one stop brighter | The whole shape slides right or left |
| Contrast | Brights get brighter, darks get darker | The shape spreads outwards (or squeezes in) |
| Highlights | Changes the bright tones; pulling it down brings back detail in a bright sky | The right side moves; the left barely changes |
| Shadows | Changes the dark tones; pushing it up opens dark areas | The left side moves |
| Whites | Sets how close the brightest pixels come to pure white | The right end moves |
| Blacks | Sets how close the darkest pixels come to pure black | The left end moves |
| Texture | Strengthens or softens fine detail: skin pores, bark, fabric | Little visible change |
| Clarity | Adds contrast along edges at a larger scale, mostly in the midtones | A small spread in the middle |
| Dehaze | Adds contrast and saturation over large areas, cutting haze (or adding it) | The whole shape spreads |
| Vibrance | Strengthens weak colours more than strong ones, and goes easy on skin | The colour channels spread apart |
| Saturation | Strengthens every colour by the same amount | The colour channels spread apart |

Highlights and Shadows are not simple curves. Most editors make them "area-aware": they
look at the pixels around each point, so they can darken a bright sky without
flattening every bright pixel the same way. That is how they recover a sky, and also
why they make halos when pushed hard. A [[Tone-Curve]] treats every pixel of the same
brightness identically.

## How to use it

1. **Check the profile first,** if your editor has one (see On your kit).
2. **White balance:** click the eyedropper on something that should be neutral grey.
3. **Exposure:** set it for the subject, not for the whole frame.
4. **Contrast:** to taste.
5. **Highlights down** until bright areas show detail. **Shadows up** until dark areas
   do, but stop while they still look dark.
6. **Whites and Blacks.** In Lightroom, hold Alt while dragging either one to see
   exactly which pixels clip.
7. **A little Texture or Clarity,** if the picture needs bite.
8. **Vibrance before Saturation,** because Vibrance is gentler.

Go down the panel quickly and roughly once. Then go down again for small corrections.

A worked example: a street at dusk, under a bright sky, with Lightroom-style sliders
that run from −100 to +100. The numbers are only an illustration:

| Step | Move | Why |
|---|---|---|
| White balance | Temperature 5500 K → 5000 K | The street lamps made everything too orange |
| Exposure | +0.5 | The meter darkened the frame because of the bright sky |
| Contrast | +10 | The light is flat |
| Highlights / Shadows | −50 / +30 | Bring back the sky; open up the shopfronts |
| Whites / Blacks | +10 / −15 | Use the full range; only the lamps clip |
| Clarity | +10 | A little edge |
| Vibrance | +10 | Lift the shop signs without touching skin |

### Overdoing it

- **Highlights −100 with Shadows +100:** the flat, grey "HDR look". Bright and dark
  areas meet in the middle, and halos appear where they touch.
- **Clarity or Texture too high:** crunchy and gritty. Skin looks dirty; edges glow.
- **Dehaze too high:** dark, heavy and over-saturated.
- **Saturation too high:** bright colours lose their detail, and skin turns orange.

Your eyes adapt to an edit while you make it. When you think you're done, look away for
a minute, then compare before and after.

## On your kit

- **Check the profile before step 1.** The profile is the editor's starting rendering
  for each camera. Your four devices start from different profiles, so their files look
  different before you touch a slider.
- **iPhone ProRAW is already tone-mapped.** Apple's processing is written into the DNG,
  so it often opens with lifted shadows and held-back highlights. Expect smaller
  Highlights and Shadows moves than on an L10 RW2.
- **An L10 V-Log JPEG or HEIF looks flat on purpose.** Don't fight it with Contrast. It
  needs its technical LUT first. → [[LUTs]]

## Common mistakes

- **Starting with saturation.** You boost colours on top of a wrong white balance and
  a wrong exposure. Start at the top.
- **Fixing overall brightness with Shadows.** If the whole photo is dark, that's
  Exposure's job. Shadows is for the dark areas only.
- **Highlights −100 and Shadows +100 on every photo.** Everything turns flat and grey.
  Keep some real darks and some real brights.
- **Clipping without knowing.** Use the clipping view when you set Whites and Blacks.
- **A new order every time.** You end up re-fixing earlier steps. Same order, every
  photo.

## Try it

Twenty minutes, a warm-up for **A4.1**. Edit one raw twice, as two virtual copies. On
the first, go top to bottom. On the second, start with Saturation and work upwards.
Count how many times you had to go back to a slider you had already set. Which version
was faster, and which looks better?

## Check yourself

> [!question]- Why set white balance before saturation?
> Saturation strengthens every colour, including a colour cast. Fix the cast first, or
> you amplify it.

> [!question]- You set Whites first, then raise Exposure by +1. What happens to your whites?
> They get brighter too, and may now clip. Exposure moves everything, so the end points
> have to be set after it.

> [!question]- What is the difference between Contrast and Clarity?
> Contrast spreads all the tones apart, the same way everywhere in the frame. Clarity
> adds contrast along edges, mainly in the midtones, so it works area by area.

> [!question]- The sky is too bright but the rest of the photo is fine. Why use Highlights rather than Exposure?
> Exposure darkens everything, including the parts that were fine. Highlights changes
> only the bright tones.

> [!question]- On a portrait, why reach for Vibrance before Saturation?
> Vibrance strengthens weak colours more than strong ones and goes easy on skin.
> Saturation pushes everything equally, and skin turns orange first.

## Related
[[White-Balance]] · [[Histogram]] · [[Tone-Curve]] · [[HSL-and-Colour-Mixer]] ·
[[Dynamic-Range]] · [[Local-Adjustments]] · [[Post-Processing-Index]]
