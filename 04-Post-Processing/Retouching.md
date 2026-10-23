---
title: Retouching
type: concept
module: 4
tags:
  - post/local
created: 2026-10-22
---
# Retouching

> [!summary] In one line
> Retouching removes or repairs small things: dust spots, blemishes, a stray wire. The
> tools are easy. The hard parts are keeping the repair invisible, and knowing when
> removing something changes what the photo claims is true.

## What it is

| Tool | What it does | Use it for |
|---|---|---|
| **Heal** | Copies texture from a nearby area, then matches it to the colour and brightness around the spot | Dust, blemishes and small marks on smooth areas: sky, skin, walls |
| **Clone** | Copies pixels exactly from another area | Edges, lines and patterns, where healing would smear |
| **Content-aware remove** | Fills the area by studying its surroundings | Larger objects: a bin, a sign, a distant person |
| **Generative remove** | An AI model invents new pixels to fill the area | Big or complicated areas; it can invent details that were never there |

In Lightroom, the Remove tool has heal, clone and content-aware modes, plus an optional
generative AI mode. darktable has a retouch module, and Capture One uses healing and
clone layers.

## How it works

### Heal versus clone

**Clone** copies the source exactly: its texture, colour and brightness. If the source
is slightly brighter than the spot you're covering, you get a visible patch.

**Heal** takes only the texture from the source. It takes colour and brightness from
the pixels around the spot, then blends the edge. That's why it vanishes so well on a
smooth sky or on skin. But next to a strong edge, it pulls in colour from the other
side: heal a spot beside a dark door frame and you get a dark smudge. Use clone there,
because it keeps edges and patterns intact.

### Content-aware and generative fills

Content-aware remove builds a fill from the pixels around the hole. Generative remove
asks a trained model to paint new pixels that fit. Both can be impressive, and both can
invent things that weren't there: extra bricks, warped lettering, a hand with the wrong
shape. Always inspect the fill at 100%.

### Dust spots

Dust on the sensor casts a small shadow onto it. That shows as a soft, dark blob, most
visible on smooth, bright areas like sky. At small apertures such as f/11–f/16, light
reaches the sensor in a narrower cone, so the shadow is sharper and easier to see. Dust
stays in one place on the sensor, so it appears in the same spot on every frame from a
session.

To find dust you can't see, make it visible for a moment. Lightroom has a view called
Visualize Spots that shows the photo as outlines, where dust appears as small rings. In
any editor, you can push Contrast and Dehaze very high, or drag a very steep curve, fix
the spots that appear, and then undo those moves.

### Skin

The usual rule for portraits: **remove what is temporary, keep what is permanent.** A
spot, a scratch or a stray hair can go. A mole, a scar or freckles stay, unless the
person asks. That respects the person, and they still recognise themselves.

**Keep the texture.** Pores are what make skin look real. Smoothing tools, or a large
negative Texture or Clarity move, make skin look like plastic, so heal with a small
brush instead. **Reduce rather than remove:** soften a line under the eyes at about half
strength rather than making it disappear.

**Frequency separation** is an advanced technique for Photoshop-style layer editors.
It splits the skin into two layers. A blurred **tone** layer holds the colour and the
soft changes of light and shade. A **texture** layer holds the fine detail: pores, fine
hairs, small lines. (Tutorials call them the low- and high-frequency layers.) You can
then heal blemishes on the texture layer and even out blotchy, uneven tone on the tone
layer, without losing the pores. It's easy to overdo: smooth the tone layer too much
and faces look flat and painted, even with the pores still there. Learn healing first;
most portraits never need more.

## How to use it

### A dust pass

1. **Crop first,** so you don't fix spots you'll cut away. → [[Crop-and-Straighten]]
2. **Zoom to 100%,** and turn on the spot view or push the contrast for a moment.
3. **Work in a grid:** left to right, top to bottom, so you don't miss an area.
4. **Heal on smooth areas, clone near edges.** Make the brush slightly larger than the
   spot.
5. **If the source looks wrong, move it.** Automatic source choice sometimes picks a
   patch with the wrong texture, or one that repeats a pattern.
6. **Copy the fixes to other frames** from the same session, then check each one.
7. **Check again after big tone moves.** More contrast reveals spots you didn't see.

Big removals go better in a pixel editor with layers, such as Photoshop or Affinity.
There you can repair one area at a time and hide a repair you don't like.

### Ethics: what's acceptable where

| Kind of work | Usually acceptable | Usually not |
|---|---|---|
| News, documentary, "unaltered" contest categories | Exposure, contrast, colour, cropping that doesn't change the meaning, dust removal, modest dodge and burn | Removing or adding anything; composites; generative fill |
| Personal and art work | Almost anything, if you're honest about it when it matters | Presenting a composite as a real moment |
| Commercial work and client portraits | Blemishes, stray hairs, distractions, changes the client agreed to | Changing someone's face or body without consent; misleading buyers about a product |

In documentary work, a photo is a claim: "this was there". Removing even a small object
breaks that claim. In 2014 the Associated Press cut ties with a photographer who had
removed a colleague's video camera from the corner of a photo taken in Syria.

**Disclosure** keeps you honest everywhere else. If you removed or added something
significant, say so in the caption. Many contests ask finalists for the original raw
file to compare. Some editors can attach Content Credentials: a record of how an image
was made and edited. Some countries now require a label on adverts in which a body has
been retouched. Rules differ between countries and change over time, and this is not
legal advice. → [[Copyright-and-Consent]]

A quick test: would the viewer feel misled if they saw the original? If yes, disclose
it, or don't do it.

## On your kit

- **The L10's lens is fixed,** so you never open the camera to change lenses. Sensor
  dust should be rarer than on an interchangeable-lens camera. Check yours: photograph a
  plain, bright sky at f/16 and look for spots.
- **Water drops on the Action 5 Pro's lens** show up as soft, distorted blobs, and
  they're hard to remove cleanly. Wipe the lens between shots instead.

## Common mistakes

- **Plastic skin.** Smoothing removes the pores that make skin look real. Heal small
  marks and keep the texture.
- **Repeating patterns.** Cloning from the same source again and again leaves visible
  copies. Vary the source.
- **Healing next to an edge.** Heal pulls in colour from across the edge and smears it.
  Clone there instead.
- **Trusting generative fill.** Check every fill for invented details and warped
  lettering.
- **Removing things from a documentary photo.** It breaks the photo's claim to show what
  was there. Burn the distraction down, or crop it, instead. → [[Dodge-and-Burn]]

## Try it

Twenty minutes. On the L10, photograph a plain, bright sky or a white wall at f/16. Find
any spots with the spot view or a steep curve, remove them, and copy the fixes to a
second frame from the same session. Then take a portrait: remove three temporary marks,
keep anything permanent, and soften one line at half strength. Compare before and after
at normal size. Can you tell what changed?

## Check yourself

> [!question]- A dust spot sits right next to a dark door frame. Heal or clone, and why?
> Clone. Heal takes colour and brightness from around the spot, so it would pull in the
> dark of the frame and leave a smudge. Clone copies a clean patch exactly.

> [!question]- Why do dust spots show more at f/16 than at f/2.8?
> At small apertures, light reaches the sensor in a narrower cone, so the dust's shadow
> is sharper and darker. At wide apertures the shadow is so soft that it almost
> disappears.

> [!question]- In a news photo, what may you usually do about a distracting sign at the edge?
> Crop it out if that doesn't change the meaning, or darken it a little with a burn. You
> may not remove it with a heal, clone or generative tool.

> [!question]- Why "remove what's temporary, keep what's permanent" on skin?
> A spot isn't part of who the person is; a mole or a scar is. Keeping permanent
> features keeps the portrait honest, and the person still recognises themselves.

> [!question]- You use generative remove on a travel photo for your portfolio. What should you do?
> Say so wherever it matters, such as in the caption and in any contest entry. Check
> contest rules first, because many forbid it. Never present the photo as an unaltered
> record.

## Related
[[Local-Adjustments]] · [[Dodge-and-Burn]] · [[Crop-and-Straighten]] · [[Portraiture]] ·
[[Documentary-and-Photojournalism]] · [[Copyright-and-Consent]] ·
[[Post-Processing-Index]]
