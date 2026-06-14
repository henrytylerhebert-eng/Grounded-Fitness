# Wodify Intelligence Specification

## Purpose

Wodify Intelligence makes Wodify easier and more useful for the owner and staff by surfacing insights, reports, recommendations, and draft communications from Wodify data.

It does not rebuild Wodify.

## System Of Record

Wodify remains the system of record for:

- Leads.
- Clients.
- Memberships.
- Attendance.
- Reservations.
- Appointments.
- Tasks.
- Communications.
- Automations.
- Invoices.
- Transactions.
- Reporting.

Grounded AI is an intelligence, accessibility, and decision-support layer on top of Wodify.

## Data Strategy

Initial build: CSV/export-based analysis only.

Use fake/sample CSV data only in the repository.

Future phase: read-only Wodify API pull after credentials, documentation, permissions, and security rules are approved.

Write actions are locked until explicitly approved in a future phase.

Current Workato/API state observed on June 12, 2026:

- No Workato API clients exist yet.
- Community connectors and AI/model connectors are available in the Workato library but are not approved for MVP use.
- Future API work requires explicit approval, least-privilege role design, credential handling, and read-only-first access planning.

## Core Architecture

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

## MVP Outputs

- Weekly Owner Brief.
- Weekly Coach Brief.
- At-Risk Member Report.
- Member Milestone Report.
- Member of the Month Candidate Report.
- Lead Pipeline Snapshot.
- Draft internal member emails.

## Primary Intelligence Areas

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

### Revenue Snapshot

- Recurring revenue.
- Plan mix.
- Failed payments.
- Discounts.
- Drop-ins.
- Revenue by member type.

### Lead Pipeline

- Lead source quality.
- Intro conversion.
- Referral tracking.
- Campaign response.
- Stale leads.

### Community Health

- Member of the Month history.
- Milestone counts.
- Coach check-ins.
- Referrals.
- Anniversaries.
- Recognition opportunities.
- Attendance streaks.

## Prohibited Actions

Grounded AI may not:

- Create, update, delete, or alter Wodify records.
- Create Wodify tasks.
- Add or change Wodify tags.
- Send Wodify communications.
- Trigger Wodify automations.
- Create Workato API clients.
- Install or connect Workato community connectors.
- Connect AI model providers through Workato.
- Convert leads to clients.
- Change memberships or holds.
- Change invoices, payments, or transactions.
- Replace Wodify reports.
- Replace Wodify automations.

## Report Output Standard

Reports should be readable by a gym owner.

Use plain language.

Show:

- What changed.
- Why it matters.
- Who needs attention.
- Recommended action.
- Confidence level.
- Missing data.

Separate facts from inferred recommendations.

Avoid vanity metrics unless they connect to attendance, retention, revenue, or lead conversion.
