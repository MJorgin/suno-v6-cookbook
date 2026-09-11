# Migrating V5 and V5.5 Prompts to v6

Evidence level for legacy guidance: `T4 legacy-v5` unless separately verified
on v6.

## What Still Travels Well

V5/V5.5 knowledge remains useful for:

- genre vocabulary;
- instrumentation;
- vocal timbre and delivery;
- section tags;
- lyric density;
- exclusion styles;
- pronunciation repair;
- broad arrangement structure.

## What Must Change

Older Suno recipes often treated a song as one Style Prompt plus lyrics. v6
workflows should add:

- model choice: `v6`, `v6-wild`, or `v6-mini`;
- source ownership;
- exact edit target;
- preserve and replace instructions;
- timestamp references;
- multimodal source descriptions;
- relationships among multiple sources;
- iterative refinement path.

## Migration Template

### Old V5 Shape

```text
Style: <genre>, <instruments>, <voice>, <mood>
Lyrics: <full lyric sheet>
```

### v6 Shape

```text
Model: v6
Creative goal: <one-sentence goal>
Style: <genre and music direction>
Vocal: <vocal identity and delivery>
Lyrics: <structured lyric sheet>
Edit/source: <what to keep, replace, isolate, or combine>
Exclude: <specific unwanted traits>
Iteration: <first repair if pronunciation, hook, or arrangement fails>
```

## V5 Parameter Caution

Older references may describe sliders, field names, model labels, or limits from
V5/V5.5. Keep the musical advice, but verify UI and plan availability in the
current Suno product. Do not present those parameters as official v6 controls
unless Suno documents them for v6.

## Recommended Experiment

Run the same short prompt through `v6-mini`, `v6`, and `v6-wild` once. Compare:

- hook memorability;
- lyric intelligibility;
- genre adherence;
- arrangement contrast;
- source preservation;
- edit locality.

Record results as `community-tested` only when the input, model, date, result,
and failure mode are documented.
