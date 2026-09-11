# What Is New in Suno v6

Last reviewed: 2026-09-11  
Primary source: [Introducing v6](https://suno.com/blog/introducing-v6)

This page separates official facts from practical prompting guidance.

## T0 Official: Three Models

Suno v6 is a family rather than one model:

| Model | Official positioning | Practical starting use |
|---|---|---|
| `v6` | Reliable, precise, polished flagship model for Pro and Premier | A known target, final polish, precise edits |
| `v6-wild` | Less predictable, more varied, exploratory model for Pro and Premier | Finding unexpected textures, structures, and ideas |
| `v6-mini` | Faster and more efficient; available to everyone | Fast drafts, cheap trials, simple ideas |

The official announcement states that v6 understands more of the language and
building blocks musicians use, including vocals, instrumentation, structure,
mood, references, and overall feel.

## T0 Official: New Creation Operations

v6 introduces or foregrounds these operations:

- Edit part of an existing song using plain language.
- Change a single lyric without rebuilding the whole song.
- Build a mashup from multiple sources in one request.
- Sample, isolate, and build a new beat in one workflow.
- Create from a vibe, genre, or mix of inspirations.
- Create with text, audio, images, and video.

The official examples include:

> Change the chorus so it's sung by a gospel choir.

> Take the vocals from x, drums from y, and add new lyrics about losing
> control; make it 80s synthwave.

> Sample the riff at 0:45, isolate the guitar, build a beat around it.

> Make a song based on this image, this audio, and my journal entry.

## T1 Official-Informed: Prompting Implication

v6 prompts should describe both the desired result and the operation:

- what source material to use;
- which element to keep;
- which element to replace or isolate;
- where in the timeline the element occurs;
- how the new material should relate to the original;
- what should remain untouched.

This is a shift from V5-era prompting, where most recipes focused on the Style
box and lyrics. In v6, the edit instruction is often the most important input.

## Model Rollout Note

Suno says previous models will be retired as Suno moves fully onto the v6
generation. Interface labels and plan availability may change faster than this
repository. Check the current Suno UI before treating a screenshot or exact
field name as permanent.
