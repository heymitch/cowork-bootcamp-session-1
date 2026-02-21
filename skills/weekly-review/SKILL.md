---
name: Weekly Review
description: Quick 5-minute weekly cleanup of Desktop and Downloads. Triggers — "weekly review", "weekly cleanup", "run my weekly review"
user-invocable: false
---

# Weekly Review

A fast, recurring cleanup. Scan Desktop and Downloads for new files since your last review, sort them using GTD buckets, and give a quick summary. Designed to run every week in under 5 minutes.

## How to Run

The user says "weekly review" or "weekly cleanup."

Start by saying:

> "Running your weekly review. I'll check what's new on your Desktop and Downloads since last time, sort it, and give you a summary. This should take about 5 minutes."

## Steps

### 1. Check Last Review Date

Look for `~/.weekly-review-log` file.
- If it exists, read the last review date from it.
- If it doesn't exist, this is the first review. Treat all files as new.

### 2. Scan for New Files

Search `~/Desktop` and `~/Downloads` for files modified or created since the last review date.

Quick summary:

> "Since your last review on [date], you've got X new files on Desktop and Y new files in Downloads."

If no new files: "Your Desktop and Downloads are clean. Nothing new since [date]. Nice work." Then update the log and stop.

### 3. Classify New Files

For each new file, assign a GTD bucket:
- **Action** — active project, needs attention
- **Reference** — useful but not urgent
- **Trash** — old, duplicate, or junk
- **Waiting** — blocked on someone else

Show a quick table:

| File | Bucket | Suggested Action |
|------|--------|-----------------|

### 4. Sort

After approval, move files to their destinations.
- Work in batches of 10 if there are many files.
- For small batches (under 10), do them all at once.

### 5. Summary

After sorting, give a quick recap:

> "Weekly review done.
> - X files sorted into Action
> - X files moved to Reference
> - X files flagged as Trash
> - X files marked as Waiting
>
> Total time: about X minutes. See you next week."

### 6. Update the Log

Write the current date to `~/.weekly-review-log`:

```
last_review: 2026-02-20
files_sorted: 12
action: 4
reference: 5
trash: 2
waiting: 1
```

This file is how you know when the last review happened.

## References

Use `../organize-machine/references/gtd-buckets.md` for classification rules.

## Rules

- **Speed matters.** This should feel fast. Don't over-explain.
- **Show the plan, get approval, then sort.** Same pattern as always.
- **Never delete without permission.** Flag Trash items and ask.
- **Skip hidden files and system files.**
- **If there are zero new files, say so and stop.** Don't waste the user's time.
- **Always update the log file** at the end, even if there was nothing to sort.
- **Plain language only.** Quick and friendly.
