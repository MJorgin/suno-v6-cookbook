# Suno v6 Cookbook v0.1 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a public-ready, evidence-labeled Suno v6 cookbook with workflow recipes, genre playbooks, original examples, and a dependency-free agent skill.

**Architecture:** The repository is a static Markdown knowledge base. Human-facing canonical docs live in `docs/`, reusable prompt recipes live in `library/`, and the agent-facing skill contains a short workflow plus selected references under `agents/skills/suno-v6-songwriter/`. No runtime code, dependency installation, browser automation, API client, or credential handling is introduced in v0.1.

**Tech Stack:** Markdown, YAML Frontmatter, Git, and shell-based static checks (`find`, `rg`, `git diff --check`).

**Spec:** `docs/superpowers/specs/2026-09-11-suno-v6-cookbook-design.md`

## Global Constraints

- Repository slug: `suno-v6-cookbook`.
- Display title: `Awesome Suno v6 Cookbook`.
- Future public repository: `MJorgin/suno-v6-cookbook`.
- English `README.md` is the primary global entry point; `README.zh-CN.md` is the Chinese entry point.
- Content license: CC-BY-4.0.
- v0.1 is Markdown-only: no package manager, no runtime dependencies, no generated website, no npm/pip package.
- The skill must not make network requests, run shell commands, request cookies/tokens/API keys, automate suno.com, or upload media.
- Every example must include YAML frontmatter with `id`, `title`, `language`, `genre`, `workflow`, `model`, `inputs`, `evidence_tier`, `verified`, `created_at`, `updated_at`, and `tags`.
- Evidence tiers are restricted to `official`, `official-informed`, `community-tested`, `working-hypothesis`, and `legacy-v5`.
- Initial examples are original and unverified unless explicitly marked otherwise; use `evidence_tier: working-hypothesis` or `official-informed`, with `verified: false`.
- Do not provide instructions for impersonating named artists, cloning named voices, using copyrighted lyrics, or uploading unauthorized audio.
- Official v6 facts must cite the official v6 announcement: `https://suno.com/blog/introducing-v6`.
- Keep all relative links valid and keep generated outputs copy-pasteable into Suno.

---

## File Structure and Responsibilities

| Path | Responsibility |
|---|---|
| `README.md` | Global English landing page, quick-start recipe, links to all sections. |
| `README.zh-CN.md` | Chinese landing page and quick-start. |
| `LICENSE` | CC-BY-4.0 grant and canonical license URL. |
| `CONTRIBUTING.md` | Submission rules, evidence labels, copyright and safety requirements. |
| `CODE_OF_CONDUCT.md` | Short community behavior policy. |
| `docs/what-is-new-in-v6.md` | Official v6 feature summary with source labels. |
| `docs/model-router.md` | Decision table for `v6`, `v6-wild`, and `v6-mini`. |
| `docs/prompt-anatomy.md` | Four-part prompt structure and output format. |
| `docs/lyric-and-section-tags.md` | Section labels, singability, and language guidance. |
| `docs/edit-and-mashup-workflows.md` | Canonical index for workflow recipes. |
| `docs/multimodal-inputs.md` | Text/audio/image/video/voice-memo input guidance. |
| `docs/genre-playbook.md` | Index for 12 genre playbooks. |
| `docs/chinese-lyrics.md` | Chinese and bilingual singability rules. |
| `docs/safety-and-copyright.md` | Trademark, copyright, voice impersonation, and user responsibility boundaries. |
| `docs/case-schema.md` | Required example frontmatter and body sections. |
| `docs/v5-to-v6-migration.md` | Migration from V5/V5.5 habits to v6 workflows. |
| `library/workflows/*.md` | Twelve actionable Suno v6 workflow recipes. |
| `library/genres/*.md` | Twelve genre/style playbooks. |
| `library/examples/*.md` | Twenty-four original copy-ready example cases. |
| `library/failure-notes/*.md` | Six failure diagnosis and repair notes. |
| `agents/skills/suno-v6-songwriter/SKILL.md` | Agent routing and output workflow. |
| `agents/skills/suno-v6-songwriter/references/*.md` | Five compact references used by the skill. |

---

### Task 1: Repository Foundation and Legal Frame

**Files:**
- Create: `LICENSE`
- Create: `CODE_OF_CONDUCT.md`
- Create: `.gitignore`
- Create: `docs/safety-and-copyright.md`
- Create: `docs/case-schema.md`

**Interfaces:**
- Consumes: Approved design spec.
- Produces: CC-BY-4.0 identity, evidence schema, safety rules that all later docs and examples cite.

- [ ] **Step 1: Create the legal and community baseline**

Add a CC-BY-4.0 `LICENSE` with the canonical URL `https://creativecommons.org/licenses/by/4.0/`. Add a concise `CODE_OF_CONDUCT.md` covering respectful feedback, no copyright-infringing submissions, no harassment, and issue-based enforcement.

- [ ] **Step 2: Add a minimal `.gitignore`**

Ignore only local system and editor artifacts:

```gitignore
.DS_Store
Thumbs.db
*.tmp
*.bak
.idea/
.vscode/
```

- [ ] **Step 3: Write safety and copyright policy**

`docs/safety-and-copyright.md` must state that the project is unofficial, does not automate Suno, does not collect credentials, rejects named-voice impersonation, and converts artist references into non-identifying technical descriptors.

- [ ] **Step 4: Write the example schema**

Document the exact YAML frontmatter and required body sections:

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
tags: [tag-a, tag-b]
---
```

Required body headings: `Goal`, `Model`, `Inputs`, `Style Prompt`, `Exclude Styles`, `Lyrics or Edit Instruction`, `Expected Result`, `Failure Modes`, `Next Iteration`, and `Evidence`.

- [ ] **Step 5: Verify and commit**

Run:

```bash
test -f LICENSE
test -f docs/safety-and-copyright.md
test -f docs/case-schema.md
git diff --check
git status --short
```

Commit:

```bash
git add LICENSE CODE_OF_CONDUCT.md .gitignore docs/safety-and-copyright.md docs/case-schema.md
git commit -m "docs: add repository legal and schema baseline"
```

### Task 2: Canonical v6 Knowledge Docs

**Files:**
- Create: `docs/what-is-new-in-v6.md`
- Create: `docs/model-router.md`
- Create: `docs/prompt-anatomy.md`
- Create: `docs/lyric-and-section-tags.md`
- Create: `docs/multimodal-inputs.md`
- Create: `docs/chinese-lyrics.md`
- Create: `docs/v5-to-v6-migration.md`

**Interfaces:**
- Consumes: `https://suno.com/blog/introducing-v6`.
- Produces: Canonical terminology and routing rules used by workflows, examples, and skill references.

- [ ] **Step 1: Summarize official v6 capabilities**

Write `docs/what-is-new-in-v6.md` with separate sections for `v6`, `v6-wild`, `v6-mini`, plain-language editing, mashup, sampling/isolation, and multimodal creation. Label direct facts as `T0 official`; label practical usage suggestions as `T1 official-informed`.

- [ ] **Step 2: Build the model router**

`docs/model-router.md` must include at least these rows: polished text-to-song, exploration, quick draft, micro lyric edit, section replacement, voice memo, image/video mood, sample/isolate, owned-source mashup, Chinese ballad, and failure repair.

- [ ] **Step 3: Define prompt anatomy**

Define Creative Intent, Music Direction, Vocal Direction, and Edit/Source Instruction. Include a good example and an overstuffed bad example. Require exclusion guidance to use a dedicated exclusion section.

- [ ] **Step 4: Write lyric and structure guidance**

Cover `[Intro]`, `[Verse]`, `[Pre-Chorus]`, `[Chorus]`, `[Bridge]`, `[Interlude]`, `[Outro]`, instrumental-only cues, and delivery cues. Mark exact UI behavior as subject to change.

- [ ] **Step 5: Write multimodal and Chinese guidance**

Multimodal guidance must tell users to describe source ownership, timestamp, target element, preserve/replace rules, and output style. Chinese guidance must cover line length, rhyme, pronouns, English inserts, numbers, punctuation, and sungability.

- [ ] **Step 6: Write V5 migration**

Use `T4 legacy-v5` for V5/V5.5 guidance. Explicitly say V5 prompts remain useful for style and lyrics but do not cover v6 editing, mashup, sampling, and multimodal instructions.

- [ ] **Step 7: Verify and commit**

Run:

```bash
for f in what-is-new-in-v6 model-router prompt-anatomy lyric-and-section-tags multimodal-inputs chinese-lyrics v5-to-v6-migration; do test -f "docs/$f.md"; done
rg -n "T0|T1|T4|v6-wild|v6-mini" docs
git diff --check
```

Commit:

```bash
git add docs
git commit -m "docs: add canonical suno v6 guides"
```

### Task 3: Twelve Workflow Recipes

**Files:**
- Create: `docs/edit-and-mashup-workflows.md`
- Create 12 files in `library/workflows/`:
  - `01-text-to-song.md`
  - `02-vibe-to-song.md`
  - `03-wild-to-flagship-refinement.md`
  - `04-lyric-micro-edit.md`
  - `05-section-replacement.md`
  - `06-voice-memo-to-song.md`
  - `07-image-or-video-to-music.md`
  - `08-sample-riff-to-beat.md`
  - `09-isolate-and-rebuild.md`
  - `10-owned-source-mashup.md`
  - `11-chinese-singability.md`
  - `12-failure-diagnosis.md`

**Interfaces:**
- Consumes: Canonical docs from Task 2.
- Produces: Stable workflow IDs used by examples and the skill.

- [ ] **Step 1: Define common recipe format**

Every workflow includes: `When to use`, `Recommended model`, `Inputs`, `Recipe`, `Copy-ready template`, `What to preserve`, `Failure signals`, `Next iteration`, and `Evidence`.

- [ ] **Step 2: Write creation workflows**

Write text-to-song, vibe-to-song, and wild-to-flagship refinement. Each must provide a fill-in template with named placeholders in angle brackets.

- [ ] **Step 3: Write edit and source workflows**

Write micro-edit, section replacement, voice memo, image/video, sample riff, isolate/rebuild, and owned-source mashup. Every source workflow must require that the user owns or has rights to the source.

- [ ] **Step 4: Write language and repair workflows**

Write Chinese singability and failure diagnosis. Failure diagnosis must separate lyric, vocal, arrangement, style adherence, and source-edit failures.

- [ ] **Step 5: Create the workflow index**

`docs/edit-and-mashup-workflows.md` links all 12 recipes and maps each to recommended models.

- [ ] **Step 6: Verify and commit**

Run:

```bash
test "$(find library/workflows -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "12"
rg -n "Copy-ready template|Evidence|own|rights" library/workflows docs/edit-and-mashup-workflows.md
git diff --check
```

Commit:

```bash
git add docs/edit-and-mashup-workflows.md library/workflows
git commit -m "docs: add suno v6 workflow recipes"
```

### Task 4: Twelve Genre Playbooks

**Files:**
- Create: `docs/genre-playbook.md`
- Create 12 files in `library/genres/`:
  - `mandopop-ballad.md`
  - `cantopop-electropop.md`
  - `english-indie-pop.md`
  - `hip-hop-trap.md`
  - `synthwave.md`
  - `lofi-bedroom.md`
  - `rock-anthem.md`
  - `electronic-dance.md`
  - `acoustic-folk.md`
  - `cinematic-ambient.md`
  - `bossa-jazz.md`
  - `hyperpop.md`

**Interfaces:**
- Consumes: Prompt anatomy and model router.
- Produces: Genre descriptors and exclusion vocabulary reused by examples.

- [ ] **Step 1: Define playbook format**

Each playbook includes: `Identity`, `Default model`, `Useful descriptors`, `Instrumentation`, `Vocal direction`, `Rhythm and production`, `Avoid`, `Chinese/English notes`, `Mini recipe`, and `Evidence`.

- [ ] **Step 2: Write six mainstream playbooks**

Write Mandopop ballad, Cantopop electropop, English indie pop, hip-hop/trap, synthwave, and lo-fi bedroom.

- [ ] **Step 3: Write six contrast playbooks**

Write rock anthem, electronic dance, acoustic folk, cinematic ambient, bossa jazz, and hyperpop.

- [ ] **Step 4: Write the playbook index**

Link all 12 files from `docs/genre-playbook.md` and state that named artists are intentionally omitted.

- [ ] **Step 5: Verify and commit**

Run:

```bash
test "$(find library/genres -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "12"
rg -n "Default model|Useful descriptors|Avoid|Evidence" library/genres docs/genre-playbook.md
git diff --check
```

Commit:

```bash
git add docs/genre-playbook.md library/genres
git commit -m "docs: add genre prompt playbooks"
```

### Task 5: Twenty-Four Original Examples and Failure Notes

**Files:**
- Create 24 files in `library/examples/`
- Create 6 files in `library/failure-notes/`

**Interfaces:**
- Consumes: Workflow IDs and genre playbooks.
- Produces: Searchable, evidence-labeled, copy-ready examples.

- [ ] **Step 1: Create 12 base creation examples**

Cover Mandopop ballad, Cantopop electropop, English indie pop, hip-hop/trap, synthwave, lo-fi bedroom, rock anthem, electronic dance, acoustic folk, cinematic ambient, bossa jazz, and hyperpop.

- [ ] **Step 2: Create 12 v6-native workflow examples**

Cover micro lyric edit, gospel-style chorus replacement, voice memo, video mood, riff sampling, guitar isolation, owned-source mashup, bilingual rewrite, podcast intro, brand-safe upbeat jingle, mumbled-vocal repair, and overstuffed-prompt repair.

- [ ] **Step 3: Apply the common schema**

All 24 files need the exact frontmatter keys and body headings from `docs/case-schema.md`. Use unique kebab-case IDs. Do not include real artist names, commercial song lyrics, private media, or unverified generated audio links.

- [ ] **Step 4: Write six failure notes**

Create notes for overstuffed style prompt, wrong model choice, mumbled Chinese/English lyrics, weak chorus hook, source-edit overreach, and genre drift. Each note includes symptom, likely cause, one conservative repair, and one exploratory repair.

- [ ] **Step 5: Verify and commit**

Run:

```bash
test "$(find library/examples -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "24"
test "$(find library/failure-notes -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "6"
rg -l "evidence_tier:" library/examples | wc -l
rg -n "api[_-]?key|cookie|password|token|curl |wget |playwright|suno.com/create" agents library || true
git diff --check
```

Commit:

```bash
git add library/examples library/failure-notes
git commit -m "docs: add original examples and failure notes"
```

### Task 6: Dependency-Free Agent Skill

**Files:**
- Create: `agents/skills/suno-v6-songwriter/SKILL.md`
- Create: `agents/skills/suno-v6-songwriter/references/model-router.md`
- Create: `agents/skills/suno-v6-songwriter/references/prompt-patterns.md`
- Create: `agents/skills/suno-v6-songwriter/references/edit-and-mashup.md`
- Create: `agents/skills/suno-v6-songwriter/references/chinese-lyrics.md`
- Create: `agents/skills/suno-v6-songwriter/references/quality-checklist.md`

**Interfaces:**
- Consumes: Canonical docs and library recipes.
- Produces: A portable skill directory with no code dependencies.

- [ ] **Step 1: Write skill frontmatter and routing rules**

Use skill name `suno-v6-songwriter`. Trigger on Suno v6 prompts, lyrics, model selection, editing, mashup, sampling, multimodal inputs, and failure repair.

- [ ] **Step 2: Write the required output contract**

Default response sections: recommended model, style prompt, exclude styles, lyrics/edit instruction, source handling, safety notes, and three iteration suggestions.

- [ ] **Step 3: Write compact references**

Keep each reference focused and copy the relevant rules from canonical docs without introducing scripts, credentials, or browser automation.

- [ ] **Step 4: Verify static safety**

Run:

```bash
find agents/skills/suno-v6-songwriter -type f -print
rg -n "curl |wget |requests|fetch\(|child_process|subprocess|playwright|api[_-]?key|cookie|password|authorization|token" agents/skills/suno-v6-songwriter || true
test -f agents/skills/suno-v6-songwriter/SKILL.md
git diff --check
```

The expected `rg` result is no match. The skill must remain Markdown-only.

- [ ] **Step 5: Commit**

```bash
git add agents
git commit -m "feat: add dependency-free suno v6 songwriter skill"
```

### Task 7: Bilingual README, Contribution Flow, and Release Copy

**Files:**
- Create: `README.md`
- Create: `README.zh-CN.md`
- Create: `CONTRIBUTING.md`
- Create: `docs/press-en.md`
- Create: `docs/press-zh-CN.md`

**Interfaces:**
- Consumes: All docs, workflows, examples, and skill.
- Produces: Public landing page and launch materials.

- [ ] **Step 1: Write English README**

The first screen must show `Awesome Suno v6 Cookbook`, one-sentence positioning, quick-start, non-official notice, safety boundary, and links to model router, workflows, examples, and skill installation.

- [ ] **Step 2: Write Chinese README**

Mirror the English README information with natural Chinese copy. Keep links relative and identical where possible.

- [ ] **Step 3: Write contribution guide**

Define evidence tiers, original-content requirement, example frontmatter checklist, rights declaration, and rejection reasons.

- [ ] **Step 4: Write launch posts**

English post should emphasize evidence-labeled recipes and agent-ready skill. Chinese post should emphasize v6 new workflows, Chinese singability, and no credentials/browser automation.

- [ ] **Step 5: Verify links and claims**

Run:

```bash
rg -n "MJorgin/suno-v6-cookbook|Awesome Suno v6 Cookbook|CC-BY-4.0|unofficial|non-official" README.md README.zh-CN.md CONTRIBUTING.md docs/press-*.md
rg -n "\]\(([^h#][^)]*)\)" README.md README.zh-CN.md
git diff --check
```

Commit:

```bash
git add README.md README.zh-CN.md CONTRIBUTING.md docs/press-en.md docs/press-zh-CN.md
git commit -m "docs: add bilingual launch and contribution guides"
```

### Task 8: Full Static Quality Gate

**Files:**
- No new content files unless verification reveals a concrete defect.
- Modify only files needed to fix failed checks.

**Interfaces:**
- Consumes: Completed repository.
- Produces: Release-ready Git working tree.

- [ ] **Step 1: Verify counts**

Run:

```bash
test "$(find library/workflows -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "12"
test "$(find library/genres -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "12"
test "$(find library/examples -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "24"
test "$(find library/failure-notes -maxdepth 1 -name '*.md' | wc -l | tr -d ' ')" = "6"
```

- [ ] **Step 2: Verify examples contain required keys**

Run:

```bash
for f in library/examples/*.md; do
  for key in id title language genre workflow model inputs evidence_tier verified created_at updated_at tags; do
    rg -q "^${key}:" "$f" || { echo "missing $key in $f"; exit 1; }
  done
done
```

- [ ] **Step 3: Verify forbidden automation and credential language is absent from the skill**

Run:

```bash
if rg -n "curl |wget |requests|fetch\(|child_process|subprocess|playwright|api[_-]?key|cookie|password|authorization|token" agents/skills/suno-v6-songwriter; then
  exit 1
fi
```

- [ ] **Step 4: Check misleading claims**

Run:

```bash
if rg -n "official project|officially certified|guaranteed|100% clone|exact voice clone" README.md README.zh-CN.md docs library agents; then
  exit 1
fi
```

- [ ] **Step 5: Check repository status and commit fixes**

Run:

```bash
git diff --check
git status --short
git log --oneline --max-count=10
```

If fixes were required, commit them with:

```bash
git add README.md README.zh-CN.md docs library agents
git commit -m "docs: pass v0.1 static quality gate"
```

If no fixes were required, create no empty commit.

## Self-Review

- Spec coverage: Tasks 1–8 cover the legal frame, official v6 knowledge, model routing, 12 workflows, 12 genre playbooks, 24 examples, Chinese guidance, safety, one static agent skill, bilingual launch materials, and static release checks.
- Placeholder scan: The plan contains no unresolved planning placeholders. Recipe templates intentionally use angle-bracket user inputs, which are explicit content fields rather than planning gaps.
- Interface consistency: Workflow slugs, skill name, evidence tiers, frontmatter keys, and required counts are identical across tasks.
