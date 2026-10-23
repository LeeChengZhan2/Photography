---
title: Histogram
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Histogram

> [!summary] In one line
> A histogram is a graph of how many pixels sit at each brightness. It tells you, more
> honestly than the screen, whether a photo has lost detail in the shadows or the
> highlights.

## What it is

The histogram is a bar chart of the photo's tones:

- **Left to right** runs from pure black to pure white: shadows on the left, mid-tones
  in the middle, highlights on the right.
- **Height** shows how many pixels have that brightness. A tall peak means a lot of the
  photo is that tone.

It shows *how many* pixels, not *where* they are. The screen can fool you in bright sun
or in a dark room. The histogram doesn't change with screen brightness, so it's the
more honest guide.

## How it works

### Clipping

Pixels pressed against either edge are **clipped**: they have hit pure black or pure
white, and any detail there is lost. A tall spike at an edge means a large clipped
area.

| Pile-up | What it means | Can you rescue it? |
|---|---|---|
| Against the right edge | Highlights clipped to white | Usually not. If the raw clipped too, the detail was never recorded |
| Against the left edge | Shadows clipped to black | Partly. Raw shadows keep some data, but lifting them shows noise |

The right edge matters most. A full pixel can't record any more light, so every
brighter tone becomes the same white. Shadows fade gradually into noise instead, so
there is often something left to lift. → [[Dynamic-Range]]

Some clipping is fine. The sun, a bare bulb, or sparkles on water are **specular
highlights**: small, very bright points. Nobody expects detail in them.

### There is no "correct" shape

The right histogram depends on the scene and on what you want:

| Photo | Typical histogram |
|---|---|
| Average daylight scene | Spread across the middle |
| Low-key (mostly dark): a night street, a moody portrait | Piled to the left, little on the right |
| High-key (mostly bright): a white backdrop, a bright beach | Piled to the right, little on the left |
| Haze or fog | A narrow hump in the middle: low contrast |
| Sun and deep shade together | Pushed against both edges: more range than the camera holds |

A night photo with a centred hump is probably too bright. Judge the histogram against
the picture you want, not against a bell curve.

### Colour channels

Many cameras and editors can also show separate histograms for red, green and blue
(**RGB**). The plain brightness histogram mostly follows green, because our eyes are
most sensitive to it. So a single colour can clip while the brightness histogram looks
fine.

Typical cases: red and orange flowers such as bougainvillea and hibiscus, blue or red
neon, coloured stage lights. A clipped channel shows as flat colour with no texture in
the petals or the sign. Check RGB for strongly coloured subjects, and darken until the
clipped channel comes off the right edge.

### The camera's histogram comes from the JPEG

Even when you shoot raw, the camera builds its histogram from a JPEG preview, with the
picture style, contrast and white balance already applied. The raw file usually holds
a little more highlight detail than the histogram suggests, often about a third of a
stop to a stop. It varies with the camera and its settings, so test yours before you
rely on it. → [[Expose-to-the-Right]]

## How to use it

1. **Before the shot**, use a live histogram if the camera shows one. Adjust until the
   important tones sit where you want them.
2. **After the shot**, check the right edge first. If something important is clipped,
   take away 1/3 to 1 stop and shoot again.
3. **Then check the left edge.** If shadows that matter are piled against it, add
   exposure or light, or decide that black shadows are fine.
4. **Turn on the highlight warning** (often called "blinkies"). Clipped areas flash in
   playback, so you see *where* they are.
5. **For strong colours, switch to RGB** and check each channel.

## On your kit

- **Lumix L10:** it can show a live histogram before you shoot; the manual explains how
  to turn it on, and how to set a highlight warning in playback. In **A1.5** you don't
  review while shooting, but afterwards the histograms are how you grade each frame.
- **iPhone 15 Pro Max:** Apple's Camera app has no histogram. Halide shows a live one as
  you shoot, and editing apps such as Lightroom show one for any photo.
- **Pocket 3 and Action 5 Pro:** their small screens make brightness hard to judge.
  Check the manual for a histogram option in Pro / PRO mode, and use it if there is
  one.

## Common mistakes

- **Aiming for a centred hump every time.** A night scene belongs on the left, a white
  scene on the right. Expose for the picture, not the graph.
- **Trusting the screen in bright sun.** Outdoors the screen looks dark, so you
  overexpose. Check the histogram instead.
- **Fearing every touch of the right edge.** Specular highlights may clip. Protect the
  bright areas that need detail: skin, clouds, a white shirt.
- **Watching only the brightness histogram.** A red flower can clip in the red channel
  alone. Check RGB for strong colours.
- **Treating the camera's histogram as the raw truth.** The raw usually has a little
  more room at the top. Test how much before you count on it.

## Try it

Fifteen minutes on the L10, with the live histogram on:

1. Shoot an average scene, a dark one (a corner at night) and a bright one (a white wall
   in sun). Expose each so it looks right to you.
2. Note where each histogram's pile sits. Sketch it if that helps.
3. Shoot a red or orange flower in sun. Open it in an editor's RGB histogram, or the
   camera's if it has one. Reduce the exposure until the red channel stops touching
   the right edge.

This supports **A1.3–A1.5**: matching brightness along the ISO ladder, reading your
meter-defeat frames, and grading your blind-manual set.

## Check yourself

> [!question]- A tall spike touches the right edge. What does it mean, and what do you do?
> A large area has clipped to pure white. Unless it's a specular highlight, like the
> sun or a lamp, reduce the exposure and shoot again.

> [!question]- Your night-street histogram sits mostly on the left. Is it underexposed?
> Not necessarily. Low-key scenes belong on the left. Check that the shadows you care
> about aren't crushed against the edge, and that the lights aren't blown.

> [!question]- The brightness histogram looks fine, but a red flower has no texture. Why?
> The red channel has clipped. The brightness histogram mostly follows green, so it
> missed it. An RGB histogram would show the red pile against the right edge.

> [!question]- In a raw file, why do clipped highlights matter more than dark shadows?
> A full pixel records nothing more, so clipped detail is gone. Dark shadows still hold
> some data, and you can lift them, at the cost of noise.

> [!question]- Why can a raw file hold detail that the camera's histogram shows as clipped?
> The histogram is built from the JPEG preview, with contrast and white balance
> applied. The raw has a little extra highlight room, often up to about a stop.

## Related
[[Dynamic-Range]] · [[Expose-to-the-Right]] · [[Exposure-Compensation]] ·
[[Metering-Modes]] · [[RAW-vs-JPEG]] · [[Zebras-and-Waveform]] · [[Fundamentals-Index]]
