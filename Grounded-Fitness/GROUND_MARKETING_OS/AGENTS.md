# AGENTS.md

## Project

This repository is for the Grounded Marketing OS.

Grounded Fitness Acadiana is a Lafayette, Louisiana functional fitness gym focused on coaching, community, strength, longevity, and real-life fitness.

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

Build only the Member Value Engine first.

Workflow:

Weekly programming email -> Wodify attendance segments -> internal member emails.

Do not build the full marketing system yet.

## Build Philosophy

Validate before architecting.
Architect before building.
Build before automating.
Automate before scaling.
Measure before claiming success.

## Member Value Engine Purpose

Help active members feel coached between workouts.

The system should:

- summarize weekly programming
- identify weekly coaching themes
- segment members by attendance pattern
- draft value-based internal emails
- support retention
- support attendance consistency
- support referrals
- protect community culture

## Member Segments

Use these initial segments:

1. Consistent
   Members attending 4+ times per week.

2. Active
   Members attending 2-3 times per week.

3. At Risk
   Members attending 0-1 times per week or showing attendance decline.

4. New
   Members in their first 90 days.

## AI Rules

AI may:

- summarize programming
- extract themes
- draft emails
- suggest segments
- recommend follow-ups
- flag retention risks
- create review-ready content

AI may not:

- send emails without human review
- alter Wodify records
- publish public content without approval
- make health promises
- diagnose members
- create pressure-based or guilt-based messaging

## Tone

Internal member emails should feel:

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

## Source of Truth

Wodify is the source of truth for:

- active members
- attendance
- member status
- membership type
- lead status
- class participation

Gmail is the source of truth for:

- weekly programming emails

Human approval is the source of truth for:

- final content
- member communication
- publishing
- business decisions

## MVP Acceptance Criteria

The MVP works when:

1. A weekly programming email can be summarized.
2. Members can be grouped into attendance-based segments.
3. Three internal emails can be drafted for the week.
4. Emails are clearly tailored by segment.
5. A human can review and approve before sending.
6. Attendance and engagement can be reviewed after sending.

## Do Not Build Yet

Do not build:

- full marketing automation
- public blog engine
- lead nurture engine
- new member success automation
- coaching standards system
- referral engine
- exit intelligence engine
- member success framework
- community partnership engine
- executive weekly brief
- knowledge base system
- community recognition automation
- ad campaigns
- YouTube automation
- Canva automation
- Google Business Profile posting
- financial analysis
- automatic Wodify writes

Document these as future modules only.

## Future Engine Map

Grounded Marketing OS should eventually include:

- Member Value Engine
- Local Authority Engine
- Lead Nurture Engine
- Community & Recognition Engine
- Analytics Engine

Current build remains Member Value Engine only.

Detailed deferred modules live in `06_ROADMAP/FUTURE_DEVELOPMENT_ROADMAP.md`.

Future modules should influence architecture and data design, but not current MVP scope.

Preserve room for:

- core member records
- attendance records
- coach records
- milestone records
- recognition records
- referral records
- content records
- communication records

## Future Community & Recognition Engine

The Community & Recognition Engine should strengthen belonging, recognition, referrals, retention, and community engagement.

Future inputs:

- Wodify attendance, milestones, anniversaries, PRs if tracked, class participation, and consistency.
- Coach observations about leadership, attitude, encouragement, and community contribution.
- Staff nominations, testimonials, and stories.

Future outputs:

- Member of the Month workflow.
- Milestone triggers.
- Attendance streak triggers.
- Coach follow-up triggers.
- Anniversary triggers.
- Referral candidate triggers.
- Community story identification.
- Community Health Dashboard.

AI may prepare candidates, reminders, outlines, and review-ready drafts.

AI may not select winners, publish recognition content, send outreach, ask for referrals automatically, decide retention actions, or use personal stories publicly without human approval and member consent.

## Future Wodify Data Intelligence Layer

The repository should eventually support Wodify CSV analysis for member engagement, retention, class performance, financial snapshots, marketing feedback, and community health.

Start with CSV exports only. Do not build a direct Wodify API integration until credentials, documentation, and data permissions are available.

Expected future exports:

- members.csv
- attendance.csv
- memberships.csv
- payments.csv
- leads.csv
- classes.csv
- coaches.csv

Privacy rules:

- Do not commit real member data.
- Keep real exports outside git.
- Use fake sample data for testing.
- Remove, hash, or mask member identifiers when possible.
- AI may flag risk, but AI may not decide action.
- AI may not send outreach automatically.
- Human review is required before member communication.
