---
name: GTD File Sorter
description: Sort files in Downloads and Desktop into GTD buckets — Action, Reference, Trash, Waiting. Triggers — "sort my files", "organize my downloads", "GTD my files", "clean up downloads"
user-invocable: false
---

# GTD File Sorter

You scan the user's Downloads and Desktop folders, classify every file into a GTD bucket (Action, Reference, Trash, or Waiting), and move them to the right place.

## How to Run

The user says something like "sort my files" or "organize my downloads" or "GTD my files."

Start by saying:

> "I'm going to look through your Downloads and Desktop. For every file, I'll decide if it's something you need to act on, something to keep for reference, something to trash, or something you're waiting on. I'll show you the full plan before I move anything."

## Steps

### 1. Scan Both Folders

Search `~/Downloads` and `~/Desktop` for all files (not directories).

Report what you find:
- Total file count per folder
- File types breakdown (PDFs, images, documents, installers, etc.)
- Oldest and newest files
- Total size if notable (e.g., "Your Downloads folder is 4.2 GB")

### 2. Classify Every File

For each file, assign it to a GTD bucket:

| Bucket | Meaning | Action |
|--------|---------|--------|
| **Action** | Active project, needs your attention | Move to a project folder |
| **Reference** | Useful later, not urgent now | Move to reference folder |
| **Trash** | Old, duplicate, or useless | Suggest deletion |
| **Waiting** | Blocked on someone else | Flag it, note who |

Use the decision tree and heuristics in the reference file to classify files. When in doubt, ask the user.

### 3. Show the Full Plan

Present your plan as a table:

| File | Type | Age | Bucket | Destination |
|------|------|-----|--------|-------------|

Group by bucket so the user can see all Trash together, all Action together, etc.

Call out:
- Anything you're not sure about
- Large files worth knowing about (> 100MB)
- Duplicates you found

Wait for approval.

### 4. Work in Batches

- Move **10 files at a time**
- After each batch, report what you did:

> "Moved 10 files. 4 to Action, 3 to Reference, 3 flagged as Trash. Want me to keep going?"

- For Trash items: collect them into a list and ask once: "Can I delete these?"

### 5. Handle Duplicates

If you find duplicate files (same name with (1), (2), etc., or identical content with different names):
- Keep the newest version
- Flag the duplicates as Trash
- Show the user which ones you'd delete

## References

Use `../organize-machine/references/gtd-buckets.md` for classification rules, file type heuristics, and edge case handling.

## Rules

- **Show the plan first.** Every time. No exceptions.
- **Never delete without explicit permission.** Suggest, list, and wait.
- **Work in batches of 10.** Check in between each batch.
- **Skip hidden files and system files.** Anything starting with a dot, anything in a system directory.
- **When in doubt, ask.** It's always better to ask than to move the wrong file.
- **Plain language only.** Explain what each file is in simple terms.
- **Flag large files.** Anything over 100MB gets called out.
- **Don't reorganize existing project folders.** Only sort loose files on Desktop and in Downloads.
