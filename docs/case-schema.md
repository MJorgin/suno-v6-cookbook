# Case Schema

Every file in `library/examples/` must use Markdown with YAML frontmatter.

## Required Frontmatter

```yaml
---
id: kebab-case-unique-id
title: Human-readable title
language: zh-CN
genre: mandopop
workflow: text-to-song
model: v6
inputs: [text]
evidence_tier: working-hypothesis
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [urban, ballad]
---
```

## Field Rules

| Field | Allowed value |
|---|---|
| `id` | Unique lowercase kebab-case identifier |
| `title` | Short human-readable title |
| `language` | IETF-style language tag such as `en`, `zh-CN`, `yue-Hant-HK`, or `bilingual-en-zh-CN` |
| `genre` | Slug matching a file or concept in `library/genres/` |
| `workflow` | A workflow slug such as `text-to-song` or `lyric-micro-edit` |
| `model` | `v6`, `v6-wild`, `v6-mini`, or `v6-mini+then-v6` |
| `inputs` | One or more of `text`, `audio`, `image`, `video`, `voice-memo`, `owned-song-a`, `owned-song-b` |
| `evidence_tier` | `official`, `official-informed`, `community-tested`, `working-hypothesis`, or `legacy-v5` |
| `verified` | `true` only for documented tests; initial cookbook examples use `false` |
| `created_at` | `YYYY-MM-DD` |
| `updated_at` | `YYYY-MM-DD` |
| `tags` | Lowercase kebab-case tags when practical |

## Required Body Sections

Every example includes these headings:

1. `## Goal`
2. `## Model`
3. `## Inputs`
4. `## Style Prompt`
5. `## Exclude Styles`
6. `## Lyrics or Edit Instruction`
7. `## Expected Result`
8. `## Failure Modes`
9. `## Next Iteration`
10. `## Evidence`

For instrumental or source-edit cases, the lyric section may contain structure
cues or a source instruction instead of sung lyrics. It still keeps the same
heading so the collection remains machine-readable.
