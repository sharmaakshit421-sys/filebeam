# FileBeam

A single-file, GitHub-powered file transfer tool. Upload files from any device → download from anywhere using your private GitHub repository as the backend.

**Live App:** [https://sharmaakshit421-sys.github.io/filebeam](https://sharmaakshit421-sys.github.io/filebeam)

---

## Quick Setup

1. Create a new private repository on GitHub (e.g. `my-transfers`)
2. Enable **GitHub Pages**: go to **Settings → Pages** → set Source to branch `main`, folder `/ (root)` → click Save
3. Generate a **Personal Access Token** with `repo` scope: [github.com/settings/tokens/new?scopes=repo&description=FileBeam](https://github.com/settings/tokens/new?scopes=repo&description=FileBeam)
4. Open the FileBeam URL (or the standalone `index.html`), enter your credentials, and click Save
5. You're ready to go!

---

## How It Works

Files are uploaded directly to your GitHub repository via the GitHub API. A personal access token with `repo` scope is required (stored only in your browser's `localStorage`). Files are stored in a configurable folder (default: `transfers/`). Maximum file size is 100MB per file (GitHub API limit).

---

## Features

Drag and drop file upload, custom folder organization, copy/download/share links, search and filter files, dark/light mode toggle, auto-retry on upload failure, confirmation dialogs for deletions, and connection testing.

---

## Deploying to GitHub Pages

To serve FileBeam via GitHub Pages:

1. Push this repo to your GitHub account
2. Go to **Settings → Pages** in your repo
3. Set Source to branch `main`, folder `/ (root)`
4. Your app will be available at `https://yourusername.github.io/filebeam`

> **Note:** GitHub Pages requires the repository to be public. For private repos, host the file locally or on any static hosting service.
