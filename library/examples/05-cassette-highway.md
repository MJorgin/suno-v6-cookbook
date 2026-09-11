---
id: cassette-highway
title: Cassette Highway
language: en
genre: synthwave
workflow: wild-to-flagship-refinement
model: v6-wild
inputs: [text]
evidence_tier: official-informed
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [synthwave, nostalgia, highway]
---

## Goal
Use a wild exploration to find an unusual bridge for a retro-futuristic highway song.

## Model
`v6-wild` for the bridge idea, followed by `v6` for a polished full song.

## Inputs
A single exploration question, hard boundaries, and a short chorus concept.

## Style Prompt
Original synthwave, analog synth bass, steady drum machine, gated snare, rising arpeggios, delayed electric guitar, warm widescreen pads, nocturnal nostalgia.

## Exclude Styles
Cartoon laser effects, nonstop guitar solo, muddy reverb, and unreadable verses.

## Lyrics or Edit Instruction
```text
Exploration question:
What is a surprising bridge for a highway song about returning to a city you left?

Boundary:
Keep English lyrics, synthwave identity, 108 BPM, and the chorus "drive me back through the static rain."

Bridge seed:
The navigation voice disappears, and the road answers in an arpeggio that sounds like an old cassette rewinding.
```

## Expected Result
One distinctive bridge texture that supports the song rather than hijacking it.

## Failure Modes
The wild result changes key, genre, or language; the effect may become literal tape noise.

## Next Iteration
Use only the arpeggio idea, rebuild the bridge with `v6`, and explicitly preserve the chorus.

## Evidence
Evidence tier: `official-informed` based on model routing between exploration and refinement.
