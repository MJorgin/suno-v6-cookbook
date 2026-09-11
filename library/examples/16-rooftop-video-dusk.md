---
id: rooftop-video-dusk
title: Rooftop Video Dusk
language: en
genre: cinematic-ambient
workflow: image-or-video-to-music
model: v6-wild
inputs: [video, text]
evidence_tier: official-informed
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [video, ambient, dusk, rooftop]
---

## Goal
Create a 45-second instrumental cue from an owned rooftop-at-dusk video.

## Model
`v6-wild` for visual interpretation, followed by `v6` for timing control.

## Inputs
An owned video, visual anchors, duration target, and instrumental preference.

## Style Prompt
Original cinematic ambient cue, slow dusk colors, distant city warmth, evolving pads, sparse piano, soft sub-bass pulse, airy wordless vocal texture after twenty seconds, spacious and hopeful.

## Exclude Styles
Literal traffic effects, drum drops, trailer impacts, spoken narration, and harsh synthesizers.

## Lyrics or Edit Instruction
```text
Create music from my attached rooftop video. I own or have rights to use this source.
Visual anchors: slow wind moving laundry, orange-to-blue light, skyline blinking on, one person looking up.
Duration: about 45 seconds.
Follow the emotional progression: isolation -> recognition -> quiet hope.
Do not sync to every camera movement; prioritize a smooth musical arc.
```

## Expected Result
A coherent cue that follows the mood rather than mimicking every sound on video.

## Failure Modes
Literal traffic sound effects, over-syncing to cuts, or an inappropriate beat.

## Next Iteration
Use `v6`, remove world-sound references, and specify three timed sections of 15 seconds each.

## Evidence
Evidence tier: `official-informed`; video input is an official v6 capability, while this cue structure is a practical prompt.
