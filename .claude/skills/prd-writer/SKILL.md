# PRD Writer

## Trigger
Activate when the user asks to "write a PRD", "create a PRD", "draft a PRD", "PRD for [feature]", or "spec out [feature]".

## Behavior

### Step 1: Clarify Before Writing
Before generating anything, ask 3-5 clarifying questions. Tailor questions to what's missing. Common gaps:

- Who specifically has this problem? (Not "users" — which users?)
- What data do we have that this is worth solving? (Usage data, support tickets, revenue impact)
- What's the scope? (MVP vs full vision)
- Are there technical constraints the engineering team has flagged?
- What's the timeline and why?

Do NOT proceed until the user answers. A PRD without clear answers to these questions will be vague and useless.

### Step 2: Generate the PRD

Use this structure:

**Title:** [Feature Name]
**Author:** [User's name if known]
**Date:** [Today's date]
**Status:** Draft

---

**1. Hypothesis**
One sentence. Testable. Format: "We believe [action] will [outcome] for [users], measured by [metric]."

**2. Problem**
- Who has this problem (specific user segment)
- How bad is it (frequency, severity, with data)
- What happens if we don't solve it

**3. Strategic Fit**
- Why this problem, why now
- How it connects to current OKRs
- Why this approach vs alternatives we considered

**4. Solution**
- Specific description of what we're building (not vague)
- User flow (step by step)
- Key interactions and states
- Include wireframe descriptions or ASCII mockups where helpful

**5. Success Metrics**
- Primary metric with target number and timeframe
- Secondary metrics (2-3)
- Guardrail metrics (what should NOT get worse)

**6. Non-Goals**
- What we're explicitly NOT doing in this version
- Features we considered and cut (and why)

**7. Open Questions**
- Flag unresolved items with owners and deadlines

### Step 3: Review
After generating, ask: "Want me to review this as an engineer, designer, or skeptic?"

## Rules
- Keep PRDs under 2 pages unless the user asks for more
- Flag missing information with `[NEED: data from X]` rather than making things up
- Use specific numbers, not "improve engagement"
- No filler. Every sentence should add information.
- If the feature involves AI, add a section for: behavior examples (10+ input/output pairs), edge cases, and evaluation criteria
