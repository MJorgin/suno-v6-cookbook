---
id: mumbled-vocal-repair
title: Mumbled Vocal Repair
language: bilingual-en-zh-CN
genre: mandopop-ballad
workflow: failure-diagnosis
model: v6
inputs: [text]
evidence_tier: working-hypothesis
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [repair, diction, bilingual, vocals]
---

## Goal
Diagnose and repair a bilingual ballad whose chorus words are mumbled and rhythmically crowded.

## Model
Use a short `v6-mini` diction test, then rebuild with `v6`; the example records the final `v6` repair.

## Inputs
Failed line description, simplified lyrics, and one changed variable: line length.

## Style Prompt
Original bilingual ballad, warm piano, soft pads, slow drums, intimate lead vocal, clear diction, language switch only at the start of each phrase, generous breath between lines.

## Exclude Styles
Rapid rap phrasing, dense English clauses, heavy reverb on the lead vocal, and multiple voices singing different words.

## Lyrics or Edit Instruction
```text
Repair the chorus diction.
Problem line: "Every time I try to say I need you more than yesterday I know"
Replace with:
[Chorus]
每次我沉默
Hear me now
心裡那句
Stay somehow

Give each phrase one breath. Put English on sustained notes, not fast passing notes.
```

## Expected Result
Clearer pronunciation, a stable bilingual pattern, and room for the emotional melody.

## Failure Modes
The model keeps too many syllables, adds echoes, or blurs Chinese and English in one phrase.

## Next Iteration
Remove English from the highest note, make it a background answer, and test one line at a time.

## Evidence
Evidence tier: `working-hypothesis`; the repair uses conservative one-variable debugging.
