---
id: gospel-chorus-release
title: Gospel Chorus Release
language: en
genre: gospel-soul
workflow: section-replacement
model: v6
inputs: [text]
evidence_tier: official-informed
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [gospel, chorus, replacement, soul]
---

## Goal
Replace an undersized chorus with a warmer gospel/soul release in an original piano-led song.

## Model
`v6` to preserve the verse while replacing the section.

## Inputs
Target section, new chorus lyrics, neighboring sections, and instrumentation boundaries.

## Style Prompt
Original gospel/soul-influenced chorus: warm piano chords, gentle Hammond-style pad, upright bass, brushed drums entering late, responsive backing harmonies, hopeful but restrained lead vocal.

## Exclude Styles
Do not turn the song into electronic dance music, add a named-artist imitation, introduce religious sermon dialogue, or change verses.

## Lyrics or Edit Instruction
```text
Replace the chorus only.
New chorus:
[Chorus]
Hold the light when the room goes quiet
Carry home what the night delayed
Even shadows learn to bend and brighten
Even I can learn to stay

Preserve the existing verse voice, key, tempo, and piano-led identity. Add backing harmonies only in the second half of the chorus.
```

## Expected Result
A broader lift that still sounds like the same recording, with call-and-response backing vocals.

## Failure Modes
The chorus becomes a different genre, backing vocals begin too soon, or verses are unexpectedly rewritten.

## Next Iteration
Replace only the second half first, keep drums out until the final line, then request one section-level rebuild.

## Evidence
Evidence tier: `official-informed`; section editing follows v6 local-edit capabilities, while gospel arrangement guidance is untested style advice.
