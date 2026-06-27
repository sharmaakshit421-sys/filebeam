# FileBeam

A single-file, GitHub-powered file transfer tool. Upload files from any device → download from anywhere using your private GitHub repository as the backend.

## Quick Setup

1. **Fork or clone** this repo, or create your own
2. Open `index.html` in your browser, or serve it via GitHub Pages
3. Enter your GitHub credentials and start transferring files

## How It Works

- Files are uploaded directly to your GitHub repository via the GitHub API
- A personal access token with `repo` scope is required (stored only in your browser's localStorage)
- Files are stored in a configurable folder (default: `transfers/`)
- Maximum file size: 100MB per file (GitHub limit)

## Features

- Drag & drop file upload
- Custom folder organization
- Copy/download/share links
- Search and filter files
- Dark/light mode toggle
- Auto-retry on upload failure
- Confirmation dialogs for deletions
- Connection testing

## GitHub Pages Deployment

To serve FileBeam via GitHub Pages:

1. Push this repo to your GitHub account
2. Go to **Settings → Pages** in your repo
3. Set Source to branch `main`, folder `/root`
4. Your app will be available at `https://yourusername.github.io/filebeam`

> **Note:** GitHub Pages only works with public repositories. For private repos, host the file locally or on any static hosting.
