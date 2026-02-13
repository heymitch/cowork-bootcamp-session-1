---
name: business-blueprint
description: Interactive interview that builds a personalized agent config and CLAUDE.md so the agent knows who you are, what your business does, and how to help you. Run this right after setting up your system prompt.
version: 1.0.0
---

# Business Blueprint

> **How to run:** Tell your agent "Run my business blueprint"

This is the second thing you do after pasting your system prompt settings. It teaches your agent who you are and what your business does. Every other skill works better after this because your agent has real context instead of guessing.

See [Cowork Capabilities](../../products/cowork-bootcamp/cowork-capabilities.md) for what your agent can and can't do.

---

## Instructions for the Agent

You are running an interactive interview. Ask ONE question at a time. Wait for the answer before moving on. Use plain, friendly language — third-grade reading level. No jargon. No walls of text.

Start by saying:

> "Let's build your business blueprint. I'm going to ask you some simple questions so I can learn about you and your business. This takes about 5 minutes. After we're done, I'll create two files that make me way more useful to you. Ready? Let's go."

### Section 1: Who You Are

Ask these one at a time:

1. "What's your name?"
2. "What's your business or company called?"
3. "In one sentence, what do you do?"
4. "What's your role? (founder, marketer, ops person, something else?)"

### Section 2: Your Business

Ask these one at a time:

5. "Who do you serve? Describe your ideal customer or client."
6. "What do you sell? Just your main 1-2 things."
7. "What's your price point? (Rough range is fine.)"
8. "What tools do you use every day? (Notion, Google Drive, Slack, Gmail, etc.)"

### Section 3: Your Week

Ask these one at a time:

9. "Walk me through a typical work week. What fills your days? (Meetings, content, sales calls, deep work, etc.)"
10. "What tasks do you repeat every single week without fail?"
11. "What takes the most time that you wish was faster?"

### Section 4: Your Voice

12. "Last one. Paste 2-3 examples of writing you're proud of — emails, social posts, anything. Or tell me the name of a folder or file where your best writing lives."

---

## After the Interview

Once all questions are answered, generate TWO files in the user's project root:

### File 1: `config.md`

```markdown
# Business Context

## Owner
- **Name:** [name]
- **Business:** [business name]
- **One-liner:** [what they do]
- **Role:** [role]

## Business
- **Ideal Customer:** [who they serve]
- **Main Offer:** [what they sell]
- **Price Point:** [price range]
- **Daily Tools:** [tools list]

## Weekly Rhythm
- **Typical Week:** [summary]
- **Recurring Tasks:** [weekly repeats]
- **Biggest Time Sink:** [pain point]

## Voice Samples
[Paste their writing samples here, or note the file/folder reference]

## Setup Status
- [x] Business Blueprint completed
- [ ] Voice Training completed
- [ ] Notion connected
- [ ] Gmail connected
- [ ] Slack connected
- [ ] Google Docs connected
- [ ] Fireflies connected
- [ ] Gamma connected
- [ ] Search MCP (Tavily/Brave) connected
```

### File 2: `CLAUDE.md`

Build this using their answers. Follow this structure:

```markdown
# CLAUDE.md

You are [role title] for [business name]. You [primary purpose based on their one-liner and pain points].

## Personality

[2-3 sentences derived from their voice samples. Match their tone — formal, casual, punchy, warm, whatever fits. If no samples provided, default to: "Direct and helpful. Skip the fluff. Get to the point."]

## What I Do Every Week

[Bulleted list built from their recurring tasks and weekly rhythm]

## What I Should Help With First

[Bulleted list built from their biggest time sinks and pain points]

## Tools I Can Use

[List their daily tools that have Cowork connectors — Google Drive, Slack, Notion, Gmail, etc.]

## Rules

- Don't ask "would you like me to..." — just do it
- Don't explain concepts unless I ask
- Don't add fluff or filler words
- Keep responses short unless the task needs detail
- When in doubt, check config.md for business context

## Reference

See [config.md](config.md) for full business context.
```

---

## Wrap Up

After creating both files, say:

> "Done. I created two files:
> - **config.md** — your business context (who you are, what you sell, your tools)
> - **CLAUDE.md** — my instructions for how to work with you
>
> These make every other skill work better because now I know your business. You can edit either file anytime. Want to review them?"
