# PM Claude Code Setup

A ready-to-use Claude Code configuration for product managers. Drop these files into your project and Claude Code immediately understands PM work.

Includes a `CLAUDE.md` context file and a PRD writer skill. Takes 60 seconds to set up.

**This setup works on its own — drop it in and Claude Code immediately understands PM work. The full PM Operating System goes much further: 41+ skills, 7 sub-agent perspectives, a complete context library, launch templates, and sprint planning workflows that I've iterated on 100+ times.**

**[Get the full PM Operating System →](https://www.news.aakashg.com/p/pm-os)**

---

## What's Inside

```
pm-claude-code-setup/
├── CLAUDE.md                           # Master context file — drop in your project root
└── .claude/
    └── skills/
        └── prd-writer/
            └── SKILL.md                # PRD writing skill — triggers on "write a PRD"
```

## Quick Setup

**Step 1:** Copy `CLAUDE.md` to your project root:
```bash
cp CLAUDE.md /path/to/your/project/
```

**Step 2:** Copy the skills folder:
```bash
cp -r .claude/ /path/to/your/project/
```

**Step 3:** Open Claude Code in your project. It loads automatically.

That's it. Claude now knows you're a PM, follows your writing style, and can write PRDs on command.

## What the CLAUDE.md Does

The `CLAUDE.md` file gives Claude persistent context about:

- **Your role and product** — so it doesn't ask "what do you do?" every session
- **Your writing style** — direct, concise, no filler words
- **Your PRD structure** — hypothesis, problem, solution, metrics, non-goals
- **Sub-agent roles** — say "review as engineer" or "review as skeptic" for different perspectives
- **Session management** — rules for context, handoffs, and parallel work

Customize the `[FILL IN]` sections with your specifics.

## What the PRD Writer Skill Does

Say "write a PRD" or "create a PRD for [feature]" and Claude:

1. Asks 3-5 clarifying questions first (never generates blind)
2. Follows a structured format: hypothesis, problem, solution, metrics, non-goals
3. Flags missing info with `[NEED: data from X]` placeholders
4. Keeps it under 2 pages unless you ask for more
5. Includes success metrics with specific numbers and guardrails

## Want the Full Setup?

This setup handles the core PM workflow. The full PM OS covers every PM task I do daily:

- 41+ custom skills for every PM task
- 7 sub-agent perspectives (engineer, designer, executive, skeptic, customer, data analyst, legal)
- Context library with your OKRs, terminology, and team structure
- Templates for launches, roadmaps, retros, and sprint planning
- Hooks for automated spell-checking and file protection

**[Get the full PM Operating System →](https://www.news.aakashg.com/p/pm-os)**

---

Built by [Aakash Gupta](https://www.aakashg.com) | [Product Growth Newsletter](https://www.news.aakashg.com)
