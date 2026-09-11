# Genre Drift

## Symptom
The result starts as one genre and becomes another, or the instrumentation contradicts the requested mood.

## Likely cause
The prompt names multiple genres without hierarchy, or a second genre is described using full-band details instead of one accent.

## Conservative repair
Name one dominant genre and keep it in the first sentence. Reduce the second influence to one rhythm, instrument, or section.

## Exploratory repair
Generate the dominant genre cleanly with `v6`; use `v6-wild` for a single fusion bridge, then decide whether the experiment deserves a separate track.
