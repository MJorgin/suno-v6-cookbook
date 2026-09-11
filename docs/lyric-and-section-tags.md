# Lyric and Section Tags

Section tags help the model map words to arrangement events. Suno interfaces
may change, so use the conventional labels as prompting structure rather than
assuming every label has a dedicated UI control.

## Common Tags

| Tag | Use |
|---|---|
| `[Intro]` | Instrumental or atmospheric opening |
| `[Verse 1]` | First narrative section |
| `[Pre-Chorus]` | Rising transition |
| `[Chorus]` | Repeated emotional and melodic hook |
| `[Post-Chorus]` | Short tag or lift after chorus |
| `[Bridge]` | Contrasting section |
| `[Interlude]` | Instrumental or melodic break |
| `[Breakdown]` | Sparser arrangement |
| `[Build]` | Energy ramp |
| `[Drop]` | Electronic payoff, only when genre-appropriate |
| `[Outro]` | Ending statement |
| `[Fade Out]` / `[End]` | Closing instruction |

## Delivery Cues

Use one short cue per section:

```text
[Verse 1 - whispered close]
[Chorus - open and warmer]
[Bridge - raw breaking]
[Outro - fading breath]
```

Avoid stacking several contradictory cues:

```text
[Chorus - whispered belting rap choir solo soft powerful]
```

## Instrumental Work

For instrumental tracks, describe the arrangement in the Style Prompt and use
minimal structural cues:

```text
[Intro - solo piano]
[Main Theme - warm cello enters]
[Bridge - higher register]
[Outro - piano alone]
```

## Lyric Density

Start with:

- ballad verses: 4–6 short lines;
- pop verses: 4–8 lines depending on tempo;
- rap verses: more words only if the beat has space;
- chorus: 2–4 repeatable hook lines;
- fast electronic genres: fewer words per section.

If a line contains many consonant clusters, long English words, or mixed
Chinese-English terminology, leave more melodic space around it.
