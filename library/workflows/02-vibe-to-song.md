# Vibe-to-Song

## When to use

Use this when you have a mood, scene, visual reference, playlist feeling, or emotional keyword but do not yet have fixed lyrics.

## Recommended model

- Exploration: `v6-wild`
- Polished realization: `v6`
- Quick scratch: `v6-mini`

## Inputs

- A scene or emotional contrast
- Genre neighborhood and sonic palette
- Language preference
- Whether the result should be instrumental, vocal-forward, or humming-led
- A short list of unwanted clichés

## Recipe

1. Describe the scene using concrete nouns and motion: rain, neon, subway, sunrise, empty room, crowded highway.
2. Name one genre and one production lane.
3. State the energy curve: calm build, sudden lift, constant tension, or gentle descent.
4. Ask `v6-wild` for three short mood variants.
5. Select the strongest variant and rebuild it with clearer lyrics and structure using `v6`.

## Copy-ready template

```text
Create an original <language or instrumental> mood piece.

Scene:
<place>, <time>, <weather/light>, <character action>.

Feeling:
<emotion> with an undercurrent of <second emotion>.

Music:
<genre>, <tempo range>, <core instruments>, <energy curve>.

Voice:
<instrumental/humming/wordless/full lyrics>, <delivery>.

Explore surprising choices, but keep the result coherent and singable.
Exclude: <cliché or instrument to avoid>.
```

## What to preserve

Preserve the scene, central emotion, and energy curve when moving from wild exploration to flagship refinement.

## Failure signals

- The output is atmospheric but has no song form.
- Too many visual details become random sound effects.
- The result sounds like a generic stock mood track.
- `v6-wild` produces a strong texture but unusable structure.

## Next iteration

Keep only one signature texture from the wild result, add a verse/chorus form, and let `v6` produce a tighter arrangement.

## Evidence

Evidence tier: `official-informed`. The exploratory behavior follows the official positioning of `v6-wild`; the refinement step uses the steadier flagship model.
