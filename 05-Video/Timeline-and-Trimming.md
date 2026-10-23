---
title: Timeline and Trimming
type: concept
module: 5
tags:
  - video/editing
created: 2026-10-22
---
# Timeline and Trimming

> [!summary] In one line
> The timeline is where you arrange clips in time. Trimming moves where clips start and
> end, and the four trims (ripple, roll, slip and slide) each change one thing while
> protecting the rest.

## What it is

The **timeline** shows your film from left to right in time. A vertical line, the
**playhead**, marks the frame you're looking at. The timeline is stacked in **tracks**:

- **Video tracks** (V1, V2, V3…) sit in the upper half. A clip on a higher track covers
  the one below it, like layers in a photo editor. Keep the main story on V1, cutaways
  on V2 and titles on V3.
- **Audio tracks** (A1, A2…) sit in the lower half. They all play at once and add
  together.

A **clip** is a piece of a source file. Its **in point** is the first frame you use,
and its **out point** is the last. The footage beyond them is still there, unused.
That spare footage is called the **handles**.

Positions are shown as **timecode**: hours, minutes, seconds and frames. `00:01:12:10`
means 1 minute, 12 seconds and 10 frames. At 25 fps the frames count from 00 to 24, so
one frame lasts 1/25 s (0.04 s). → [[Frame-Rate]]

## How it works

A clip is a window onto its source file. Trimming moves the edges of that window; it
never deletes footage. That's why a trim can only lengthen a clip if there are handles.
You can't show frames the camera didn't record.

Every trim must decide what happens to the neighbours. If one clip gets longer,
something else must get shorter, or the film must get longer. The four trims are four
different answers. In this sketch each letter is one second of a clip:

```
Start   |AAAA|BBBBBB|CCCCC|    A 4 s · B 6 s · C 5 s · film 15 s
Ripple  |AAA|BBBBBB|CCCCC|     A's end trimmed 1 s · B and C move left · film 14 s
Roll    |AAAAA|BBBBB|CCCCC|    the A/B cut moves 1 s later · film 15 s
Slip    |AAAA|bbbbbb|CCCCC|    B shows a different 6 s of its source · film 15 s
Slide   |AAAAA|BBBBBB|CCCC|    B moves 1 s later · A longer, C shorter · film 15 s
```

| Trim | You drag | What changes | Film length | Handles needed |
|---|---|---|---|---|
| **Ripple** | One edge of one clip | That clip's length; everything after it moves | Changes | Only to lengthen |
| **Roll** | The cut between two clips | One clip grows, the other shrinks by the same amount | Same | In the clip that grows |
| **Slip** | The inside of one clip | Which part of its source shows | Same | On the side you slip towards |
| **Slide** | A whole clip | Its position; the neighbours grow and shrink | Same | In the neighbour that grows |

**Ripple** is the everyday trim: it tightens a shot and closes the gap in one move.
**Roll** moves a cut without touching anything else, so it's how you find the best
frame for a cut on action. **Slip** keeps a shot's place and length but changes what's
in it: use it when the shot is the right length but the action starts too late.
**Slide** moves a short shot, like a cutaway, earlier or later between its neighbours.

**Snapping** makes clip edges and the playhead jump to each other when they get close.
That's what stops tiny gaps. A gap of one frame plays as a flash of black. Turn
snapping off for fine positioning, then on again (N in Resolve, S in Premiere Pro).

**Linked audio and video.** A clip recorded with sound arrives with its audio linked to
its picture. Linked clips move and trim together, so lips stay in sync. To trim only
the sound or only the picture, for a J- or L-cut, turn off linked selection. Or, in
Resolve and Premiere Pro, Alt-click the part you want (Option-click on a Mac).
→ [[Cuts-and-Transitions]]

## How to use it

### Playing with J, K and L

Desktop editors share the same three playback keys. Keep your right hand on them.

| Keys | What happens |
|---|---|
| L | Play forwards; press again to play faster |
| J | Play backwards; press again to play faster |
| K | Stop |
| Hold K, tap L or J | Step one frame forwards or backwards |
| Hold K and L together | Play forwards slowly |
| Up and down arrows | Jump to the previous or next cut (Resolve, Premiere Pro) |

To find an exact frame: press L until you're close, K to stop, then hold K and tap J or
L until you land on it.

### Putting clips on the timeline

1. Open a clip in the source viewer. Press I at the first frame you want and O at the
   last. These keys work in Resolve, Premiere Pro and Final Cut Pro.
2. Put the timeline's playhead where the clip should go.
3. Choose **insert** or **overwrite**. Insert pushes everything after the playhead
   later. Overwrite covers whatever is already there. In Resolve these are F9 and F10;
   in Premiere Pro, the comma and full-stop keys.

### Finding the trims in your editor

- **Premiere Pro** has a tool for each: Ripple Edit (B), Rolling Edit (N), Slip (Y) and
  Slide (U).
- **Resolve:** switch to Trim Edit mode (T). The trim you get depends on where you
  click, and the pointer changes shape to show which.
- **Final Cut Pro** and **CapCut's** main track ripple by default: they close gaps for
  you.
- With the normal selection tool, Resolve and Premiere Pro **don't** ripple. Dragging
  an edge shorter just leaves a gap.

### A trimming routine

1. Play across the cut from about two seconds before it, at full speed.
2. Decide what's wrong: too long (ripple), wrong moment (roll), wrong content (slip),
   or wrong place (slide).
3. Trim by a few frames, not by seconds.
4. Play it again at full speed. Never judge a cut from a still frame.

## Common mistakes

- **Leaving one-frame gaps.** They flash black on playback. Keep snapping on, and trim
  with ripple rather than dragging edges with the selection tool.
- **Leaving linked selection off.** Then a picture can move without its sound, and lips
  drift out of sync. Turn it back on after every J- or L-cut. Many editors mark
  out-of-sync clips with a red number.
- **Stopping the recording too soon.** Without handles, roll and slip have nothing to
  work with. When you film, start a few seconds before the action and stop a few
  seconds after it. → [[Shot-Sizes-and-Coverage]]
- **Judging cuts while scrubbing.** Dragging the playhead shows frames, not rhythm.
  Play across every cut at full speed.
- **Building everything on one track.** Cutaways and titles on V1 get chopped up
  whenever you trim the story. Keep the story on V1 and the extras above it.

## Try it

Twenty minutes, any editor, to prepare for **A5.2**:

1. On your phone, film three clips of someone clapping once: a wide, a close-up of the
   hands, and a close-up of the face. Start each clip early and stop it late.
2. Put them on the timeline in that order. Write down each clip's length.
3. Try each trim once: ripple, roll, slip and slide. After each, write down what moved
   and whether the film's length changed. Undo before the next one.
4. Use J, K and L to find the exact frame where the hands meet in the wide. Cut to the
   hands close-up on that moment. Roll the cut two frames earlier, then two later, and
   keep whichever looks smoothest at full speed.

## Check yourself

> [!question]- Why does a ripple trim change the film's length, but a roll trim doesn't?
> A ripple changes one clip and moves everything after it to close or open the gap. A
> roll moves the cut between two clips: one gets longer by exactly what the other
> loses, so the total stays the same.

> [!question]- A cutaway is the right length and in the right place, but the action in it starts too late. Which trim fixes it without touching the neighbours?
> A slip. It keeps the clip's position and length and changes which part of the source
> shows inside it. Slip it so the clip starts later in the source, and the action
> arrives sooner.

> [!question]- You try to roll a cut one second later, but it stops after half a second. Why?
> Rolling the cut later makes the first clip longer, and that clip has run out of
> handles. The camera only recorded half a second more after its current out point.

> [!question]- Playback shows a flash of black between two shots. What is it, and how do you stop it happening?
> A gap of a frame or two between the clips. Close it with a ripple trim or a ripple
> delete, and keep snapping on so edges join exactly.

> [!question]- Why trim the picture and the sound separately for a J-cut, and why turn linked selection back on afterwards?
> A J-cut needs the next shot's sound to start before its picture, so the two edits
> must sit in different places. With linked selection left off, you can move a picture
> without its sound by accident, and lips drift out of sync.

## Related
[[Video-Editing-Workflow]] · [[Cuts-and-Transitions]] · [[Pacing-and-Rhythm]] ·
[[Shot-Sizes-and-Coverage]] · [[Frame-Rate]] · [[Non-Destructive-Editing]] ·
[[Video-Index]]
