# Contributing to Awesome Suno v6 Cookbook

Thank you for helping improve the cookbook. The project is most useful when contributions are original, testable, safe, and honest about evidence.

## What to contribute

- New workflow recipes or improvements to existing recipes.
- Genre playbooks without named-artist impersonation.
- Original examples with complete YAML frontmatter.
- Documented failure cases and repair attempts.
- Corrections to outdated claims or links.
- Translations, especially Chinese and English improvements.

## What not to contribute

- Commercial song lyrics or close rewrites of copyrighted lyrics.
- Pirated audio, ripped music, unauthorized samples, or private recordings.
- Instructions for cloning a named singer, public figure, or private individual.
- Browser automation, API clients, upload tools, credential collection, or package-manager setup for v0.1.
- Claims of official partnership, certification, deterministic generation quality, or exact voice reproduction.
- Affiliate links, promotional spam, or generated low-effort list padding.

## Evidence requirements

Use one of the supported labels:

- `official`
- `official-informed`
- `community-tested`
- `working-hypothesis`
- `legacy-v5`

Official facts should link to Suno's announcement, help center, release notes, or product documentation. Community-tested submissions should describe the model, date, prompt shape, result, and what changed between attempts.

## Adding an example

Every file in `library/examples/` must include these frontmatter fields:

```yaml
id:
title:
language:
genre:
workflow:
model:
inputs:
evidence_tier:
verified:
created_at:
updated_at:
tags:
```

The body must include: Goal, Model, Inputs, Style Prompt, Exclude Styles, Lyrics or Edit Instruction, Expected Result, Failure Modes, Next Iteration, and Evidence.

## Source-based contributions

For audio, image, video, voice memo, sample, isolation, or mashup cases:

- state that the source is owned or licensed;
- use fictional file names rather than uploading private media;
- identify timestamps and target layers;
- separate preservation and replacement instructions;
- avoid any workflow that assumes commercial media can be uploaded.

## Writing style

- Prefer copy-ready blocks over abstract advice.
- Keep prompts specific but short enough to test.
- Name one dominant genre per song.
- Use neutral vocal traits instead of named performers.
- Keep Chinese lyrics singable: short lines, natural word order, clear hooks, and deliberate English inserts.
- Do not overstate results; model outputs vary.

## Pull request checklist

- [ ] Relative links resolve.
- [ ] Required counts and headings pass the documented static checks.
- [ ] New examples use complete frontmatter and unique kebab-case IDs.
- [ ] Source cases include rights language.
- [ ] No private media, credentials, cookies, or personal data are committed.
- [ ] The change passes `git diff --check`.

Please open an issue first for large structural changes or new content categories.
