---
title: Metering Modes
type: concept
module: 1
tags:
  - fundamentals/exposure
created: 2026-10-22
---
# Metering Modes

> [!summary] In one line
> The camera's light meter assumes every scene averages out to middle grey. Metering
> modes choose which part of the frame it reads. Knowing when it's wrong is the skill.

## What it is

A **light meter** measures light and suggests an exposure. The meter inside your camera
measures *reflected* light: the light bouncing off the scene towards the lens.

A **metering mode** decides which part of the frame the meter reads, and how much each
part counts:

| Mode | What it reads | Good for |
|---|---|---|
| Evaluative (also called matrix or multi-zone) | The whole frame, split into many zones and weighed by the camera's own logic | Most scenes; your default |
| Centre-weighted | The whole frame, with extra weight on the middle | Centred subjects; predictable results |
| Spot | A small circle, a few per cent of the frame | Backlit faces, a performer on stage, the moon |
| Highlight-weighted (some cameras) | Mostly the brightest areas, to stop them clipping | Stage lighting, spotlit subjects |

Brands use different names for the same idea. Canon says "evaluative", Nikon says
"matrix".

## How it works

### The middle-grey assumption

The meter can't tell what it's looking at. A white wall in shade and a grey wall in sun
can send back exactly the same amount of light. So the meter makes one assumption:
**the scene averages out to middle grey**, the tone of a standard grey card (often
called 18% grey). Most everyday scenes do: some bright parts, some dark, averaging
somewhere in the middle.

> [!note] Is middle grey really 18%?
> Not quite. Meters are set by a standard formula, not by a grey card, and most aim a
> little darker than an 18% card: about half a stop, often quoted as about 12%. So when
> you spot-meter a real grey card, add about +0.5 EV. Kodak's own grey-card
> instructions said the same.

When the scene is average, the meter is right. When it isn't, the meter drags it
towards grey anyway:

| Scene | What the meter thinks | Result | Fix |
|---|---|---|---|
| Snow, white sand, a white wall | "Too bright", so it darkens | Dull grey whites | +1 to +2 EV |
| A black jacket, a black cat | "Too dark", so it brightens | Washed-out grey blacks | −1 to −2 EV |
| A person against a bright sky | Mostly bright sky, so it darkens | Dark face, near silhouette | +1 to +2 EV, or spot meter the face |
| A singer in a spotlight on a dark stage | Mostly dark stage, so it brightens | Blown-out face and clothes | −1 to −2 EV, or spot / highlight-weighted |

The fix is [[Exposure-Compensation]], set in EV (one EV is one stop). You tell the
meter how far from grey your subject really is.

### How each mode decides

- **Evaluative** compares its zones. It often gives extra weight to the area around your
  focus point, and it tries to recognise hard scenes such as a bright sky. That makes
  it the best general mode, but also the hardest to predict.
- **Centre-weighted** averages the whole frame, with the middle counting most. It's
  simple, so you learn its mistakes quickly.
- **Spot** reads only a small circle, at the centre or at your focus point (the manual
  says which). Whatever you point it at becomes middle grey, whatever surrounds it.
- **Highlight-weighted** finds the brightest important areas and keeps them from
  clipping. The rest of the frame may go dark. It suits stage shows.

### Spot metering a known tone

Point the spot at something roughly middle grey: grey concrete, grass, or clear blue
sky away from the sun. Or point it at a known tone and adjust. A white wall with
texture sits about 2 stops above middle grey, so spot-meter it and add about +2 EV. A
black jacket with texture sits about 2 stops below, so take away about 2.

### The Zone System

Ansel Adams and Fred Archer turned this into a method around 1940: the **Zone System**.
It splits the tones from black (zone 0) to white (zone X) into zones one stop apart.
Whatever you spot-meter, the meter places on **zone V**, middle grey. You choose the
zone that tone belongs on and move the exposure by the difference. In M: spot-meter the
tone, set the scale to 0, then move the shutter by that many stops. Zone VII (a white
wall with texture) is +2 EV; zone III (a black jacket with texture) is −2 EV.

It still helps on digital. You decide where a tone should sit *before* you shoot, not
in editing. It is also the most precise way to
[[Expose-to-the-Right|expose to the right]]: spot-meter the brightest area that must
keep detail, then place it as high as your camera allows. Middle grey sits only about 3
stops below clipping (→ [[Dynamic-Range]]), so try +2 to +3 EV on that reading, and
check the highlight warning.

### How phones meter

A phone meters the whole scene, looks for faces, and often merges several frames to
hold bright and dark areas together. Ordinary scenes rarely fool it, but a bright
window or a stage still can. You steer it by touch:

- **Tap** the screen to set focus and exposure on that spot.
- **Press and hold** to lock both (AE/AF LOCK: auto-exposure and autofocus lock), so
  they stay put when you recompose.
- **Drag the sun icon** up or down to brighten or darken.

## How to use it

1. **Leave evaluative on** for everyday shooting. It's right most of the time.
2. **Read the scene first.** Is it mostly bright, mostly dark, or a bright background
   behind the subject? Then the meter will be wrong, and you know which way.
3. **Correct with exposure compensation** in P, A or S. Start with the amounts in the
   table above, then check the [[Histogram]].
4. **Switch to spot** when a small subject sits against a very different background: a
   face against a window, a performer on a dark stage.
5. **In M mode the meter still works.** It shows a scale, for example −3 … 0 … +3. Zero
   means "matches the meter's middle-grey guess". You decide whether to agree.
6. **Lock and recompose** when the right reading is in the wrong place. Meter the face,
   lock the exposure (most cameras have an exposure-lock button), then frame the shot.

## On your kit

- **Lumix L10:** the device to learn metering on. It offers multi, centre-weighted,
  spot and highlight-weighted metering (the last one sets exposure to protect the
  brightest areas). Multi is its evaluative mode: use it for A1.4, as the assignment
  says.
- **iPhone 15 Pro Max:** tap, press and hold for AE/AF LOCK, then drag the sun icon.
  It's the nearest thing to spot metering plus exposure compensation.
- **Pocket 3 and Action 5 Pro:** they meter automatically unless you set shutter and
  ISO yourself in Pro / PRO mode. Then the brightness is your job, as in M.

## Common mistakes

- **Trusting the meter on white or black subjects.** It makes both grey. Add exposure
  for white, take it away for black.
- **Spot metering a highlight by accident.** A spot on a white shirt darkens the whole
  photo by about 2 stops. Know exactly where the spot is.
- **Changing modes to fix every scene.** A new mode changes what the meter reads, not
  its middle-grey assumption. Exposure compensation is usually quicker.
- **Believing the meter shows the "right" exposure.** It shows middle grey. A night
  street or a white beach shouldn't look middle grey.
- **Ignoring the meter in M.** The scale in the viewfinder is still your meter. Read
  it, then decide.

## Try it

Fifteen minutes on the L10, in A mode with evaluative metering:

1. Fill the frame with a white wall and shoot. Then fill it with a black jacket or bag,
   in the same light, and shoot.
2. Compare them. Both will come out a similar grey.
3. Reshoot the wall at +1.7 EV and the jacket at −1.7 EV. Check both histograms.
4. Switch to M and spot metering. Point the spot at something mid-grey nearby and set
   the shutter until the scale reads 0. Shoot both subjects at that setting.

This is **A1.4**, plus one extra step.

## Check yourself

> [!question]- Why does a white wall come out grey with evaluative metering?
> The meter assumes the scene averages to middle grey. A frame full of white wall
> looks "too bright" to it, so it cuts the exposure until the wall is grey. Add about
> +1.5 to +2 EV.

> [!question]- Your friend stands in front of a bright window. Which metering mode would you use, and why?
> Spot, on the face. Evaluative sees mostly bright window and darkens everything. A
> spot reads only the face and makes it middle grey, so the window can't fool it; the
> window clips. Light skin sits a little above middle grey: add about +0.7 to +1 EV.

> [!question]- In spot mode you meter a white shirt by mistake. What happens to the photo?
> The shirt becomes middle grey, so the whole photo comes out about 2 stops too dark.

> [!question]- In step 4 of Try it, why do the wall and the jacket both look right with one setting?
> They're in the same light, and the exposure came from a mid-tone, not from either
> subject. So white records as white and black as black.

> [!question]- On your iPhone you tap a dark doorway. What happens to the sunny street around it?
> The phone exposes for the doorway, so everything brightens and the street may clip.
> Its frame merging can save some of it, but not always.

## Related
[[Exposure-Compensation]] · [[Histogram]] · [[Exposure-Triangle]] · [[Shooting-Modes]] ·
[[Dynamic-Range]] · [[Back-Button-Focus]] · [[Contrast-Ratio]] · [[Fundamentals-Index]]
