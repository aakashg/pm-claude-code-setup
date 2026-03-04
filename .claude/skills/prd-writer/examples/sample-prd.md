# PRD: In-App Calendar Integration

## Hypothesis

Adding a shared project calendar to our project management tool will increase weekly active usage by 15% within 90 days of launch, because teams currently switch to external tools (Google Calendar, Outlook) to track deadlines, causing missed dates and fragmented workflows.

## Problem

**Who has it:** Mid-market project teams (50-200 people) using our tool for task management.

**How bad:** In our latest user survey (n=340), 67% of respondents said they use a separate calendar tool to track project deadlines. Support tickets related to "missed deadlines" increased 23% QoQ. Exit interviews cite "no calendar view" as the #3 reason for churn.

**Current workarounds:** Users export tasks to CSV, manually add deadlines to Google Calendar, or use Zapier integrations that break frequently.

## Strategic Fit

- **Why this:** Calendar view is the #1 requested feature (412 upvotes on our feedback board). Competitors Asana and Monday.com both launched calendar views in the past 12 months.
- **Why now:** We're losing deals to competitors specifically because of this gap. Sales reports 3 lost deals >$50K ARR in Q4 citing "no calendar."
- **Why not alternatives:** A Zapier-only solution doesn't reduce friction enough. Embedding Google Calendar creates a dependency and limits our ability to add PM-specific features later.

## Solution

### Core Features

1. **Calendar View** — A month/week/day view showing all tasks with due dates. Accessible from the main navigation.
2. **Drag-and-Drop Rescheduling** — Users can drag a task to a new date to update its due date.
3. **Google Calendar Sync** — Two-way sync with Google Calendar. Project deadlines appear in Google Calendar; external events appear in our calendar as blocked time.
4. **Milestone Markers** — Project milestones displayed as pins on the calendar, distinct from regular tasks.

### Out of Scope for V1

- Outlook/Exchange sync (V2)
- Resource capacity planning
- Time tracking from calendar
- Recurring task patterns

### Key Flows

1. User navigates to Calendar tab, sees all tasks with due dates plotted on a month view.
2. User drags a task from March 5 to March 8. A confirmation toast appears. The task's due date updates across all views.
3. User clicks "Connect Google Calendar," completes OAuth, and sees external events appear as grey blocks within 30 seconds.

## Success Metrics

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Weekly active users | 12,400 | 14,260 (+15%) | 90 days post-launch |
| Calendar view adoption | 0% | 40% of WAU | 90 days post-launch |
| "Missed deadline" support tickets | 89/month | 65/month (-27%) | 90 days post-launch |

### Guardrails

- Page load time for calendar view: < 2 seconds (p95)
- Task update latency after drag-and-drop: < 500ms
- Google Calendar sync delay: < 60 seconds
- No increase in overall app crash rate

## Non-Goals

- We are NOT building a standalone calendar product. This is a view of existing project data.
- We are NOT replacing Google Calendar. The sync is additive, not competitive.
- We are NOT building resource management. Capacity planning is a separate initiative.
- We are NOT supporting calendars without due dates. Tasks without due dates do not appear.

## Open Questions

- [NEED: data from Engineering] What's the estimated effort for Google Calendar two-way sync vs. one-way?
- [NEED: data from Design] User research on whether week view or month view should be the default.
- [NEED: data from Legal] GDPR implications of syncing external calendar data.
