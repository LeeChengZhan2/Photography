---
title: Video Editing Workflow
type: concept
module: 5
tags:
  - video/editing
created: 2026-10-22
---
# Video Editing Workflow

> [!summary] In one line
> Editing a film follows a fixed order: copy and organise the footage, build the story
> from rough to fine, lock the picture, then do colour and sound, then export. Working
> in that order stops you doing the same job twice.

## What it is

A workflow is the order you do the jobs in. Every editor follows the same order,
because each stage needs the one before it. DaVinci Resolve even lays out its pages
this way: Media, Cut, Edit, Fusion, Color, Fairlight, Deliver.

| Stage | What you do | It's done when |
|---|---|---|
| Ingest | Copy the cards to the computer and back them up | Two copies exist on two drives |
| Organise | Sort clips into bins, rename them, mark the good moments | You know what you have |
| Assembly | Put every useful shot on the timeline in story order | The whole story is there, too long |
| Rough cut | Cut it down until the story works | It makes sense from start to end |
| Fine cut | Trim each cut to the exact frame | Every cut feels right at full speed |
| Picture lock | Decide the picture won't change any more | You stop moving clips |
| Colour and sound | Match and grade the clips; mix the sound | It looks and sounds like one film |
| Export | Render the finished files | You've watched the export to the end |

A **bin** is a folder inside the editor that holds links to your clips. Only the names
change between editors, so pick one from [[Resources]] and stay with it.

## How it works

**Work from big decisions to small ones.** Which scenes, in what order, is a big
decision; which frame to cut on is a small one. Polish a cut in a scene you later
delete and the polishing was wasted. So the story comes first and the frames last.

**Picture lock protects colour and sound.** A grade is attached to a clip. A music fade
or a change in voice level is attached to a moment in time. Move a cut afterwards and
the fade lands in the wrong place, and a new shot arrives ungraded. Colour and sound
don't depend on each other, so you can do them in either order.

**Editing never changes your camera files.** The timeline is a list of instructions:
which file, which frames, which adjustments. This is
[[Non-Destructive-Editing|non-destructive editing]]. It's also why moving or renaming a
file after you import it breaks the project: the editor looks in the old place and
marks the clip "media offline".

**Proxies fix stuttering playback.** Most cameras and phones record H.264 or H.265,
which store most frames as changes from the frames around them. To show one frame, the
computer must rebuild it from others, so jumping around, playing backwards and 10-bit
4K make playback stutter. A **proxy** is a small, easy-to-play copy of a clip, such as
1080p ProRes Proxy or DNxHR LB. You edit with proxies; the editor switches back to the
originals for colour and export. Resolve's "optimised media" does the same job.
→ [[Codecs-and-Bitrate]]

## How to use it

### 1. Ingest

1. Make one folder per project, named by date and subject: `2027-02-27-coffee-sequence`.
2. Inside it, make the same folders every time: `01-footage` (with one folder per
   device), `02-audio`, `03-music`, `04-project`, `05-proxies` and `06-exports`.
3. Copy each card or phone into its device folder. Copy everything; choose later.
4. Make a second copy on another drive before you format any card.
   → [[Ingest-and-Backup-Workflow]]
5. Keep footage out of this vault: it's far too big for git, and the vault ignores it.

### 2. Organise

1. Start a project and set its frame rate to match your footage (25 fps if you followed
   [[Frame-Rate]]) **before** you import. Some editors can't change it later.
2. Import the folders. Make bins: one per device or one per scene, plus `Selects`,
   `Music` and `Sound`.
3. Watch everything once. Press L twice to play at double speed.
   → [[Timeline-and-Trimming]]
4. Mark the good moments with markers or favourites. Rename clips by shot size and
   content: `CU hands pour`, `WS stall morning` (CU is close-up, WS is wide shot).
5. If playback stutters, make proxies now. In Resolve: select the clips, right-click,
   Generate Proxy Media.

### 3. Cut

1. **Assembly.** Drag your selects onto the timeline in story order. Don't trim
   carefully yet. It will be two or three times too long, and that's fine.
2. **Rough cut.** Remove whatever doesn't serve the story. Watch from the start after
   each pass. → [[Story-Structure]]
3. **Fine cut.** Trim to the frame, cut on action, add J- and L-cuts, set the pace.
   → [[Cuts-and-Transitions]]
4. **Picture lock.** Watch once without stopping. If nothing needs to move, duplicate
   the timeline as `v4-locked`. Duplicate before every big change too, as a backup.

### 4. Finish

1. **Colour:** correct each clip, then grade the whole film. → [[Shot-Matching]]
2. **Sound:** balance dialogue, ambience, effects and music. → [[Sound-Mixing]]
3. **Export** a master and the versions you'll post, then watch the export to the
   end. → [[Video-Export-Settings]]
4. **Archive** the footage, the project and the master. Proxies and render files can
   go, because the editor can rebuild them. → [[Archive-Strategy]]

Resolve keeps projects in a database you can't see: export each one as a `.drp` file
into `04-project` after every session. Other editors' project files go there too.

### A time budget for a one-minute film

The Module 5 exit test asks for a one-minute film from 30 minutes of footage in under
three hours. One way to spend them:

| Stage | Minutes |
|---|---|
| Ingest, back up, make bins | 15 |
| Watch everything, mark selects | 30 |
| Assembly | 20 |
| Rough cut | 35 |
| Fine cut and picture lock | 30 |
| Colour and sound | 40 |
| Export and watch | 10 |
| **Total** | **180** |

Set a timer for each stage, and move on when it rings. A finished film teaches more
than a perfect half of one.

## On your kit

- **iPhone:** Apple Log needs ProRes, and ProRes files are many times larger than the
  iPhone's normal video. Copy them off after every shoot. Its normal video is HDR by
  default, so decide before you import whether you'll convert it.
- **Pocket 3 and Action 5 Pro:** 10-bit D-Log M clips can stutter on a laptop. Make
  proxies before you start cutting.

## Common mistakes

- **Editing straight from the card.** When the card is formatted or lost, the project
  loses its footage. Copy and back up first, then import from the drive.
- **Moving files after you import them.** Set up the folders first. If clips go "media
  offline", use the editor's relink command and point it at the new folder.
- **Polishing before the story works.** Perfect cuts in a scene you later delete are
  wasted. Rough cut the whole film first.
- **Not watching the export.** Some problems are easy to miss until the exported file:
  a viewing LUT that never made it into the export, or one applied twice; a music
  track left muted. Watch the export once, all the way through.

## Try it

Thirty minutes, any device, as a dry run for **A5.2** (the video version of A0.2):

1. Film eight short clips of one small task at home, such as making tea.
2. Ingest them into the folder structure above, and make the second copy.
3. Make two bins, rename every clip, and mark one good moment in each.
4. Build a rough 20-second assembly and export it.
5. Write down how long each stage took, and fix whatever was annoying.

## Check yourself

> [!question]- Why does picture lock come before colour and sound?
> Colour is attached to clips, and sound changes are attached to moments in time. If
> you move cuts afterwards, fades and level changes land in the wrong place and new
> shots arrive ungraded. Locking first means you do that work once.

> [!question]- Playback stutters on your D-Log M clips, but the export looks perfect. What's happening, and what do you do?
> The clips are slow to decode, so the computer can't rebuild frames fast enough to
> play them live. Rendering doesn't have to happen in real time, so the export is
> fine. Make proxies, edit with them, and export from the originals.

> [!question]- You renamed your footage folder, and every clip now says "media offline". Why?
> The project doesn't contain the footage. It stores the path to each file, and the
> path changed. Relink the clips to the new folder, or change the name back.

> [!question]- Your assembly is three minutes long for a one-minute film. Is something wrong?
> No. An assembly holds every useful shot in story order, so it should be too long.
> Cutting it down is the rough cut's job. A short assembly usually means you dropped
> shots before you knew whether you needed them.

## Related
[[Ingest-and-Backup-Workflow]] · [[Codecs-and-Bitrate]] · [[Timeline-and-Trimming]] ·
[[Story-Structure]] · [[Shot-Matching]] · [[Sound-Mixing]] · [[Video-Export-Settings]] ·
[[Video-Index]]
