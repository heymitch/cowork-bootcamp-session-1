---
name: Folder Architect
description: Create a personalized folder structure based on how you work. Triggers — "create folder structure", "organize my folders", "set up my file system"
user-invocable: false
---

# Folder Architect

You help the user design and build a folder structure that fits their life. You ask a few questions, pick a template, customize it, and create the folders.

## Steps

### 1. Look at What Exists

Before asking questions, quickly scan:
- `~/Desktop` — what kinds of files are there?
- `~/Downloads` — what's been downloaded recently?
- `~/Documents` — is there already a structure here?
- Home directory — any existing project folders?

Use what you find to make smarter suggestions. Don't report everything you see — just use it as context.

### 2. Ask 3 Questions

Ask these one at a time. Keep it conversational.

**Question 1:** "What kind of work do you do? (Examples: freelancer, developer, writer, student, business owner — or just describe it in your own words)"

**Question 2:** "Do you work with clients or customers? If so, how many at a time?"

**Question 3:** "What's the biggest mess right now — what folder or area drives you crazy?"

### 3. Pick and Customize a Template

Based on the answers, pick the closest template from the reference file. Then customize it:
- Add folders specific to their work
- Remove folders they won't use
- Rename folders to match their language (if they call clients "accounts," use "Accounts")
- Keep it to 2-3 levels deep max — deeper than that and people stop using it

### 4. Show the Plan

Present the proposed folder structure as a tree:

```
~/Organized/
├── [folder]/
│   ├── [subfolder]/
│   └── [subfolder]/
...
```

Explain each top-level folder in one sentence.

Ask: "Does this look right? Anything you'd add or change?"

### 5. Create the Folders

After approval, create all folders using `mkdir -p`.

Report what you created:

> "Done. Created X folders. Your new structure is at ~/Organized/. Want me to start moving your existing files into it?"

### 6. Scan and Move

After creating folders, immediately scan Desktop, Downloads, and Documents for files that belong in the new structure. Show a move plan (file → destination), then execute on confirmation. Do not ask "want me to scan?" — just scan, show the plan, and ask "ready to move these?"

If a folder isn't accessible, say which one and offer to handle the rest.

## References

Use `../organize-machine/references/folder-templates.md` for starter templates and the "How to Pick" guide.

## Rules

- **Never create folders without approval.** Show the plan, wait for a yes.
- **Keep it simple.** 2-3 levels deep max. Fewer folders is better than more.
- **Use plain names.** No abbreviations, no codes, no dates in folder names (unless the user wants them).
- **Don't touch existing folder structures.** Build new ones alongside what exists. The user can migrate when ready.
- **If the user already has a good system, say so.** Don't rebuild for the sake of rebuilding.
- **Ask before migrating files.** Creating folders and moving files are separate steps.
- **Plain language only.** Explain everything like you're talking to someone who's never organized a computer before.
