# CLAUDE.md for Product Managers

> Drop this file in your project root. Claude Code reads it automatically every session.
> Customize the [FILL IN] sections with your details.

---

## Who I Am

- Role: [FILL IN] (e.g., Senior PM, B2B SaaS)
- Company: [FILL IN]
- Product: [FILL IN]
- Target users: [FILL IN]
- Current focus: [FILL IN] (e.g., Q1: mobile app launch)

## North Star Metrics

- Primary: [FILL IN] (e.g., weekly active users)
- Secondary: [FILL IN]
- Guardrails: [FILL IN] (e.g., churn rate, latency)

---

## How I Write PRDs

Structure every PRD like this unless I say otherwise:

1. Hypothesis (one sentence, testable)
2. Problem (who has it, how bad, with data)
3. Strategic fit (why this vs alternatives)
4. Solution (specifics, not vague descriptions)
5. Success metrics (numbers, plus guardrails)
6. Non-goals (what we're NOT doing)

For AI features, add: behavior examples (15-25 input/output pairs), edge cases, eval criteria.

### PRD Rules

- IMPORTANT: Never generate a PRD without asking 3-5 clarifying questions first.
- Default to short. If it's over 2 pages, ask if that's needed.
- Flag missing info with "[NEED: data from X]" placeholders.
- Use RICE scoring when I ask you to prioritize.

---

## Writing Style

- Direct and concise. No filler.
- Active voice. Short paragraphs.
- Match the audience: casual for Slack, structured for docs, precise for specs.
- Lead with the ask or recommendation, context after.
- Never use: delve, landscape, synergy, leverage, robust, streamline, cutting-edge.

---

## Sub-Agent Roles

When I say "review as [role]," adopt that perspective:

- **Engineer:** Is this feasible? What's missing from the spec? Edge cases?
- **Designer:** Is the flow clear? Where will users get confused?
- **Executive:** Does this align with strategy? What's the ROI case?
- **Skeptic:** What could go wrong? What are we assuming that's false?
- **Customer:** Would I use this? What's confusing?

---

## Current OKRs

[FILL IN, e.g.:]
O1: Increase activation rate for new users
- KR1: 7-day activation from 23% to 35%
- KR2: Time to first value under 3 minutes

---

## Company Terminology

[FILL IN terms Claude should know, e.g.:]
- "Tiger team" = cross-functional sprint for urgent projects
- "P0" = drop everything priority

---

## Power Features

### @ References (Don't Paste, Point)

Never paste large docs into chat. Reference them instead:

```
Read @templates/prd-template.md and use that structure.
Check @docs/okrs-q1.md for current objectives.
Summarize @meeting-notes/standup-03-04.md into action items.
```

Claude reads the file on demand. Your context window stays clean.

### Plan Mode (Shift+Tab)

Use before any complex task. Plan Mode forces Claude to outline its approach before executing. You approve the plan, then it runs.

Best for: PRDs with multiple stakeholders, multi-file edits, anything where "undo" is expensive.

### Session Handoffs

Long projects span multiple sessions. Use this pattern:

1. Before ending: "Write a HANDOFF.md — current state, decisions made, open questions, next steps."
2. Next session: "Read @HANDOFF.md and continue."
3. Or use `claude --continue` to resume your last session directly.

### Hooks (Guaranteed Automation)

Unlike instructions in this file (which are advisory), hooks run deterministically. Ask Claude to set them up:

- "Write a hook that spell-checks every file I edit"
- "Write a hook that blocks writes to /templates/"
- "Write a hook that notifies me when a task finishes"

Configure via `/hooks` or `.claude/settings.json`. Hooks use exit codes: 0 = proceed, 2 = block with feedback.

### Self-Improving CLAUDE.md

This file should get smarter every session:

1. When Claude makes a mistake, correct it.
2. Then: "Add a rule to CLAUDE.md so you don't make that mistake again."
3. Claude proposes the rule. You approve. It edits this file.
4. Next session, the rule is loaded automatically.

Prune quarterly. For each line, ask: "Would removing this cause mistakes?" If not, cut it.

### Context Hygiene

- Use `/clear` between unrelated tasks. Context bleed is the #1 quality killer.
- Cap conversations at ~50 exchanges. Quality degrades past this.
- Use `Shift+Tab` before complex multi-step tasks. Plan first, execute after approval.
- Run parallel sessions in multiple terminals for independent tasks (research in one, writing in another).

### Useful Commands

```
/clear            Reset context (CLAUDE.md reloads automatically)
/hooks            Configure automation hooks
/init             Generate a starter CLAUDE.md from your project
Shift+Tab         Toggle Plan Mode
claude --continue Resume last session
claude --resume   Pick a specific past session
```

---

## MCP Connections

[FILL IN any MCP servers you've connected, e.g.:]
- Notion: reading/writing product docs
- Linear/Jira: creating and updating tickets
- Slack: sending messages, reading channels
- Google Drive: accessing shared docs

---

> **Want the full PM OS?** This starter covers the basics. The complete system has 41+ skills, 7 sub-agents, a context library, and templates. [Get it here →](https://www.news.aakashg.com/p/pm-os)
