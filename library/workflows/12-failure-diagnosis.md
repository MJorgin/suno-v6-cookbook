# Failure Diagnosis

## When to use

Use this when a result is wrong but the cause is unclear. Diagnose one variable at a time instead of adding more style words.

## Recommended model

- Isolation test: `v6-mini`
- Controlled repair: `v6`
- Directional alternative: `v6-wild`

## Inputs

- The failed prompt
- The generated result description
- The one problem that matters most
- A reference to the section, source timestamp, or lyric line involved

## Recipe

1. Classify the failure: lyric, vocal, arrangement, style adherence, or source edit.
2. Remove half of the style descriptors and run a minimal prompt.
3. Change only one variable: lyrics, model, source range, genre, voice, or structure.
4. Compare the minimal result with the original result.
5. Reintroduce one useful descriptor at a time.
6. Use `v6-wild` only when the controlled version is correct but creatively boring.

## Copy-ready template

```text
Diagnose and repair one failure at a time.

Failed goal:
<what the result should have done>.

Main failure type:
<lyric / vocal / arrangement / style adherence / source edit>.

Minimal repair prompt:
Create an original <language> <genre> song about <one idea>.
Lead voice: <one trait>.
Core instruments: <two instruments max>.
Lyrics:
[Chorus]
<simple hook>

Do not add:
<the descriptors that may be causing drift>.
```

## What to preserve

Preserve the diagnosis record. Knowing which variable changed the result is more valuable than a single lucky generation.

## Failure signals

- Every new prompt changes five variables.
- The prompt contains more than three genres.
- Source instructions ask to preserve and replace the same element.
- A local edit is used to solve a global arrangement problem.

## Next iteration

Create a three-row test matrix: model, prompt length, and source/lyric change. Keep every other variable fixed.

## Evidence

Evidence tier: `working-hypothesis`, based on conservative prompt-debugging practice and the official model distinctions.
