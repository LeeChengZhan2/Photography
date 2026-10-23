---
title: Codecs and Bitrate
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-22
---
# Codecs and Bitrate

> [!summary] In one line
> A codec is the method used to squeeze video into a file, and the bitrate is how much
> data it may use per second. Together they decide the quality, the file size, and
> whether the footage edits smoothly or stutters.

## What it is

Uncompressed video is enormous, so every camera compresses it. Three terms get mixed up:

| Term | What it is | Examples |
|---|---|---|
| Container | The file wrapper: holds the video, the sound and information about them | .mov, .mp4 |
| Codec | The method that compresses the picture inside | H.264, H.265 (HEVC), ProRes |
| Bitrate | How much data the codec may use per second | 100 Mbps |

The container is the box; the codec is how the contents were packed. A .mov file can
hold H.264, H.265 or ProRes, so the file extension tells you almost nothing about
quality.

The three codecs you'll meet:

| Codec | Compression | Where you'll see it | In the editor |
|---|---|---|---|
| H.264 (AVC) | Long-GOP, heavy | Older cameras, phones, most web delivery | Plays on almost anything |
| H.265 (HEVC) | Long-GOP, heavier and more efficient | Modern phones and cameras; 10-bit | Can stutter on slower computers |
| ProRes | Intra-frame, light | Apple's editing codec; Apple Log on the iPhone | Smooth, but the files are huge |

## How it works

### Long-GOP and intra-frame

GOP means "group of pictures". Long-GOP codecs (H.264, H.265) store a complete frame
only every so often. In between, they store just what changed from the frames around
it. In a still interview little changes, so the in-between frames are tiny. That's why
these codecs make small files.

The cost comes in editing. To show one in-between frame, the computer must first decode
the last complete frame, then rebuild every change up to the one you want. Scrubbing,
cutting and playing backwards repeat that work constantly.

Intra-frame codecs (ProRes, and some cameras' "All-I" modes) compress every frame on
its own, a bit like a series of JPEGs. The files are much bigger, but any frame can be
shown straight away. That's why ProRes edits smoothly.

### H.264 vs H.265

H.265 is a newer design. It finds more ways to throw away data you won't miss, so it
often reaches similar quality at roughly half to two-thirds of H.264's bitrate. It also
handles 10-bit well. The price is more computing power to decode it.

### Bitrate and quality

Bitrate is measured in megabits per second (Mbps). More bits per second means fewer
compression artefacts: blocky patches, smeared fine detail and banding. Fine, moving
detail needs the most: leaves in wind, rain, water, crowds. Noise counts as fine detail
too, so high-ISO footage suffers first.

A byte is eight bits. To turn a bitrate into a file size:

- MB per minute ≈ Mbps × 60 ÷ 8 = Mbps × 7.5
- 100 Mbps × 7.5 = 750 MB per minute

Rough sizes, for planning cards and drives:

| Recording | Typical bitrate | Per minute |
|---|---|---|
| 1080p, H.264 | About 10–30 Mbps | About 75–225 MB |
| 4K, H.265 or H.264 | About 50–150 Mbps | About 0.4–1.1 GB |
| 4K, ProRes 422 HQ, 25–30 fps | About 600–700 Mbps | About 4–6 GB |

Exact numbers vary with the device, the frame rate and the setting. Check a test clip's
details to see what yours really records.

### 8-bit vs 10-bit

8-bit stores 256 levels per colour channel; 10-bit stores 1024. On a finished clip you
won't grade, you'll rarely see the difference. Grade it hard, especially log, and
smooth 8-bit areas such as skies break into bands. → [[Bit-Depth]]

### 4:2:0 vs 4:2:2

Your eye sees fine detail mostly in brightness, much less in colour. So video saves
space by storing colour at a lower resolution than brightness. This is called chroma
subsampling:

| Label | Colour detail stored | Where you'll see it |
|---|---|---|
| 4:4:4 | Full | High-end work |
| 4:2:2 | Half the width | ProRes 422; some cameras' 10-bit modes |
| 4:2:0 | Half the width and half the height: a quarter | Most H.264 and H.265 footage, and nearly all web video |

For normal viewing you'll struggle to see the difference. It matters when you push
colour hard or cut out a green screen, where colour edges need to be precise.

### Why H.265 can stutter, and how proxies help

Many computers have a hardware decoder: a part of the chip built to unpack common
codecs quickly. When a clip's exact variant isn't supported (10-bit 4:2:2 H.265 is a
common gap), the processor has to do all the work itself, and playback stutters.

**Proxies** fix this. The editor makes small, easy-to-decode copies of your clips,
often low-resolution ProRes or DNxHR. You edit with the copies, and the editor swaps
the originals back in for the export. DaVinci Resolve and Premiere Pro both offer
proxies. They cost disk space and some waiting up front. → [[Video-Editing-Workflow]]

## How to use it

1. **Record the best setting your editing computer can handle.** A high bitrate and
   10-bit help most when you plan to grade.
2. **Use 10-bit for log and HLG.** 8-bit is fine for a standard profile you won't push.
3. **Plan storage from the bitrate.** Multiply Mbps by 7.5 for MB per minute, then by
   the minutes you expect to shoot. Double it for a
   [[Ingest-and-Backup-Workflow|backup]].
4. **Test playback before a big edit.** Put a clip from each device on a timeline and
   scrub it. If it stutters, make proxies before you start.
5. **Deliver in H.264 or H.265.** Every platform plays them. ProRes is for editing, not
   for sharing. → [[Video-Export-Settings]]

## On your kit

- **iPhone 15 Pro Max:** Apple Log needs ProRes. Internal ProRes stops at 4K 30 fps;
  4K 60 fps needs an external USB-C SSD. At several gigabytes a minute, ProRes fills
  the phone fast, so copy it off after each shoot. Video is HDR (Dolby Vision) by
  default.
- **Pocket 3 and Action 5 Pro:** 10-bit D-Log M needs a 10-bit codec. On devices like
  these that usually means H.265, so test it in your editor and expect to make proxies.
- **Lumix L10:** check its menu for each recording mode's codec, bit depth and bitrate.
  Choose a 10-bit mode for V-Log.
- **All four in one timeline (A5.5):** a mix of ProRes and H.265 is normal. Set the
  timeline to one frame rate and resolution, and let the editor handle the codecs.

## Common mistakes

- **Judging quality by resolution alone.** 4K at a low bitrate can look worse than
  1080p at a healthy one, especially with leaves, water or noise.
- **Confusing Mbps with MB/s.** A small b is bits; a capital B is bytes, eight times
  bigger. 100 Mbps is 12.5 MB/s.
- **Editing H.265 straight from the card on a slow computer.** It stutters. Copy the
  files to a fast drive and make proxies.
- **Recording ProRes "just in case".** It fills storage fast. Use it when you need it,
  as you do for Apple Log.
- **Reading quality from the file extension.** .mov or .mp4 says nothing about the
  codec or bitrate inside.

## Try it

Fifteen minutes, with one clip from each device you own:

1. Film 30 seconds of the same busy scene on each device, such as leaves moving in the
   wind or a busy road.
2. For each clip, find the codec, bit depth, bitrate and file size. Your editor's clip
   information shows them, or a free tool such as MediaInfo.
3. Work out the MB per minute from the bitrate (Mbps × 7.5), and compare it with the
   real file size.
4. Put all the clips on one timeline. Scrub back and forth, and note which ones stutter.

A preview of **A5.5**, where every camera's files meet in one timeline.

## Check yourself

> [!question]- You get two files, clip.mov and clip.mp4. Can you tell which is better quality?
> No. .mov and .mp4 are containers. Either can hold H.264, H.265 or other codecs, at any
> bitrate. Look at the codec, bit depth and bitrate inside.

> [!question]- ProRes files are far bigger than H.265 files. Why do they edit more smoothly?
> ProRes compresses every frame on its own, so the computer can show any frame straight
> away. H.265 stores most frames as changes from other frames, so the computer must
> rebuild each one before it can show it.

> [!question]- A camera records at 150 Mbps. Roughly how much space do 10 minutes take?
> 150 × 7.5 = 1125 MB per minute, about 1.1 GB. Ten minutes is about 11 GB, and twice
> that once you keep a backup.

> [!question]- Your 10-bit H.265 clips play fine in a media player but stutter in the editor. What's going on, and what do you do?
> Playing forward is the easy case. Editing means jumping around, scrubbing and playing
> backwards, and every jump means rebuilding frames from their group. Without a hardware
> decoder for that variant, the computer falls behind. Make proxies.

> [!question]- When does 4:2:2 matter more than 4:2:0?
> When you push colour hard in the grade, or cut out a green screen. Both need precise
> colour edges, and 4:2:2 keeps twice as much colour detail. For normal viewing, the
> difference is hard to see.

## Related
[[Bit-Depth]] · [[Log-Profiles]] · [[Frame-Rate]] · [[Video-Editing-Workflow]] ·
[[Video-Export-Settings]] · [[Ingest-and-Backup-Workflow]] · [[Video-Index]]
