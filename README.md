# Tracker CTRL v3.2

A self-contained task tracker with Ash and Wifey, task reporting, and light/dark modes.

## Publish on GitHub Pages

1. Create a public GitHub repository (for example `Tracker-CTRL`).
2. Upload **the contents of this folder** to the repository root, including `index.html`.
3. Open repository **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, then Save.
4. Wait for deployment, then open `https://YOUR-USERNAME.github.io/Tracker-CTRL/`.

## Data and privacy

Task data is stored in your browser's localStorage, not on GitHub. GitHub Pages is public: do not put passwords or private task data directly in `index.html` or commit backups to the repository. Different devices/browsers do not sync automatically. Use the tracker Export/Import feature to move data manually. Keep backups before replacing the site.

## Local use

Open `index.html` in a modern browser, or serve the folder using `python3 -m http.server 8000` and open `http://localhost:8000`.

## What's new in v3.2

- View Report preview and image output follow the global Light/Dark mode.
- GitHub Pages-ready `index.html`, `.nojekyll`, `.gitignore`, and publishing instructions.
