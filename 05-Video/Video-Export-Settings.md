---
title: Video Export Settings
type: concept
module: 5
tags:
  - video/delivery
created: 2026-10-22
---
# Video Export Settings

> [!summary] In one line
> Exporting turns your timeline into a file people can play. Match the frame rate to
> your footage, use H.264 for uploads and a high-quality master for keeping, and export
> SDR when you've mixed cameras.

## What it is

An export writes every frame of your timeline into a new video file. Resolve calls it
rendering, and does it on its Deliver page. These settings decide what the file is:

| Setting | What it decides | Usual choice |
|---|---|---|
| Resolution | Pixels across and down | Same as the timeline: 1920 × 1080 or 3840 × 2160 |
| Frame rate | Frames per second | Same as the footage, such as 25 fps |
| Codec | How the picture is compressed | H.264 for uploads |
| Bitrate | How much data per second | See the table below |
| Audio | Sound format and quality | AAC, 48 kHz, stereo |
| Colour | SDR or HDR | SDR Rec.709 |
| Aspect ratio | The shape of the frame | 16:9, 9:16, 1:1 or 4:5 |

A **codec** is the method used to compress the picture. **Bitrate** is how much data
each second of video may use, in megabits per second (Mbps). The **container** (MP4,
MOV) is the file that holds the video and the sound together.

## How it works

**Every export is a new compression.** The editor decodes your clips, applies the edit
and compresses the result again, losing a little detail. The platform then compresses
your upload once more. So upload better quality than the platform will show, and keep
a master that's barely compressed at all.

**Codecs trade size against ease.** → [[Codecs-and-Bitrate]]

| Codec | File size | Plays on | Use it for |
|---|---|---|---|
| **H.264** | Small | Almost everything | Uploads, sending to people |
| **H.265 (HEVC)** | Smaller for the same quality | Newer devices and apps; slower to edit | Uploads where size matters |
| **ProRes** | Very large | Editors and most professional tools | The master you keep |

ProRes is Apple's format. Where your editor can't write it, **DNxHR** does the same job.

**Bitrate is a data budget per second.** The picture's detail and movement share it. A
still interview needs little. Rain, leaves or a fast pan need much more, or they break
up into blocks. Higher resolution and frame rate need more too.

**Frame rate must match the source.** A 25 fps timeline exported at 30 fps needs 5
extra frames every second. The editor usually repeats one frame in every five, so
movement stutters five times a second. Export at the frame rate you shot and edited.
→ [[Frame-Rate]]

**SDR and HDR are different signals.** SDR (standard dynamic range) Rec.709 is what
normal screens show, and what your log footage becomes after its technical LUT. HDR
(high dynamic range) holds brighter highlights and more colour, but only HDR screens
show it properly; platforms convert it for everyone else. An HDR clip read as SDR
looks flat and wrong, and SDR clips look dull beside HDR ones. → [[Colour-Spaces]]

**Cropping to vertical costs pixels.** A 9:16 frame cut from the middle of a 16:9 one
keeps the full height but only a slice of the width:

| Source | Its 9:16 crop | Enough for 1080 × 1920? |
|---|---|---|
| 3840 × 2160 (4K) | 1215 × 2160 | Yes: it only has to shrink |
| 1920 × 1080 (HD) | About 608 × 1080 | No: it has to be enlarged, and looks soft |

The crop keeps less than a third of the frame's width, so the subject must be near the
centre. → [[Frame-and-Aspect-Ratio]]

## How to use it

### Starting settings

| Use | Resolution | Codec and container | Video bitrate | Audio |
|---|---|---|---|---|
| Upload, HD, 25 fps | 1920 × 1080, or 1080 × 1920 vertical | H.264, MP4 | About 10–20 Mbps | AAC, 48 kHz, 320 kbps |
| Upload, 4K, 25 fps | 3840 × 2160 | H.264, MP4 | About 35–60 Mbps | AAC, 48 kHz, 320 kbps |
| Smaller file | As above | H.265, MP4 | About half to two-thirds of the H.264 figure | AAC, 48 kHz, 320 kbps |
| Master to keep | The timeline's | ProRes 422 HQ or DNxHR HQ, MOV | Set by the codec | Uncompressed (PCM), 48 kHz, 24-bit |

At 50 fps, allow about one and a half times these bitrates. A 4K ProRes master can take
several gigabytes per minute, so keep it on your archive drive.

### Aspect ratios

| Ratio | Pixels | Where it's used |
|---|---|---|
| 16:9 | 1920 × 1080 | YouTube, TVs, computers |
| 9:16 | 1080 × 1920 | Reels, TikTok, YouTube Shorts |
| 1:1 | 1080 × 1080 | Square posts in a feed |
| 4:5 | 1080 × 1350 | Instagram feed posts |

### Reframing for vertical

1. Finish and lock the 16:9 edit. Duplicate the timeline and set it to 1080 × 1920.
2. Go through it shot by shot. Move each frame so the subject sits inside the vertical
   slice. Where the subject moves, keyframe the position.
3. Some editors can track the subject for you (Premiere Pro's Auto Reframe, Resolve's
   Smart Reframe), though not in every version. Check every shot either way.
4. Keep titles and captions away from the bottom and right edges, where the apps put
   their buttons and text.
5. Watch it all again. Some cuts that worked wide won't work tall; replace those shots.

### Captions

| | Burned in (open captions) | Separate file (closed captions) |
|---|---|---|
| What it is | Text drawn into the picture | A text file uploaded with the video, usually `.srt` |
| Viewer can turn it off | No | Yes |
| Looks the same everywhere | Yes | Depends on the player |
| Can be translated or searched | No | Yes |
| Best for | Reels and TikTok, often watched muted | YouTube |

An `.srt` file is plain text: each caption has a number, a time range such as
`00:00:01,000 --> 00:00:03,500`, and its words. Keep each caption to about 40
characters a line, two lines at most. Editors such as CapCut can write captions from
the speech; always check them, because they mishear names and local words.

## On your kit

- **iPhone:** normal video is HDR (Dolby Vision) by default. When it's cut with your
  other cameras, convert its clips to SDR Rec.709 in the editor, or turn HDR off before
  you shoot. Then export SDR Rec.709. → [[Shot-Matching]]
- **Pocket 3:** rotate the screen to film vertical. For the 9:16 version of **A5.6**,
  a few extra shots filmed upright can replace cropped ones.

## Common mistakes

- **Changing the frame rate on export.** 25 fps footage exported at 30 fps stutters.
  Export at the timeline's frame rate.
- **Exporting HDR from a mixed timeline.** The cameras won't match, and the result
  varies by platform and screen. Export SDR Rec.709.
- **Exporting only a compressed upload.** Any later version compresses it again. Keep
  a ProRes or DNxHR master.
- **Enlarging an HD crop for vertical.** It looks soft. Film at a higher resolution,
  such as 4K, if you plan to crop, or film the vertical shots upright.

## Try it

Twenty minutes, practice for **A5.6**:

1. Take any 20-second edit.
2. Export it three ways: H.264, H.265, and ProRes or DNxHR. Write down the file sizes,
   and whether you can see any difference on your screen.
3. Make a 9:16 copy of the timeline, reframe each shot, and export it.
4. Play it on your phone. Check that nothing important is cut off or hidden under the
   app's buttons.

## Check yourself

> [!question]- Your timeline is 25 fps, and you export at 30 fps. What happens?
> The footage has 25 frames a second and the file needs 30, so the editor repeats one
> frame in every five. Movement stutters five times a second. Export at 25 fps.

> [!question]- You crop a 9:16 frame from 4K footage and from HD footage. Which can fill a 1080 × 1920 frame without enlarging, and why?
> The 4K one. Its crop is 1215 × 2160, larger than 1080 × 1920, so it only has to
> shrink. The HD crop is about 608 × 1080 and must be enlarged, which looks soft.

> [!question]- Why export SDR Rec.709 when your film mixes iPhone and DJI clips?
> The iPhone records HDR by default, while your DJI clips are SDR Rec.709 after their
> LUTs. HDR and SDR can't match in one film, and different screens show HDR
> differently. One SDR Rec.709 film looks consistent on almost every screen.

> [!question]- When would you burn captions in, and when would you upload a separate file?
> Burn them in for vertical apps, where many people watch with the sound off and
> caption files may not be supported. Upload an `.srt` to YouTube, so viewers can turn
> captions off, translate them or search them.

## Related
[[Codecs-and-Bitrate]] · [[Frame-Rate]] · [[Frame-and-Aspect-Ratio]] ·
[[Colour-Spaces]] · [[Shot-Matching]] · [[Export-Settings]] · [[Sound-Mixing]] ·
[[Video-Index]]
