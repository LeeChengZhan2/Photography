---
title: Printing
type: concept
module: 4
tags:
  - post/output
created: 2026-10-22
---
# Printing

> [!summary] In one line
> A print can't glow, so it shows every decision the screen hid. Give it enough pixels
> for the viewing distance, choose the paper on purpose, soft proof, and expect to
> brighten the print version.

## What it is

Printing turns pixels into ink on paper. It involves four decisions:

1. **Size and resolution:** how big, and how many pixels per inch.
2. **Paper:** glossy, lustre, matte or fine art.
3. **Matching the screen:** soft proofing and brightness.
4. **Who prints it:** a print lab or your own printer.

A print is also the most honest view of your work. You can't zoom, the screen's glow
is gone, and people look at it for longer.

## How it works

### Resolution and viewing distance

**ppi** (pixels per inch) is how many of your pixels fill each inch of paper. About
300 ppi looks fully sharp at reading distance, around 30 cm, because that's close to
the finest detail the eye can see that close. The eye sees less detail further away,
so a large print viewed from a metre or two looks just as sharp at about 150 ppi.

Printers quote **dpi** (dots per inch). Those are ink droplets, several per pixel.
It's a different number; you only set ppi.

Print size = pixels ÷ ppi. The L10's 4:3 frame is 5200 × 3900 px:

| Resolution | Print size | Good for |
|---|---|---|
| 300 ppi | About 44 × 33 cm | Close viewing: A4 or A3 easily |
| 200 ppi | About 66 × 50 cm | A wall print seen from a step away |
| 150 ppi | About 88 × 66 cm | A large print seen from across a room |

Short of pixels? AI upscaling can enlarge a file convincingly for moderate sizes. It
invents the new detail, so check the result at 100%.

### Paper

| Paper | Surface | Strengths | Trade-offs |
|---|---|---|---|
| Glossy | Shiny | Deepest blacks, most saturated colour | Reflections and fingerprints |
| Lustre (semi-gloss) | Fine texture, slight sheen | Nearly as rich as glossy, fewer reflections | The usual lab default; a safe first choice |
| Matte | No shine | No glare, a soft, quiet look | Weaker blacks, duller colours, needs more sharpening |
| Fine art (cotton rag, baryta) | Heavy; textured or satin | Long-lasting, beautiful surface | Costly; matte and glossy kinds exist |

Choose for the photo and for the wall. A glossy print opposite a window shows the
window.

### Why prints look darker than screens

A screen emits light. Paper only reflects the light in the room. So:

- Paper white is much dimmer than screen white.
- The darkest ink is still far from true black. A good screen can show a contrast of
  1000:1 or more; a glossy print manages a few hundred to one, and matte paper less.
- Most people edit on screens far brighter than any print.

The result: shadows close up, and the whole print looks darker and flatter than the
screen. → [[Dynamic-Range]]

What to do about it:

- **Lower your screen's brightness** for print work, to about 80–120 cd/m².
  → [[Colour-Management]]
- **Soft proof** with the printer's profile for that paper, and adjust a print copy.
- **Make the print version brighter,** often by a fraction of a stop, especially in the
  shadows.
- **Make a test strip:** print the same crop at three brightness steps (0, +⅓ and
  +⅔ stop) on one sheet. Pick the best under the light where the print will hang.

### Print labs and home printers

| | Print lab | Home printer |
|---|---|---|
| Cost | Pay per print; cheap for occasional prints | Printer, ink and paper; ink is expensive |
| Quality | Calibrated machines, consistent results | As good as your profiles and setup |
| Control | Choose from their papers | Full control, instant test prints |
| Files | Their format and colour space | Print from the master through a colour-managed print dialog |

For **A4.6**, a lab is the simple choice. Ask four things: which file format, which
colour space, whether they offer a printer profile for soft proofing, and how to turn
off automatic correction, so your choices aren't re-edited.

Singapore's humidity is hard on paper, as it is on lenses. Keep paper sealed, and keep
prints in sleeves or framed behind glass.

## How to use it

A checklist for a first print:

1. **Pick the photo and the size,** A4 or larger.
2. **Check the pixels:** print size in inches × 300 ppi, or less for a big print.
3. **Choose the paper.** Lustre if unsure.
4. **Lower the screen brightness** and soft proof with the lab's profile.
5. **Make a print copy** and adjust it: brighter shadows, check the colours.
6. **Export for print:** the lab's colour space, sharpening for that paper, JPEG at
   quality 100 or TIFF. → [[Export-Settings]]
7. **Order a small test first** if you can.
8. **Judge the print under daylight-balanced light,** about 5000 K, not under a warm
   lamp.

## On your kit

- **Lumix L10:** your best print source. 5200 px on the long edge (5408 px at 3:2)
  prints A3 at about 300 ppi.
- **iPhone 15 Pro Max:** 48 MP ProRAW from the 1× lens has the most pixels you own.
  Other lenses give 12 MP, about 4000 × 3000 px, which still covers A4 at 300 ppi.
- **Pocket 3:** a 3072 px square, cropped to A4's shape, prints at about 260 ppi. That
  looks fine at arm's length.
- **Action 5 Pro:** 40 MP leaves room for big prints. Use Standard (Dewarp) for
  anything with straight lines.

Noise that shows at 100% on screen often disappears in a print. Judge the print, not
the zoomed screen.

## Common mistakes

- **Printing straight from an edit made on a bright screen.** The print comes out dark
  and muddy. Lower the brightness, soft proof, and make a test strip.
- **Confusing ppi with dpi.** You set ppi. The printer's dpi is about ink droplets.
- **Insisting on 300 ppi for a big wall print.** It's viewed from further away. 150–200
  ppi is enough.
- **Leaving the lab's auto-correction on.** It re-edits your file. Ask them to turn it
  off.
- **Judging the print under a warm lamp.** Everything looks yellow. Use daylight or a
  daylight-balanced bulb.

## Try it

This is **A4.6**: print one photo, A4 or larger, and note everything the screen lied
about.

1. Follow the checklist above.
2. Before the full print, make a test strip at 0, +⅓ and +⅔ stop.
3. When the print arrives, hold it next to the screen. Write down three differences:
   brightness, shadows, colour.

The capstone also asks for one print. This first one teaches you what to change.

## Check yourself

> [!question]- Why doesn't a large print viewed from two metres need 300 ppi?
> The eye sees less detail further away. At two metres it can't resolve 300 pixels per
> inch, so about 150 ppi looks just as sharp.

> [!question]- Why do prints usually look darker than the same photo on screen?
> A screen emits light; paper only reflects room light. Paper white is dimmer, black ink
> isn't truly black, and most screens are set far brighter than a print can be.

> [!question]- When would you choose matte paper over glossy?
> When glare would be a problem, or for a soft, quiet look. You accept weaker blacks and
> duller colours, and add more output sharpening.

> [!question]- How large can the L10's 4:3 frame print at 300 ppi?
> 5200 ÷ 300 is about 17.3 inches, or 44 cm. 3900 ÷ 300 is 13 inches, or 33 cm. So
> about 44 × 33 cm: bigger than A3's 42 × 29.7 cm.

> [!question]- Why ask the lab to turn off automatic correction?
> It re-edits your file to an average look, undoing the brightness and colour choices
> you made while soft proofing.

## Related
[[Colour-Management]] · [[Export-Settings]] · [[Sharpening]] · [[Colour-Spaces]] ·
[[Dynamic-Range]] · [[Portfolio-Construction]] · [[Post-Processing-Index]]
