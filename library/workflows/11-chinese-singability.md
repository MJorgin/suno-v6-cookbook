# Chinese Singability Workflow

## When to use

Use this for Mandarin, Cantonese, bilingual Chinese/English, or English lyrics inserted into Chinese songs when pronunciation, line length, or emotional delivery is unstable.

## Recommended model

- Default: `v6`
- Fast diction test: `v6-mini`

## Inputs

- Chinese variant: Mandarin, Cantonese, or bilingual
- Core hook in plain language
- Line length target
- Pronouns and tense choices
- English insert words, if any
- Vocal delivery notes

## Recipe

1. State the Chinese variant before writing lyrics.
2. Keep each line around one breath and one complete image.
3. Prefer common sung vocabulary over dense written phrases.
4. Put repeated sounds in the chorus hook.
5. Limit English inserts to short words that fit the stress pattern.
6. Test difficult lines with `v6-mini`, then produce the polished version with `v6`.

## Copy-ready template

```text
Create an original <Mandarin/Cantonese/bilingual> song with clear, natural singing.

Language:
<language variant>, with occasional English only for <word/phrase>.

Singability rules:
- Keep lines short enough for one breath
- Prefer natural spoken word order
- Make the chorus hook repeat <phrase>
- Avoid dense literary allusions and long number strings

Music:
<genre>, <tempo>, <instruments>.

Voice:
<tone>, <emotion>, <delivery>.

Lyrics:
[Verse]
<line>
[Chorus]
<repeatable hook>
```

## What to preserve

Preserve the Chinese variant, repeated hook, and simple emotional sentence. Pronunciation improvements should not turn the song into formal prose.

## Failure signals

- Words are blurred or rewritten.
- English stress breaks the Chinese phrase.
- The lyric reads well on paper but has too many syllables.
- Cantonese and Mandarin phrasing are mixed unintentionally.

## Next iteration

Shorten the line, replace difficult consonant clusters, move English to a background vocal, and add section-level delivery notes.

## Evidence

Evidence tier: `official-informed`. v6 supports language-based generation, while the singability rules are practical composition guidance requiring user testing.
