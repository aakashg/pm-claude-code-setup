# Quickstart Guide

Get Claude Code working as your PM assistant in 60 seconds.

## Step 1: Copy the Files

```bash
# Copy CLAUDE.md to your project root
cp CLAUDE.md /path/to/your/project/

# Copy the skills
cp -r .claude/ /path/to/your/project/
```

## Step 2: Customize CLAUDE.md

Open CLAUDE.md and fill in the `[FILL IN]` sections:
- Your role and company
- Your product and target users
- Your north star metrics
- Your current OKRs
- Your company terminology

This takes 5 minutes and makes every Claude interaction better.

## Step 3: Use It

Open Claude Code in your project directory. Try:

- **"Write a PRD for [feature]"** — triggers the PRD writer skill
- **"Review as engineer"** — gets technical feasibility feedback
- **"Review as skeptic"** — stress-tests your assumptions
- **"Review as customer"** — checks if a real user would care

## Step 4: Add More Skills

Browse [PM Claude Skills](https://github.com/aakashg/pm-claude-skills) for 5 more drop-in skills.

## Troubleshooting

**Claude doesn't seem to know my context:**
- Make sure CLAUDE.md is in your project ROOT directory
- Check that you filled in the [FILL IN] sections

**Skills aren't triggering:**
- Skills must be in `.claude/skills/[name]/SKILL.md`
- Try the exact trigger phrase listed in the SKILL.md

**Context feels stale:**
- Use `/clear` between unrelated tasks
- Don't let conversations run past ~50 exchanges

---

*This is the starter setup. The full PM OS has 41+ skills, 7 sub-agents, and a complete context library. [Get it here →](https://www.news.aakashg.com/p/pm-os)*
