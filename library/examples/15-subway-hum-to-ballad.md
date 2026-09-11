---
id: subway-hum-to-ballad
title: Subway Hum to Ballad
language: zh-CN
genre: mandopop-ballad
workflow: voice-memo-to-song
model: v6
inputs: [voice-memo, text]
evidence_tier: official
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [voice-memo, mandopop, melody]
---

## Goal
Turn an original phone-recorded hum into a complete Mandarin ballad while preserving the core melody.

## Model
`v6` for source-to-song control and vocal continuity.

## Inputs
A user-owned voice memo, timestamp, target genre, and original lyric theme.

## Style Prompt
Original Mandarin ballad built from the owned voice memo: warm piano, soft pads, restrained modern drums entering in the pre-chorus, later cello and quiet harmonies, intimate lead vocal.

## Exclude Styles
Do not preserve background subway noise, invent copyrighted lyrics, imitate a named singer, or make an EDM drop.

## Lyrics or Edit Instruction
```text
Create an original song from my voice memo. I own or have rights to use this source.
Source: subway-hum.m4a, useful timestamp 00:08-00:26.
Preserve the hummed melody and its gentle pause before the third phrase.
Ignore train noise and unclear syllables.
Theme: returning home after a long day and realizing someone waited for you.
Create clear original Mandarin lyrics and a finished ballad arrangement.
```

## Expected Result
The memo's melody becomes the verse motif, with noise removed and a polished arrangement added.

## Failure Modes
The model keeps subway noise, invents inaccurate words, or loses the melody under generic drums.

## Next Iteration
Shorten the source to one eight-second phrase, provide lyrics explicitly, and request melody preservation only.

## Evidence
Evidence tier: `official` for multimodal source creation; rights and timestamp wording are official-informed.
