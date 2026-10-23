---
title: Autofocus Modes
type: concept
module: 1
tags:
  - fundamentals/focus
created: 2026-10-22
---
# Autofocus Modes

> [!summary] In one line
> Autofocus settings answer two questions: *when* the camera focuses (once, or all the
> time) and *where* in the frame it looks. Match both to the subject and the camera stops
> guessing for you.

## What it is

Autofocus (AF) is set with two separate controls, plus a helper:

| Setting | The question it answers | Usual choices |
|---|---|---|
| Focus mode | When does the camera focus? | Single (AF-S), continuous (AF-C), manual (MF) |
| AF area mode | Where in the frame does it look? | Single point, zone, wide / tracking |
| Subject detection | What kind of thing should it look for? | Faces, eyes, bodies, animals; more on some cameras |

The names vary between brands. The ideas are the same everywhere.

## How it works

### Focus modes: once, or all the time

- **Single AF (AF-S):** press the shutter halfway (or press an AF button). The camera
  focuses once, then locks for as long as you hold. It usually won't take the photo
  until it has found focus. Best for things that stay still.
- **Continuous AF (AF-C):** the camera keeps refocusing while you hold the button, and
  predicts where a moving subject is going. It usually fires even if focus isn't
  perfect, because a moving subject won't wait. Best for people, children and animals.
- **Manual focus (MF):** you set the focus yourself. → [[Manual-Focus]]

### Area modes: where to look

| Area mode | What it does | Use it for |
|---|---|---|
| Single point | Focuses on one small area that you place | Still subjects; exactly the eye or detail you choose |
| Zone | Uses a group of points; the camera picks inside it | A moving subject that stays in one part of the frame |
| Wide / tracking | Searches the whole frame, or follows a subject you start it on | Erratic movement, usually with subject detection on |

Without subject detection, wide area often picks the nearest or most contrasty thing.
That is not always your subject.

### Subject detection

The camera's software recognises a type of subject (a face, an eye, a body, an animal)
and puts the focus there, often on the nearest eye. With AF-C and tracking, it follows
the subject around the frame. It works best when the subject is reasonably large in the
frame and not hidden behind other things.

### Phase detect and contrast detect

There are two main ways a camera can tell whether something is in focus:

- **Contrast detect:** the camera moves the focus and watches the picture. Sharp edges
  have the most contrast, so it searches for the peak. It has to go slightly past the
  peak to know where it was, so it may wobble back and forth ("hunt"). It is accurate,
  but slower with moving subjects.
- **Phase detect:** special pixels look at the subject through opposite sides of the
  lens. If the two views don't line up, the subject is out of focus. How far apart they
  are tells the camera which way to move and how far, in one step. It is fast and good
  for tracking.

Many current cameras use both ("hybrid AF"). The L10's manual says which system it uses.

### The focus-and-recompose problem

Focus sets a distance measured straight out from the camera: a flat sheet, parallel to
the sensor. Focus on an eye with the centre point, then turn the camera to put the face
near the edge. The sheet turns with the camera, and the focus now falls slightly behind
the eye.

With deep depth of field nobody notices. Up close at a wide aperture, you will. On the
L10 at 24 mm, f/1.7 and 50 cm from a face, only about 8 cm is sharp, and only about 4 cm
of that is in front of the focus point. Turn the camera 30° to recompose and the eye
ends up about 7 cm in front of the new focus sheet: outside the zone.
→ [[Depth-of-Field]]

The fix: move the AF point onto the eye instead of moving the camera, or use eye
detection.

### When autofocus struggles

- **Low light:** too little light for the AF system to see detail.
- **Low contrast:** a plain wall, a clear sky, fog, a white shirt. Nothing to grip.
- **Repeating patterns:** blinds, railings, tiled walls. AF can lock on the wrong one.
- **Things in the way:** fences, wet glass, leaves. AF grabs the nearest thing.
- **Too close:** nearer than the minimum focus distance, AF can't lock at all.
- **A small subject on a busy background:** AF picks the background.

## How to use it

| Situation | Focus mode | Area mode and detection |
|---|---|---|
| Landscape, building, product | AF-S | Single point on what matters; detection off |
| Posed portrait | AF-S or AF-C | Eye detection, or a single point on the nearest eye |
| Children, pets, people walking | AF-C | Wide / tracking or zone, with detection on |
| Through a fence or glass | AF-S with the smallest point, or MF | Single point; detection off |
| Dark room, plain subject | AF-S, or MF | Single point on any edge at the same distance |

Rules of thumb:

1. **Moving subject? Use AF-C.** A person walking towards you covers about 30 cm in a
   fifth of a second. At 75 mm and f/2.8, the sharp zone at 2 m is only about 25 cm deep.
2. **Focus on the eye nearest the camera.** People look at eyes first, and at portrait
   distances the zone is thin.
3. **At wide apertures, move the point, don't recompose.** Because the focus sheet turns
   with the camera.
4. **Separate focusing from the shutter.** Then you can track and lock without changing
   any menus. → [[Back-Button-Focus]]

## On your kit

- **L10:** normal AF works from 50 cm. Closer than that, flip the focus selector to
  **AF Macro**, which reaches 3 cm at 24 mm (30 cm at 75 mm). The **[AF ON]** button
  starts AF without touching the shutter; set [Shutter AF] to off and it becomes your
  only focus button. Check the manual for the area modes, which subjects it detects,
  and whether you can tap the touch screen to move the AF point.
- **iPhone 15 Pro Max:** Apple's Camera app picks a subject itself, often a face. Tap
  the screen to focus (and expose) somewhere else. Press and hold to lock both (AE/AF
  LOCK), which also stops focus wandering during video. Very close up, it can switch to
  the ultra-wide's macro, which focuses at about 2 cm.
- **Pocket 3:** it focuses by itself, from 20 cm. Its subject tracking turns the gimbal
  to keep a chosen subject in the frame. Check its manual for how to pick and release
  the subject.
- **Action 5 Pro:** no autofocus at all. The focus is fixed, and everything from about
  35 cm is sharp.

## Common mistakes

- **Leaving AF-S on for a moving subject.** Focus locks where the subject *was*. Switch
  to AF-C.
- **Letting wide area choose without detection.** It often picks the nearest or
  brightest thing. Use a single point, or turn subject detection on.
- **Focusing and recomposing at f/1.7 up close.** The eye drops out of the zone. Move the
  AF point instead.
- **Trying to focus closer than 50 cm in normal AF on the L10.** It can't. Switch to AF
  Macro.
- **Blaming autofocus for every soft photo.** If something else in the frame is sharp,
  focus missed. If nothing is sharp and edges are streaked, it's movement: use a faster
  shutter. → [[Shutter-Speed]]

## Try it

Fifteen minutes, on the L10, at 75 mm and f/2.8, in good light. Ask someone to walk
slowly towards you from about 6 m away.

1. **AF-S, single point:** focus once as they start, then shoot five frames as they come
   closer without refocusing.
2. **AF-C, single point or zone on them:** keep the button held and shoot five frames.
3. **AF-C, wide or tracking, with face or eye detection** (if the L10 offers it): shoot
   five more.
4. Check all fifteen at 100% and count the sharp ones in each set.

This is practice for the Module 1 exit test: "moving kid, indoors, want them sharp".

## Check yourself

> [!question]- A child is running around a playground. Which focus mode and area mode do you choose, and why?
> AF-C with wide / tracking or zone, and face or eye detection on. AF-S would lock where
> the child was a moment ago, and at 75 mm and f/2.8 the sharp zone is only about 25 cm
> deep.

> [!question]- You focus on an eye with the centre point at f/1.7, then recompose so the face is near the edge. Why is the eye soft?
> Focus is a flat sheet facing the camera, and it turned when the camera turned. The
> focus now falls behind the eye, and up close at f/1.7 the zone is only a few
> centimetres deep. Move the AF point instead.

> [!question]- At dusk, the camera hunts back and forth on a plain white wall. Why, and what do you do?
> There is little light and no contrast, so the AF system has nothing to measure. Focus
> on an edge at the same distance (a door frame, a light switch), or use manual focus.

> [!question]- Why can phase detect move focus straight to the right place, while contrast detect has to hunt?
> Phase detect compares two views of the subject, which tells it the direction and the
> amount to move. Contrast detect only learns "sharper" or "less sharp", so it must pass
> the peak to find it.

> [!question]- A photo of a walking friend is soft. How do you tell a focus miss from motion blur?
> Look for anything sharp. If the background or something else is sharp, focus landed
> in the wrong place. If nothing is sharp and edges are streaked or doubled, it's
> movement: use a faster shutter.

## Related
[[Back-Button-Focus]] · [[Manual-Focus]] · [[Depth-of-Field]] · [[Shutter-Speed]] ·
[[Sports-and-Action]] · [[Wildlife-and-Birds]] · [[Macro]] · [[Fundamentals-Index]]
