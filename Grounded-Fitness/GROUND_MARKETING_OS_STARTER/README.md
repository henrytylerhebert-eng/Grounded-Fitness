# Grounded Marketing OS Starter

Grounded Marketing OS is an AI accessibility and decision-support layer for Wodify.

It is not a replacement CRM, membership system, scheduling system, payments system, communications platform, or automation engine.

Grounded Fitness Acadiana already has valuable operational data inside Wodify, but that data is hard to access, interpret, and turn into timely action. Grounded AI makes Wodify more accessible and useful by turning exports and future read-only API data into owner briefs, coach briefs, member insights, retention flags, recognition opportunities, and draft communications.

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

Initial build scope: CSV/export-based analysis only.

Do not connect live APIs yet. Do not create, update, delete, or alter Wodify records. Do not send emails, SMS, chat messages, announcements, marketing emails, automated emails, or workflow emails. Do not convert leads to clients. Do not change memberships, payments, communication settings, templates, or automation toggles.

## Business Identity

- Business: Grounded Fitness Acadiana.
- Website: https://www.groundedfitnessacadiana.com/
- YouTube: @GroundedFitnessAcadiana
- Instagram: grounded_fitness_acadiana
- Facebook: https://www.facebook.com/GroundedFitnessAcadiana
- Google Business Profile: Grounded Fitness Acadiana
- Address: 401 East Cypress Street, Lafayette, LA 70501
- Phone: (225) 810-6134

## Golden Rule

Do not market Grounded Fitness as CrossFit.

Use public-facing language such as functional fitness, coaching, strength, conditioning, real-life fitness, movement quality, community, longevity, and consistency.

Avoid public-facing language such as CrossFit gym, box, WOD, RX, elite fitness, beast mode, and no excuses.

## Current MVP

The MVP is a CSV/export-based intelligence workflow that produces owner-readable markdown reports and draft communications from fake/sample Wodify data.

MVP outputs:

- Weekly Owner Brief.
- Weekly Coach Brief.
- At-Risk Member Report.
- Member Milestone Report.
- Member of the Month Candidate Report.
- Lead Pipeline Snapshot.
- Draft internal member emails.

## Package Structure

- `AGENTS.md`: Complete Codex operating instructions.
- `DECISIONS.md`: Decision log.
- `00_FOUNDATION/`: Business anchor, domain, naming, module, and scope foundations.
- `01_VALIDATION/`: Assumptions and validation log.
- `02_AI_BOUNDARIES/`: AI and human review rules.
- `03_MEMBER_VALUE_ENGINE/`: MVP requirements and member insight workflow.
- `04_WODIFY_INTELLIGENCE/`: Wodify object map, CSV strategy, report specs, and schema assumptions.
- `05_WODIFY_AUTOMATION_AUDIT/`: Wodify Workflow Builder, recipe, template, environment, API, and automation-gap audit.
- `05_COMMUNITY_RECOGNITION_ENGINE/`: Recognition intelligence module.
- `06_LOCAL_AUTHORITY_ENGINE/`: Future content intelligence module.
- `07_LEAD_NURTURE_ENGINE/`: Future lead intelligence module.

## Direction

Never rebuild Wodify.

Read from Wodify, analyze, summarize, recommend, and draft.

Human review comes before action.
