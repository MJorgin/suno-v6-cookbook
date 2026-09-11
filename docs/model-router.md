# Suno v6 Model Router

Use this as a starting point, not a guarantee.

| Task | First choice | Alternative | Why |
|---|---|---|---|
| Clear genre, clear lyrics, polished first result | `v6` | `v6-mini` | Precision and consistency matter |
| Explore an unusual combination | `v6-wild` | `v6` | Wild is designed for less predictable results |
| Fast scratch melody or rough hook | `v6-mini` | `v6` | Faster iteration before spending premium generations |
| Replace one lyric line | `v6` | `v6-mini` | Local consistency matters |
| Replace one section while preserving the rest | `v6` | `v6-wild` for a radical section | The default goal is controlled preservation |
| Turn a voice memo into a full arrangement | `v6` | `v6-wild` for texture | Keeps the melodic intent easier to compare |
| Turn an image or video into mood music | `v6-wild` | `v6` | Visual prompts often benefit from broad interpretation |
| Sample a timestamp and isolate an instrument | `v6` | `v6-wild` for reinterpretation | Source extraction and rebuild need specificity |
| Mashup multiple owned sources | `v6` | `v6-wild` | Multiple preservation rules benefit from the flagship model |
| Chinese ballad or dense Chinese lyrics | `v6` | `v6-mini` for drafts | Pronunciation and emotional continuity need the safer default |
| Prompt is overstuffed or the result drifts | `v6-mini` with a shorter prompt | `v6` after simplification | Reduce variables before asking for a polished result |
| First result is too conventional | `v6-wild` | — | Use wild as a variation engine |
| Wild result is promising but messy | `v6` | — | Rebuild the best idea with a precise final prompt |

## Two-Model Loop

For ambitious songs, a strong default loop is:

1. `v6-mini` for a cheap structural draft.
2. `v6-wild` for two or three directional variations.
3. Pick the strongest hook, arrangement, or texture.
4. Rewrite a precise `v6` prompt with only the winning elements.
5. Use local edit instructions for final line and section changes.

Do not ask one model to preserve everything and surprise you at maximum
intensity. Those goals conflict; split them into separate generations.
