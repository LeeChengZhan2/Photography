---
title: Computational Photography
type: concept
module: 0
tags:
  - fundamentals/phone
created: 2026-10-22
---
# Computational Photography

> [!summary] In one line
> Your iPhone doesn't take one picture: it captures several frames, merges them and
> processes the result in software. That's how a small sensor makes clean, bright
> photos, and why a phone photo isn't one exposure that you controlled.

## What it is

**Computational photography** means using software, and usually several frames, to
make a photo that the lens and sensor couldn't make in a single exposure. Every photo
from the iPhone's Camera app goes through it, without asking you.

A camera like the L10 works the traditional way. You press the shutter, the sensor
records one exposure, and the camera saves it. What you set is what you get.

Neither approach is better; they answer different questions. The phone asks "what will
look good?" The L10 asks "what did you set?" For learning exposure, you need the second.

## How it works

The phone's sensor is small, so each frame collects little light. A single frame is
noisy, and it can't hold a bright sky and a dark face at the same time.
→ [[Sensor-Size-and-Crop-Factor]] The phone makes up for that in software.

### Several frames, merged

While the Camera app is open, the phone is already capturing frames and keeping the
latest ones in memory. When you press the shutter, it takes frames from just before and
just after, and merges them.

| Feature | When it works | What it does |
|---|---|---|
| **Smart HDR** | Most scenes | Merges darker and brighter frames to keep highlight and shadow detail, then brightens or darkens areas separately (local tone mapping) |
| **Deep Fusion** | Medium to low light | Merges frames pixel by pixel to keep fine texture with less noise |
| **Night mode** | Low light; it switches on by itself | Captures frames for a second or more (longer on a tripod), lines them up and stacks them |

Merging several frames collects more light in total, which lowers noise and widens the
range of tones the photo can hold. → [[Dynamic-Range]] The phone also recognises parts
of the scene, such as sky, skin and faces, and processes each one differently.

The cost shows when things move or contrast is extreme: ghost copies of a moving
subject, halos along a skyline, shadows lifted until they look grey and flat.

### Pixel binning

The main camera's 48 MP sensor groups its pixels in fours, each group under the same
colour filter. In dim light the phone can add each group together and behave like a
12 MP sensor with bigger pixels: less detail, but less noise. In good light it can read
all 48 million pixels for detail. That's why Night mode saves 12 MP, while ProRAW on
the 1× lens can save 48 MP. Ordinary 1× photos land in between, at 24 MP by default.
The phone chooses for you, so check your own files' resolution when you do **A0.1**.

### Portrait mode: a depth map and fake blur

A small sensor gives deep depth of field, so there's little natural background blur.
Portrait mode creates it in three steps:

1. The phone estimates a **depth map**: how far away each part of the picture is.
2. It finds the outline of the subject.
3. It blurs everything else, more for things it thinks are further away.

It fails wherever the depth map is wrong: loose hair, glasses frames and lenses, the
gaps between arms and body, fences, and anything see-through. You get sharp patches in
the background, blurred bites out of the subject, or halos around the edges.

The blur is stored as an edit, so you can change its strength or remove it later in the
Photos app. The f-numbers on that slider describe the fake blur. The lens's real
aperture never changes.

### Photographic Styles and Live Photos

**Photographic Styles** change tone and colour while the photo is processed. On this
model a Style bakes in at capture: you can't remove it later, and you can't use one
with ProRAW. Leave Standard on if you plan to edit.

**Live Photos** record about 1.5 seconds before and after the shot as a short clip,
stored with the photo. Later you can pick a different frame, or blend the clip's frames
into a "long exposure" effect: silky water or light trails without a tripod.
→ [[Long-Exposure]]

### ProRAW is computational too

ProRAW gives you raw-style control over white balance and exposure, but it's built from
the same merged frames. It's already demosaiced (its colours already filled in), it
already has Apple's noise reduction, and Apple's tone mapping is stored inside the
file. It's an excellent everyday raw, but not a record of one exposure.
→ [[RAW-vs-JPEG]]

## How to use it

Let the phone do its work when the photo matters more than the lesson: a backlit
friend, a dark restaurant, a quick snapshot. It's very good at those.

Take control when you're learning, measuring, or fighting the processing:

- **Single-frame raw in Halide** for **A1.3**'s ISO ladder, so you measure the sensor's
  noise, not Apple's noise reduction.
- **AE/AF lock:** press and hold on the subject. Focus and exposure stay fixed while you
  recompose.
- **Exposure compensation:** after locking, drag the sun icon to brighten or darken.
  → [[Exposure-Compensation]]
- **Night mode off** when you want a short exposure of something moving, or the real
  darkness of a scene. Switch it off with its icon in the Camera app.
- **Portrait mode off** when the subject has fine edges. Use the 5× lens, a closer
  subject and a distant background for real blur instead. → [[Depth-of-Field]]

When you see grey shadows that should be dark, halos, waxy skin or ghosting, the
processing has gone too far. Shoot ProRAW and develop it yourself, or use the L10.

## On your kit

- **iPhone 15 Pro Max:** everything above. ProRAW is 48 MP on the 1× lens only; the
  0.5×, 2× and 5× lenses, Night mode, flash and macro shots save 12 MP. The 2× is a
  12 MP crop from the middle of the main sensor, not a separate camera. Manual shutter
  and ISO need Halide or Lightroom, and the shutter tops out around 1 s.
- **Lumix L10:** records one exposure per frame, so its raw file shows exactly what the
  sensor did. Its JPEGs are still processed (Photo Style, noise reduction,
  sharpening), but from that one frame. Live View Composite is a deliberate exception:
  you choose it, and you watch it add only new bright areas during a long exposure.
- **Pocket 3 and Action 5 Pro:** DJI processes their JPEGs and video too, with noise
  reduction, sharpening and colour. On the Action 5 Pro, Standard (Dewarp) straightens
  the fisheye bend in software, and its stabilisation, for video only, crops and shifts
  each frame. The Pocket 3 steadies itself with a mechanical gimbal instead. Both
  cameras' raw DNG files are fair material for A1.3.

## Common mistakes

- **Measuring the phone with ProRAW.** It's merged and noise-reduced, so an ISO ladder
  in ProRAW flatters the sensor. Use Halide's single-frame RAW.
- **Believing Portrait mode's f-number.** "f/1.4" on the slider is a label for fake
  blur. The lens's real aperture is fixed.
- **Leaving a Photographic Style on, then editing.** On this phone the Style is baked
  in. Use Standard if you'll edit.
- **Comparing one L10 frame with a merged phone photo, and blaming the L10.** The phone
  combined several frames. To match its range with the L10, bracket and merge frames
  yourself. → [[Photo-Merges]]
- **Assuming the phone saw what you saw.** Night mode can make a dark street look like
  dusk. If the darkness was the point, take control.

## Try it

Twenty minutes, one backlit scene: a person or an object in front of a bright window.

1. Shoot it in Apple's Camera app as a normal HEIF photo.
2. Shoot it again with ProRAW on.
3. Shoot it a third time in Halide as a single-frame RAW, with the same framing.
4. Compare the three on your computer: the window, the shadows, and the noise at 100%.
   Lift the shadows on the Halide file and see what Apple's merge was doing for you.

This is the background you need for **A1.3** on the iPhone.

## Check yourself

> [!question]- Why can an iPhone photo of a friend against a bright sky show both the sky and the face, when one L10 frame can't?
> The phone merged darker and brighter frames, then brightened the face area on its own.
> One L10 frame is a single exposure, so it has to choose between the sky and the face,
> unless you bracket and merge frames yourself.

> [!question]- Your ProRAW ISO ladder looks clean even at high ISO. Why is that misleading?
> ProRAW is merged from several frames and already noise-reduced. It shows what Apple's
> processing achieves, not what the sensor does at each ISO. A single-frame raw does.

> [!question]- Why does Portrait mode blur stray hairs and glasses wrongly, when a real wide aperture doesn't?
> Real blur comes from optics: each point blurs according to its true distance.
> Portrait mode blurs according to an estimated depth map, and fine or see-through
> details are exactly where that estimate goes wrong.

> [!question]- You shot a holiday with a warm Photographic Style on. Can you remove it later?
> Not on this model. Styles bake in at capture, and they don't work with ProRAW. Leave
> Standard on whenever you plan to edit.

> [!question]- Why does the 48 MP sensor save only 12 MP in Night mode?
> In dim light the phone adds each group of four pixels together, to collect more light
> per pixel and cut noise. Four pixels become one, so 48 MP becomes 12 MP.

## Related
[[RAW-vs-JPEG]] · [[Sensor-Size-and-Crop-Factor]] · [[Dynamic-Range]] ·
[[Noise-Reduction]] · [[Depth-of-Field]] · [[Exposure-Compensation]] · [[Long-Exposure]] ·
[[Fundamentals-Index]]
