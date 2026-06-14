# Module Map

Grounded AI modules are intelligence layers only.

They should make Wodify easier to understand and act on. They should not duplicate Wodify functionality.

## Core Flow

```text
Wodify
↓
Data Export or Read-Only API Pull
↓
Grounded AI Intelligence Layer
↓
Owner Briefs / Coach Briefs / Member Insights / Draft Content
↓
Human Review
↓
Optional Wodify Task, Tag, or Communication
```

## MVP Modules

### Wodify Data Access Layer

Purpose: Consume fake/sample Wodify CSV exports first, and later support approved read-only API pulls.

Owns: parsing, field mapping, missing-data detection, source notes, and read-only data normalization.

Does not own: Wodify records, API writes, imports, syncs, mutations, or automations.

### Member Engagement Intelligence

Purpose: Surface member attendance patterns, consistency, decline, missed weeks, milestones, and at-risk signals.

Outputs:

- At-Risk Member Report.
- Member Milestone Report.
- Member insights for owner and coach briefs.
- Draft internal member email inputs.

### Coach Brief Engine

Purpose: Turn member and class signals into coach-readable weekly notes.

Outputs:

- Weekly Coach Brief.
- Members to check in with.
- Milestones to recognize.
- Missing-data flags.
- Suggested talking points.

### Community & Recognition Intelligence

Purpose: Surface recognition opportunities from attendance, milestones, anniversaries, nominations, and community contribution.

Outputs:

- Member of the Month Candidate Report.
- Recognition opportunities.
- Milestone candidates.
- Anniversary candidates.

### Lead Pipeline Intelligence

Purpose: Summarize Wodify lead data and identify where human follow-up may be useful.

Outputs:

- Lead Pipeline Snapshot.
- Stale lead flags.
- Lead source notes.
- Missing conversion data.

### Revenue Snapshot Intelligence

Purpose: Summarize Wodify revenue, invoice, transaction, discount, plan mix, and payment data when exports are available.

Outputs:

- Revenue snapshot.
- Failed payment notes.
- Plan mix notes.
- Missing-data flags.

### Content Drafting Layer

Purpose: Draft review-ready internal emails, recognition copy, owner notes, coach notes, and future public content from approved source context.

Does not send or publish.

### Human Review Layer

Purpose: Gate every action before member communication, public publishing, Wodify task creation, Wodify tagging, or Wodify communication.

Human review is required before action.

## Future Roadmap Modules

These remain roadmap only unless explicitly activated:

- Local Authority Engine.
- Lead Nurture Engine.
- New Member Success Engine.
- Coaching Standards Engine.
- Referral Engine.
- Exit Intelligence Engine.
- Member Success Framework.
- Community Partnership Engine.
- Executive Weekly Brief.
- Grounded Knowledge Base.
