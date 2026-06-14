# AGENTS.md

## Project

This repository is for the Grounded Marketing OS.

Grounded Fitness Acadiana is a Lafayette, Louisiana functional fitness gym focused on coaching, community, strength, conditioning, longevity, consistency, movement quality, and real-life fitness.

## Hard Rule

Never rebuild Wodify.

Read from Wodify, analyze, summarize, recommend, and draft.

Human review comes before action.

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

Initial build scope is CSV/export-based analysis only.

Do not connect live APIs yet.

Do not create Workato API clients yet.

Do not install or connect Workato community connectors yet.

Do not connect AI model providers through Workato yet.

Do not create, update, delete, or alter Wodify records.

Do not send emails, SMS, or chat messages.

Do not schedule, publish, toggle, or configure Wodify communications.

Do not create or publish Wodify email templates.

Do not change Wodify Communication settings.

Do not convert leads to clients.

Do not change memberships or payments.

## Golden Rule

Do not market Grounded Fitness as CrossFit.

Use public-facing language such as:

- functional fitness
- coaching
- strength
- conditioning
- real-life fitness
- movement quality
- community
- longevity
- consistency

Avoid public-facing language such as:

- CrossFit gym
- box
- WOD
- RX
- elite fitness
- beast mode
- no excuses

## Current Build Focus

Build only the CSV/export-based Grounded AI Intelligence Layer first.

The first MVP should produce:

- Weekly Owner Brief
- Weekly Coach Brief
- At-Risk Member Report
- Member Milestone Report
- Member of the Month Candidate Report
- Lead Pipeline Snapshot
- Draft internal member emails

Do not build the full marketing system.

Do not duplicate Wodify functionality unless explicitly requested.

## Build Philosophy

Validate before architecting.

Architect before building.

Build before automating.

Automate before scaling.

Measure before claiming success.

## Source Of Truth

Wodify is the source of truth for operational records, including leads, clients, memberships, attendance, reservations, appointments, tasks, communications, automations, invoices, transactions, and reporting.

Human approval is the source of truth for:

- final content
- member communication
- publishing
- recognition decisions
- referral asks
- retention actions
- business decisions

Grounded AI may produce intelligence outputs only:

- summaries
- reports
- recommendations
- risk flags
- candidate lists
- draft communications
- missing-data notes

## AI Rules

AI may:

- read fake/sample Wodify CSV exports
- summarize operational patterns
- separate facts from inferred recommendations
- create owner-readable markdown reports
- draft internal member emails for review
- flag at-risk members
- surface milestone opportunities
- identify Member of the Month candidates
- summarize lead pipeline status
- recommend coach follow-up
- identify missing data

AI may not:

- create, update, delete, or alter Wodify records
- write Wodify tasks, tags, communications, automations, memberships, payments, or lead statuses
- send emails, SMS, chat messages, or announcements
- convert leads to clients
- change memberships, holds, invoices, payments, or transactions
- publish public content without approval
- make health promises
- provide medical advice
- diagnose members
- create pressure-based or guilt-based messaging
- select Member of the Month
- ask for referrals automatically
- decide retention actions
- use personal stories publicly without human approval and member consent
- invent attendance trends
- invent member quotes or testimonials
- invent campaign results
- present missing metrics as success
- market Grounded as CrossFit

## Tone

Internal member drafts should feel:

- human
- helpful
- encouraging
- coach-led
- grounded
- simple
- relational

They should not feel:

- salesy
- automated
- corporate
- guilt-based
- loud
- generic

Owner and coach briefs should be plain-language, direct, and useful.

Reports should show:

- what changed
- why it matters
- who needs attention
- recommended action
- confidence level
- missing data

## Do Not Build

Do not build:

- a CRM
- a membership system
- attendance tracking
- scheduling
- payments
- communications infrastructure
- replacement Wodify automations
- production Wodify API integration
- Workato API clients
- Workato community connector installation
- AI model connector integration through Workato
- automatic Wodify writes
- automatic outreach
- Wodify communication settings changes
- Wodify marketing email sending or scheduling
- Wodify automated email toggles
- Wodify template creation or publishing
- Wodify in-app chat automation
- Wodify calendar-event automation
- public blog publishing
- ad campaigns
- YouTube automation
- Canva automation
- Google Business Profile posting

## Privacy Rules

Never commit real member data.

Use fake sample data only.

All real exports must stay outside git.

Use `.gitignore` for:

- `/data_exports/`
- `/data_raw/`
- `/private/`
- `*.csv`
- `*.xlsx`

Remove, hash, or mask member identifiers when possible.

No automated outreach.

No health promises.

No medical advice.

No CrossFit public branding.

## Evidence Rules

Separate confirmed facts from inference.

If a source is missing, say `Unknown`.

If performance, attendance, engagement, revenue, retention, or lead conversion data is missing, say `No measurements found`.

Do not invent events, incidents, testimonials, campaign results, PRs, health outcomes, member behavior, attendance trends, revenue, or source evidence.
