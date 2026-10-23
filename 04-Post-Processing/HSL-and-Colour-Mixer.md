---
title: HSL and Colour Mixer
type: concept
module: 4
tags:
  - post/colour
created: 2026-10-22
---
# HSL and Colour Mixer

> [!summary] In one line
> The HSL panel, or colour mixer, changes the hue, saturation and luminance of one band
> of colour, such as only the blues, and leaves the rest alone. It's how you calm a loud
> sign, deepen a sky or even out skin.

## What it is

Every colour can be described by three properties:

| Property | Question it answers | Example move |
|---|---|---|
| **Hue** | Which colour is it? | Shift a blue sky towards aqua or towards purple |
| **Saturation** | How strong is it, compared with grey? | Make orange skin less intense |
| **Luminance** | How bright is it? | Make green leaves darker |

The panel splits the colour wheel into bands. Lightroom has eight: red, orange, yellow,
green, aqua, blue, purple and magenta. Each band gets its own hue, saturation and
luminance slider. Depending on the version, Lightroom calls it the HSL / Color panel or
the Color Mixer. Other editors have their own versions of the same idea.

## How it works

### Bands with soft edges

The editor reads each pixel's hue and works out how much it belongs to each band. The
bands overlap with soft edges, so a pixel halfway between orange and yellow gets part
of the orange move and part of the yellow move. Soft edges stop hard lines appearing in
the photo. They also mean a move can leak into neighbouring colours.

### It works only on colour that's already there

The sliders scale the colour a pixel already has. A grey pixel has almost no hue and no
saturation, so the panel can barely change it. You can't turn a grey, overcast sky blue
with the Blue saturation slider: there is no blue there to strengthen.

### It's global

The panel changes every pixel of that colour, everywhere in the frame. Darken the blues
for the sky, and a blue shirt, a blue sign and blue shadows darken too. To limit a move
to one area, combine it with a mask. → [[Local-Adjustments]]

### Luminance and black and white

When a photo becomes black and white, each colour turns into a grey. Two colours with
different hues but similar brightness, like a red flower and its green leaves, can turn
into the same grey. The flower disappears into the leaves.

The luminance sliders decide which grey each colour becomes. Make the reds lighter or
the greens darker, before or during the conversion, and the flower stands out again.
That's why black and white is made by mixing colours, not by turning saturation down to
zero. → [[Black-and-White-Conversion]]

In colour work, luminance is the quiet tool. A slightly darker blue makes a sky look
deeper without making it louder.

## How to use it

### Common uses

| Subject | Band | Typical move | Why |
|---|---|---|---|
| Skin | Orange (some red) | Saturation −5 to −15, Luminance +5 to +15 | Most skin, light or dark, sits in the orange band. This calms redness and brightens faces |
| Sky | Blue (some aqua) | Luminance −10 to −30, Saturation +5 to +10 | A deeper sky without touching anything else |
| Foliage | Yellow and green | Yellow hue towards green; Green saturation down a little | Leaves are mostly yellow-green. This makes them look fresher and calmer |
| Neon signs, LEDs | Red, magenta, blue | Saturation down, Luminance down a little | Very strong colours clip and lose their letters. Less saturation brings the shapes back |

The numbers assume sliders that run from −100 to +100, and they are only a starting
point.

### The targeted tool

Most editors have a targeted adjustment tool. Click a colour in the photo and drag up or
down, and the editor moves the right bands for you. It's also the quickest way to learn
which bands a colour really belongs to: a "blue" sky is often partly aqua.

### Steps for a sky

1. Set white balance and the basic tones first. White balance shifts every hue, so
   colour mixer moves made before it need redoing. → [[Basic-Panel-Order]]
2. Choose Luminance and the targeted tool, and drag down on the sky.
3. Zoom to 100% where the sky meets trees or buildings. Look for halos and noise.
4. If you see either, back off until they go.

## On your kit

- **Raw files take bigger moves.** On 8-bit files, such as JPEGs and many HEICs, strong
  moves cause bands and blotches in smooth skies. The L10's RW2 and the DNGs from your
  other devices have more room.
- **iPhone Photographic Styles bake in at capture on this model.** A styled HEIC or
  JPEG already has its colours shifted, and your moves stack on top. ProRAW can't take a
  style, so it starts without one.
- **Matching devices for A4.5.** Each camera renders colour its own way, so the L10 and
  the iPhone show different greens and different skin. The colour mixer is one of the
  main tools for pulling them together.

## Common mistakes

- **Moving a whole band to fix one object.** The panel is global. Add a mask to limit
  it.
- **Big hue shifts on skin.** Skin looks ill, green or magenta, very quickly. Keep hue
  moves small.
- **Pushing sky luminance down hard.** Halos and noise appear along edges. Stop before
  they show.
- **Fixing a colour cast with HSL.** A cast affects every colour, which makes it white
  balance's job. Fix it there first.
- **Making black and white with the saturation sliders.** Colours of equal brightness
  merge into one grey. Use the luminance or black-and-white mix sliders.

## Try it

Fifteen minutes. Take a frame from **A3.6**, where one colour is the subject. Use the
colour mixer to make that colour the hero: lower the saturation of the other bands, and
adjust the hue and luminance of the hero colour. Then make a black-and-white virtual
copy, and set the luminance sliders so the hero still stands out in grey. That second
step is practice for the black-and-white version in **A4.1**.

## Check yourself

> [!question]- The sky and a man's shirt are both blue. You darken Blue luminance for the sky. What happens to the shirt, and why?
> It darkens too. The colour mixer changes every pixel of that colour, wherever it is.
> Add a mask to limit the move to the sky.

> [!question]- Why can't the Blue saturation slider make a grey overcast sky blue?
> The slider scales the colour a pixel already has. A grey sky has almost no hue or
> saturation, so there is nothing to strengthen.

> [!question]- In black and white, a red flower merges into its green leaves. Which slider fixes it?
> The luminance slider for either colour, or the matching black-and-white mix slider.
> Make the red lighter or the green darker, so the two become different greys.

> [!question]- Why make colour mixer moves after setting white balance, not before?
> White balance shifts every hue in the photo. Moves made before it would be aimed at
> the wrong colours, and you would have to redo them.

## Related
[[White-Balance]] · [[Basic-Panel-Order]] · [[Black-and-White-Conversion]] ·
[[Colour-Grading]] · [[Local-Adjustments]] · [[Colour-Theory-for-Photographers]] ·
[[Post-Processing-Index]]
