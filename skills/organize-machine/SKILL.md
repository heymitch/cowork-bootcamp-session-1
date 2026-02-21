---
name: Organize Machine
description: Your first agent skill. Organize files on your computer using GTD principles. Triggers — "organize my machine", "organize my computer", "scan my screenshots", "organize my screenshots", "sort my files", "organize my downloads", "GTD my files", "create folder structure", "organize my folders", "set up my file system", "weekly review", "weekly cleanup"
user-invocable: true
---

# Organize Machine

## Routing

Route to the right sub-skill based on intent:

| User Says | Sub-Skill to Run |
|-----------|-----------------|
| "organize my machine" / "organize my computer" | Run the **Full Flow** (see below) |
| "scan screenshots" / "organize screenshots" / "clean up screenshots" | `../screenshot-scanner/SKILL.md` |
| "sort my files" / "organize downloads" / "GTD my files" / "clean up downloads" | `../gtd-file-sorter/SKILL.md` |
| "create folder structure" / "organize my folders" / "set up my file system" | `../folder-architect/SKILL.md` |
| "weekly review" / "weekly cleanup" / "run my weekly review" | `../weekly-review/SKILL.md` |

## Full Flow (First Time)

When the user says "organize my machine" or this is their first time, run these in order:

1. **Screenshot Scanner** — Warm them up by organizing screenshots. Quick win.
2. **GTD File Sorter** — Expand to all files on Desktop and Downloads.
3. **Folder Architect** — Build a folder structure that fits their workflow.

After all three, tell them:

> "Your machine is organized. To keep it this way, say 'weekly review' once a week. Five minutes keeps the chaos from coming back."

## First Time?

If you can't tell whether the user has run this before, ask:

> "Is this your first time organizing with me? I can do the full walkthrough, or just run a quick cleanup."

- Full walkthrough = Full Flow above
- Quick cleanup = Weekly Review

## Rules

- **Route, don't execute.** This skill picks the right sub-skill and hands off. The sub-skills have the detailed instructions.
- **When in doubt, ask.** If the user's request is ambiguous, show the options and let them choose.
- **Plain language only.** Third-grade reading level. Always.
