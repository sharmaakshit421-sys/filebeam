# FileBeam — Presentation Script

**Audience:** General users, students, or team members who need to transfer files between devices.
**Duration:** ~8–10 minutes
**Slides:** 8

---

## Slide 1 — Title Slide

**Title:** FileBeam
**Subtitle:** Transfer Files Between Devices — Using GitHub

**Speaker Notes:**
> Good morning/afternoon everyone. Today I want to introduce you to a tool called FileBeam. If you have ever needed to move a file from your work laptop to your personal computer, or from a restricted university or office machine to your phone, you know how frustrating it can be. USB drives get blocked, email attachments have size limits, and cloud storage sites are often blocked too. FileBeam solves this problem in a completely different way — by using your own GitHub repository as a secure, private bridge between devices. Let me walk you through how it works.

---

## Slide 2 — The Problem

**Title:** Why Is File Transfer So Hard?

**Visual:** Split screen showing common barriers

**Key Points on Slide:**
- USB drives blocked in many workplaces and schools
- Cloud storage (Google Drive, Dropbox) often restricted
- Email attachments limited to 25MB
- Sharing links is insecure — anyone with the link can access
- "AirDrop" only works between Apple devices

**Speaker Notes:**
> Think about your own experience. You finish work on a document at the office, and you want to take it home to finish the last bit. You plug in a USB — blocked. You try to upload to Google Drive — blocked. You email it to yourself — attachment too large. You could share a public link, but then that file is accessible to anyone who has that link — which might include sensitive information. These aren't edge cases. These are everyday problems for students, professionals, and anyone who works across multiple environments. That's exactly why FileBeam exists.

---

## Slide 3 — The Solution

**Title:** How FileBeam Works

**Visual:** Simple architecture diagram — Device A → GitHub Repo → Device B

**Key Points on Slide:**
- Open-source, single-file web app
- Uses your private GitHub repository as the transfer bridge
- Upload from Device A → files stored in your repo
- Download from Device B → grab files from the same repo
- Zero third-party servers — everything goes through GitHub

**Speaker Notes:**
> Here's the big idea. FileBeam doesn't need its own server. It doesn't store your files on someone else's cloud. Instead, it uses your own GitHub repository — the same place you already store code projects. You upload a file from your restricted device, and FileBeam pushes it directly into a folder in your GitHub repo using GitHub's API. Then, from your personal device, you open the same app, and you download that file right out of your repo. It's like having your own private, cloud-agnostic file transfer service. And because it's a single HTML file, there's nothing to install — it runs entirely in your browser.

---

## Slide 4 — Quick Setup

**Title:** Setup in 5 Minutes

**Visual:** Numbered steps

**Key Points on Slide:**
1. Create a new private repository on GitHub (e.g. `my-transfers`)
2. Go to Settings → Pages → set source to `main` branch, `/root` folder
3. Generate a Personal Access Token with `repo` scope
4. Open the FileBeam URL, enter your credentials, and click Save
5. You're ready to go!

**Speaker Notes:**
> Setting up FileBeam is incredibly simple — it takes about five minutes. First, you create a new private repository on GitHub. Just give it a name like "my-transfers" and make it private. Second, you enable GitHub Pages on that repository — I'll show you exactly where to click. Third, you generate a personal access token — this is like a password that lets the app talk to your repo on your behalf. You only see this token once, so copy it and save it somewhere safe. Fourth, you open the FileBeam URL in your browser, paste in your username, repo name, and token, and hit Save. And that's it. Your credentials are saved in your browser's local storage — they never leave your device, and they're never sent to any third party.

---

## Slide 5 — Upload Tab

**Title:** Uploading Files

**Visual:** Screenshot mockup of the upload interface

**Key Points on Slide:**
- Drag and drop or click to browse
- Supports any file type — documents, images, videos, archives
- Maximum file size: 100MB (GitHub limit)
- Custom folder naming — organize uploads into folders
- Progress bar and status for each file
- Auto-retry on failed uploads

**Speaker Notes:**
> Once you're set up, uploading files is as simple as dragging and dropping them into the browser. You can also click to browse your files. FileBeam supports any file type — PDFs, Word documents, images, videos, zip archives, anything. Each file gets a timestamp prefix so nothing ever overwrites another. You can also organize your uploads into custom folders — maybe separate folders for "work", "photos", "backup" — whatever makes sense for your workflow. If an upload fails — maybe due to a network hiccup — FileBeam automatically retries up to three times, so you don't have to start over manually. You'll see a progress bar and status indicator for each file, so you always know what's happening.

---

## Slide 6 — My Files Tab

**Title:** Managing Your Files

**Visual:** Screenshot mockup of the files list

**Key Points on Slide:**
- View all uploaded files with size and type
- Search and filter by filename
- One-click download
- Copy shareable download link
- Delete files with confirmation dialog
- Refresh to sync with your repository

**Speaker Notes:**
> On the other side — your personal device — you open the same FileBeam URL and switch to the "My Files" tab. Here you'll see every file you've uploaded, organized with file type icons, sizes, and folder labels. You can search by filename if you have a lot of files. Each file has three actions: Download — which saves it directly to your device; Copy Link — which copies a shareable URL you can paste into a chat or email; and Delete — which removes the file from your GitHub repo, with a confirmation dialog so you don't accidentally delete anything. Hit Refresh at any time to sync with the latest state of your repository.

---

## Slide 7 — Security & Privacy

**Title:** Why It's Secure

**Key Points on Slide:**
- Your token is stored only in your browser's localStorage
- Token is never shared with third parties
- Repository is private — only you can access it
- No server logs, no tracking, no analytics
- GitHub's infrastructure handles file storage securely
- Clear Config button wipes all credentials instantly

**Speaker Notes:**
> One of the biggest concerns with any file transfer tool is security. Let me be clear about how FileBeam handles this. First, your personal access token — the key that gives the app permission to interact with your repo — is stored exclusively in your browser's local storage. It never leaves your device. It's not sent to me, it's not sent to any server, it's not tracked anywhere. Second, your repository is private, which means only people with your GitHub credentials can see what's inside. Third, GitHub itself provides enterprise-grade security for file storage — your files benefit from the same infrastructure that hosts millions of private code repositories. And finally, if you ever want to remove everything, there's a "Clear Config" button that wipes all your credentials from the browser in one click.

---

## Slide 8 — Wrap Up

**Title:** FileBeam at a Glance

**Key Points on Slide:**
- Free, open-source, single HTML file
- Works on any device with a browser
- No installation, no accounts on third-party services
- Ideal for: restricted laptops, cross-device work, quick backups
- Repo: `github.com/sharmaakshit421-sys/filebeam`
- Live URL: `https://sharmaakshit421-sys.github.io/filebeam` (after enabling Pages)

**Speaker Notes:**
> To summarize, FileBeam is a free, open-source tool that turns your GitHub repository into a personal file transfer service. It's a single HTML file — no installation, no accounts on third-party services, no hidden costs. It works on any device with a web browser. It's perfect for students working between campus and home, professionals in restricted work environments, or anyone who needs a quick, secure way to move files around. The entire project is hosted on GitHub at `github.com/sharmaakshit421-sys/filebeam`, and once you enable GitHub Pages on the repository, you can access it from any browser. Thank you — I'm happy to take any questions.

---

## Q&A Prep

**Anticipated Questions and Answers:**

**Q: What's the maximum file size?**
A: 100MB per file, which is GitHub's API limit for content uploads. For larger files, you'd want to use a dedicated file transfer service.

**Q: What happens if my repository gets full?**
A: GitHub has generous storage limits. You can also delete old files through the app or directly on GitHub to free up space.

**Q: Can multiple people use the same repo?**
A: Yes, but only if they share the same GitHub credentials. This is meant for personal use. For team sharing, consider granting collaborators access to the repo.

**Q: Is this safe for sensitive files?**
A: As long as your repository is private and your device is secure, yes. However, be mindful that GitHub employees with admin access could theoretically see private repo contents. For highly sensitive data, use encrypted file transfer tools.

**Q: Does it work offline?**
A: The upload feature requires an internet connection to reach GitHub's API. However, the downloaded files remain on your device after download.
