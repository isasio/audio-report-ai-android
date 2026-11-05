# Audio Report AI 0.1.0 — bundled offline build

Website: https://isasio.github.io/audio-report-ai-android/  
Privacy policy: https://isasio.github.io/audio-report-ai-android/privacy.html  

Self-contained Android APK with the on-device models included:

- LFM3-1.7B QAD Q4_0 GGUF for report drafting
- whisper tiny GGML model for transcription

## Install

1. Download the APK.
2. Allow installation from your browser/file manager if prompted.
3. Install and open the app.
4. Wait for the one-time model preparation screen.
5. Create a session and start recording or importing audio.

Requires Android 10 or newer and about 3 GB of free storage. The APK is ~1.1 GB;
first launch copies the models into app-private storage.

## Privacy

No account, ads, analytics, telemetry, or `INTERNET` permission. Audio,
transcripts, reports, modes, and models stay in app-private storage unless you
explicitly export through the system file picker.

## Important

- This is a documentation aid, not a medical device. Reports remain drafts until
  a qualified human reviews and approves them.
- The bundled whisper model is the small `tiny` model; transcription quality is
  limited. You can import a better whisper.cpp model from device storage.
- LFM3 is distributed under the LFM Open License v1.0, including its
  commercial-use threshold. See `THIRD_PARTY_NOTICES.txt` and the license files
  in `LICENSES/`.
- The APK is signed with the project GitHub release key. Uninstall any older
  build signed with a different key before installing this APK.
