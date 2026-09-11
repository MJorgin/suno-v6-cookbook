---
id: overstuffed-prompt-repair
title: Overstuffed Prompt Repair
language: en
genre: synthwave
workflow: failure-diagnosis
model: v6-mini
inputs: [text]
evidence_tier: working-hypothesis
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [prompt-repair, synthwave, simplification, mini]
---

## Goal
Repair a synthwave result that drifts because the original prompt contains too many genres, instruments, and plot points.

## Model
`v6-mini` for a minimal structural test, then `v6` after the core works.

## Inputs
A failed overstuffed prompt description and a deliberately minimal replacement.

## Style Prompt
Original synthwave: analog bass, steady drum machine, rising arpeggio, warm pad, delayed electric guitar, one nocturnal memory. That is the complete style direction for the test.

## Exclude Styles
Orchestra, trap hi-hats, jazz trumpet, reggae groove, metal guitar, film dialogue, and multiple story settings.

## Lyrics or Edit Instruction
```text
Minimal repair prompt:
Create an original English synthwave song about driving back to a city that changed.
Analog synth bass, drum machine, rising arpeggio, warm pad, delayed guitar.
Breathy controlled vocal and a repeated chorus:
"Drive me back through the static rain."

Do not add orchestral, trap, jazz, metal, reggae, spoken dialogue, or more than one scene.
```

## Expected Result
A coherent genre test that reveals whether the core concept works before extra detail is added.

## Failure Modes
Even the minimal version drifts, which suggests the model route or core concept—not the missing detail—is the problem.

## Next Iteration
Add one element at a time: first guitar, then a bridge texture, then a production effect. Regenerate after each change.

## Evidence
Evidence tier: `working-hypothesis` based on isolating prompt variables.
