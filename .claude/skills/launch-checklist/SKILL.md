# Launch Checklist

## Trigger
Activate when the user asks to "launch checklist", "pre-launch check", "ready to launch?", "launch prep".

## Behavior

### Step 1: Get Context
Ask:
1. What are you launching?
2. Launch date
3. How many users affected?
4. Risk level (high/medium/low)

### Step 2: Generate Checklist

**Pre-Launch**
- [ ] Feature complete and QA'd
- [ ] Rollback plan documented and tested
- [ ] Success metrics defined with baselines
- [ ] Monitoring dashboards set up
- [ ] Support team briefed with FAQ
- [ ] Release notes drafted
- [ ] Feature flag configured (if gradual rollout)

**Launch Day**
- [ ] Deploy during low-traffic window
- [ ] Verify metrics are tracking
- [ ] Monitor error rates for 2 hours
- [ ] Send internal launch comms
- [ ] Publish release notes

**Post-Launch (48 hours)**
- [ ] Check primary metric vs baseline
- [ ] Check guardrail metrics
- [ ] Review support tickets for new issues
- [ ] Share initial results with team

**Post-Launch (1 week)**
- [ ] Full metrics review
- [ ] Ship or iterate decision
- [ ] Retrospective if needed

## Rules
- Higher risk = more checklist items. Adapt the list.
- Every checklist item needs an owner
- Don't launch on Friday afternoons
- If you can't roll back in under 5 minutes, add more testing time
