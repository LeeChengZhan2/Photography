---
title: My Kit
type: concept
module: 0
status: drafted
confidence: 1
tags:
  - gear/kit
created: 2026-08-19
---
# My Kit

> [!warning] Claude drafted the numbers — verifying them *is* A0.1
> Every figure below came from Claude's memory of published specs, which is precisely
> what A0.1 tells you not to do ("from the manual/specs, not memory"). Open each
> product page, confirm or correct every row, then delete this callout and set your own
> `confidence`. The A0.1 box in [[Progress-Tracker]] stays unticked until you have.

## In one sentence
Three fixed-aperture, wide-angle, motion-first devices — so shutter and ISO are mine to
control, depth of field mostly isn't, and a fourth camera is what would unlock the
aperture half of Module 1.

## The kit

### iPhone 15 Pro Max
| | |
|---|---|
| Main sensor | 1/1.28" · 48 MP |
| Optical lenses | 13 mm f/2.2 ultra-wide (12 MP) · 24 mm f/1.78 main (48 MP) · 120 mm f/2.8 5× tetraprism (12 MP) |
| Extra focal lengths | 28 mm and 35 mm — *crops of the main sensor*, not lenses |
| Aperture | **Fixed.** No iris on any of the three lenses |
| Stabilisation | Second-generation sensor-shift OIS on the main lens |
| Stills formats | HEIF/JPEG · Apple ProRAW (12-bit DNG, 12 MP or 48 MP) |
| Video | 4K60, ProRes, **Apple Log**, HDR / Dolby Vision |
| Manual control | Not in the native Camera app. Shutter and ISO need a third-party app — Halide, Blackmagic Camera, Lightroom Mobile |
| Close focus | Macro via the ultra-wide, around 2 cm — verify: ____________ |

**Its job here:** the camera that's always with you, the 48 MP ProRAW file, and the only
optic in the kit reaching past 24 mm.

### DJI Pocket 3
| | |
|---|---|
| Sensor | 1" CMOS — the largest in the kit |
| Lens | 20 mm equivalent, f/2.0, fixed |
| Aperture | **Fixed** at f/2.0 |
| Focus | Autofocus |
| Stabilisation | 3-axis **mechanical** gimbal |
| Stills formats | JPEG · raw DNG |
| Video | 4K, 10-bit **D-Log M** and HLG |
| Manual control | Pro mode — shutter, ISO, EV, white balance |

**Its job here:** the best low-light sensor you own and the only mechanically
stabilised one. Also the device that makes [[LUTs]] real work rather than theory.

### DJI Osmo Action 5 Pro
| | |
|---|---|
| Sensor | 1/1.3" · 40 MP stills |
| Lens | Ultra-wide, f/2.8, **fixed focus** — no autofocus at all |
| FOV modes | Ultra-Wide / Wide / Standard / Dewarp — crops and corrections, not a zoom |
| Aperture | **Fixed** at f/2.8 |
| Stills formats | JPEG · raw DNG |
| Video | 4K120, 10-bit **D-Log M** and HLG |
| Environment | Waterproof to 20 m with no case |
| Manual control | Pro mode — shutter, ISO, EV |

**Its job here:** the places a camera shouldn't go — water, mud, mounted, held at ankle
height in traffic. Fixed focus means it is always sharp from roughly arm's length to
infinity, which for that job is a feature rather than a limitation.

### Camera #4 — planned, not bought
Nothing on this page is a recommendation. But three numbers decide what a fourth body
actually *adds* to the three above, and they're worth settling before you spend:

- **Does the iris vary, and how wide does it open?** This is the one capability all
  three current devices lack entirely.
- **Sensor size**, because that determines how much depth-of-field control a given
  aperture actually buys you. → [[Sensor-Size-and-Crop-Factor]]
- **What focal lengths it can reach.** The kit today is 13–120 mm equivalent with a hole
  through the middle of it.

Fill this row in when it exists: ____________________

## What this kit can and cannot do

Four structural facts. Each one shapes an assignment, so they matter more than any
spec row above.

1. **No variable aperture anywhere.** All three irises are fixed. Aperture is a
   *constant* in your exposure triangle rather than a control — so [[Aperture]] can be
   read and reasoned about, but not yet demonstrated by you.
2. **Small sensors behind wide lenses means deep depth of field.** Nearly everything is
   in focus whether you want it or not. Subject separation has to be engineered from
   subject distance and background choice, not bought with an f-stop. The iPhone's
   Portrait mode *simulates* the rest in software. → [[Depth-of-Field]]
3. **Wide is the default.** Only the iPhone's 5× lens reaches past 24 mm, so perspective
   compression is a one-lens experiment for now.
4. **Two of the three are motion-first.** They write real raw DNG files, but they were
   designed around a gimbal and a helmet mount. Their image quality is not the
   constraint; their ergonomics for slow, deliberate still photography are.

### What this kit is unusually good at
Available light (the Pocket 3's 1" sensor) · motion, timelapse and hyperlapse · POV and
angles a camera can't physically reach · and **10-bit log video**, which is the reason
[[LUTs]] is genuinely relevant to you instead of being trivia.

## Module by module

| Module | Shootable with this kit | Needs care, or camera #4 |
|---|---|---|
| 0 — Orientation | Yes, entirely | — |
| 1 — Exposure | Shutter and ISO ladders: DJI Pro mode, iPhone via a third-party app | **A1.1, the aperture ladder, cannot be shot on any device you own** |
| 2 — Light | Yes, entirely — light doesn't care what you're holding | — |
| 3 — Composition | Yes | Focal length is nearly a constant; compression studies need the 5× |
| 4 — Post-Processing | Yes — all three write raw DNG | LUTs apply to your *video*, not your stills → [[LUTs]] |
| 5 — Genres | Street, landscape, travel, documentary | Shallow-DOF portraiture, and anything needing reach |
| 6 — Seeing & Critique | Yes, entirely | — |

> [!important] Flagged for the [[Roadmap]]
> A1.1 is scheduled for week 1 and assumes an aperture you can change. With this kit it
> is not shootable. Decide deliberately: reorder it after A1.2 and A1.3, borrow a body
> for one afternoon, or hold it until camera #4 — then write the decision into
> [[Roadmap]]. Don't leave it sitting there as a silent blocker.

## How I set it in the field
<!-- Yours. The button, not the concept. -->
- **Manual shutter/ISO on the iPhone — which app, and where:** ____________________
- **Getting into Pro mode on the Pocket 3:** ____________________
- **Getting into Pro mode on the Action 5 Pro:** ____________________
- **Turning raw DNG on, per device:** ____________________
- **Which device I reach for by default, and whether that's a decision or a habit:**
  ____________________

## What I got wrong
<!-- Replace with what YOU actually believed. -->
- 🔸 Before reading this, how many of your three devices did you think had an aperture
  you could change? What did you take the f-number on the spec sheet to mean?
- 🔸 The Pocket 3 is f/2.0 and the Action 5 Pro is f/2.8 — about a stop apart. Which of
  the two actually gives shallower depth of field on the same subject, and why is the
  f-number not the whole answer?
- 🔸 Portrait mode and a real f/1.4 lens produce different-looking blur. Name one thing
  the software gets wrong that optics cannot.

## Proof from my own frames
<!-- A0.1 isn't finished until you've shot one frame on each device and confirmed from
     the actual metadata what format, resolution and settings you got. -->
- 

## Related
[[Aperture]] · [[Exposure-Triangle]] · [[Sensor-Size-and-Crop-Factor]] ·
[[Depth-of-Field]] · [[RAW-vs-JPEG]] · [[Camera-Menu-Baseline]] ·
[[Ingest-and-Backup-Workflow]] · [[LUTs]]

## Source
- Claude draft, 2026-08-19, from memory of published specifications — **replace this
  line** with the official spec page for each device once you've checked them
- 
