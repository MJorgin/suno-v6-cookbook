# Isolate and Rebuild

## When to use

Use this when a source contains one useful layer, such as a vocal, guitar, synth, percussion pattern, or ambient texture, and the rest should be replaced.

## Recommended model

- Default: `v6`
- Experimental reconstruction: `v6-wild`

## Inputs

- Source audio you own or have rights to use
- Timestamp and layer to isolate
- Layers to ignore or remove
- New genre, tempo, and instrumentation
- Whether the isolated layer should be clean, processed, or transformed

## Recipe

1. Confirm source rights and identify the target layer.
2. State the timestamp and whether the desired layer is melody, rhythm, harmony, or timbre.
3. Name the layers to ignore: crowd noise, drums, bass, pads, background vocals, or effects.
4. Describe the new supporting arrangement as original material.
5. Generate a controlled version with `v6`; use `v6-wild` only for a reinterpretation.

## Copy-ready template

```text
Isolate one layer from my cleared source and rebuild an original track around it. I own or have rights to use this source.

Source:
<file name>, timestamp <mm:ss-mm:ss>.
Target layer: <vocal / guitar / synth / percussion / ambient texture>.
Ignore: <unwanted layers and noise>.

Transformation:
<keep dry / lightly processed / heavily transformed>.

New arrangement:
<genre>, <tempo>, <new instruments>, <structure>.
Keep the target layer recognizable, but all supporting music should be new.
```

## What to preserve

Preserve the useful layer and its intended timing or pitch. Replace unrelated layers deliberately rather than asking for a vague remix.

## Failure signals

- Bleeding instruments remain central to the result.
- The new arrangement fights the source key or tempo.
- The source is processed beyond recognition despite a request to preserve it.
- The result resembles an existing released remix.

## Next iteration

Tighten the timestamp, choose one layer, and state whether recognition or transformation is the priority.

## Evidence

Evidence tier: `official` for v6 isolation and rebuilding capabilities; `official-informed` for the controlled rebuild pattern.
