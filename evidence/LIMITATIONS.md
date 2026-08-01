# AuraTone AI — Evidence Limitations & Disclosure

To ensure complete transparency for external reviewers and recruiters, this document lists all explicit scope limitations and unverified claims regarding **AuraTone AI Desktop**.

---

## 1. Scope Disclosures

1. **Private Implementation**: The complete Rust/Tauri frontend, audio playback engine, and proprietary algorithms reside in a private repository (`KKEEY92/AuraTone-AI-by-KKEEy`).
2. **No Public Signed Binary**: There is currently no publicly downloadable, Apple-signed, or notarized macOS `.dmg` / `.app` binary release.
3. **No Public Notarization Evidence**: Apple Developer notarization tickets are managed internally and are not published in public evidence.
4. **Unverified Claims**:
   - **120 Hz Waveform Rendering**: The 120 Hz rendering performance claim is an internal target and is not publicly benchmarked or independently verified in this repository.
   - **SLSA Level 3**: Supply-chain Levels for Software Artifacts (SLSA) Level 3 compliance is an internal CI goal and has not been publicly certified.
5. **Codebase Versioning**: The private codebase identifies as version `2.0.0`, whereas the latest audited Git release tag is `v1.3.0`.
6. **Component vs. Product Validation**: The evidence provided in this package demonstrates specific component schemas and DSP outputs; it does not independently prove full production readiness of a commercial product.
