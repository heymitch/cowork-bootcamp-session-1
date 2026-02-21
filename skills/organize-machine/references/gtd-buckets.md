# GTD Buckets — File Classification Rules

Every file on your computer belongs in one of four buckets. No exceptions.

## The Four Buckets

### 1. Action
**What it means:** This file is part of something you're actively working on right now.
**What to do:** Move it to the right project folder.

Examples:
- A contract you need to sign this week
- A design mockup for a client project due Friday
- A spreadsheet you update every day
- Meeting notes from yesterday's call
- A draft blog post you're still editing
- A proposal PDF with a client's name and a recent date

**Quick test:** "Will I touch this file in the next 7 days?" If yes, it's Action.

### 2. Reference
**What it means:** This is useful, but you don't need it right now. You might need it later.
**What to do:** Move it to a reference folder. Label it clearly so future-you can find it.

Examples:
- Tax documents from last year
- A recipe PDF you saved from the internet
- An insurance policy document
- Notes from a conference you attended
- A how-to guide you downloaded
- A template you use once a quarter
- A photo of your passport

**Quick test:** "Would I be annoyed if I deleted this and needed it later?" If yes, it's Reference.

### 3. Trash
**What it means:** This file has no future value. It's old, duplicate, or irrelevant.
**What to do:** Suggest deletion. Never auto-delete — always ask first.

Examples:
- Screenshots of a login screen from 6 months ago
- A file called "Untitled" with nothing useful in it
- Duplicate downloads (report.pdf, report (1).pdf, report (2).pdf)
- Old installers (.dmg, .exe) for apps you already installed
- Screenshots of error messages you already fixed
- Blurry photos or accidental screenshots
- Files in a language you don't read that you don't remember saving

**Quick test:** "If this file disappeared, would I ever notice?" If no, it's Trash.

### 4. Waiting
**What it means:** You need someone else to do something before this file is useful.
**What to do:** Flag it, note who you're waiting on, and move on. Check back later.

Examples:
- A contract you sent to a client for their signature
- A form that needs your accountant's review
- A shared document where you're waiting for feedback
- A quote from a vendor you haven't heard back from
- Application materials pending a decision

**Quick test:** "Is the next step someone else's job?" If yes, it's Waiting.

---

## Decision Tree

Ask these questions in order. Stop at the first "yes."

```
Is this file part of an active project I'm working on this week?
  → YES → Action

Am I waiting on someone else before I can use this?
  → YES → Waiting

Would I be upset if I lost this file?
  → YES → Reference

Has it been more than 30 days since I touched or needed this?
  → YES → Probably Trash (ask the user)

None of the above?
  → Reference (when in doubt, keep it)
```

---

## File Type Heuristics

Use these as starting guesses. Always confirm with the user.

| File Type | Age | Likely Bucket |
|-----------|-----|---------------|
| Screenshots (.png, .jpg) | < 7 days | Action — probably relevant to current work |
| Screenshots (.png, .jpg) | 7-30 days | Reference or Trash — ask the user |
| Screenshots (.png, .jpg) | > 30 days | Trash — unless it shows something important |
| PDFs with a person/company name | Any | Action or Reference — check if project is active |
| PDFs with generic names | > 30 days | Trash — likely forgotten downloads |
| Installers (.dmg, .exe, .pkg) | Any | Trash — already installed or not needed |
| Duplicate files (name (1), name (2)) | Any | Trash — keep the newest, suggest deleting copies |
| Zip files (.zip, .tar) | > 30 days | Trash — probably already extracted |
| Spreadsheets (.xlsx, .csv) | < 30 days | Action — likely current work |
| Spreadsheets (.xlsx, .csv) | > 90 days | Reference or Trash |
| Text/notes files (.txt, .md) | Any | Reference — unless clearly junk |
| Video files (.mp4, .mov) | > 30 days | Reference or Trash — large files worth asking about |
| Audio files (.mp3, .wav, .m4a) | Any | Reference — could be recordings worth keeping |

---

## Edge Cases

**Duplicates:** Keep the newest version. Suggest deleting the rest. If filenames are different but content looks the same, flag it and ask.

**Files you're not sure about:** When in doubt, classify as Reference. It's better to keep something you don't need than to delete something you do. Ask the user: "I'm not sure about this one — does [filename] mean anything to you?"

**Empty files:** Trash. Files with no content have no value.

**Very large files (> 100MB):** Always flag these. The user might not realize how much space they're taking up. Ask before moving or deleting.

**Files with no extension:** Open them and check. They might be important. If you can't tell what they are, ask.

**Hidden files (starting with .):** Skip these entirely. They're system files. Don't touch them.

**Files in progress:** If a file looks like it's being actively edited (recent modification date, application-specific temp files), leave it alone. Flag it as Action but don't move it until the user confirms.
