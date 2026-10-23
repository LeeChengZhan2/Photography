---
title: Colour Spaces
type: concept
module: 4
tags:
  - post/colour
created: 2026-10-22
---
# Colour Spaces

> [!summary] In one line
> A colour space defines which real colours a file's numbers stand for. Edit in a wide
> one, export in the one your viewer expects (sRGB for the web), and embed the profile,
> or colours come out washed out or oversaturated.

## What it is

A colour space is a recipe for turning RGB numbers into real colours. It fixes three
things: exactly which red, green and blue its three **primaries** are, what counts as
white, and a tone curve.

The range of colours a space can describe is its **gamut**. It's usually drawn as a
triangle inside a horseshoe shape that holds every colour people can see. The corners
of the triangle are the primaries. A bigger triangle reaches more saturated colours.

| Space | Gamut | Main use |
|---|---|---|
| sRGB | The smallest here | The web, most screens; the safe default |
| Display P3 | Wider, mostly in reds and greens | Apple devices, iPhone photos, many modern screens |
| Adobe RGB (1998) | Wider, mostly in greens and cyans | Print work; a JPEG option on many cameras |
| ProPhoto RGB | Huge: far beyond any screen or printer | A working space for editing, in 16-bit |
| Rec.709 | Same primaries and white as sRGB | HD video |

Display P3 shares sRGB's white and tone curve, so the only difference is the wider
primaries. HDR video uses a much wider standard again, called Rec.2020.

## How it works

### Same numbers, different colours

The numbers red 255, green 0, blue 0 mean "the most saturated red this space has". In
sRGB that's one red. In Display P3 it's a deeper red. So numbers alone are ambiguous.
The **embedded profile** is the label in the file that says which space they belong to.
A colour-managed app reads the label and shows the right colour. → [[Colour-Management]]

### What a mismatch looks like

| What happened | What you see |
|---|---|
| A P3, Adobe RGB or ProPhoto file is read as sRGB (profile stripped or ignored) | Washed out and dull; ProPhoto looks very flat |
| An sRGB file is shown on a wide-gamut screen by an app that ignores profiles | Oversaturated: skin too red, grass too green |
| A file in a wide space is converted to sRGB | Very saturated colours, like neon signs and flowers, lose detail and flatten |

The first case is the classic one. A saturated colour needs less extreme numbers in a
wide space, because the space's primaries are already more saturated. Read those
numbers as sRGB, and you get duller colours.

### Gamut and bit depth

Gamut is how far the range reaches. [[Bit-Depth]] is how finely it's divided. Spread
256 levels across ProPhoto's huge range and each step is a big jump, so skies band.
Wide spaces need 16-bit.

### Colours that don't fit

When you convert to a smaller space, colours outside it must move to the nearest colour
that fits. A bright red flower can turn into a flat red blob with no detail. Soft
proofing with a gamut warning shows you which colours will move before you export.

## How to use it

### Which space to edit in

- **Raw files** have no colour space until they're developed. Your raw developer works
  in its own wide internal space, so you only choose a space when you export.
- **Handing a file to a layer editor:** a 16-bit TIFF in ProPhoto RGB, Adobe RGB or
  Display P3.
- **Camera JPEGs and phone HEICs:** stay in the space they came in. Converting an sRGB
  JPEG to a wider space adds no colours; they were already limited to sRGB.

### Which space to export in

| Destination | Space | Because |
|---|---|---|
| Web and social | sRGB | It's what browsers and apps assume for a file with no profile, and nearly every screen can show it |
| Print lab | What the lab asks for, often sRGB | Labs set up their machines for one space |
| Home printer, colour-managed | The wide master | The printer profile does the conversion |
| Archive master | 16-bit TIFF in a wide space, or keep the raw and edits | Keeps every colour for later |
| SDR video | Rec.709 | The standard for HD delivery |

A P3 export looks richer only on a wide-gamut screen in a colour-managed app, and some
platforms convert or strip it. sRGB looks right nearly everywhere.

## On your kit

- **Lumix L10:** an RW2 has no colour space until developed. Cameras usually offer
  sRGB or Adobe RGB for their JPEGs; that setting affects the JPEG, HEIF and preview,
  not the raw.
- **iPhone 15 Pro Max:** its photos are in Display P3, which is why they look rich on
  the phone. When you export them for the web from a computer, convert to sRGB. Its
  video is HDR (Dolby Vision) by default, which sits in the wider Rec.2020 world.
- **Log footage:** Apple Log, D-Log M and V-Log each need a technical transform to
  Rec.709, such as the LUT each maker publishes. → [[LUTs]]

## Common mistakes

- **Exporting ProPhoto or Adobe RGB JPEGs for the web.** Many viewers show them dull.
  Export sRGB.
- **Exporting without the profile embedded.** Viewers have to guess. Embed it.
- **Converting a JPEG to a wider space to "get more colour".** Nothing is gained. The
  colours were already limited.
- **ProPhoto in 8-bit.** The steps are too coarse; skies band. Use 16-bit.
- **Assuming a wide-gamut export looks better for everyone.** Only some screens and apps
  can show it.

## Try it

Fifteen minutes, with one vivid photo: a neon sign, a flower, or an iPhone photo:

1. In your editor, soft proof the photo with sRGB as the profile and turn on the gamut
   warning. Which colours fall outside sRGB?
2. Export it twice: an sRGB JPEG and a ProPhoto RGB JPEG.
3. Open both in a web browser, then in a simple image viewer or chat app. Note where
   they look the same and where the ProPhoto copy looks dull.

Do this before you export the **A4.5** set, so all twelve leave in the same space.

## Check yourself

> [!question]- What does "gamut" mean, and is a bigger one always better?
> It's the range of colours a space can describe. Bigger helps only if the screen or
> printer can show the extra colours, the file has enough bit depth, and every app
> reads the profile.

> [!question]- Your Adobe RGB JPEG looks dull after you upload it. Why?
> The site stripped or ignored the profile, so the numbers were read as sRGB. In a wide
> space a saturated colour has less extreme numbers, so read as sRGB they look duller.

> [!question]- Why is sRGB the safe choice for the web?
> Browsers and apps assume sRGB when a file has no profile, and nearly every screen can
> show it. So it looks right almost everywhere.

> [!question]- Does converting an sRGB JPEG to ProPhoto RGB give you more colours to work with?
> No. The colours were already limited to sRGB when the JPEG was made. The conversion
> only relabels them in a bigger space.

## Related
[[Colour-Management]] · [[Bit-Depth]] · [[Export-Settings]] · [[LUTs]] ·
[[Video-Export-Settings]] · [[RAW-vs-JPEG]] · [[Post-Processing-Index]]
