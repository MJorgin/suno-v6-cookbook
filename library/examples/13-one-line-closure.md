---
id: one-line-closure
title: One Line Closure
language: en
genre: english-indie-pop
workflow: lyric-micro-edit
model: v6
inputs: [text]
evidence_tier: official
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [micro-edit, lyric-fix, closure]
---

## Goal
Replace one verse line that gives away the ending too early while preserving the existing recording.

## Model
`v6` for local consistency.

## Inputs
The exact old line, exact new line, and a preservation list.

## Style Prompt
No new style request. Keep the existing indie-pop arrangement, key, tempo, voice, and instrumentation.

## Exclude Styles
Do not change genre, add strings, change the lead voice, or rewrite neighboring lines.

## Lyrics or Edit Instruction
```text
Make a local lyric edit only.
Section: Verse 2, line 3
Original line: "I knew then we were already through"
Replace with: "I held the words I wanted from you"
Match the existing melody, rhythm, phrasing, and emotion. Keep every other lyric unchanged.
```

## Expected Result
A line with nearly the same syllable count that delays the reveal and fits the existing melody.

## Failure Modes
Adjacent lyrics change, the vocal tone shifts, or the new line contains too many stressed words.

## Next Iteration
Shorten the replacement to eight syllables and specify that the final word must rhyme with the following line.

## Evidence
Evidence tier: `official` for local lyric replacement; the prompt wording is official-informed.
