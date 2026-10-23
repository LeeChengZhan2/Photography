---
title: Non-Destructive Editing
type: concept
module: 4
tags:
  - post/workflow
created: 2026-10-22
---
# Non-Destructive Editing

> [!summary] In one line
> In a raw editor, your edits are saved as a list of instructions and the original file
> never changes. You can undo, change or copy any edit at any time, and only an export
> makes new pixels.

## What it is

There are two ways to edit a photo:

| | Destructive | Non-destructive |
|---|---|---|
| What changes | The pixels in the file | Nothing in the original file |
| What is saved | New pixels, over the old ones | A list of instructions: the "recipe" |
| Going back | Only if you kept a copy | Any time, step by step |
| Typical tools | A simple image editor that saves over a JPEG | Every raw editor: Lightroom, Capture One, darktable, RawTherapee |

A recipe might read: "white balance 5200 K, exposure +0.7, contrast +15, crop to 3:2". It
takes a few kilobytes. The original stays exactly as the camera wrote it.

## How it works

### The recipe is replayed every time

When you open a photo, the editor reads the untouched original, applies the recipe in a
fixed order, and shows the result on screen. Move a slider, and the editor changes one
line of the recipe and redraws the preview. Nothing is written into the original.

That's why you can undo an edit from last year, or change the crop after you've
finished the colour. Raw files can't be edited any other way. A raw file is sensor
data, not a finished picture, so the editor always builds the picture from it.
→ [[RAW-vs-JPEG]]

### Where the recipe lives

| Storage | How it works | Examples |
|---|---|---|
| **Catalogue** | One database file holds the recipes for all your photos | Lightroom Classic; Capture One catalogues |
| **Sidecar file** | A small text file next to each photo, with the same name | XMP files in Adobe Camera Raw and darktable; RawTherapee's .pp3; DxO PhotoLab's .dop |

XMP (Extensible Metadata Platform) is a standard format for information about a file.
A sidecar such as `beach-012.xmp` sits beside `beach-012.RW2` in the same folder.

Each has a weak spot. Lose the catalogue and you lose every edit at once. Copy a photo
without its sidecar and the edit stays behind. Lightroom Classic can also write XMP
sidecars, which gives you a second copy of your recipes.

Recipes don't travel well between editors. Another app can often read the ratings and
keywords in an XMP file, but not the develop settings, because each editor's processing
is its own.

### Three ways to keep more than one version

- **Virtual copy:** a second recipe for the same original. It costs almost no disk
  space. Capture One calls these variants; darktable calls them duplicates.
- **Snapshot:** a saved point in one photo's edit that you can jump back to.
- **History:** every change, recorded as a step. Click an earlier step to go back.

Use a virtual copy when you want two versions to exist side by side. Use a snapshot as
a bookmark before an experiment.

### Export makes new files

Exporting renders the recipe into a new file, such as a JPEG for the web or a TIFF for
print. The original and the recipe stay as they were. Need a different size next year?
Export again from the same recipe. → [[Export-Settings]]

### What destructive editing does

Open a JPEG in a simple editor, brighten it, press Save, and the brighter pixels replace
the old ones. The original is gone. JPEG makes it worse: every save compresses the
picture again, so small artefacts (blocky patches, ripples at edges) build up with each
round. This is called generation loss.

Pixel editors with layers, such as Photoshop and Affinity, can work non-destructively
too. Adjustment layers sit above the pixels, as long as you keep the layered file and
export a copy.

## How to use it

- **Never edit the only copy of anything.** Raw editors protect the raw for you, and
  they treat a JPEG the same way, so edit JPEGs there too.
- **Use virtual copies for alternatives.** A4.1's three interpretations are three
  virtual copies of one raw, not three files.
- **Take a snapshot before a big experiment,** so you can jump back in one click.
- **Back up the recipes with the photos:** the catalogue, or the sidecars.
  → [[Archive-Strategy]]
- **Export to a separate folder,** with new file names. Never export over an original.
- **Copy whole folders, not single files,** so sidecars travel with their photos.

## On your kit

- **Your edits never change the picture inside an RW2 or DNG.** One detail: Adobe apps
  write their XMP into a DNG file itself, not into a separate sidecar. The DNG's date
  changes; its picture doesn't.
- **Some looks are destructive at capture.** The L10's Real Time LUT bakes a look into
  its JPEG and HEIF files. On the iPhone, Photographic Styles bake in at capture on this
  model. Shoot RAW alongside on the L10, or ProRAW on the iPhone (ProRAW can't take a
  style), and the look stays a decision you can change. → [[LUTs]]
- **Phone gallery apps often keep the original** and let you revert an edit. Check that
  yours does before you rely on it.

## Common mistakes

- **Copying raws without their sidecars.** The edits stay behind. Copy whole folders.
- **Backing up the photos but not the catalogue.** You keep the negatives and lose every
  edit. Back up both.
- **Duplicating files to try another version.** It doubles the storage and splits the
  history. Make a virtual copy instead.
- **Re-editing and re-saving a JPEG.** Every save adds artefacts. Export again from the
  raw instead.
- **Treating the export as the edit.** The export is one rendering; the recipe is the
  edit. Keep the recipe, and export again when you need to.

## Try it

Twenty minutes, a small version of **A4.1**. Make three virtual copies of one raw. Edit
them as bright and airy, moody and contrasty, and black and white. Reset one copy to
zero and watch the original come back. Then look at the raw in File Explorer: its size
and date haven't changed. Export all three into a new folder.

## Check yourself

> [!question]- You edit an RW2 for an hour, then check it in File Explorer: its date and size haven't changed. Where did the hour of work go?
> Into the recipe: inside the catalogue, or in a sidecar file next to the raw. The raw
> itself is only ever read, never written.

> [!question]- You send a friend only the RW2 file. What do they see when they open it?
> The unedited raw, rendered with their editor's defaults. Your edits are in your
> catalogue or sidecar. Even with the sidecar, a different editor usually can't read
> your develop settings.

> [!question]- Why does saving a JPEG ten times make it worse, while exporting from a raw ten times doesn't?
> Each JPEG save compresses an already-compressed picture, so artefacts build up. Each
> export starts again from the untouched raw and the recipe, so nothing accumulates.

> [!question]- When would you use a virtual copy rather than a snapshot?
> When you want two versions to exist at once: a colour and a black-and-white version,
> or one crop for print and another for the web. A snapshot is only a bookmark in one
> photo's history, so you see one state at a time.

## Related
[[Editing-Workflow]] · [[RAW-vs-JPEG]] · [[Archive-Strategy]] · [[Export-Settings]] ·
[[LUTs]] · [[Developing-a-Look]] · [[Post-Processing-Index]]
