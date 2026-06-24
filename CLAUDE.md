# CLAUDE.md — AuraTone Architecture Showcase

## Repository Overview

This is a **documentation-only** repository showcasing the architecture of AuraTone AI, a proprietary DJ/production workstation. **No source code is included** — the actual application source is private and proprietary (© 2026 Kevin Kuck). This repo serves as a public architecture write-up for portfolio and reference purposes.

## What AuraTone AI Does

AuraTone is an AI-assisted audio mastering and harmonic-mixing engine that:
- Analyzes audio tracks (key, BPM, energy detection)
- Masters audio to loudness targets (LUFS normalization, high-pass filtering, artifact cleanup)
- Builds harmonically coherent sets using Camelot-wheel key matching (±1 step)
- Provides Gemini AI assistance on top of the DSP core
- Supports Traktor Pro import/export (`.nml`)

## System Architecture (Reference)

The proprietary system uses a hybrid TypeScript + Python stack:

| Layer | Technology | Purpose |
|---|---|---|
| Frontend | React, Vite, Tailwind, recharts | Workstation UI, waveform/Camelot visualization |
| API | Node.js, Express | Upload handling, job orchestration |
| DSP Engine | Python, librosa, ffmpeg | Audio analysis, mastering, harmonic set building |
| AI | Google Gemini (`@google/genai`) | Guidance and automation |
| Infrastructure | Firebase | Backend services |
| Distribution | Native macOS app packaging | Desktop delivery |

## Repository Structure

```
/
├── README.md          # Architecture showcase documentation (Mermaid diagrams, capability tables)
└── CLAUDE.md          # This file — AI assistant guide
```

## Working in This Repository

### What belongs here
- Architecture documentation and diagrams
- Capability descriptions and engineering notes
- Demo placeholders (screenshots, videos)
- Portfolio-facing content describing the system design

### What does NOT belong here
- Source code from the proprietary AuraTone application
- API keys, credentials, or environment configurations
- Internal implementation details that would expose proprietary logic

### Conventions
- The README uses centered HTML layout with badge shields for visual presentation
- Mermaid diagrams are used for architecture visualization
- Content is written in English; some placeholder comments may be in German
- Author attribution: Kevin Kuck / KKI

### Branching
- `master` is the default branch
- Feature branches follow the pattern `claude/<description>`

## Key Domain Concepts

- **Camelot Wheel**: A key-mixing system where compatible keys are ±1 position on the wheel, enabling smooth harmonic transitions between tracks
- **LUFS**: Loudness Units Full Scale — the broadcast/club standard for loudness normalization
- **High-pass filter**: Typically 30 Hz cutoff to remove sub-bass rumble and artifacts
- **librosa**: Python library for audio/music analysis (key detection, BPM, spectral features)
- **NML**: Traktor Pro's playlist/collection XML format for DJ software interoperability

## For AI Assistants

- This repo is documentation only — do not attempt to run, build, or test code
- Edits should maintain the existing README formatting style (centered badges, Mermaid diagrams, emoji headers, tables)
- Respect the proprietary boundary: describe architecture and capabilities, never fabricate implementation code
- The author is Kevin Kuck; maintain proper copyright attribution
