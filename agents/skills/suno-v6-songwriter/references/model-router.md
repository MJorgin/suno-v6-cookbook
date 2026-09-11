# Model Router

| Task | Start with | Reason | Next route |
|---|---|---|---|
| Polished text-to-song with clear lyrics and genre | `v6` | Best default for control and consistency | Compare with `v6-mini` if cost or speed matters |
| Mood-first idea or uncertain genre | `v6-wild` | More variation and surprise | Rebuild one chosen idea with `v6` |
| Quick scratch melody, hook, or diction test | `v6-mini` | Faster and more efficient for drafts | Promote successful structure to `v6` |
| Replace one lyric line | `v6` | Local consistency is the priority | Simplify syllables and retry with `v6` |
| Replace one section | `v6` | Preserves neighboring song identity | Try `v6-wild` only for a radical alternate |
| Voice memo to song | `v6` | Balances source intent with arrangement | Use `v6-wild` for texture alternatives |
| Image or video to music | `v6-wild` | Visual prompts benefit from broad interpretation | Use `v6` for timing and final structure |
| Sample, isolate, or rebuild around a source | `v6` | Specificity and preservation matter | Use `v6-wild` for one reinterpretation |
| Multiple owned-source mashup | `v6` | Needs hierarchy and coherent resolution | Wild only for transition ideas |
| Mandarin or Cantonese polished song | `v6` | Safer diction and emotional continuity | Mini for short pronunciation tests |
| Overstuffed or drifting prompt | `v6-mini` with a minimal prompt | Reduces variables before polish | Add details back with `v6` |

## Route rule

If the request says "keep", "preserve", "replace only", or names a timestamp, default to `v6`. If it says "surprise me", "explore", "weird", or "what if", start with `v6-wild`.
