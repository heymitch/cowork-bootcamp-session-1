---
name: Organize Machine
description: Your first agent skill. Organize files on your computer using GTD principles. Starts with screenshots, expands to your whole desktop and downloads.
version: 1.0.0
---

# Organize Machine

> **This is your first real skill.** It proves that your agent can DO things on your computer — not just talk about them.

> **How to run:** Tell your agent "Organize my machine"

See [Cowork Capabilities](../../products/cowork-bootcamp/cowork-capabilities.md) for what your agent can and can't do.

---

## Instructions for the Agent

You are running a file organization skill. Work in phases. Use plain, friendly language — third-grade reading level. Explain what you're about to do before you do it. **Never move, rename, or delete anything without showing your plan and getting a thumbs up first.**

Start by saying:

> "Let's organize your computer. I'm going to look at what's on your Desktop and Downloads, then help you sort through it. I'll show you a plan before I touch anything. You're in control the whole time. Ready?"

---

## Phase 1: The Screenshot Warm-Up

This is where you prove an agent is different from a chatbot. You're not giving advice — you're doing the work.

1. **Scan the Desktop** for screenshots and images (`.png`, `.jpg`, `.jpeg`, `.gif`, `.webp`, `.heic`)
2. **Show the user:**
   - Total count of screenshots/images found
   - Date range (oldest to newest)
3. **Focus on the last 14 days.** For each screenshot:
   - Look at it and describe what it shows
   - Suggest a short, clear filename
   - Suggest a folder it belongs in — or flag it for deletion
4. **Group similar screenshots together** (same app, same topic, same project)
5. **Show the full plan.** Wait for approval.
6. **Organize 10 files** as a preview. Then stop and check in:

> "Here's what I did with the first 10. Want me to keep going with the rest?"

---

## Phase 2: The Full GTD Sweep

Now go beyond screenshots. This is where the real value hits.

### Expand to Downloads and Documents

Scan `~/Downloads` (this is the disaster zone for most people). For every file, decide which bucket it falls into:

| Bucket | What it means | What to do |
|--------|--------------|------------|
| **Action** | Part of an active project | Move to a project folder |
| **Reference** | Useful but not urgent | Move to reference folder |
| **Trash** | Old, duplicate, or irrelevant | Suggest deletion (never auto-delete) |
| **Waiting** | Needs someone else's input | Flag it and move on |

### Create a Simple Folder Structure

If the user doesn't have an organized folder system, suggest this:

```
~/Organized/
├── Projects/    ← active work lives here
├── Reference/   ← useful stuff you might need later
└── Archive/     ← done but worth keeping
```

Ask before creating any folders. Some people already have a system they like.

### Work in Batches

- Organize **10 files at a time**
- After each batch, show what you did and ask: "Keep going?"
- **Never delete anything without explicit permission** — always say "I recommend deleting these" and wait

---

## Phase 3: The Habit

After organizing, tell the user:

> "Nice work. Your Desktop and Downloads are clean. Here's the thing — they'll get messy again. That's normal.
>
> Run this skill once a week as your 'weekly review.' Just say 'organize my machine' and I'll handle it. Five minutes a week keeps the chaos from piling up.
>
> This is what a skill is. You didn't Google how to organize files. You didn't watch a tutorial. You told your agent to do it, and it did. That's the difference."

---

## Rules

- **Show the plan first.** Always. No exceptions.
- **Never delete without permission.** Suggest, don't execute.
- **Work in batches of 10.** Check in between each batch.
- **Plain language only.** If a 9-year-old wouldn't understand it, rewrite it.
- **Be encouraging.** This is their first time watching an agent act on their files. Make it feel good.
- **Skip hidden files and system files.** Only touch user-created content.
- **If something looks important and you're not sure, ask.** Better to ask than to move the wrong thing.
