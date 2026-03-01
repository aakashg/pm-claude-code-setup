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

---

## Troubleshooting

Common issues and how to fix them.

### Claude doesn't seem to follow my CLAUDE.md instructions

- **Check the file location.** CLAUDE.md must be in your project root (the directory where you run `claude`). Claude Code loads it automatically from the working directory.
- **Check file size.** If your CLAUDE.md exceeds ~150 lines, Claude may start ignoring parts of it. Prune aggressively. Move domain knowledge into skills.
- **Check for conflicting instructions.** If two rules contradict each other, Claude picks one unpredictably. Audit for conflicts.
- **Restart the session.** Run `/clear` or start a new terminal. Claude loads CLAUDE.md at session start.

### Skills aren't triggering

- **Verify the path.** Skills must be at `.claude/skills/<skill-name>/SKILL.md` (exact casing matters).
- **Check the trigger.** The SKILL.md needs a clear trigger phrase that matches how you're asking. If your SKILL.md says "triggers when user asks to write a PRD" but you say "draft a spec," Claude may not connect them.
- **Test with an explicit request.** Try: "Use the prd-writer skill to write a PRD for X." If that works but natural language doesn't, refine your trigger description.
- **Check that SKILL.md isn't empty or malformed.** Open it and verify it has content.

### Claude forgets context mid-conversation

- **You've hit context limits.** Long conversations degrade quality after ~50 exchanges. Use `/clear` and start fresh with a summary.
- **Use handoffs.** Before clearing, ask Claude to write a HANDOFF.md summarizing state, decisions, and next steps. Start the new session with "Read @HANDOFF.md and continue."
- **Don't paste huge docs.** Use `@` references instead of pasting entire documents into chat.

### Hooks aren't running

- **Check `.claude/settings.json`.** Hooks are configured there, not in CLAUDE.md.
- **Check exit codes.** Hooks use exit 0 (proceed) and exit 2 (block + feedback). Other exit codes may cause unexpected behavior.
- **Check permissions.** Hook scripts need to be executable (`chmod +x`).

### MCP servers won't connect

- **Verify credentials.** Most MCP servers need API keys or OAuth tokens. Check that yours are current.
- **Check the server config.** MCP connections are configured in Claude Code settings, not CLAUDE.md. CLAUDE.md just documents them for your reference.
- **Restart Claude Code.** MCP connections are established at startup.

### "I changed CLAUDE.md but nothing changed"

Claude reads CLAUDE.md at session start. If you edited it mid-session:
1. Run `/clear` to reset context (CLAUDE.md reloads automatically)
2. Or start a new terminal session
