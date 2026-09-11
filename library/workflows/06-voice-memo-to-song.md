# Voice Memo to Song

## When to use

Use this to turn a hummed melody, sung fragment, phone recording, or rough instrumental idea into a complete arrangement.

## Recommended model

- Default: `v6`
- Texture exploration: `v6-wild`

## Inputs

- A voice memo that you own or have rights to use
- The timestamp containing the useful idea
- Target genre and language
- Whether to preserve melody, rhythm, lyrics, vocal timbre, or mood
- Desired final structure

## Recipe

1. Confirm that you own or have rights to the recording and that it contains no unauthorized third-party performance.
2. Trim the memo to the clearest phrase before upload if your Suno workflow supports file selection.
3. State the exact timestamp and the element to preserve.
4. Separate source attributes from new production choices.
5. Start with `v6`, then use `v6-wild` only for alternative arrangements.

## Copy-ready template

```text
Create an original song from my voice memo. I own or have rights to use this source.

Source:
<file name>, useful timestamp <mm:ss-mm:ss>.

Preserve from the source:
- <melody / rhythm / lyric phrase / emotional mood>

Do not preserve:
- <background noise / uncertain words / rough timing>

Target:
<language>, <genre>, <structure>, <vocal direction>, <instrumentation>.
The final result should feel like a finished song, not a field recording.
```

## What to preserve

Preserve the identifiable melodic or rhythmic intent, not room noise, distortion, or accidental conversation.

## Failure signals

- The result merely adds effects to the raw memo.
- Lyrics from an unclear mumble are invented incorrectly.
- The melody disappears under a generic beat.
- Source noise becomes a rhythmic feature.

## Next iteration

Narrow the source timestamp, name one element to preserve, and provide corrected lyrics in brackets.

## Evidence

Evidence tier: `official` for multimodal/source-based creation; `official-informed` for rights and timestamp guidance.
