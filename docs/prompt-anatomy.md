# Suno v6 Prompt Anatomy

A complete v6 recipe has four layers.

## 1. Creative Intent

Describe the song's purpose, story, and emotional trajectory.

```text
A quiet late-night city ballad about choosing to stay instead of leaving.
The emotion moves from restrained doubt in verse one to tender certainty in
the final chorus.
```

## 2. Music Direction

Use objective musical language:

- genre and scene;
- era or production reference without naming an artist;
- tempo or tempo feel;
- key or harmonic color if known;
- instruments and arrangement density;
- mix texture, space, and dynamics.

```text
Mandopop ballad, 72 BPM, sparse piano intro, warm fingerpicked acoustic guitar
in verse two, soft brushed drums entering before chorus, intimate close vocal,
gentle string pad only under the final chorus.
```

## 3. Vocal Direction

Describe voice and delivery rather than asking for a named person:

- apparent age and gender if relevant;
- timbre and register;
- breathiness, rasp, clarity, power, restraint;
- language and pronunciation priorities;
- lead/background relationship.

```text
Female lead, clear mid-alto, gentle breath at verse starts, controlled and
intimate rather than belting; subtle doubled harmonies only in the chorus.
```

## 4. Edit or Source Instruction

For source-based workflows, be explicit:

```text
Use my owned voice memo only for the melody and phrase timing. Keep the verse
melody, replace the rough guitar-piano accompaniment with a sparse studio
arrangement, and do not preserve background noise.
```

## Style Prompt Template

```text
<genre and scene>, <tempo feel>, <core instruments>, <arrangement path>,
<vocal identity and delivery>, <production space>, <emotional arc>.
Avoid: <unwanted genres, instruments, vocal habits, production effects>.
```

## Bad: Synonym Pile

```text
Dreamy ethereal magical floating soft gentle airy tender quiet emotional
cinematic beautiful nostalgic ambient pop.
```

The terms repeat one idea and leave little musical structure.

## Better: Each Term Does Work

```text
Intimate dream pop, 82 BPM, clean electric arpeggios, soft sub-bass, brushed
electronic drums entering in chorus, breathy female mid-alto, close vocal with
short reverb, sparse verse and wider synth-pad chorus.
Avoid: distorted guitars, rap, choir, aggressive EDM drop.
```

Keep exclusions specific and short. Use the Exclude Styles field when available
rather than packing many "no" statements into the main style prompt.
