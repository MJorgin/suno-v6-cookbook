# Overstuffed Style Prompt

## Symptom
The track changes genres, contains random instruments, or follows only a few words from a long prompt.

## Likely cause
Too many genres, instruments, moods, references, and plot points compete at the same priority level.

## Conservative repair
Reduce the style prompt to one genre, two instruments, one voice trait, and one emotional idea. Use `v6-mini` for a quick test.

## Exploratory repair
Run the same core with `v6-wild` after removing negative references. Keep one surprising texture and rebuild with `v6`.
