# AuraTone AI Desktop — Public Technical Evidence & Architecture

> **Notice on Implementation Status:**  
> AuraTone AI Desktop is a native audio analysis and harmonic mixing application.  
> The full source code implementation is maintained in a private repository (`KKEEY92/AuraTone-AI-by-KKEEy`).  
> This public repository contains the architecture documentation, schema definitions, and sanitized technical evidence verifying selected DSP and analysis components.

---

## 1. Overview & Purpose

This directory provides verified, publicly accessible technical evidence for the **AuraTone AI Desktop** project without exposing proprietary source code, credentials, or internal infrastructure details.

A private technical demonstration or code audit is available upon direct request to the author.

---

## 2. Evidence Package Structure

- [`MANIFEST.yaml`](MANIFEST.yaml): Machine-readable index of evidence assets, versioning data, and audit scope.
- [`DSP_VALIDATION.md`](DSP_VALIDATION.md): Technical documentation of the Python/Rust DSP pipeline, LUFS measurement via FFmpeg `ebur128`, and key/BPM detection.
- [`LIMITATIONS.md`](LIMITATIONS.md): Transparent disclosure of unverified claims, missing public binaries, and private scope boundaries.
- [`SECURITY_AND_SCOPE.md`](SECURITY_AND_SCOPE.md): Audit records confirming the absence of credentials, personal data, and proprietary code in public assets.
- [`PUBLIC_CHANGELOG.md`](PUBLIC_CHANGELOG.md): Tracked milestones for public documentation and audited tags.
- [`examples/library_analysis.sample.json`](examples/library_analysis.sample.json): Sanitized sample JSON output produced by the AuraTone DSP engine.
- [`hashes/SHA256SUMS`](hashes/SHA256SUMS): SHA-256 cryptographic checksums for all public evidence files.

---

## 3. Disclosures & Boundaries

1. **Private Source Code**: The complete application build, Tauri/Rust shell, and proprietary DSP routines are not publicly licensed.
2. **Binary Releases**: There is currently no signed or notarized public macOS binary download available.
3. **Audit Baseline**: The underlying private codebase identifies as version `2.0.0`, while the latest audited Git release tag is `v1.3.0`.
4. **Verification Boundary**: This evidence package validates specific component capabilities (DSP schema, analysis outputs, architecture design), but does not constitute a full public open-source release.
