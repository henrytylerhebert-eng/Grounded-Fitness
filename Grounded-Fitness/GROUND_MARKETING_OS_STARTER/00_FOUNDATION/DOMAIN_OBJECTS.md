# Domain Objects

These are intelligence-layer objects, not replacement Wodify objects.

Wodify owns operational records. Grounded AI reads exports, analyzes, summarizes, recommends, and drafts.

## Current MVP Objects

### Wodify Export

Source: Wodify CSV/export.

Purpose: Provides sample operational data for analysis.

Rules:

- Use fake/sample data only in the repository.
- Real exports stay outside git.
- Missing source fields are marked `Unknown`.

### Source Inventory

Purpose: Lists which files, fields, date ranges, and object types are available for a report run.

Minimum fields:

- Export name.
- Object type.
- Date range if available.
- Fields present.
- Fields missing.
- Notes.

### Insight

Purpose: Plain-language interpretation of Wodify export data.

Insight types:

- Member engagement.
- Retention risk.
- Lead pipeline.
- Revenue snapshot.
- Class utilization.
- Milestone.
- Recognition opportunity.
- Missing data.

### Inferred Recommendation

Purpose: A suggested human-reviewed action based on source facts.

Rules:

- Must be labeled as inference.
- Must include confidence level.
- Must include source basis.
- Must not perform action.

### Owner Brief

Purpose: Weekly markdown summary for leadership.

Should include:

- What changed.
- Why it matters.
- Who needs attention.
- Recommended action.
- Confidence level.
- Missing data.

### Coach Brief

Purpose: Weekly markdown summary for coaches.

Should include:

- Members to check in with.
- Attendance drops.
- New member notes.
- Milestones.
- Recognition opportunities.
- Suggested talking points.
- Missing data.

### Report

MVP report types:

- Weekly Owner Brief.
- Weekly Coach Brief.
- At-Risk Member Report.
- Member Milestone Report.
- Member of the Month Candidate Report.
- Lead Pipeline Snapshot.

### Draft Internal Member Email

Purpose: Human-reviewed draft generated from report findings.

Must be:

- Coach-led.
- Specific.
- Helpful.
- Human.
- Low-pressure.
- Free of CrossFit branding.
- Free of health promises.
- Free of medical advice.

### Human Review

Purpose: Required approval step before communication or optional action inside Wodify.

Human approval is the source of truth for final communication and business action.

### Optional Wodify Action Candidate

Purpose: A recommendation that a human may choose to perform inside Wodify.

Examples:

- Create task candidate.
- Tag candidate.
- Communication candidate.

Grounded AI must not perform the Wodify action.

## Future Record Vocabulary

These records are architectural placeholders only. They must not duplicate Wodify ownership.

### Core Member Reference

Future use: reference Wodify client records across intelligence outputs.

### Attendance Reference

Future use: interpret attendance frequency, missed weeks, decline, streaks, class utilization, and retention signals from Wodify data.

### Coach Reference

Future use: connect class trends, coach brief notes, follow-up opportunities, and recognition workflows.

### Milestone Reference

Future use: identify 25, 50, 100, 250, and 500 visit recognition, benchmark tracking, and anniversary triggers.

### Recognition Candidate

Future use: Member of the Month, coach recognition, community stories, and recognition history.

### Referral Candidate

Future use: ambassador signals and referral opportunities for human review.

### Content Draft

Future use: public content, member education, local authority, website stories, social posts, and coach onboarding.

### Communication Draft

Future use: member emails, coach follow-ups, referral requests, recognition drafts, public posts, and executive briefs.
