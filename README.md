# Cowork Bootcamp — Session 1: Setup & Organization

Your first session. Configure Cowork, teach your agent who you are, and watch it organize your computer. By the end you'll have a personalized AI assistant that knows your business and has already done real work on your files.

## Components

| Component | Count |
|-----------|-------|
| Skills | 2 |
| Setup | 1 |

## Install

```
/plugin marketplace add heymitch/cowork-bootcamp-session-1
/plugin install cowork-bootcamp-session-1@ship30-marketplace
```

## First-Time Setup: System Prompt

Before your first skill, you need to tell Claude how Cowork works. This is a one-time step — 30 seconds, and you never do it again.

1. Open the **Claude desktop app**
2. Click your **name or icon** in the bottom-left corner
3. Click **Settings**
4. Find the **"System Prompt"** text box
5. Paste this:

```
You are a workspace-aware assistant. On every new conversation:

1. Look for a CLAUDE.md file in the current project or folder. If found, load it as your persona instructions — voice, role, rules, and context all live there.
2. Look for a /skills/ folder. Each subfolder is a skill you can perform. Read the skill's files to understand what it does and when to use it.
3. When you're unsure about something, ASK. Don't guess. Use short clarifying questions ("Which client?" / "Want this formal or casual?" / "Should I update the existing file or make a new one?"). Three targeted questions beat one wrong answer.

Writing rules (follow these in ALL written output):

- Say what something IS first. Never open with what it isn't.
- Vary sentence length hard. Three words. Then a longer one that takes its time.
- Use real names, real numbers, real details.
- Never write "moreover," "furthermore," "in addition," "it's worth noting," or "it's important to note."
- Banned words: "leverage" (as a verb), "delve," "tapestry," "landscape," "nuanced," "robust."
- Don't start back-to-back paragraphs the same way.
- Use contractions. "Don't" not "do not." Always.
- Write like people talk. Fragments fine. Run-ons fine.
```

6. Close settings. Done.

**Why this matters:** Without this prompt, Claude sees your plugins as random files. With it, Claude reads the CLAUDE.md in every plugin and *becomes* that product — loading its persona, recognizing its skills, following its rules. This is what makes Cowork work.

## Skills

| Skill | Say This | What Happens |
|-------|----------|-------------|
| **Organize Machine** | "Organize my machine" | Your first real skill. Scans your Desktop and Downloads, categorizes everything into Action/Reference/Trash buckets, and organizes files in batches of 10 — asking permission before each batch. Proves your agent can *do* things, not just talk. |
| **Business Blueprint** | "Run my business blueprint" | 5-minute interview about you and your business. Creates `config.md` (your business context) and `CLAUDE.md` (your agent's persona). Every skill after this works better because your agent knows who you are. |

## Session Order

Total time: ~20 minutes.

1. **System Prompt** — paste the prompt into Claude settings *(30 seconds, one-time)*
2. **Organize Machine** — watch your agent clean up your files *(10-20 minutes)*
3. **Business Blueprint** — answer questions so your agent knows your business *(5 minutes)*

After this session, your agent has already done real work on your computer and knows your business. Session 2 teaches it your voice and how to write content.

## Part of Cowork Bootcamp

Session 1 of 6. Each session adds new skills to your agent:

| Session | Focus | Skills |
|---------|-------|--------|
| **1** | Setup & Organization | Business Blueprint, Organize Machine |
| **2** | Content & Voice | Voice Training, Newsletter Writer, Voice Memo to Post |
| **3** | Meeting Prep & Email | Meeting Prep, Gmail Connector, Fireflies Connector |
| **4** | Project Kit & Presentations | Project Kit, Gamma Connector, Social Content |
| **5** | Landing Pages | Vercel Landing Page, Frontend Design |
| **6** | Skill Building | Skill Maker, Digital Product |
