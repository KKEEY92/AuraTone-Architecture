# AuraTone AI — DSP Validation Example & Pipeline Specification

## 1. Scope & Verification Target

This document specifies the technical design and output format of the **AuraTone AI DSP Subsystem**.  
The DSP subsystem performs audio signal processing, loudness estimation, tempo (BPM) detection, and harmonic key mapping for local digital audio files.

---

## 2. Technical Stack & Dependencies

- **Loudness Analysis**: Integrated FFmpeg `ebur128` filter engine computing Integrated LUFS, Loudness Range (LRA), and True Peak.
- **Audio Processing**: Python 3.12+ / NumPy / SciPy audio analysis modules.
- **Tauri Supervisor**: Rust-based process supervisor managing non-blocking asynchronous execution of the local DSP engine.
- **Input Formats**: WAV, MP3, FLAC, AAC, AIFF.
- **Output Schema**: JSON metadata formatted for DJ library indexing and Camelot wheel harmonic matching.

---

## 3. Sample Validation Output Structure

The analysis output maps audio features to standardized attributes:

| Feature | Algorithm / Tool | Unit / Standard |
|---|---|---|
| Integrated Loudness | FFmpeg `ebur128` | LUFS |
| Loudness Range | FFmpeg `ebur128` | LU |
| True Peak | FFmpeg `ebur128` | dBTP |
| Tempo (BPM) | Spectral Peak & Autocorrelation | BPM |
| Musical Key | Chromagram Peak Detection | Camelot Key (e.g., `4A`, `8B`) |

---

## 4. Known Boundaries

- This document presents a verified component example based on the private AuraTone DSP architecture.
- Full automated test suite execution requires access to the private repository test harness.
