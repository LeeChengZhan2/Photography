---
title: Editing Workflow
type: concept
module: 4
tags:
  - post/workflow
created: 2026-10-22
---
# Editing Workflow

> [!summary] In one line
> Editing is five stages in a fixed order: ingest, cull, develop, export, archive. The
> order protects your files and saves hours, and a fixed routine is what lets you
> finish 200 frames in under two hours.

## What it is

A workflow is the route every photo takes from the memory card to a finished, safely
stored file. It has five stages:

| Stage | What you do | What you have at the end |
|---|---|---|
| **Ingest** | Copy the files off the card, back them up, import them into your editor | Two copies of every file, in a named folder |
| **Cull** | Choose the frames worth editing and reject the rest | A short list of picks |
| **Develop** | Edit the picks: tone, colour, crop, local work | Saved edit settings for each pick |
| **Export** | Make finished files for a purpose: screen, print, a client | New JPEG or TIFF files |
| **Archive** | Store raws, edits and exports for the long term | Three copies, one of them off-site |

"Develop" is the old darkroom word for turning film into a picture. Raw editors use it
for the editing stage.

## How it works

Each stage hands its result to the next, and each one is cheaper when the stage before
it was done properly. That is why the order matters.

- **Ingest comes first** because the card is your only copy. Cards fail, get lost and
  get formatted by accident. Nothing else happens until a second copy exists.
  → [[Ingest-and-Backup-Workflow]]
- **Cull comes before develop** because editing is the expensive stage. At about
  5 minutes per frame, editing all 200 frames of a shoot would take over 16 hours.
  Editing the best 12 takes one hour. → [[Culling-Discipline]]
- **Develop comes before export** because in a raw editor your edits are only
  instructions. Export is the step that turns them into pixels in a new file.
  → [[Non-Destructive-Editing]]
- **Archive comes last** because the archive should hold the edits and the exports
  too. Until then, the backup you made at ingest protects the raws.

You can go back a stage, and non-destructive editing makes that safe. But every trip
back costs time. The biggest leak is re-culling while you develop: "maybe this other
frame is better". Finish the cull, then trust it.

### A time budget: the Gate 4 test

Gate 4 asks you to turn a folder of 200 frames into a coherent set of twelve in under
two hours. That only works with a budget for each stage:

| Stage | Time | How it fits |
|---|---|---|
| Ingest | 5 min | Import the folder and check the backup. Copying runs on its own |
| Cull | 30 min | About 4 s per frame on a first pass (13 min), then a slower pass on the 30–40 survivors |
| Develop | 60 min | 15–20 min on the strongest frame to set the look, then 3–4 min on each of the other eleven |
| Export | 5 min | One saved preset; mostly waiting for the computer |
| Archive | 10 min | Back up the raws, the edits and the exports; check the copies |
| **Total** | **1 h 50 min** | Ten minutes of slack, so the cull and develop limits are hard limits |

**A4.3** practises the cull alone, at the same pace: 100 frames to 10 keepers in 15
minutes. The weekly hour to edit and cull in the [[Roadmap]] is the same plan, smaller:
about 15 minutes of culling and 40 of developing.

### Catalogue-based and folder-based editors

Raw editors keep track of your photos in one of two ways.

| | Catalogue-based | Folder-based |
|---|---|---|
| How it works | You import photos into a database, called the catalogue | You browse your folders directly |
| Where edits live | Inside the catalogue file | In a small "sidecar" file next to each photo |
| Examples | Lightroom Classic; Capture One catalogues | Adobe Bridge with Camera Raw; RawTherapee; Capture One sessions |
| Strengths | Fast search across years: ratings, keywords, collections | Simple; the edits travel with the photos |
| Weak spot | Move or rename files outside the app and it loses them | Searching across many folders is slow |
| What to back up | The catalogue as well as the photos | The sidecars, which sit with the photos anyway |

Darktable does both: a library database plus a sidecar for every photo. Either kind
works. What matters is one editor, one folder structure, and never moving files behind
the editor's back. → [[Archive-Strategy]]

### Computer, iPad or iPhone

A computer is the best place for the whole workflow. The big screen shows missed focus,
keyboard shortcuts make culling fast, and the backup drives plug into it.

An iPad or iPhone is fine for a first look on the way home, or a quick edit to share.
But a phone screen is too small to judge sharpness, and raw files fill a phone fast.
Keep one home for the library: files edited on two devices without syncing become two
versions that disagree. Lightroom and Capture One both have iPad apps, so check how
yours syncs before you edit on more than one device.

## How to use it

A weekly session:

1. **Ingest straight after the shoot.** Check that the backup opens before you format
   the card.
2. **Cull in one sitting, with a timer.** Flags only on the first pass.
3. **Develop the picks only.** Start with the strongest frame, because it sets the look
   for the rest. Work in a fixed order. → [[Basic-Panel-Order]]
4. **Export with saved presets**, one for screens and one for print, so you decide those
   settings once. → [[Export-Settings]]
5. **Archive.** Run the backup, then write the shoot log.

Time-box every stage, because editing expands to fill whatever time you give it. For a
set like A4.5, build the look on one frame, copy the settings to the others, then adjust
each one. → [[Developing-a-Look]]

## On your kit

- **All four devices write raw:** RW2 from the L10, ProRAW DNG from the iPhone, DNG from
  the Pocket 3 and the Action 5 Pro. One editor can handle all four.
- **The L10 is a 2026 camera.** Raw editors need an update before they can read a new
  camera's raw files. Check that your editor's current version opens the L10's RW2
  before you rely on it.
- **The iPhone has no card.** Its photos land in the phone's library first. Some
  transfer methods convert files on the way, so check that what arrives on the computer
  is the DNG or HEIC you shot, not a converted JPEG.
- **Mixed devices take longer to develop.** Each one renders colour and contrast
  differently, so a set made from L10 and iPhone files needs extra time to match. Plan
  for that in A4.5.

## Common mistakes

- **Editing before culling.** You polish frames you later reject. Cull the whole shoot
  first, then edit only the picks.
- **Formatting the card before checking the backup.** Open a few files from the backup
  first. A copy that won't open is not a copy.
- **Moving files in File Explorer behind a catalogue's back.** The catalogue loses track
  of them. Move and rename files inside the editor.
- **Switching editors mid-module.** The speed this module builds is muscle memory. Pick
  one editor from [[Resources]] and stay with it.
- **No time limit.** Without one, developing swallows the whole session. Set a timer for
  each stage.

## Try it

Thirty minutes, a small version of the Gate 4 test. Take 50 frames from any earlier
shoot and turn them into a coherent set of three. Run all five stages with a timer, and
write each stage's time in a shoot log. Which stage ran over, and why?

This also rehearses **A4.3**, the timed cull.

## Check yourself

> [!question]- Why cull before you develop, rather than editing as you go?
> Editing is the slow stage. At about 5 minutes a frame, editing 200 frames takes over
> 16 hours; editing the best 12 takes one. Culling first means you only spend that time
> on frames you will keep.

> [!question]- You move a folder of raws to a new drive with File Explorer, and your catalogue now shows them as missing. What happened?
> A catalogue stores the location of every file. It didn't see the move, so it still
> looks in the old place. Point the catalogue to the new folder, and next time move
> files from inside the editor.

> [!question]- Why does archive come after export, and what protects the raws until then?
> The archive should hold the finished work: raws, edit settings and exports. Those only
> all exist after developing and exporting. Until then, the second copy you made at
> ingest protects the raws.

> [!question]- In a Gate 4 practice run, the cull took 70 minutes. What most likely went wrong?
> The first pass was too slow. You were comparing and ranking, which is the second
> pass's job. A first pass takes a few seconds per frame and answers only "maybe" or
> "no".

> [!question]- Is a folder-based editor safer than a catalogue-based one?
> Neither is safer by itself. A catalogue keeps all your edits in one file that must be
> backed up. Sidecars sit beside the photos and must travel with them. Each fails only
> if you break its rule.

## Related
[[Ingest-and-Backup-Workflow]] · [[Culling-Discipline]] ·
[[Non-Destructive-Editing]] · [[Basic-Panel-Order]] · [[Export-Settings]] ·
[[Archive-Strategy]] · [[Developing-a-Look]] · [[Post-Processing-Index]]
