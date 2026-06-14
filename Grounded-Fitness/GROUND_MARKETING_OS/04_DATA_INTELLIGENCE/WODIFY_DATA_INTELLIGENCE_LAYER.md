# Wodify Data Intelligence Layer

The Grounded Marketing OS should eventually support analysis of Wodify data for member engagement, retention, class performance, financial snapshots, marketing feedback, and community health.

This is a future data layer. It should not interrupt the current Member Value Engine build, and it should start with CSV exports before any direct Wodify API integration.

## Build Status

Status: Future module documented only.

Current strategy: Start with CSV exports from Wodify.

Do not build a direct Wodify API integration until credentials, documentation, and data permissions are available.

## Primary Use Cases

### Member Engagement

- Attendance frequency.
- Attendance decline.
- Missed weeks.
- New member ramp-up.
- Milestone tracking.
- Reactivation opportunities.
- Referral opportunities.

### Retention

- Churn risk.
- Inactive members.
- Declining members.
- Freeze and cancellation patterns.
- First-30/60/90-day retention.

### Class Performance

- Attendance by class time.
- Class utilization.
- High-performing classes.
- Low-performing classes.
- Coach and class trends.

### Financial Snapshot

- Recurring revenue.
- Plan mix.
- Failed payments.
- Discounts.
- Drop-ins.
- Revenue by member type.

### Marketing Feedback

- Lead source quality.
- Intro conversion.
- Referral tracking.
- Campaign response.

### Community Health

- Member of the Month history.
- Milestone counts.
- Coach check-ins.
- Referrals.
- Anniversaries.
- Recognition opportunities.
- Attendance streaks.

## Expected Wodify CSV Exports

- `members.csv`
- `attendance.csv`
- `memberships.csv`
- `payments.csv`
- `leads.csv`
- `classes.csv`
- `coaches.csv`

## Privacy Rules

Do not commit real member data.

All real exports must stay outside git.

The root `.gitignore` must exclude:

- `/data_exports/`
- `/data_raw/`
- `/private/`
- `*.csv`
- `*.xlsx`

Use fake sample data for testing.

Remove, hash, or mask member identifiers when possible.

AI may flag risk.

AI may not decide action.

AI may not send outreach automatically.

Human review is required before member communication.

## First Reports To Build

1. Grounded Weekly Command Report.
2. Weekly Member Engagement Report.
3. Attendance Risk Report.
4. New Member 90-Day Report.
5. Class Utilization Report.
6. Revenue Snapshot Report.
7. Lead Conversion Report.
8. Community Health Dashboard.

The Grounded Weekly Command Report should be designed first inside Wodify Custom Reports when possible. It combines the most important operating views into one owner-facing report:

- At-risk members.
- New member 90-day watch.
- Lead pipeline health.
- Class health.
- Recognition and community.
- Revenue and membership risk.
- Owner action list.

Detailed design lives in `../07_WODIFY_AUDIT/GROUNDED_WEEKLY_COMMAND_REPORT_SPEC.md`.

Question-by-question Custom Reports data requirements live in `../07_WODIFY_AUDIT/CUSTOM_REPORTS_DATA_REQUIREMENTS.md`.

## Report Output Standard

Reports should be readable by a gym owner.

Use plain language.

Each report should show:

- What changed.
- Why it matters.
- Who needs attention.
- Recommended action.
- Confidence level.
- Missing data.

Avoid vanity metrics unless they connect to attendance, retention, revenue, or lead conversion.

## Evidence Rules

If a required export is missing, record `Unknown`.

If a metric cannot be calculated from available exports, record `No measurements found`.

If source data is incomplete, include a confidence level and missing-data note.

Do not infer revenue, churn risk, lead quality, or retention outcomes without source data.
