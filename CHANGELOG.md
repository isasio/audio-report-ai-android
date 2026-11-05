# Changelog

All notable user-visible changes are recorded here.

## [Unreleased]

### Planned

- Physical-device M0 validation and documented device requirements
- Recommended whisper model for Spanish quality
- Audio focus/interruption handling
- Report editing, regeneration controls, and PDF export
- Release automation and CI checks
- Play internal/closed testing
- Play Asset Delivery evaluation for bundled models

## [0.1.0] — 2026-10-30

### Added

- Local audio recording with foreground-service notification
- SAF audio import, decoding, 16 kHz mono WAV normalisation, and playback
- On-device whisper.cpp transcription with user-importable models
- Timestamped raw transcript, corrections, review states, and retained original
  text
- Manual speaker names and roles
- LFM3-1.7B QAD Q4_0 report drafting with grammar-constrained JSON
- Per-section evidence validation and explicit human approval
- Report versioning and draft status
- Short, normal, long, and extensive report lengths
- Formal, clinical, executive brief, veterinary SOAP, and saved custom modes
- Collapsible transcript/report cards, clipboard copy, and TXT/JSON exports via
  SAF
- Self-contained GitHub APK with LFM3 and whisper tiny, plus first-launch model
  installation
- In-app model/third-party license notices
- Model-less Play AAB upload kit

### Known limitations

- whisper tiny has limited Spanish accuracy; larger models can be imported
- Physical-device M0 benchmarks are incomplete
- Audio focus/interruption handling is not implemented
- Report editing and PDF export are not implemented
- The ASR engine decision remains open
- LFM license/distribution and clinical reviews remain open
- No auto-update; the app has no `INTERNET` permission
- GitHub bundled APK is ~1.1 GB and requires about 3 GB free storage
