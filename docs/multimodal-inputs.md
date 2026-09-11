# Multimodal Inputs

v6 can create with text, audio, images, video, voice memos, and combinations of
sources. A multimodal prompt should identify the source, rights, target
element, and preservation rules.

## Source Description Checklist

- Ownership: "I own this recording" or "I have rights to use it".
- Input type: voice memo, video, image, owned song, sample, or text note.
- Timestamp: for audio or video, state the segment such as `0:45–0:52`.
- Target element: melody, riff, vocal, drum groove, color palette, motion, or
  mood.
- Keep rule: what must remain recognizable.
- Replace rule: what should become new.
- Output target: genre, tempo, language, arrangement, and section.

## Voice Memo Template

```text
Use my owned voice memo at <timestamp> for melody and phrase timing only.
Preserve the contour of the chorus, but replace the rough timing where words
overlap. Build a <genre> arrangement with <instruments>. Do not preserve room
noise, conversation, or the original accompaniment.
```

## Image or Video Template

```text
Use the visual as mood and narrative inspiration, not as lyrics to copy.
Translate <color/light/motion/subject> into <tempo>, <instrument texture>, and
<vocal delivery>. The song should feel like <emotional scene>, with a <section
arc>.
```

## Sampling and Isolation Template

```text
From my owned recording, isolate the <instrument/vocal> at <timestamp>. Keep
its rhythm and pitch character, remove the other layers, then build a new
<genre> beat around it. Treat the isolated element as a motif, not a full
arrangement.
```

## Multi-Source Mashup Template

```text
Source A is my owned song and provides <element>. Source B is my owned song
and provides <element>. Add new <language> lyrics about <theme>. Keep the
tempo close to <BPM>, resolve key differences toward <target mood>, and make
the first chorus clearly state the hook.
```

When a source is not owned, do not upload it. Describe only broad,
non-infringing traits and create an original source.
