# Support and Troubleshooting

## Which build should I install?

- **GitHub bundled APK:** self-contained, includes LFM3 and whisper tiny. Large
  download and first-launch copy. This is the only distribution channel.

Do not mix builds signed with different keys. Uninstall the old app before
switching channels; this removes its local sessions and reports.

## The APK is about 1.1 GB. Why?

The APK contains:

- LFM3-1.7B QAD Q4_0 GGUF (~1.05 GB)
- whisper tiny GGML (~77 MB)

They are inside the APK so the app works fully offline after installation.

## How much free storage do I need?

About **3 GB**:

- ~1.1 GB for the installed APK;
- ~1.1 GB for the first-launch copy of the models into app-private storage;
- working space for audio and reports.

## First launch is taking a long time

The app copies both models from the APK into private storage once. Expect tens
of seconds on fast devices and several minutes on slow storage. Keep the screen
on and the app foregrounded. If it fails, free space and tap Retry.

## “App not installed” or “signature mismatch”

You have an existing build signed with a different key, for example:

- a previous GitHub APK signed with another key;
- a debug build.

Uninstall the existing app, then install the new APK. Uninstalling removes local
sessions, transcripts, reports, and imported models.

## Android warns about the APK

GitHub builds are signed by the project and distributed only through GitHub
Releases. Android may show a standard sideload warning. Only install builds from
the official release page:

https://github.com/isasio/audio-report-ai-android/releases

Verify the SHA-256 before installing.

## How do I verify the download?

Compare the APK checksum with `SHA256SUMS.txt`:

```bash
sha256sum -c SHA256SUMS.txt
```

Expected current SHA-256:

```text
13da879f0af10e9a850100e59cb421869a99818c8a30daabe4c1fe544a0bdcac
```

On Windows PowerShell:

```powershell
Get-FileHash .\audio-report-ai-0.1.0-bundled.apk -Algorithm SHA256
```

## Transcription quality is poor

The bundled model is whisper **tiny**, which favours speed and size. Spanish
accuracy can be limited. You can import a larger whisper.cpp GGML model from
device storage; the app will use the imported model instead of the bundled one.

A larger model increases storage use and slows transcription.

## Can the app update itself?

No. The app has no `INTERNET` permission, so it cannot check for or download
updates. Download new releases manually from the GitHub Releases page.

## Does the app send my data anywhere?

No. There is no `INTERNET` permission, account, analytics, telemetry, ads, or
automatic upload. Audio, transcripts, reports, modes, and models stay in
app-private storage unless you explicitly export through the Android file
picker.

See [PRIVACY.md](PRIVACY.md).

## How do I delete my data?

- Delete audio, transcript, or reports from the session detail screen.
- Delete the whole session to remove its audio, transcript, reports, and
  evidence.
- Uninstall the app to remove all app-private data.

The developer has no server copy and cannot delete data remotely.

## Reports are only drafts

This is intentional. Every report must be reviewed and explicitly approved by a
human. The app does not diagnose or treat and is not a medical device.

## Can I use the app in airplane mode?

Yes. Core recording, import, transcription, report generation, and export work
offline.

## How do I report a bug?

Open an issue here:

https://github.com/isasio/audio-report-ai-android/issues

Include the app version, Android version, device model, and steps to reproduce.

**Never attach audio, transcripts, reports, patient names, or other clinical
data.** Use synthetic examples. For sensitive details, describe the problem
without the content.

## Why is PDF export not available?

PDF and richer report editing are planned but not part of 0.1.0. Current export
formats are TXT and JSON.

## License questions

The APK includes LFM Open License v1.0 and MIT license texts, plus attribution
notices. See:

- [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)
- [LICENSES](LICENSES)

The LFM license includes a commercial-use threshold. Review it before commercial
distribution or deployment.
