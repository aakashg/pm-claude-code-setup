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

> **Want the full PM OS?** This starter covers the basics. The complete system has 41+ skills, 7 sub-agents, a context library, and templates. [Get it here →](https://www.news.aakashg.com/p/pm-os)
