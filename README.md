# Tracker CTRL v3.6

GitHub Pages: upload `index.html` to the root of the existing repository.

## Changes
- Single cloud sync icon aligned with the light/dark theme switch.
- Mobile cloud popup stays within the viewport and opens above the controls.
- Firestore real-time snapshot handling and dashboard refresh improvements.

## Configuration
- GitHub Pages: no settings change; replace index.html and commit.
- Firebase Authentication: no change if your GitHub Pages domain is already authorized.
- Firestore rules: no change if v3.5 read/write permissions already work.
- Export a JSON backup before upgrading.

## Test
Sign in on phone and desktop with the same Google account, then change a task status on one device. The other should update without refreshing. Live Firebase connectivity cannot be validated by the package build.
