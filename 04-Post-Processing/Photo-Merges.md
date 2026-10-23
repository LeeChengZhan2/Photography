---
title: Photo Merges
type: concept
module: 4
tags:
  - post/merge
created: 2026-10-22
---
# Photo Merges

> [!summary] In one line
> A merge combines several frames into one photo that a single frame couldn't hold:
> more dynamic range (HDR), a wider view (panorama) or more depth of field (focus
> stacking). Each only works if the frames were shot to be merged.

## What it is

Sometimes one frame can't record what you see. A merge solves that by shooting several
frames that each capture part of the problem, then combining them in software.

| Merge | The problem | What you shoot | What you get |
|---|---|---|---|
| HDR merge | Brightness range too wide for one exposure | The same frame at several exposures (a bracket) | One file with detail in both highlights and shadows |
| Panorama | Scene too wide or tall for the lens | Overlapping frames, turning the camera | One wider, higher-resolution image |
| Focus stack | Not enough depth of field | The same frame focused at different distances | One image sharp from front to back |

## How it works

### HDR merge

A sensor records only a limited range of brightness. → [[Dynamic-Range]] A bracket
covers more: for example three frames at −2, 0 and +2 EV. The dark frame keeps the
sky; the bright frame keeps the shadows. The software takes clean highlights from one
and clean shadows from the other. Many raw developers save the result as a new
raw-like DNG file.

That file holds more range than a screen can show. You still have to edit it down,
just like a raw: lower the highlights, lift the shadows. The famous **"HDR look"**
(grey skies, glowing halos around buildings, no true blacks, oversaturated colour)
comes from pushing that step too far, not from the merge itself. Keep some shadows
dark and some highlights bright, and an HDR merge just looks like a good photo.

Modern sensors hold a lot in one raw file. Bracket only when the range is extreme: the
sun in the frame, or a dark room with a bright window.

### Panorama stitching

The software finds the same details in overlapping frames, lines them up, and bends
them onto one surface. Three things make that work:

- **Rotate around the lens, not your body.** Swing the camera around a point inside the
  lens. Otherwise near and far objects shift against each other between frames
  (parallax), and the software can't line both up. For distant scenes it matters less.
- **Overlap each frame by about 30%,** so the software has plenty of shared detail to
  match.
- **Lock exposure, white balance and focus,** in manual. If each frame meters itself,
  the sky changes brightness from frame to frame and the joins show.

Shoot a horizontal panorama with the camera held upright (portrait orientation). Each
frame is taller, so you get more height and more room to crop the uneven edges.

### Focus stacking

Close up, depth of field shrinks to millimetres. → [[Depth-of-Field]] In a landscape,
you may want a flower 50 cm away and hills far away both sharp. You could stop down,
but small apertures cost sharpness to diffraction. A stack avoids that. Shoot several
frames, moving focus from near to far so the sharp zones overlap. The software keeps
the sharpest part of each frame. Raw developers often can't do this; a layer editor
(in Photoshop, Auto-Blend Layers) or a dedicated stacking app can.

### Ghosting

Anything that moves between frames (people, leaves, waves, cars) appears in different
places in each one. The merge shows half-transparent copies, called **ghosts**. Most
HDR tools have a deghost setting that takes moving areas from one frame only. Shoot the
frames quickly, and avoid wind for focus stacks.

## How to use it

1. **Decide at capture.** A merge needs frames shot for it; you can't make one from a
   single frame later.
2. **Use a tripod if you have one.** If not, brace against a railing or wall, or use a
   fast shutter and let the software align the frames.
3. **HDR:** three frames 2 stops apart covers most scenes. Change only the shutter
   speed, so depth of field stays the same.
4. **Panorama:** manual exposure set for the brightest part, camera upright, about 30%
   overlap, a steady turn.
5. **Focus stack:** fix the aperture (f/4–f/5.6 on the L10, before diffraction), then
   step focus from nearest to furthest. Use manual focus. → [[Manual-Focus]]
6. **Merge first, then edit** the merged file like any raw.

## On your kit

- **Lumix L10:** the best merge camera you own: full manual control and RW2 raw files.
  Check the manual for auto bracketing; otherwise change the shutter speed by hand in
  M. AF Macro reaches 3 cm at 24 mm, where a focus stack
  helps most. → [[Macro]]
- **iPhone 15 Pro Max:** it already merges for you. Multi-frame HDR, Night mode and
  Deep Fusion combine several frames into every photo, ProRAW included.
  → [[Computational-Photography]] That's why phone files rarely need an HDR merge.
- **Pocket 3:** its stills are only about 8–9 MP, so a panorama is a good way to get more
  pixels. Rotate the screen for vertical framing.
- **Action 5 Pro:** the fisheye bends lines differently across the frame, which makes
  stitching harder. Use Standard (Dewarp) if you try a panorama.

## Common mistakes

- **Overcooking the HDR.** Halos and grey skies give it away. Keep real blacks and
  bright highlights.
- **Letting each panorama frame meter itself.** The brightness changes and the joins
  show. Lock exposure in manual.
- **Bracketing with the aperture.** Depth of field changes between frames and the merge
  goes soft. Bracket with the shutter speed.
- **Too little overlap.** The software can't match the frames. Overlap by about a third.
- **Merging scenes full of movement.** Use deghosting, or pick another subject.

## Try it

Thirty minutes:

1. Take your **A4.2** bracket (−3 to +3 EV). Merge the −2, 0 and +2 frames into an HDR
   file. Edit it to look natural, then push it until it looks "HDR". Note the point
   where it turns.
2. Shoot a five-frame panorama of a skyline from a footbridge on the L10: upright,
   manual exposure, about 30% overlap. Stitch it.

## Check yourself

> [!question]- Why must the frames of an HDR bracket change shutter speed, not aperture?
> Changing the aperture changes depth of field, so each frame would have a different
> sharp zone and the merge would blur. The shutter changes only brightness, for still
> scenes.

> [!question]- Why does turning your body, rather than the lens, cause problems in a panorama with a close foreground?
> The lens moves sideways as you turn, so near and far objects shift against each
> other between frames. That parallax means the software can't line up both at once.

> [!question]- Where does the overcooked "HDR look" actually come from?
> From the edit after the merge: extreme local contrast and lifted shadows push
> everything towards the middle grey. The merge just collects the data; a gentle edit
> looks natural.

> [!question]- Why focus stack a landscape instead of just stopping down to f/16?
> On the L10, diffraction softens everything from about f/5.6–f/8. A stack keeps each
> frame at a sharp aperture and builds the depth from several frames.

## Related
[[Dynamic-Range]] · [[Depth-of-Field]] · [[Computational-Photography]] · [[Macro]] ·
[[Landscape]] · [[Hyperfocal-Distance]] · [[Post-Processing-Index]]
