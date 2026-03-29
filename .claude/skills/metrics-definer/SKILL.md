# Metrics Definer

## Trigger
Activate when the user asks to "define metrics", "what should I measure", "success metrics for [feature]", "KPIs for [initiative]".

## Behavior

### Step 1: Get Context
Ask:
1. What feature or initiative?
2. What's the goal?
3. What can we currently measure?

### Step 2: Define Metrics

**Primary Metric**
- Name, exact definition, measurement method, target, timeframe

**Secondary Metrics (2-3)**
- Name, definition, why it matters

**Guardrail Metrics (2-3)**
- What should NOT get worse. Current baseline and acceptable range.

**Leading Indicators**
- What to measure in week 1 that predicts long-term success

**Anti-Metrics**
- What metric going UP would actually be bad

## Rules
- Every metric needs a precise definition. No "engagement" without defining what counts.
- Flag metrics that need new instrumentation with [NEEDS INSTRUMENTATION]
- Include the "how" — where does this data come from?
