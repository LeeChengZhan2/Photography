---
title: Black-and-White Conversion
type: concept
module: 4
tags:
  - post/colour
created: 2026-10-22
---
# Black-and-White Conversion

> [!summary] In one line
> A good black-and-white photo is built from colour: you decide how bright each colour
> becomes in grey. Plain desaturation skips that decision, which is why it so often
> looks flat.

## What it is

Converting to black and white turns every colour into a tone of grey. There are two
ways to do it:

| Method | How it decides each grey | Result |
|---|---|---|
| Desaturate | A fixed blend of each pixel's red, green and blue | Often flat: different colours turn into the same grey |
| Channel mixing (B&W mixer) | You choose how light or dark each colour becomes | Separation where you want it |

Your raw developer's black-and-white mode includes a mixer with a slider for each
colour band. Lightroom has eight: red, orange, yellow, green, aqua, blue, purple and
magenta. Other apps may use fewer or different bands.

## How it works

### Why desaturation looks flat

In colour, a red chilli on green leaves stands out because the hues differ. But red
and green of similar brightness become nearly the same mid-grey. In black and white
the chilli melts into the leaves. Desaturation throws away the colour contrast and
keeps only the brightness contrast, which may be small.

### Channel mixing

The raw file still knows what colour each pixel was. The mixer uses that: raise the
red slider and every red thing turns a lighter grey; lower the blue slider and every
blue thing turns darker. Now the chilli can be light grey against dark leaves.

### The film filter idea

Black-and-white film photographers did this with a coloured filter on the lens. A
filter passes its own colour and blocks its opposite. A red filter blocks blue light,
so a blue sky prints dark and white clouds stand out. The mixer does the same after the
fact:

| Film filter | Effect on film | Mixer move |
|---|---|---|
| Yellow | Sky a little darker | Blue down slightly |
| Orange | Sky darker, skin smoother | Blue down, orange up |
| Red | Sky very dark, dramatic clouds, foliage darker | Blue and aqua down hard, red up |
| Green | Foliage lighter, red lips and skin darker | Green up, red down |

### Tonal separation

Without colour, neighbouring areas must differ in tone to read as separate things.
Three tools build that:

- **Global contrast,** with the [[Tone-Curve]] or the contrast slider.
- **Black and white points.** A true black and a true white somewhere usually stop the
  photo looking muddy, though a quiet, grey photo can be a choice.
- **Local contrast,** with the texture and clarity sliders, and [[Dodge-and-Burn]] to
  lead the eye.

### White balance becomes a tone control

On a raw file, changing white balance after conversion changes the greys. Warmer
usually makes skin and yellows lighter and a blue sky darker. That happens because the
mixer works on the colours, and white balance changes the colours before the mix.

## How to use it

1. **Set exposure first,** as for colour.
2. **Convert with your app's black-and-white mode or profile,** not the saturation
   slider.
3. **Use the mixer.** Many apps have a tool you drag on the photo: drag up on the sky to
   lighten blue, down to darken it.
4. **Set contrast and the black and white points.** Watch the [[Histogram]].
5. **Dodge and burn** to direct the eye.
6. **Tone it, if you like,** and keep it subtle (see below).

### Seeing in tones

Black and white strips the photo down to light, shape and texture. It suits strong
light and shadow, texture, graphic shapes, and scenes where colour distracts. It
rarely rescues a weak photo. Squint at a scene and you see its light and dark masses.
→ [[Tonal-Composition]]

To practise seeing this way, set your camera to a monochrome picture mode with RAW on
(check the manual for the mode). The screen shows black and white, while the raw file
keeps every colour for the mixer.

### Toning, in brief

Toning adds one gentle colour to the greys, as darkroom printers once did with
chemicals. **Sepia** is a warm brown; **selenium** is a cooler purple-brown; a **split
tone** has warm highlights and cool shadows. Use the colour-grading wheels at low
strength. → [[Colour-Grading]]

## On your kit

- **Lumix L10 (RW2), Pocket 3 and Action 5 Pro (DNG):** raw files keep full colour, so
  the mixer has everything to work with.
- **iPhone 15 Pro Max:** convert ProRAW or HEIC in editing; the colour is still there.
- **A camera JPEG or HEIF shot in a monochrome mode** has lost its colour for good. If
  you shoot black and white in camera, shoot RAW alongside.

## Common mistakes

- **Desaturating.** Colours of similar brightness merge. Use the mixer.
- **Hoping black and white rescues a weak photo.** It removes colour, not problems.
  Convert because light and shape carry the photo.
- **Pushing one colour slider to the end.** Hard moves bring out noise and glowing
  edges where colours meet, such as leaves against a darkened sky. Move gently, or use
  a gradient mask on the sky instead.
- **No real black or white anywhere.** The photo looks muddy. Set the end points.
- **Too much clarity.** It turns into a gritty, crunchy look. Use it sparingly.

## Try it

Twenty minutes, on one raw file with blue sky and something red, orange or yellow in
it:

1. Make two copies. Desaturate the first one with the saturation slider.
2. Convert the second in black-and-white mode. Recreate a red filter: blue and aqua
   down, red up.
3. Compare them side by side. Where did the first copy lose separation?
4. Change the white balance on the second copy and watch the greys move.

This prepares the black-and-white version in **A4.1**, and builds on the greyscale
squint test in **A3.7**.

## Check yourself

> [!question]- Why can a red chilli on green leaves disappear when you desaturate?
> Desaturation keeps only brightness. A red and a green of similar brightness become
> nearly the same grey, so the colour contrast that separated them is gone.

> [!question]- You want a dark, dramatic sky. Which mixer sliders do you move, and what film filter does that imitate?
> Blue and aqua down, which darkens the sky while white clouds stay bright. It imitates
> a red filter, which blocked blue light on film.

> [!question]- Why does changing white balance change the greys in a black-and-white raw conversion?
> The mixer works on colours, and white balance changes the colours before the mix.
> Warmer usually lightens skin and darkens a blue sky.

> [!question]- You darkened the blue slider hard, and now the sky is noisy, with glowing edges around the trees. Why?
> A big move stretches small colour differences and noise in the sky. Edge pixels mix
> leaf and sky colour, so they get different treatment and glow. Use a gentler move, or
> a gradient mask on the sky.

## Related
[[Tonal-Composition]] · [[Tone-Curve]] · [[Dodge-and-Burn]] · [[HSL-and-Colour-Mixer]] ·
[[Colour-Grading]] · [[White-Balance]] · [[Post-Processing-Index]]
