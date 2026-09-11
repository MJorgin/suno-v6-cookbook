# Wild-to-Flagship Refinement

## When to use

Use this workflow when you need fresh ideas first, but want the final result to be controlled, polished, and repeatable.

## Recommended model

- Divergence: `v6-wild`
- Convergence: `v6`

## Inputs

- One creative question
- A boundary list of elements that must not change
- Three or fewer wild directions
- Lyrics or thematic notes

## Recipe

1. Ask `v6-wild` a single question, such as "what is an unexpected bridge for this song?"
2. Generate two or three alternatives.
3. Label each result by the one idea worth preserving: rhythm, instrument, harmony, hook, or story twist.
4. Rewrite the chosen idea in concise prompt language.
5. Pass the idea to `v6` with explicit preservation rules.

## Copy-ready template

```text
I will use a wild exploration first, then a polished realization.

Exploration question for v6-wild:
What is a surprising but coherent <section/instrument/arrangement> idea for a song about <theme>?

Hard boundaries:
- Keep <language>
- Keep <genre core>
- Keep <emotional arc>
- Do not change <hook or melody identity>

Refinement instruction for v6:
Use only this idea from the exploration: <one chosen idea>.
Build a polished original song around it while preserving <boundary list>.
```

## What to preserve

Carry over one idea only. Preserving every wild result usually creates arrangement drift.

## Failure signals

- The refined version copies random quirks without a reason.
- The song loses its original genre or language.
- The wild result is interesting for ten seconds but cannot support a full song.

## Next iteration

Reduce the wild contribution to one section or one instrument, then run `v6` again with a shorter prompt.

## Evidence

Evidence tier: `official-informed`, based on the official distinction between the predictable flagship route and the more exploratory `v6-wild` model.
