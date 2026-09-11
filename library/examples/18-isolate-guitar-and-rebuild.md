---
id: isolate-guitar-and-rebuild
title: Isolate Guitar and Rebuild
language: en
genre: rock-anthem
workflow: isolate-and-rebuild
model: v6
inputs: [audio, text]
evidence_tier: official
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [isolation, guitar, rebuild, cleared-source]
---

## Goal
Isolate a guitar motif from a rough full-band demo owned by the user and rebuild the rest as a tighter rock anthem.

## Model
`v6` for extraction accuracy and controlled replacement.

## Inputs
Owned demo audio, target timestamp, layer to isolate, and new arrangement brief.

## Style Prompt
Original modern rock anthem rebuilt around the isolated guitar motif: crunch rhythm guitars, propulsive live drums, locked bass, dynamic verse, wide group-vocal chorus, analog warmth.

## Exclude Styles
Do not keep the rough demo drums, preserve room chatter, copy an existing remix, or add electronic drops.

## Lyrics or Edit Instruction
```text
Isolate one layer from my cleared source and rebuild an original track around it. I own or have rights to use this source.
Source: band-demo-room.m4a, timestamp 00:34-00:48.
Target layer: clean lead guitar motif.
Ignore: rough drums, bass, background talk, amp hiss.
Transformation: keep the guitar motif dry and recognizable in the verse, then double it with crunch guitars in the chorus.
All supporting music should be new.
```

## Expected Result
The guitar motif remains identifiable while the old rhythm section and room noise disappear.

## Failure Modes
Bleeding drums remain, the motif is processed beyond recognition, or the rebuild changes its key.

## Next Iteration
Narrow to a four-second timestamp and state that recognition takes priority over transformation.

## Evidence
Evidence tier: `official` for isolation/rebuild capability; workflow details are official-informed.
