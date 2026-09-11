# Prompt Patterns

## Four-part new-song prompt

```text
Creative intent:
<one sentence: story, scene, and emotional arc>

Music direction:
<genre>, <tempo>, <two to four instruments>, <production texture>, <energy curve>

Vocal direction:
<language>, <tone>, <delivery>, <harmony approach>

Lyrics:
[Verse]
<original lines>
[Chorus]
<repeated hook>

Exclude:
- <unwanted sound>
- <unwanted vocal approach>
```

## Better descriptor shape

- Use concrete sound: "warm upright piano", "soft brushed drums", "glassy synth arpeggio".
- Use one dominant genre. A second genre should be an accent, not another full arrangement.
- Give the chorus a repeatable title phrase.
- Put negative instructions under `Exclude`, not scattered through the style paragraph.
- Keep each verse line to one image or one thought.

## Common reductions

| Overstuffed idea | Cleaner version |
|---|---|
| Synthwave plus trap plus jazz plus orchestra | Synthwave with one muted brass accent in the bridge |
| Emotional, cinematic, huge, tiny, aggressive, soft | Quiet verse, widescreen but controlled chorus |
| Many instruments named at once | Two core instruments plus one accent |
| Named performer comparison | Neutral voice traits and era/production language |

## Exploration to refinement

Ask `v6-wild` one bounded question. Carry only one answer into `v6`:

```text
Exploration question: <one question>
Hard boundaries: <language, genre, hook, tempo, voice>.
After exploration, use only: <one idea>.
Rebuild a polished song with `v6` and preserve the boundaries.
```
