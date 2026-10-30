# Privacy statement

Audio Report AI for Android is designed to process documentation data locally.

## What the app processes

- Audio recorded with the microphone
- Audio files imported through the Android system file picker
- Transcripts, including raw and corrected text and timestamps
- Speaker names and roles entered by the user
- Report drafts, versions, evidence links, approval status, and writing modes
- User-imported model files and app settings

## Where data goes

The app has **no `INTERNET` permission** and no account system. Audio,
transcripts, reports, modes, and models remain in app-private storage. The
developer does not receive them. There are no analytics, ads, telemetry, remote
logging, or crash-reporting SDKs.

Files leave the app only when the user explicitly chooses an export destination
through the Android system file picker. The destination app or service may have
its own privacy practices.

## Permissions

- **Microphone:** used only when the user starts a recording.
- **Notifications:** used for the visible recording foreground-service
  notification and its stop action.
- **Foreground service / microphone:** keeps a user-initiated recording active
  while the app is in the background.
- **Wake lock:** helps complete a recording without the device sleeping.
- **File access:** uses the Android system file picker for import/export; no
  broad storage permission is requested.

Permissions can be denied or revoked in Android settings.

## Retention and deletion

Data stays in app-private storage until the user deletes it. Sessions, audio,
transcripts, and reports can be deleted inside the app. Uninstalling the app
removes its private data.

## Medical disclaimer

This app is a documentation aid, not a medical device. It does not diagnose,
treat, or replace professional judgement. Reports are drafts until a qualified
person reviews and approves them.

## Contact

For privacy questions, open an issue in this repository.
