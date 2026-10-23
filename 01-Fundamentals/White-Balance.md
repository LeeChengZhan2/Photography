---
title: White Balance
type: concept
module: 1
tags:
  - fundamentals/colour
created: 2026-10-22
---
# White Balance

> [!summary] In one line
> White balance tells the camera what colour the light is, so white things look white.
> Set it wrong and the whole photo turns orange, blue or green; set it on purpose and it
> becomes a creative choice.

## What it is

Light has a colour. A household bulb is orange, shade under a blue sky is blue, and
many fluorescent tubes are slightly green. Your brain adjusts for this without you
noticing, so a white shirt looks white under all of them. A camera can't do that by
itself. **White balance** (WB) is the setting that removes the colour of the light, or
keeps some of it on purpose. Two controls describe it:

| Control | Axis | What it fixes |
|---|---|---|
| **Colour temperature**, in kelvin (K) | Blue ↔ amber | Warm or cool light: bulbs, sunsets, shade |
| **Tint** | Green ↔ magenta | Green or pink casts from many tubes and LEDs |

## How it works

### Colour temperature

The kelvin scale comes from heating an object. As it gets hotter, it glows red, then
orange, then white, then bluish. So a lower number means warmer (more orange) light, and
a higher number means cooler (bluer) light. Roughly: a candle is about 1900 K, a warm
household bulb 2700–3000 K, the low sun at sunrise and sunset 2000–3500 K, midday sun
and camera flash 5000–5500 K, an overcast sky 6000–7000 K, and open shade under a blue
sky 7000–8000 K or more. → [[Colour-Temperature-of-Light]]

### The camera setting works the other way round

When you set the camera to 3200 K, you are telling it "the light is orange, like a
bulb". It adds blue to cancel the orange. Under bulbs, whites come out white. In
daylight, the photo turns blue, because there was no orange to cancel. So **a lower K
setting makes the photo bluer; a higher K setting makes it warmer.**

Kelvin only covers blue to amber. Many tubes and cheap LEDs also add green, which no
kelvin value removes. That is the job of **tint**: move it towards magenta.

### Why the camera has to guess, and when auto fails

The sensor only records how much red, green and blue light arrived. A white wall in
orange light and an orange wall in white light can send exactly the same mix. Your brain
uses everything it knows about the scene; the camera has to guess.

Auto white balance (AWB) studies the frame and guesses which areas should be neutral.
It does well in ordinary scenes with a mix of colours. It fails when the guess is wrong:

- **One-colour scenes:** a frame full of leaves or a red wall. AWB treats the colour as a
  cast and pushes against it, so the colour you wanted turns dull.
- **Mixed light:** window light plus bulbs. AWB picks a compromise that suits neither.
- **Sunsets:** the orange glow *is* the subject. AWB "corrects" it away.
- **A series of frames:** AWB can change from shot to shot as the framing changes.

### Presets and custom white balance

| Preset | Roughly | Use it for |
|---|---|---|
| Daylight | 5200–5500 K | Direct sun; sunsets you want to stay warm |
| Cloudy | About 6000 K | Overcast; it also warms sunlight a little |
| Shade | About 7000–7500 K | Open shade; removes the blue |
| Tungsten (incandescent) | About 3000–3200 K | Warm household bulbs |

Exact values vary between cameras. When none fits, use a **custom white balance**:
fill the centre of the frame with a grey card or plain white paper in the subject's
light, and use the camera's custom WB function. A grey card is made to be neutral.
Printer paper often contains brighteners that glow slightly blue, which can push the
result a little warm, but it is a good start.

### Why RAW forgives white balance

A RAW file stores the sensor data *before* white balance is applied. The WB setting is
saved as a note in the file and used only when the file is processed, so in a raw editor
you can change it later with no loss of quality. → [[RAW-vs-JPEG]]

A JPEG or HEIF has white balance baked into its colours. Large corrections often look
wrong (odd skin tones, banding in skies), because some colour information is gone.

## How to use it

| Situation | Setting | Why |
|---|---|---|
| Sunny day outdoors | Daylight | Matches the light, and stays the same from frame to frame |
| Sunset or golden hour | Daylight, not AWB | AWB removes the warm glow you came for |
| Shade, overcast, after a storm | Cloudy or Shade | Removes the blue cast |
| Indoors under warm bulbs | Tungsten, or about 3000 K | Neutral whites; set about 3500 K to keep some warmth |
| Hawker centre under tubes | Custom WB, or fix the tint in post | Tubes often add green |

In a raw editor, set white balance first, because every later colour move builds on it.
→ [[Basic-Panel-Order]]

**Creative white balance.** Neutral is one choice among several. Candlelight should feel
warm and blue hour should feel blue. Set a lower K value at blue hour to deepen the
blue, or pick Cloudy in sunlight for warmer skin.

### Mixed light

When two light colours hit the scene, one setting can't neutralise both. Choose:

- **Neutralise the subject's light** and let the other stay warm or cool.
- **Remove a light:** room lights off and window only, or the other way round.
- **Fix it in post:** on a RAW file, a mask can have its own temperature.
  → [[Local-Adjustments]]

### Matching white balance in video

Most video, including log footage, has white balance baked in: log keeps more room to
adjust, but it is not raw. → [[Log-Profiles]]

So set a fixed kelvin value instead of AWB, which can drift as people walk through the
frame, and use the same value on every camera. Each camera still renders colour a little
differently, so expect to match the clips in the edit. → [[Shot-Matching]]

## On your kit

- **L10:** shoot RAW (RW2) alongside JPEG or HEIF while you learn, so white balance
  stays a decision. Check the manual for how to set a kelvin value and a custom WB. If
  you use [REAL TIME LUT], settle WB first: the LUT works on the colours WB produces.
  → [[LUTs]]
- **iPhone 15 Pro Max:** Apple's Camera app sets white balance automatically; ProRAW
  keeps it adjustable later. Photographic Styles bake in at capture on this model and
  can't be used with ProRAW. For video at a fixed kelvin value, use a manual app such
  as Blackmagic Camera.
- **Pocket 3 and Action 5 Pro:** raw DNG stills keep WB adjustable. For video,
  especially 10-bit D-Log M, check the Pro / PRO mode settings for a fixed white balance.

## Common mistakes

- **Leaving AWB on for sunsets.** It removes the glow. Use Daylight.
- **Getting the kelvin setting backwards.** A lower K setting makes the photo bluer. You
  are telling the camera how orange the light is.
- **Fixing a green cast with the temperature slider.** Temperature only moves blue to
  amber. Use tint, towards magenta.
- **Thinking RAW makes white balance irrelevant.** The preview and histogram still use
  the camera's setting, and frames shot on AWB may each need a different fix.
- **Using AWB in video.** It drifts mid-shot. Fix a kelvin value.

## Try it

Twenty minutes on the L10, shooting RAW + JPEG, beside a window in the late afternoon,
with a sheet of white paper in the frame:

1. Shoot one frame each on AWB, Daylight, Shade and Tungsten.
2. Set a custom WB from the paper and shoot one more.
3. Compare the JPEGs side by side. Which is neutral? Which looks best? They may differ.
4. Open one RAW in a raw editor and click the WB eyedropper on the paper. Compare it with
   the custom WB JPEG.

You'll use this again in **A2.4** (four times of day) and **A5.5** (every camera).

## Check yourself

> [!question]- You set the L10 to 3200 K outdoors at noon. What happens, and why?
> The photo turns blue. 3200 K tells the camera the light is orange, so it adds blue to
> cancel it. The daylight had no orange to cancel, so the blue stays.

> [!question]- Under hawker-centre tubes everything looks green, and the temperature slider doesn't help. Why, and what does?
> The cast is on the green–magenta axis, which temperature doesn't touch. Move the tint
> towards magenta, or set a custom WB from a grey card or white paper.

> [!question]- Why can you change white balance freely on a RAW file but not on a JPEG?
> In RAW, white balance is only a note, applied when the file is processed. In a JPEG it
> is baked into colours that have already been processed, so large changes lose quality.

> [!question]- You film one scene on the Pocket 3 and the L10. Why set both to the same kelvin value, and is that enough?
> AWB drifts and decides differently on each camera, so a shared fixed value gives a
> common start. It isn't enough: each camera renders colour a little differently, so you
> still match the clips in the edit.

## Related
[[Colour-Temperature-of-Light]] · [[RAW-vs-JPEG]] · [[Basic-Panel-Order]] ·
[[Log-Profiles]] · [[Shot-Matching]] · [[LUTs]] · [[Colour-Grading]] ·
[[Fundamentals-Index]]
