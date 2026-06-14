# Module Map

The Grounded Marketing OS will eventually contain multiple engines. Only the Member Value Engine is active in the initial build.

Future engine map:

- Member Value Engine.
- New Member Success Engine.
- Coaching Standards Engine.
- Referral Engine.
- Exit Intelligence Engine.
- Member Success Framework.
- Local Authority Engine.
- Lead Nurture Engine.
- Community Partnership Engine.
- Executive Weekly Brief.
- Grounded Knowledge Base.
- Community & Recognition Engine.
- Analytics Engine.
- Wodify Audit.

## Active Module

### Member Value Engine

Purpose: Create a repeatable weekly workflow that turns programming and attendance context into useful internal member emails.

Workflow:

1. Receive weekly programming email.
2. Extract weekly training themes.
3. Segment members from Wodify attendance data.
4. Draft internal value-based member emails.
5. Human reviews.
6. Send.
7. Track attendance and engagement.

Current status: Foundation only.

Automation status: Manual workflow first. Production integrations are not built.

## Future Modules

### New Member Success Engine

Purpose: Increase first 90-day retention.

Status: Roadmap only. Do not build yet.

Potential focus: first class, first week, first 10 visits, first 30-day check-in, benchmark tracking, and first event participation.

### Coaching Standards Engine

Purpose: Create a consistent Grounded experience regardless of coach.

Status: Roadmap only. Do not build yet.

Potential focus: coaching playbook, member interaction standards, follow-up standards, new member standards, recognition standards, and coach development resources.

### Referral Engine

Purpose: Create a structured referral system.

Status: Roadmap only. Do not build yet.

Potential focus: referral candidate identification, milestone-based referral triggers, member ambassador program, Bring-a-Friend campaigns, and referral tracking.

### Exit Intelligence Engine

Purpose: Understand why members leave.

Status: Roadmap only. Do not build yet.

Potential focus: exit interviews, cancellation categorization, attendance analysis before departure, churn pattern analysis, and win-back opportunities.

### Member Success Framework

Purpose: Define success beyond membership status.

Status: Roadmap only. Do not build yet.

Potential focus: health, performance, and lifestyle success categories.

### Local Authority Engine

Purpose: Turn Grounded's coaching knowledge into local, educational public content for Lafayette and Acadiana.

Status: Future. Do not build yet.

Future channels:

- Website/blog.
- Instagram.
- Facebook.
- YouTube.
- Google Business Profile.
- Canva creative production.

### Lead Nurture Engine

Purpose: Help prospective members learn about Grounded in a soft, informative, low-pressure way.

Status: Future. Do not build yet.

Future channels:

- Website forms.
- Email.
- Social content.
- Google Business Profile.

### Community Partnership Engine

Purpose: Build local authority through strategic partnerships.

Status: Roadmap only. Do not build yet.

Potential partners:

- Physical therapists.
- Chiropractors.
- Healthcare providers.
- Local businesses.
- Youth sports organizations.
- Schools.

### Executive Weekly Brief

Purpose: Provide Grounded leadership with a weekly operational summary.

Status: Roadmap only. Do not build yet.

Potential sections:

- New members.
- At-risk members.
- Attendance trends.
- Revenue snapshot.
- Member milestones.
- Community events.
- Marketing activity.
- Recommended actions.

### Grounded Knowledge Base

Purpose: Capture institutional knowledge.

Status: Roadmap only. Do not build yet.

Potential content:

- Coaching lessons.
- Success stories.
- FAQs.
- Objections.
- Nutrition questions.
- Member wins.
- Local insights.

### Wodify Data Intelligence Layer

Purpose: Analyze Wodify data for member engagement, retention, class performance, financial snapshots, marketing feedback, and community health.

Status: Future Analytics Engine foundation. Document only. Do not build yet.

Initial data strategy: CSV exports from Wodify.

Do not build a direct Wodify API integration until credentials, documentation, and data permissions are available.

First reports to build later:

- Grounded Weekly Command Report.
- Weekly Member Engagement Report.
- Attendance Risk Report.
- New Member 90-Day Report.
- Class Utilization Report.
- Revenue Snapshot Report.
- Lead Conversion Report.

### Wodify Audit

Purpose: Inventory what already exists in Wodify, Workato, Wodify Communication, and Wodify Sites before Grounded builds or automates anything.

Status: Active documentation module. Audit only. Do not build integrations or automations from this module during the MVP.

Current focus:

- Workflow Builder recipes.
- Workflow Email Templates.
- Workato environment properties.
- API client readiness.
- Communication settings and surfaces.
- Marketing Emails.
- Automated Emails.
- Reusable Templates.
- Wodify Sites blog and personalization.

Operating rule: Wodify remains the source of truth and execution layer. Grounded AI may analyze, recommend, and draft for review, but may not send, publish, toggle, install, update, or write back to Wodify.

### Community & Recognition Engine

Purpose: Strengthen belonging, recognition, referrals, retention, and community engagement.

Status: Phase 1.5 candidate. Not MVP, but likely high-priority after Member Value Engine validation.

This engine operationalizes recognition, coaching follow-up, relationships, and culture. For Grounded, it may be more valuable than a traditional local authority module because people rarely leave communities where they feel seen.

Future inputs:

- Wodify attendance, milestones, anniversaries, PRs if tracked, class participation, and consistency.
- Coach observations about leadership, attitude, encouragement, and community contribution.
- Staff nominations, testimonials, and stories.

Future workflows:

- Member of the Month.
- Member milestone triggers.
- Attendance streak triggers.
- Coach follow-up triggers.
- Anniversary triggers.
- Referral candidate triggers.
- Community story identification.
- Community calendar reminders.
- Community Health Dashboard.

Human decision rule: AI may prepare candidates and drafts, but coaches and staff make the final decision.

## Architectural Record Requirements

Design future data vocabulary so these records can be added later without redesigning the repository:

- Core member records.
- Attendance records.
- Coach records.
- Milestone records.
- Recognition records.
- Referral records.
- Content records.
- Communication records.

The MVP remains intentionally small.

## Integration Map

Future integration assumptions only:

- Gmail: source of truth for weekly programming emails.
- Wodify: source of truth for active members, attendance, member status, membership type, lead status, and class participation.
- Website/blog: future authority content.
- Canva: creative production.
- Instagram: future distribution.
- Facebook: future distribution.
- YouTube: future distribution.
- Google Business Profile: future local visibility and distribution.
- Wodify CSV exports: future analytics source for engagement, retention, class performance, financial snapshots, marketing feedback, and community health.

## Boundary Rule

No module should automate outreach, publishing, or record changes until the manual workflow has been validated and human approval rules are active.

Human approval is the source of truth for final content, member communication, publishing, and business decisions.
