---
title: Sound Mixing
type: concept
module: 5
tags:
  - video/sound
created: 2026-10-22
---
# Sound Mixing

> [!summary] In one line
> Mixing balances the layers of sound (dialogue, ambience, effects and music) so the
> most important one is always clear. It also sets the whole film to a sensible
> loudness for where it will play.

## What it is

A film's sound is built in layers. Give each layer its own tracks, so you can set its
level once and adjust it as a group.

| Layer | What it is | Example | Tracks |
|---|---|---|---|
| **Dialogue** | Speech: interviews, conversation, voice-over | A stallholder describing her morning | A1–A2 |
| **Ambience** | The background sound of a place | Hawker centre chatter, fans, distant traffic | A3 |
| **Effects** | Single sounds tied to something on screen | A wok scraping, a cup set down | A4 |
| **Music** | Score or song | A calm piano track | A5–A6 |

**Room tone** is the ambience of a quiet room with nobody talking. Every room has one.
Dialogue usually wins: when someone speaks, everything else makes room.

## How it works

**Two meters measure two different things.** A **peak meter** shows the loudest
instant, in **dBFS** (decibels relative to full scale). 0 dBFS is the ceiling: anything
louder is **clipped** and distorts. A **loudness meter** shows how loud the sound
*feels* over time, so a door slam and a steady hum can share a peak and still differ.

**LUFS in plain words.** LUFS (loudness units relative to full scale) measures how loud
a whole film sounds to human ears, averaged over its length. The numbers are negative,
and closer to zero is louder. A change of 1 LU is a change of 1 dB. The figure for the
whole film is its **integrated** loudness.

**Platforms turn loud films down.** Many streaming platforms turn any film louder than
their reference level down to it. Spotify documents −14 LUFS; YouTube doesn't publish
its figure, but measurements put it at about −14 LUFS too. A mix at −8 LUFS is turned
down by about 6 dB: making it louder gained nothing. Some platforms also turn quiet
films up; YouTube's normalisation doesn't, so don't mix too quietly either. Targets
differ by platform and can change; European TV uses −23 LUFS. Also keep the **true
peak** (in dBTP), the real top of the sound wave, below about −1 dBTP.

**Music and speech fight for the same space.** The sounds that make words clear sit
mostly between about 1 and 5 kHz, where much of a song's melody sits too. At similar
levels, the music covers the words. Lowering the music while someone talks, called
**ducking**, gives the words room. EQ can carve out a little more.

**EQ (equalisation)** turns ranges of frequencies up or down. Low frequencies are
rumble and weight; high frequencies are clarity and hiss.

| Range | What lives there | A common move on a voice |
|---|---|---|
| Below about 80 Hz | Rumble, wind, traffic, handling noise | Remove it with a high-pass (low-cut) filter |
| About 200–400 Hz | Boxy, muddy room sound | A small cut if the voice sounds muffled |
| About 2–5 kHz | Clarity and presence | A small boost, or a small cut in the music instead |
| About 5–8 kHz | Sharp "s" sounds (sibilance) | Reduce if harsh, with a de-esser |

An 80 Hz high-pass suits almost any voice, which has little useful sound below it.

**Noise reduction** learns what the noise sounds like from a moment with no speech,
then removes it from the rest. AI voice tools do the same job by recognising speech.
Either way, too much makes voices sound watery or robotic, so use the least that works.

**A compressor** turns down the loudest moments of a track, so quiet and loud words sit
closer together; then you raise the whole track. A **limiter** is a strict compressor
that stops anything passing a ceiling. One on the final mix catches stray peaks.

## How to use it

### A mixing routine

1. **Sort the tracks** into the four layers.
2. **Clean the dialogue:** a high-pass filter at about 80 Hz, gentle noise reduction, a
   little EQ, then light compression.
3. **Set the dialogue level** so speech peaks around −12 to −6 dBFS.
4. **Lay ambience under everything,** including under every dialogue edit, so the
   background never drops to silence. → [[Recording-Sound]]
5. **Place the effects** and set them by ear.
6. **Add the music and duck it** under speech (below).
7. **Measure the whole film** (Resolve has a loudness meter on its Fairlight page). For
   online, the usual convention is about −14 LUFS integrated, with true peaks below
   about −1 dBTP. Adjust the master level, with a limiter on the final mix.
8. **Listen on two systems:** headphones, then a phone speaker. A phone speaker has
   almost no bass, so anything that relies on bass disappears.

As starting points, let music under speech peak around −24 to −18 dBFS, ambience
around −30 to −20 dBFS and effects around −20 to −10 dBFS. Then trust your ears.

### Ducking music under speech

1. On the music track, add a volume keyframe about half a second before the speech
   starts, and another where it starts.
2. Lower the music at the second keyframe, often by 10–15 dB, until every word is easy
   to follow. Ramp it back up the same way when the speech ends.
3. Listen. If you notice the music moving, make the ramps longer. Some editors,
   Premiere among them, can duck automatically, but doing it by hand first teaches
   you what to listen for.

### Music you're allowed to use

A song you can stream is licensed for listening, not for your film. Use it anyway and
you risk a **copyright claim**: platforms detect music automatically, and the owner
can have your sound muted, the video blocked, or its ad income paid to them instead.

- **The platform's own music library.** YouTube, Instagram and TikTok offer music
  cleared for use on their platform. Often it's cleared *only* there, so check before
  you post the same file elsewhere. Instagram's and TikTok's main libraries are for
  personal posts; business accounts get a smaller library cleared for commercial use.
- **Royalty-free libraries.** You pay once, or subscribe, and then don't pay per view.
  It doesn't mean free or copyright-free: read what the licence covers (which
  platforms, commercial use, credit).
- **Creative Commons music.** Free, with conditions: CC BY needs a credit, and NC means
  non-commercial use only. Avoid ND (no derivatives): the licence counts putting music
  to pictures as changing it. With SA (share-alike), your film must carry the same
  licence.
- **Music you made yourself**, or written permission from whoever owns it.

> [!warning] Not legal advice
> Licences and platform rules differ and change. Keep a note of where each track came
> from and what its licence allows. → [[Copyright-and-Consent]]

## On your kit

- **Every device records its own sound.** In **A5.5** and **A5.6**, use the device
  closest to the person speaking as your sound source, and mute the others.
- **Line clips up by sound.** Clap once in front of every camera at the start of a
  take; the clap makes a sharp spike in each waveform. Resolve and Premiere can
  also sync clips by their waveforms automatically.
- **A camera's own microphone is wherever the camera is,** often metres from the
  speaker. Expect room echo and background noise, so the cleaning steps matter more.

## Common mistakes

- **Mixing as loud as possible.** Platforms turn it down anyway, and the squashed sound
  stays squashed. Aim for about −14 LUFS and leave the peaks room.
- **Music fighting the words.** If you strain to hear a word, the music is too loud
  there. Duck it.
- **Silence between dialogue edits.** The background vanishes and comes back, which
  sounds like a fault. Fill every gap with ambience or room tone.
- **Too much noise reduction.** A watery, robotic voice is worse than a little hiss.
  Back it off until the voice sounds natural.
- **Mixing only on headphones.** Most people will hear it on a phone speaker. Check
  there before you export.

## Try it

Thirty minutes, a small version of **A5.4**:

1. Record 30 s of a place's sound, then two sentences of your voice somewhere quiet.
2. Put your voice on A1, the place's sound on A3, and a royalty-free music track on A5.
3. Put a high-pass filter at 80 Hz on the voice. Duck the music under the words.
4. Measure the integrated loudness, and adjust the master to about −14 LUFS.
5. Listen on headphones, then on your phone's speaker. Write down what changed.

## Check yourself

> [!question]- Your film measures −8 LUFS, and the platform plays at about −14 LUFS. What happens to it?
> The platform turns it down by about 6 dB to match everything else. Making it loud
> gained nothing, and the compression you used to get there still flattens the sound.

> [!question]- Why lower the music only while someone speaks, rather than keeping it quiet all through the film?
> Speech and music share the frequencies that make words clear, so music at full level
> covers the words. Between the words, the music can carry the mood at full strength.
> Ducking gives you both.

> [!question]- Why lay ambience under a scene even when the dialogue is clean?
> Every dialogue cut also cuts its background. Without steady ambience underneath, the
> background jumps or drops to silence at each cut, which sounds like a fault.

> [!question]- You found the perfect song on a streaming app. Why can't you just use it?
> Your subscription lets you listen; it doesn't license the song for your film.
> Platforms detect it automatically and can mute or block the video. Use music whose
> licence covers what you're doing.

## Related
[[Recording-Sound]] · [[Copyright-and-Consent]] · [[Cuts-and-Transitions]] ·
[[Pacing-and-Rhythm]] · [[Video-Editing-Workflow]] · [[Video-Export-Settings]] ·
[[Video-Index]]
