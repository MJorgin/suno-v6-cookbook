# Text-to-Song

## When to use

Use this workflow when you already know the language, genre, emotional arc, and lyric idea, and want a polished first result.

## Recommended model

- Default: `v6`
- Fast sketch: `v6-mini`
- Stylistic surprise: `v6-wild` only after the core concept is clear

## Inputs

- Core emotion in plain language
- Genre and decade references without naming a living artist as an impersonation target
- Vocal direction, language, and tempo
- Original lyrics or a request for original lyrics
- Elements to exclude

## Recipe

1. Write one sentence describing the emotional story.
2. Choose genre, tempo, instrumentation, and production width.
3. Describe the lead voice using neutral traits: breathy, bright, restrained, raspy, intimate, or powerful.
4. Add section tags before each lyric block.
5. Put negative directions in a separate exclusion list.
6. Generate two versions on `v6`, then compare hook clarity, pronunciation, and arrangement.

## Copy-ready template

```text
Create an original <language> song.

Creative intent:
The song is about <specific situation>. The emotional arc moves from <starting feeling> to <ending feeling>.

Music direction:
<genre>, <tempo>, <instruments>, <production texture>. Keep the arrangement <sparse/full/cinematic/lo-fi>.

Vocal direction:
<gender-neutral description if needed>, <tone>, <delivery>, <harmony direction>.

Lyrics:
[Verse]
<original line>
<original line>
[Chorus]
<original hook>

Exclude:
- <unwanted instrument>
- <unwanted vocal style>
- <unwanted production effect>
```

## What to preserve

Preserve the story sentence, hook lyric, language, and lead-vocal temperament during later edits.

## Failure signals

- The chorus does not have a memorable repeated phrase.
- The genre changes halfway through the song.
- Dense lyrics are mumbled or sung unnaturally.
- The arrangement follows an excluded reference.

## Next iteration

Shorten each verse line, strengthen the repeated hook, remove one production descriptor, and regenerate with `v6`.

## Evidence

Evidence tier: `official-informed`. The v6 announcement describes improved precision and multimodal creation; this recipe translates those capabilities into a controlled text-first workflow.
