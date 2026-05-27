# 🎙️ TTS Studio

> **Multi-character Text-to-Speech studio powered by ElevenLabs**  
> Built for generating cinematic Hindi audio for Jain animated stories — and any multi-character narrative.

🔗 **Live:** [abhishek249.github.io/tts-studio](https://abhishek249.github.io/tts-studio)

---

## ✨ What it does

Paste a script with `[character]` tags → assign ElevenLabs voices to each character → click **Generate** → download numbered MP3 segments ready for InShot, CapCut, or any video editor.

No stitching. No timing headaches. Each segment is numbered so your video editor knows the sequence.

---

## 🎬 Demo

https://github.com/user-attachments/assets/placeholder-video

> *Connect → Assign voices → Paste script → Generate → Download*

---

## 🚀 Quick Start

1. Open [abhishek249.github.io/tts-studio](https://abhishek249.github.io/tts-studio)
2. Paste your **ElevenLabs API key** → click **Connect**
3. Your voices load automatically — assign each character a voice
4. Write or paste your script using `[character]` tags
5. Click **Generate all segments**
6. Download numbered MP3s → import into InShot / CapCut

---

## 📝 Script Format

Simple tag-based format — one line per dialogue:

```
[narrator] यह उस महान काल की बात है — इस अवसर्पिणी के चतुर्थ आरक के अन्तिम समय की।

[jambu] [reverent] हे भगवन्! अन्तकृदशा में किस विषय का प्रतिपादन किया है?

[sudharma] [calm] हे जम्बू! प्रथम वर्ग में दस अध्ययन हैं — गौतम, समुद्र, सागर, गम्भीर...

[gautam] [emotional] हे प्रभो! मैं श्रमण दीक्षा अंगीकार करूँगा।

[arishtanemi] [divine] वत्स! जाओ। माता-पिता से आज्ञा लो।

[dharini] [tearful] जाओ बेटा। मोक्ष-मार्ग पर जाओ।
```

### Character tags
Click any character chip to insert their tag at cursor position.

### Emotion tags
`[भावुक]` `[शांत]` `[रोते हुए]` `[धीरे]` `[गर्जना]` `[whisper]` `[excited]` `[reverent]`

---

## 📁 Output

Each segment downloads as a numbered MP3:

```
01_narrator.mp3
02_jambu.mp3
03_sudharma.mp3
04_narrator.mp3
05_gautam.mp3
...
```

Import all into InShot → place each clip on the timeline → sync with AI-generated scene images → done.

---

## 👥 Characters & Voice Mapping

Character → voice assignments are stored in [`characters.json`](./characters.json) in this repo — shared across all collaborators, no browser storage.

```json
{
  "characters": [
    {
      "id": "narrator",
      "name": "Narrator",
      "voiceId": "o76sLDABsemuKZKvLV1a",
      "voiceName": "Katha vaachak"
    },
    {
      "id": "sudharma",
      "name": "Sudharma",
      "voiceId": "S6fdx8hmfwbuJn0oSUXj",
      "voiceName": "Acharya Sudharma Swami Ji"
    }
  ]
}
```

To update: change voice in the sidebar → click **Save to repo** → enter GitHub token.

---

## 🎛️ Voice Settings

Per character, adjustable:

| Setting | What it does |
|---|---|
| **Stability** | Consistency of voice (higher = more consistent) |
| **Similarity boost** | How closely it matches the original voice |
| **Style** | Expressiveness / emotion intensity (v3 only) |

---

## 🤖 Models

| Model | Best for |
|---|---|
| **v3 alpha** | Hindi — best emotion & expressiveness ⭐ |
| **Multilingual v2** | Production quality, stable |
| **Turbo v2.5** | Faster generation, lower cost |

---

## 🗂️ Project Context

This studio is part of a larger project to create an AI-generated animated movie based on **Varga 1 of the Antgaddashang Sutra** (8th Jain Agama) — the story of Gautam Kumar's journey to liberation.

**Pipeline:**
```
TTS Studio (audio) → Ideogram AI (scene art) → InShot (edit) → YouTube
```

**Related repo:** [gautam-movie-audio](https://github.com/Abhishek249/gautam-movie-audio)

---

## 🛠️ Tech

- Vanilla HTML/CSS/JS — zero dependencies, zero build step
- [ElevenLabs API](https://elevenlabs.io/api) for TTS
- [Material Design 3](https://m3.material.io/) design system (Google Fonts + Icons)
- Hosted on GitHub Pages

---

## 📄 License

MIT
