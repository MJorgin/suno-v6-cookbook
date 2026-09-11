# Lyric Micro-Edit

## When to use

Use this when one word, phrase, rhyme, pronunciation, or sentence is wrong and the surrounding melody and arrangement should remain intact.

## Recommended model

- Default: `v6`
- Low-stakes draft: `v6-mini`

## Inputs

- The exact original line
- The exact replacement line
- The section name
- The syllable or rhythm target
- Elements that must remain unchanged

## Recipe

1. Quote the existing line exactly.
2. Provide the new line exactly as it should be sung.
3. Match syllable count and stress pattern as closely as possible.
4. State that the melody, voice, tempo, instrumentation, and other lyrics should remain.
5. If pronunciation fails, simplify vowels and consonant clusters before changing the arrangement.

## Copy-ready template

```text
Make a local lyric edit only.

Section: <Verse 2 / Chorus / Bridge>
Original line: "<exact existing line>"
Replace with: "<exact new line>"

Singing requirement:
Match the existing melody, rhythm, phrasing, and emotion. The new line has approximately <number> syllables.

Preserve:
- Same lead voice
- Same tempo and key
- Same instrumentation
- All surrounding lyrics
```

## What to preserve

Preserve everything except the specified line. Do not introduce a new style request during a micro-edit.

## Failure signals

- Other lines are rewritten.
- The voice or tempo changes.
- The replacement line has too many syllables.
- Chinese, English, or bilingual words are over-enunciated unnaturally.

## Next iteration

Make the replacement shorter, mark the stressed syllables with spaces or punctuation, and request only the affected line again.

## Evidence

Evidence tier: `official` for the existence of plain-language local replacement in v6; `official-informed` for the controlled prompting pattern.
