# Section Replacement

## When to use

Use this when an entire verse, pre-chorus, chorus, bridge, or outro is weak while the rest of the song is worth keeping.

## Recommended model

- Controlled replacement: `v6`
- Radical alternative section: `v6-wild`, then `v6`

## Inputs

- Target section
- Existing lyrics if available
- Narrative job of the new section
- Maximum line count and line length
- Transition points into and out of the section

## Recipe

1. Identify the section's job: introduce tension, lift energy, reveal a twist, or close the story.
2. Write the new section separately before requesting the edit.
3. Match the neighboring section's language and syllable density.
4. Request replacement of only the named section.
5. Ask `v6` to preserve the preceding transition, following section, vocal identity, and production.

## Copy-ready template

```text
Replace one section only.

Target section: <section name>
Section job: <what this section must accomplish>
New section lyrics:
[<Section>]
<line>
<line>

Preserve:
- The lead voice and singing language
- All lyrics outside the target section
- Tempo, key, instrumentation, and production style
- Natural transition from <previous section> into <section> and into <next section>
```

## What to preserve

Keep the song's existing voice, harmonic world, and section boundaries. The replacement should sound like the same recording session.

## Failure signals

- The replacement creates a second genre.
- The new section introduces unexplained characters or facts.
- The transition ignores the previous melody.
- The chorus becomes less repetitive and therefore less hook-like.

## Next iteration

Reduce the section to its strongest two lines, specify the energy level at the boundary, and regenerate with `v6`.

## Evidence

Evidence tier: `official-informed`, extending v6's local editing capability from single lines to a clearly bounded section.
