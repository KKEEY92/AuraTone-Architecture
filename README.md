<div align="center">

<img src="https://img.shields.io/badge/AuraTone_AI-Architecture_Showcase-1DB954?style=for-the-badge" alt="AuraTone"/>
<img src="https://img.shields.io/badge/TypeScript-React-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
<img src="https://img.shields.io/badge/Python-DSP-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python DSP"/>
<img src="https://img.shields.io/badge/Gemini-AI-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini"/>

<br/>

# 🎚️ AuraTone AI — Architecture Showcase

### AI-assisted audio mastering & harmonic-mixing engine

*Public architecture write-up of a proprietary system — how AuraTone analyzes,
masters and harmonically sequences tracks. **No source code included.***

</div>

> 🔒 **Source code is private & proprietary.** Documentation only.
> © 2026 Kevin Kuck — All Rights Reserved. Demo / access on request.

---

## 📋 What is AuraTone AI?

AuraTone is a **DJ / production workstation**: it analyzes audio (key, BPM, energy),
masters it to loudness targets, and builds **harmonically coherent sets** — a software
replacement for hardware analysis/mastering workflows, with Gemini assistance on top.

## 🏗️ System Architecture

```mermaid
graph TB
    subgraph UI["🖥️ Frontend (React / Vite)"]
        APP["Workstation UI"]
        VIZ["Waveform / Camelot wheel (recharts)"]
    end
    subgraph API["⚙️ Node / Express API"]
        UP["Upload / job orchestration"]
    end
    subgraph DSP["🐍 Python DSP Engine"]
        ANA["Analysis — key / BPM / energy (librosa)"]
        MAST["Mastering — LUFS / high-pass (ffmpeg)"]
        HARM["Harmonic set builder (Camelot ±1)"]
    end
    subgraph EXT["☁️ Services"]
        GEM["Gemini (@google/genai)"]
        FB["Firebase"]
    end
    APP --> UP --> DSP
    DSP --> ANA & MAST & HARM
    APP <--> GEM
    APP <--> FB
    DSP --> VIZ
```

## ✨ Capabilities

| Module | What it does |
|---|---|
| **Analysis** | Key, BPM and energy detection (librosa-based). |
| **Mastering** | Loudness normalization to a LUFS target, high-pass, artifact cleanup (ffmpeg). |
| **Harmonic mixing** | Camelot-style key flow (±1 step) → coherent sets/playlists. |
| **Interop** | Traktor Pro import/export (`.nml`). |
| **AI assist** | Gemini for guidance/automation around the DSP core. |
| **Delivery** | Web app **and** native macOS app launcher. |

## 🧰 Tech & APIs

**React + Vite + Tailwind** (UI) · **Express/Node** (API) · **Python DSP** (librosa, ffmpeg) ·
**Google Gemini** (`@google/genai`) · **Firebase** · **recharts** (visualization) ·
native macOS app packaging.

## 🎯 Engineering Notes

- **Hybrid TS + Python**: React/Express front, Python for the heavy DSP — clean separation of UI and signal processing.
- **Loudness-correct mastering** targeting broadcast/club LUFS levels with a 30 Hz high-pass and artifact removal.
- **Harmonic coherence** enforced algorithmically (Camelot wheel) for smooth transitions.

## 🎬 Demo

> _Placeholder — Demo-Video / Screenshots folgen._
> <!-- ![AuraTone UI](docs/auratone-ui.png) -->

## 📄 License & Copyright

**© 2026 Kevin Kuck — All Rights Reserved.** Architecture documentation only; the AuraTone
source code is proprietary and not included here.

<div align="center"><sub>Built by Kevin Kuck · KKI</sub></div>
