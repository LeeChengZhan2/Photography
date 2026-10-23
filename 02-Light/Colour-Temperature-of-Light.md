---
title: Colour Temperature of Light
type: concept
module: 2
tags:
  - light/colour
created: 2026-10-22
---
# Colour Temperature of Light

> [!summary] In one line
> Every light has a colour, from orange candlelight to blue shade, measured in kelvin.
> Your eyes adjust to it and your camera doesn't, so knowing the colour of the light
> helps you set white balance, spot mixed light, and use warmth on purpose.

## What it is

Most light looks "white" to you because your eyes adapt within seconds. A camera
records the colour as it is, unless you tell it what to treat as neutral. That setting
is [[White-Balance]].

**Colour temperature** places a light on the amber–blue scale, in kelvin (K). Lower
numbers are more orange; higher numbers are more blue. Rough values:

| Source | About |
|---|---|
| Candle flame | 1800–1900 K |
| Household tungsten bulb, warm-white LED | 2700–3000 K |
| Low sun at golden hour | 2000–3500 K |
| Studio tungsten lamp | 3200 K |
| Direct sun, middle of the day | 5000–5500 K |
| Flash | About 5500 K |
| Overcast sky | 6000–7000 K |
| Open shade under a blue sky | 7000–10000 K |
| Blue hour | Very blue, often 9000 K or more |

Treat these as rough guides. Haze, cloud, time and the exact lamp all move them.

## How it works

### Why kelvin, and why it seems backwards

Heat a piece of iron and it glows dull red, then orange, then yellow, then white. Hotter
objects, such as some stars, glow bluish-white. The kelvin number is the temperature at
which an ideal hot object glows that colour. A tungsten filament at about 2800 K glows
orange. The surface of the sun, close to 5800 K, glows nearly white.

So in physics, orange light means a *lower* temperature. Artists call orange "warm" and
blue "cool" because of how the colours feel, which is the opposite way round. That is
why higher K means cooler-looking light.

Shade and blue hour aren't hot objects. They are lit by the blue sky, because air
scatters blue light more than red. Their kelvin number describes the colour a hot
object *would* need to glow to match them.

### Why sunlight changes colour

- **Low sun (golden hour):** its light travels through far more air. Scattering removes
  much of the blue on the way, so what reaches you is orange.
- **Shade on a sunny day:** no direct sun reaches it, only light from the blue sky. Faces
  and shadows turn blue.
- **Blue hour:** the sun is below the horizon. The only light is the deep blue sky,
  which balances nicely with warm city lights.

### Tint: the second axis

Kelvin only covers amber to blue. Fluorescent tubes and many LEDs don't glow like hot
objects. Their light has peaks and gaps across the colours, and it often looks green,
sometimes magenta. White balance fixes that with a separate **tint** control
(green–magenta). Spiky light can also make some colours, especially skin, look dull
even after white balance. That is a colour-rendering problem. → [[Continuous-Light]]

### Mixed sources

A camera can make only one colour of light neutral at a time. In a room with daylight
from a window (about 6000 K) and tungsten lamps (about 2800 K):

- White balance for the window, and the lamp-lit areas turn orange.
- White balance for the lamps, and the window-lit areas turn blue.

Surfaces add colour too. Light bounced off green leaves, a red wall or a yellow umbrella
tints whatever it lands on. In Singapore's tree-lined parks, faces in shade often pick up
a green cast.

## How to use it

1. **Look at the shadows.** Their colour tells you what fills them: blue shadows on a
   sunny day are lit by the sky.
2. **Set white balance for the light on the subject**, usually the face. Let the rest
   fall where it falls.
3. **In mixed light, choose:** switch off or block one source, move the subject so one
   source dominates, or keep the mix as mood. Warm lamps against a blue window at dusk
   can be beautiful. With flash, a coloured gel can match it to the room.
   → [[Balancing-Flash-and-Ambient]]
4. **Keep warmth when it's the point.** Auto white balance tends to neutralise golden
   hour. A fixed daylight setting (about 5500 K) keeps the gold.
5. **Be early.** Sunrise in Singapore is around 7:00 and sunset around 19:00. Near the
   equator the sun rises and sets steeply, so golden hour lasts only about 20–30
   minutes, and blue hour roughly 15–25 minutes. Buildings and haze near the horizon
   often cut golden light even shorter. Definitions vary; watch the light, not the
   clock.

## On your kit

- **Shoot raw on every device** (RW2 on the L10, ProRAW or DNG on the others). White
  balance is stored as a setting in a raw file, so you can change it later with no
  loss. In a JPEG or HEIF it is baked in, and big corrections cost quality.
- **For video, use a fixed white balance** wherever the device or app lets you. Auto
  white balance can drift mid-clip as the light changes, and colour is much harder to
  fix in video than in a raw still.
- **iPhone:** leave Photographic Styles on Standard while you study colour, because a
  style bakes into the file at capture on this model.

## Common mistakes

- **Mixing up the light and the setting.** Higher-K *light* is bluer. But setting a
  higher K in white balance makes the photo *warmer*, because you're telling the camera
  the light is blue and it adds orange to compensate.
- **Correcting golden hour back to neutral.** You went out for that colour. Use a fixed
  daylight setting, or warm it back up in editing.
- **Trusting auto white balance in mixed light.** It averages the sources, so nothing
  looks right. Pick the one that matters.
- **Fixing a green cast with the temperature slider.** Green is on the tint axis. Move
  tint towards magenta.
- **Arriving at sunset time.** In Singapore the best light is often already gone behind
  the buildings. Arrive 30 minutes early.

## Try it

About an hour around sunset, on any device, as a small version of **A2.4**:

1. Frame one subject facing west: a building, a tree, a street. Set a fixed daylight
   white balance and shoot raw.
2. Shoot the same frame every five minutes, from 30 minutes before sunset to 20 minutes
   after.
3. Line the frames up. Note when the light turned gold, when the gold left, and when
   the sky went deep blue. That is how short your window is.

## Check yourself

> [!question]- Why does open shade look blue on a sunny day?
> No direct sunlight reaches it. It is lit only by the blue sky, which has a high colour
> temperature, so faces and shadows there turn blue.

> [!question]- You set white balance to 3200 K outdoors at noon. What does the photo look like, and why?
> Strongly blue. You told the camera the light was orange tungsten, so it added blue to
> compensate. The real light was about 5500 K, so the added blue shows.

> [!question]- A room has a window on one side and a warm lamp on the other. Auto white balance makes everything look odd. Why, and what can you do?
> There are two colours of light, and white balance can neutralise only one. Balance
> for the light on the face, switch one source off, or keep the mix as mood.

> [!question]- An office under fluorescent tubes looks green, and the temperature slider doesn't fix it. Why?
> Green–magenta is a separate axis from amber–blue. Fix it with the tint control,
> moving towards magenta.

> [!question]- Why must you be set up early for golden hour in Singapore?
> Near the equator the sun climbs and sinks steeply, so the low, warm light lasts only
> about 20–30 minutes, and buildings and haze shorten it further.

## Related
[[White-Balance]] · [[Natural-Light]] · [[Continuous-Light]] ·
[[Balancing-Flash-and-Ambient]] · [[Colour-Theory-for-Photographers]] ·
[[RAW-vs-JPEG]] · [[Light-Index]]
