# Tracker CTRL v3.8

GitHub Pages: upload `index.html` to the existing repository root. No GitHub Pages or Firebase configuration changes are expected if v3.7 already worked.

## Changes
- Cloud sync connects automatically after Google sign-in and listens for Firestore changes.
- Edits save to Firebase and propagate to other signed-in devices.
- Initial empty cloud with local tasks requires one manual upload to prevent accidental data loss.
- In-app confirmation dialogs replace browser confirmation dialogs for manual cloud operations.
- A local pre-cloud backup is stored in localStorage before automatically loading cloud data. Export JSON backups separately for reliable recovery.

## Testing
Verify on two devices using the same Google account. Browser and live Firebase testing are not included in this build.
