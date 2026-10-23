---
title: Archive Strategy
type: concept
module: 4
tags:
  - post/workflow
created: 2026-10-22
---
# Archive Strategy

> [!summary] In one line
> An archive is where finished shoots live for years. Keep three copies on two kinds of
> storage with one off-site, back up the catalogue too, and test that you can restore.

## What it is

[[Ingest-and-Backup-Workflow]] gets your files off the card and into two places on the
day you shoot. This note picks up from there: keeping them safe for years, not days.

Your archive is your photo library plus its backups. The standard plan is called
**3-2-1**:

| Rule | Meaning | Protects you from |
|---|---|---|
| **3** copies | The original plus two backups | Any single copy failing |
| **2** kinds of storage | Different devices: the computer's drive and an external drive, or a drive and the cloud | Two copies failing the same way at the same time |
| **1** off-site | One copy in another building, or in the cloud | Fire, flood, theft, or a power surge that hits everything at home |

## How it works

### Why each number

- **Three copies:** every drive fails eventually, and you don't get to choose when.
  With three independent copies, losing all of them at once is very unlikely.
- **Two kinds:** copies that share a weakness fail together. Two drives of the same
  model, bought the same day, can wear out the same way. One program that syncs all
  your copies can copy one mistake to all of them.
- **One off-site:** whatever happens to your room happens to every copy in it.
  Singapore's frequent thunderstorms are one more reason not to keep every copy plugged
  into the same wall.

### A sync is not a backup

A sync service keeps folders identical. Delete a folder by mistake, and the sync deletes
it everywhere. A backup keeps older versions, so you can go back to last week. If you use
a cloud folder, check whether it keeps deleted files and old versions, and for how long.

### Folder structure: year, then date and name

```
Photos/
  2026/
    2026-11-01-aperture-ladder/
    2026-12-13-four-times-of-day/
  2027/
    2027-01-23-a4-3-cull-test/
      exports/
    2027-02-06-chinatown-blue-hour/
```

- **Year folders** stop any one folder from growing to hundreds of entries.
- **Date first** (`YYYY-MM-DD`) sorts in time order in any app, on any computer.
- **A short name** makes the shoot findable without opening it. Use the same name as
  the shoot log, so the two match.
- **An `exports` folder** inside each shoot keeps the finished files with their raws.

### Backing up the catalogue

With a catalogue-based editor, your edits live in the catalogue, not in the photos.
Without it, you keep the negatives and lose every edit. → [[Non-Destructive-Editing]]

Lightroom Classic offers to back up its catalogue when you quit. By default that backup
goes in a folder next to the catalogue, on the same drive, so on its own it doesn't
count. Make sure your backup routine copies the catalogue's folder too. Preview files
can be rebuilt, so they matter less.

### The cloud, in general terms

A cloud backup service copies your files to a data centre somewhere else: an off-site
copy that happens on its own. It costs a monthly fee and upload time. Raw files are tens
of megabytes each, so the first upload of a big library can take days on a home
connection, and Module 5's video is far larger. Check that the service keeps deleted
files and old versions. If your photos show people, read its privacy terms too.

### Testing a restore

A backup you have never restored from is a hope, not a backup. Drives fail quietly,
settings change, and a folder gets left out by accident. The only proof is getting files
back.

## How to use it

### What to keep

| Keep | Why |
|---|---|
| The raws (at least the picks) | They're your negatives. Future software will get more out of them |
| The catalogue or the sidecars | They hold your edits |
| Final exports | The finished photo as you meant it, as shared or printed |
| No need: previews, caches, test exports | Your editor can rebuild them |

Whether to keep the rejects is a separate choice. → [[Culling-Discipline]]

### A routine

1. **At ingest:** raws go into `year/date-name`, with a second copy straight away.
2. **After export:** run the backup, so it includes the new edits and exports.
3. **Every month:** update the off-site copy.
4. **Every three months:** do a restore test.
5. **Every year:** check free space and drive health. Replace old backup drives before
   they fail, not after.

You already have two copies from Module 0. 3-2-1 adds the third copy and moves one away
from home. Cloud isn't the only way: an external drive kept somewhere else, such as at
work or at a relative's home, and updated every month, is the classic off-site copy.

### This vault is the notebook

This vault's git repository holds notes and small reference JPEGs only. Raw files never
go in. Git keeps every version of every file forever, so a few hundred raws would make
the repository too big to clone or sync. That's why raw formats are blocked in
`.gitignore` on purpose. The photos live in your archive, and your shoot logs point to
them by folder name. → [[Conventions]]

## On your kit

- **Each device adds its own files:** RW2 from the L10 (plus JPEG or HEIF if you shoot
  both), ProRAW DNG or HEIC from the iPhone, DNG or JPEG from the two DJIs. Files from
  one shoot go in one shoot folder, whichever device made them.
- **Video grows the archive fastest.** All four devices shoot log video, and Module 5
  will add more data than all your stills. Check your free space before it starts.
- **The iPhone's photo library is not an archive.** If it syncs to a cloud service,
  that is a sync, not a backup: deleting on one device usually deletes everywhere. Copy
  the originals into your archive like any other camera's files.

## Common mistakes

- **Treating a sync folder as a backup.** A mistake syncs everywhere. Use backup
  software or a service that keeps old versions.
- **All copies in one room.** One fire, flood or theft takes them all. Keep one copy
  off-site.
- **Forgetting the catalogue.** The photos come back, but the edits don't. Back up the
  catalogue's folder too.
- **Never testing a restore.** You find out a backup is broken on the day you need it.
  Test every few months.
- **Reorganising the archive outside the editor.** A catalogue loses track of moved
  files. Move and rename them inside the editor.

## Try it

Thirty minutes. Restore one shoot from Module 1 out of your backup into a temporary
folder. Open three of its raws and check that the edits are there. Time it, and note
anything missing. Then write your 3-2-1 map in a shoot log: every copy, the device it's
on, and where that device lives. This builds on **A0.2**'s dry run.

## Check yourself

> [!question]- Your photos are on your laptop and on an external drive that sits next to it. Is that 3-2-1?
> No. It's two copies in one place. A theft, fire or power surge can take both. You
> need a third copy, and one of the copies off-site.

> [!question]- Your cloud folder syncs automatically, and you delete a shoot folder by mistake. What happens?
> The sync deletes it everywhere. Unless the service keeps deleted files or old
> versions, it's gone. That's why a sync is not a backup.

> [!question]- The raws are backed up three times. Why back up the catalogue as well?
> In a catalogue-based editor, the edits live in the catalogue, not in the raws.
> Without it you'd have unedited negatives and many hours of lost work.

> [!question]- Why name a folder `2027-02-06-chinatown` rather than `Chinatown Feb`?
> A date-first name sorts in time order everywhere, never clashes with next year's
> shoot, and matches your shoot log's name.

> [!question]- Why do raw files stay out of this vault's git repository?
> Git keeps every version of every file forever. Large raws would soon make the
> repository too big to clone or sync. The vault is the notebook; the archive holds the
> negatives.

## Related
[[Ingest-and-Backup-Workflow]] · [[Editing-Workflow]] · [[Non-Destructive-Editing]] ·
[[Culling-Discipline]] · [[Export-Settings]] · [[Conventions]] ·
[[Post-Processing-Index]]
