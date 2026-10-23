---
title: Colour Grading
type: concept
module: 4
tags:
  - post/colour
created: 2026-10-22
---
# Colour Grading

> [!summary] In one line
> Colour correction makes colours accurate and consistent; colour grading then shifts
> them on purpose to set a mood. Correct first, grade second, and grade less than you
> think.

## What it is

Two jobs use the same sliders, so people mix them up:

| | Colour correction | Colour grading |
|---|---|---|
| Goal | Neutral, accurate, consistent colour | A mood or a look |
| Typical tools | White balance, exposure, removing casts | Colour wheels, split toning, curves, LUTs |
| Is there a right answer? | Mostly: a grey wall should look grey | No, it's a choice |
| When | First | Second |

Correction answers "what did it look like?" Grading answers "what should it feel
like?" A grade only behaves predictably on a corrected file.

## How it works

### The colour wheels

Most editors grade with three wheels: one for the **shadows**, one for the
**midtones**, one for the **highlights**, often with a fourth for the whole image.

- Drag the point in a wheel towards a colour to tint that brightness range.
- The direction picks the hue. The distance from the centre sets the strength.
- A brightness slider under each wheel lightens or darkens that range.

Lightroom's Color Grading panel adds **Blending** (how much the three ranges overlap)
and **Balance** (moves the split point between shadows and highlights). Video editors
call the same three wheels Lift, Gamma and Gain.

The wheels sort pixels by brightness, not by colour. A blue shadow tint reaches every
dark pixel, whether it's a dark red shirt or a dark green tree. That's why grading
gives a whole frame one mood so quickly, and why it can't touch one colour alone. For
that you use [[HSL-and-Colour-Mixer]].

### Split toning

Split toning means one tint for the highlights and another for the shadows. Older
versions of Lightroom had a Split Toning panel; the wheels do the same job with more
control. The classic pairing is warm highlights with cool shadows.

That pairing looks natural for a reason. Outdoors, sunlit areas are lit by warm direct
sun, while shadows are lit by the blue sky. Warm highlights and cool shadows exaggerate
something your eye already accepts. → [[Colour-Temperature-of-Light]]

### Common looks

| Look | How it's built | Feels | Watch out for |
|---|---|---|---|
| Warm | Highlights and midtones towards orange | Nostalgic, friendly, golden | Orange skin, yellow whites |
| Cool | Shadows and midtones towards blue | Calm, clinical, night | Grey, lifeless skin |
| Muted | Lower saturation, lifted blacks, soft contrast | Quiet, film-like | Flat and muddy if overdone |
| Teal and orange | Shadows towards teal, highlights towards orange | Cinematic | Everything looks the same |

Teal and orange works on people because skin is orange and teal is its opposite on the
colour wheel. Pushing the background towards teal makes skin stand out by contrast.
→ [[Colour-Theory-for-Photographers]]

### Protecting skin

Skin of every complexion sits in a fairly narrow band of orange hues. Shift it green,
magenta or grey and the person looks ill, even if the viewer can't say why. Skin is
where a grade fails first. Video editors' vectorscopes even show a "skin tone line" to
check against.

## How to use it

1. **Correct first.** White balance, exposure and contrast, in that order, until
   neutral things look neutral. → [[Basic-Panel-Order]]
2. **Say the mood in words.** "Warm, quiet afternoon" gives you a direction to test
   against. "Make it look good" doesn't.
3. **Grade with small moves.** On a 0–100 scale, wheel strengths of 5–15 are often
   enough. Start with the highlights and shadows.
4. **Check the skin.** If a face has turned green or grey, mask it out of the grade, or
   restore it with the orange hue and saturation in the colour mixer.
5. **Toggle the grade off and on.** If the photo looks better without it, it was too
   much, or the wrong mood.
6. **Look again after a break.** Your eyes adapt to a colour cast within minutes, so a
   strong grade starts to look normal while you work.

A creative [[LUTs|LUT]] is a grade baked into a table. Build the grade with sliders
while you learn, so you can reopen and change it. To use one grade across a set, save
it as a preset. → [[Developing-a-Look]]

## On your kit

- **Lumix L10:** Real Time LUT bakes a grade into the JPEG or HEIF in camera. Shoot RAW
  alongside, so the RW2 stays ungraded and you can grade it later.
- **iPhone 15 Pro Max:** Photographic Styles bake a grade in at capture on this model
  and can't be used with ProRAW. Leave Standard on if you plan to grade.
- **Log footage and stills** (the L10's V-Log, the iPhone's Apple Log, the DJIs' D-Log M)
  need their technical LUT before any grade. Grading flat log directly gives muddy,
  unpredictable results.
- **Mixing devices:** correct each device's files to neutral first, then grade them all
  together. In Module 5 this becomes [[Shot-Matching]].

## Common mistakes

- **Grading before correcting.** The grade sits on top of the cast, so every frame
  comes out different. Neutralise first.
- **Grading too strongly.** If people notice the grade before the subject, pull it
  back.
- **Teal and orange on everything.** It's one look, not a default. Choose the mood from
  the subject.
- **Ignoring skin.** Check every face at the end of a grade.
- **Heavy grades on 8-bit JPEGs.** Smooth skies break into bands. Grade the raw.
  → [[Bit-Depth]]

## Try it

Twenty minutes, on one raw file with a person and some sky in it:

1. Correct it: white balance, exposure, contrast.
2. Make three virtual copies. Grade one warm, one cool and one teal and orange, using
   only the colour wheels.
3. Check each face at 100%. Fix any skin that turned ill.
4. Toggle each grade off and on. Write one sentence on which mood serves the subject.

This is a small version of **A4.1**, where one file gets three interpretations.

## Check yourself

> [!question]- Why must you correct white balance before you grade?
> The grade is added on top of whatever is already there. A cast left in the file
> shifts every tint, so the same grade looks different on each frame. On a neutral
> base it behaves predictably.

> [!question]- Why do warm highlights and cool shadows look natural?
> Outdoors, highlights are lit by warm direct sun and shadows by the blue sky. The grade
> exaggerates a colour split your eye already expects.

> [!question]- You push the shadows towards teal and a face in the shade turns grey-green. Why, and what do you do?
> The shadow wheel tints every dark pixel, including skin in shadow. Mask the face out
> of the grade, or restore its orange with the colour mixer.

> [!question]- After half an hour of grading, the photo looks right. The next morning it looks far too strong. What happened?
> Your eyes adapted to the colour cast while you worked, so it slowly looked normal.
> Take breaks and toggle the grade off and on to see it fresh.

## Related
[[White-Balance]] · [[HSL-and-Colour-Mixer]] · [[Colour-Theory-for-Photographers]] ·
[[LUTs]] · [[Developing-a-Look]] · [[Shot-Matching]] · [[Post-Processing-Index]]
