---
id: glacier-bloom
title: Glacier Bloom
language: en
genre: cinematic-ambient
workflow: image-or-video-to-music
model: v6-wild
inputs: [image, text]
evidence_tier: official-informed
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [ambient, glacier, visual, instrumental]
---

## Goal
Turn an owned image of sunlight touching a glacier into a slowly blooming instrumental cue.

## Model
`v6-wild` first for visual interpretation, then `v6` for controlled timing.

## Inputs
An owned glacier image plus text anchors for light, motion, and structure.

## Style Prompt
Original cinematic ambient, evolving cold-air pads, sparse high piano fragments, low cello pulse, distant granular shimmer, gradual register lift around one minute, wide reverb, restrained hopeful ending, mostly instrumental.

## Exclude Styles
Sudden drum beats, constant cymbal swells, trailer impacts, literal wind effects, and four competing melodies.

## Lyrics or Edit Instruction
```text
Use my glacier image. I own or have rights to use this source.
Visual anchors: blue-white ice, slow sunlight moving across a crack, tiny meltwater motion.
Follow emotional progression rather than literal sound effects: stillness -> warmth -> fragile bloom.
Wordless vocals may enter after 1:10 but no sung lyrics.
```

## Expected Result
A spacious cue with one clear peak and no generic trailer climax.

## Failure Modes
Over-literal wind or water sounds, excessive swells, or a beat that contradicts the visual stillness.

## Next Iteration
Remove vocals and drums, specify a 16-bar pad evolution, then rebuild with `v6`.

## Evidence
Evidence tier: `official-informed`; multimodal input is official, while cue structure is a practical hypothesis.
