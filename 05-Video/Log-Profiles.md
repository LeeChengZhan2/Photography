---
title: Log Profiles
type: concept
module: 5
tags:
  - video/capture
created: 2026-10-22
---
# Log Profiles

> [!summary] In one line
> A log profile records a flat, grey-looking picture that keeps more of the scene's
> brightness range for grading later. It needs 10-bit recording and a conversion before
> it looks normal, so it's worth it only when you'll grade the footage.

## What it is

A **picture profile** decides how the camera turns the light it measured into numbers
in the file. A standard profile adds contrast and colour, so the clip looks finished
straight away. A **log profile** does the opposite: it keeps as much of the scene's
[[Dynamic-Range|dynamic range]] (the stops between the darkest and brightest detail)
as it can, and leaves the finishing to you.

| | Standard profile | Log profile |
|---|---|---|
| Looks like | Finished: contrast, saturated colour | Flat, grey, washed out |
| Highlights and shadows | Clipped or crushed earlier | Kept further into both ends |
| Needs grading | No | Yes, always |
| Needs 10-bit | Helps, but 8-bit works | Yes |

Each maker has its own log curve: V-Log (Panasonic), Apple Log, and D-Log M (DJI).
Each needs its own conversion.

## How it works

### Where the stops go

A sensor responds in a straight line: twice the light gives twice the signal. If a file
stored those numbers directly, the brightest stop would take half of all the available
values. Each stop below would get half as many as the one above it.

In a 10-bit file, with 1024 values, that looks like this:

| Stop, counting down from the brightest | Values it gets if stored directly |
|---|---|
| 1st | 512 |
| 2nd | 256 |
| 3rd | 128 |
| 4th | 64 |
| 5th | 32 |
| 6th and below | 32, shared between them all |

The shadows would be starved, and that's where noise lives and where your eye notices
steps. So every profile bends this line. A standard profile bends it for a
good-looking picture and gives up the stops at both ends. A log curve bends it so that
each stop gets roughly the same share of values. The bright stops are squeezed
together and the dark ones spread out. That is what makes the picture flat: every tone
is pushed towards the middle.

### Why log wants 10-bit

8-bit video has 256 levels per colour channel. 10-bit has 1024: four times as many.
→ [[Bit-Depth]]

Log spreads many stops across those levels, so each stop gets fewer levels than in a
standard profile. Grading then stretches the contrast back, pulling neighbouring levels
apart. In 8-bit the gaps show as bands in smooth areas, such as skies and walls. In
10-bit there are four times as many steps, so the stretch stays smooth.

### Why log needs a conversion

No screen expects a log curve. Shown as it is, log looks grey and lifeless. Before you
grade, convert it to a normal (Rec.709) picture with the maker's **technical LUT**, or
with a **colour-space transform** that does the same job with maths. The conversion
must match the exact curve and camera. [[LUTs]] covers this in depth, including which
LUT belongs to which of your devices.

After the conversion, you grade for the look you want. → [[Colour-Grading]]

### Exposing log

Follow the maker's guidance for each curve. Many log curves look best exposed a little
brighter than a standard profile would suggest. The reason is noise: log's darkest
stops are noisy, and extra light makes them cleaner. You bring the brightness back
down in the grade.

Don't overdo it. Log highlights still clip, and clipped detail is gone. Watch the
highlights with zebras or a waveform. → [[Zebras-and-Waveform]]

Log often has a higher minimum ISO than a standard profile. On the L10, V-Log starts at
ISO 500. In bright light, that means more ND or a smaller aperture.

### HLG: the middle path

HLG (hybrid log-gamma) is an HDR profile. It keeps more highlight range than a standard
profile, yet looks finished on an HDR screen without grading. It suits you when you want
more range without the grading work. The catch: HDR clips look wrong next to SDR clips,
so don't mix them in one film without converting. → [[Video-Export-Settings]]

## How to use it

Ask one question first: **will I grade this?**

| Situation | Profile | Because |
|---|---|---|
| High contrast you'll grade: sun and shade, a sunset, a window | Log | It keeps both ends for you to place |
| Several cameras to match in one film (A5.5) | The same kind on all: log on all, or standard on all | Matching starts easier from the same treatment |
| A quick clip for social media today | Standard or HLG | No time to grade; log adds work for no gain |
| A dim scene you can't expose generously | Standard | Underexposed log turns noisy once converted |
| Footage that will never be graded | Standard | Log only pays off in the grade |

When you do shoot log:

1. **Record 10-bit.** If a mode offers log only in 8-bit, use a standard profile.
2. **Expose as the maker says**, usually a little brighter than standard, never
   clipped.
3. **View through a LUT on the camera, if it can**, so you judge the picture, not the
   grey.
4. **In the edit, apply the matching technical LUT first**, then grade.

## On your kit

All four devices shoot log. Which LUT goes with which device is in the LUTs note linked
above.

- **Lumix L10:** V-Log, for video and stills. It starts at ISO 500 (125 extended), so
  in daylight it needs over two stops more ND than at ISO 100 (above 60 fps the base
  drops to ISO 250). The camera can use a LUT two ways: [REAL TIME LUT] records the
  look into the clip, while [LUT View Assist (Monitor)] only shows it on screen and
  keeps the clip in V-Log. It also offers HLG and Like709 if you don't want to grade.
- **iPhone 15 Pro Max:** Apple Log needs ProRes. Internal ProRes stops at 4K 30 fps;
  4K 60 fps needs an external USB-C SSD. ProRes files are large.
  → [[Codecs-and-Bitrate]] Apple publishes a Log → Rec.709 LUT on its developer site.
- **Pocket 3 and Action 5 Pro:** 10-bit D-Log M. Each has its own DJI LUT, so the
  Pocket 3's LUT doesn't suit the Action 5 Pro's footage, or the other way round. D-Log
  M is also a different curve from DJI's D-Log.

## Common mistakes

- **Shooting log in 8-bit.** Grading pulls the levels apart and skies band. Record
  10-bit, or use a standard profile.
- **Using the wrong LUT.** D-Log instead of D-Log M, or one DJI camera's LUT on the
  other's footage, gives wrong contrast and colour that still looks plausible. Match
  the LUT to the exact camera and curve.
- **Putting a creative look straight onto log.** It comes out muddy. Convert first,
  then add the look.
- **Exposing log by eye.** The flat picture tricks you. Use zebras or the waveform, and
  the maker's guidance.
- **Shooting log for everything.** Every clip then needs grading. Use a standard
  profile or HLG when you won't grade.

## Try it

Twenty minutes, on the Pocket 3 or the Action 5 Pro:

1. Find a high-contrast scene. Standing under an HDB void deck, looking out at a sunlit
   street, works well.
2. Film 10 seconds in the Normal profile, then 10 seconds in D-Log M. Keep the frame
   rate and shutter the same.
3. In your editor, apply DJI's LUT for that camera to the D-Log M clip.
4. Try to recover the bright street and the dark ceiling in both clips. Compare the
   highlights, the shadows, and any skin.
5. Write down which clip was worth the extra work, and why.

A first step towards **A5.5**, where every camera's log needs its own conversion.

## Check yourself

> [!question]- Why does log footage look grey and flat before conversion?
> The log curve gives every stop roughly the same share of values, which pushes all the
> tones towards the middle. The contrast a standard profile would add hasn't been added
> yet. The picture is unfinished, not wrong.

> [!question]- Why does log want 10-bit rather than 8-bit?
> Log packs many stops into the available levels, and grading stretches them apart
> again. 8-bit has only 256 levels per channel, so the stretch leaves visible bands in
> skies and walls. 10-bit has four times as many steps.

> [!question]- You film V-Log on the L10 in bright sun. Why do you need more ND than in a standard profile?
> V-Log starts at ISO 500, over two stops above ISO 100. With the shutter fixed at
> 1/50 s, those extra stops have to be blocked by ND or a smaller aperture.

> [!question]- A friend wants a 15-second clip for social media this evening. Log or not?
> Not. Log only pays off when you grade, and every clip would need converting and
> grading first. A standard profile, or HLG for an HDR platform, gives a finished clip
> straight away.

> [!question]- After the LUT, your log clip looks good apart from a white sky with no detail. Can grading fix it?
> No. The sky clipped at capture, so there's no detail left to recover. Log keeps more
> highlight range than a standard profile, but it still has a limit. Protect the
> highlights with zebras or the waveform.

## Related
[[LUTs]] · [[Dynamic-Range]] · [[Bit-Depth]] · [[Colour-Grading]] ·
[[Codecs-and-Bitrate]] · [[Shot-Matching]] · [[Zebras-and-Waveform]] · [[Video-Index]]
