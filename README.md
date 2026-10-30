# Tracker CTRL v3.3 · GitHub Pages

## Publish
Upload `index.html` and `.nojekyll` to the repository root, then enable **Settings > Pages > Deploy from a branch > main > /(root)**.

## Firebase setup (REQUIRED)
1. Enable **Authentication > Google** in Firebase Console. Add `YOUR-USERNAME.github.io` under Authentication > Settings > Authorized domains.
2. Create Firestore in **production mode**. Copy the rules from `firestore.rules` into Firestore > Rules and click Publish. These rules include **both** tasks and settings. The older task-only rules will block synchronization of outlets/settings.
3. Open the published HTTPS website, expand **Cloud Sync** at the bottom-left and sign in with Google.
4. **Export JSON backup first** from Settings. On your first device, choose **Upload this device's tasks to cloud** only if the cloud is empty. On your second device, choose **Use cloud tasks on this device**.
5. Changes are synced to the same Google account. Other Google accounts get separate datasets. The app stays usable locally if signed out, but offline changes made while signed out are not automatically merged into the cloud.

## Important limitations
- Cloud sync needs internet and the Firebase CDN; opening the HTML with file:// may prevent Google sign-in. GitHub Pages HTTPS is recommended.
- Each task is a separate Firestore document. Rapid conflicting edits to the **same task** on two devices are last-write-wins. Outlet and profile settings are stored together and likewise last-write-wins.
- Avoid editing local tasks while waiting for initial cloud selection. Changes made while signed out are local only.
- Firestore offline persistence is not enabled in this version. When disconnected, local edits remain in this browser, but automatic reconnection merging is not guaranteed. Export a backup before major changes.
- Firebase web config is public by design. Never commit service-account credentials.
- Firestore security rules control data access. Anyone with access to your Google account can access your tracker data.
