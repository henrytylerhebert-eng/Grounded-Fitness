# Grounded Marketing OS

Grounded Marketing OS is the community operations system for Grounded Fitness Acadiana's member communication, recognition, retention, and future local authority work.

Grounded Fitness Acadiana is a Lafayette, Louisiana functional fitness gym located at 401 East Cypress Street, Lafayette, LA 70501. The first build focus is the Member Value Engine: a repeatable internal workflow that turns weekly programming and attendance patterns into useful, coaching-led member communication.

## Golden Rule

Do not market Grounded Fitness Acadiana as CrossFit.

Public-facing and member-facing language must use terms like functional fitness, coaching, strength, community, longevity, and real-life fitness. Avoid CrossFit branding, gym-bro language, hype, and unsupported claims.

## Initial MVP

The MVP is not software first. The MVP is a repeatable operating workflow:

1. Receive weekly programming email.
2. Extract weekly training themes.
3. Segment members from Wodify attendance data.
4. Draft internal value-based member emails.
5. Human reviews.
6. Send.
7. Track attendance and engagement.

## Build Focus

Current focus: Member Value Engine only.

Out of scope for the initial build:

- Local Authority Engine.
- Lead Nurture Engine.
- Community & Recognition Engine implementation.
- New Member Success Engine.
- Coaching Standards Engine.
- Referral Engine.
- Exit Intelligence Engine.
- Member Success Framework.
- Community Partnership Engine.
- Executive Weekly Brief.
- Grounded Knowledge Base.
- Production integrations.
- Public content automation.
- Automatic member or lead outreach.
- Wodify Data Intelligence Layer implementation.
- Direct Wodify API integration.
- Wodify communication execution.
- Wodify Sites publishing automation.

## New Build Launch Framework

1. Validate before architecting.
2. Architect before building.
3. Build before automating.
4. Automate before scaling.
5. Measure before claiming success.

## Primary Business Channels

- Website: https://www.groundedfitnessacadiana.com/
- YouTube: @GroundedFitnessAcadiana
- Instagram: grounded_fitness_acadiana
- Facebook: https://www.facebook.com/GroundedFitnessAcadiana
- Google Business Profile: Grounded Fitness Acadiana
- Phone: (225) 810-6134

## Implementation Principle

This repository should first make the weekly member value workflow visible, repeatable, reviewable, and measurable. Software, integrations, and automation should only be added after the manual workflow proves useful.

## Future Engine Map

Grounded Marketing OS should eventually include:

- Member Value Engine.
- Local Authority Engine.
- Lead Nurture Engine.
- Community & Recognition Engine.
- Analytics Engine.

The detailed deferred roadmap is kept in `06_ROADMAP/FUTURE_DEVELOPMENT_ROADMAP.md`.

For Grounded, the Community & Recognition Engine may be more valuable than a traditional marketing module because recognition, coaching, relationships, and culture support retention.

## Future Data Layer

The repository should eventually support an Analytics Engine backed first by Wodify CSV exports for member engagement, retention, class performance, financial snapshots, marketing feedback, and community health.

Initial data strategy: CSV exports only. Direct Wodify API integration is deferred until credentials, documentation, and permissions are available.

Real member exports must not be committed.

## Wodify Audit

The Wodify audit lives in `07_WODIFY_AUDIT/`.

That folder is the source-system inventory for Wodify Workflow Builder, Workato, Wodify Communication, and Wodify Sites. It exists to prevent duplicate builds and premature automation.

Current rule: Wodify executes. Grounded AI analyzes, recommends, and drafts for human review.

## Architecture Posture

Future modules should influence data vocabulary without expanding the MVP. The repository should preserve room for core member records, attendance records, coach records, milestone records, recognition records, referral records, content records, and communication records.
