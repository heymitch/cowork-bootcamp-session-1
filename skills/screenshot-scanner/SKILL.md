---
name: Screenshot Scanner
description: Scan and organize screenshots on your Desktop. Triggers — "scan my screenshots", "organize my screenshots", "clean up screenshots"
user-invocable: false
---

# Screenshot Scanner

You scan the user's Desktop for screenshots and images, describe what each one shows, suggest better filenames, and organize them into the right folders.

## How to Run

The user says something like "scan my screenshots" or "organize my screenshots."

Start by saying:

> "I'm going to scan your Desktop for screenshots and images. I'll look at each one, tell you what it shows, and suggest where it should go. I won't move anything until you say so."

## Steps

### 1. Scan for Images

Search `~/Desktop` for files ending in: `.png`, `.jpg`, `.jpeg`, `.gif`, `.webp`, `.heic`

Report what you find:
- Total count
- Date range (oldest to newest)
- Breakdown by type if helpful (e.g., "14 PNGs, 3 JPGs")

### 2. Describe Each Image

For each screenshot or image:
- Look at it (you can read images)
- Write a one-sentence description of what it shows
- Suggest a clear, descriptive filename (e.g., `slack-error-message-feb-2026.png` instead of `Screenshot 2026-02-15 at 3.42.11 PM.png`)
- Classify it using GTD buckets (see references below)
- Suggest a destination folder

### 3. Group Similar Files

If you find multiple screenshots of the same app, topic, or project, group them together. Example:

> "I found 5 screenshots that all show your Figma project. I'd move them all to `Projects/website-redesign/screenshots/`."

### 4. Show the Plan

Present your full plan as a table:

| File | Description | New Name | Bucket | Destination |
|------|-------------|----------|--------|-------------|

Wait for approval before doing anything.

### 5. Work in Batches

- Organize **10 files at a time**
- After each batch, stop and check in:

> "Done with the first 10. Here's what I did. Want me to keep going?"

- If the user says stop, stop. No pushback.

## References

Use the GTD classification rules in `../organize-machine/references/gtd-buckets.md` to decide which bucket each file belongs in.

## Rules

- **Never move a file without showing the plan first.**
- **Never delete anything.** You can suggest deletion, but the user must confirm.
- **Skip hidden files** (anything starting with a dot).
- **Skip system files** and anything that looks like it belongs to macOS.
- **Work in batches of 10.** Always check in between batches.
- **If you can't tell what an image shows, say so.** Ask the user instead of guessing.
- **Plain language only.** No jargon, no technical terms unless the image itself is technical.
