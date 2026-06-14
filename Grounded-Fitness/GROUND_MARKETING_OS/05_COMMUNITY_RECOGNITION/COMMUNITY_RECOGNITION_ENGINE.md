# Community & Recognition Engine

The Community & Recognition Engine strengthens belonging, recognition, referrals, retention, and community engagement.

This engine treats culture as an operating system. Some of the most important member communication is not marketing content; it is recognition, coaching, relationships, and staff follow-through.

## Build Status

Status: Future module documented only.

Current boundary: Do not automate public posting, member outreach, referral requests, or recognition decisions.

AI may prepare candidates, reminders, outlines, and review-ready drafts.

Humans select winners, approve communication, and decide action.

## Purpose

The Community & Recognition Engine should help Grounded:

- Recognize members who show consistency, progress, leadership, and community contribution.
- Help members feel seen between workouts.
- Surface coach follow-up opportunities.
- Support referrals through genuine ambassador identification.
- Protect community culture.
- Create retention through belonging, not pressure.

## Inputs

### Wodify

- Attendance.
- Milestones.
- Anniversaries.
- PRs if tracked.
- Class participation.
- Consistency.

### Coaches

- Observations.
- Leadership.
- Attitude.
- Encouragement.
- Community contribution.

### Staff

- Nominations.
- Testimonials.
- Stories.

## Outputs

### Member Of The Month Workflow

This should be a formal monthly workflow, not an unstructured question of who to pick.

Monthly trigger:

AI prepares:

- Top attendance candidates.
- Most improved candidates.
- Community impact candidates.
- Coach nominations.

Human selects the winner.

After human selection, the system can create review-ready drafts for:

- Facebook post.
- Instagram post.
- Website story.
- Google Business Profile post.
- Email feature.
- Member spotlight video outline.

No draft is published without human approval.

### Member Milestone Engine

Milestone triggers should create coach or staff recognition opportunities.

Initial visit milestones:

- 25 visits: coach notified.
- 50 visits: social post candidate.
- 100 visits: recognition candidate.
- 250 visits: major celebration.
- 500 visits: legacy member.

Membership anniversaries:

- 1 year: recognition opportunity.
- 2 years: recognition opportunity.
- 3 years: recognition opportunity.

Milestones are candidates for recognition, not automatic posts.

### Staff & Coach Trigger System

This system should help staff operationalize personal follow-up without automating the relationship.

New member triggers:

- 3 visits: coach reminder to check in.
- 10 visits: coach reminder to celebrate progress.
- 30 days: coach reminder to schedule a conversation.

Attendance drop trigger:

- Example: a member previously attended 4x per week and now attends 1x per week.
- System flags the member for coach-led outreach.
- Outreach is not automated.

### Coach Content Trigger Engine

Each week, the system should identify possible community stories and content opportunities.

Story examples:

- Member returned after injury.
- First pull-up.
- First push-up.
- Consistency streak.
- Weight-loss milestone.
- Confidence story.

Important boundary: health, injury, weight-loss, and personal stories require human confirmation and member consent before public use.

### Community Calendar Engine

The system should remind staff ahead of recurring community events.

Examples:

- Murph.
- Bring A Friend Week.
- Nutrition Challenge.
- Holiday Workouts.
- Member Appreciation Month.
- Community Service Event.

Reminder outputs should be staff-facing planning prompts, not automatic campaigns.

### Referral Trigger Engine

Referral requests should not go to everyone.

Look for ambassador signals:

- High attendance.
- Positive engagement.
- Testimonials.
- Milestone completion.
- Community contribution.
- Coach nomination.

AI may suggest referral candidates. A human decides whether and how to ask.

## Community Health Dashboard

Future dashboard should track:

- Member of the Month history.
- Milestone counts.
- Coach check-ins.
- Referrals.
- Anniversaries.
- Recognition opportunities.
- Attendance streaks.

Dashboard status: Future. Do not build yet.

## Acceptance Criteria For A Future Manual Pilot

A manual Community & Recognition pilot is ready when:

- Wodify can provide attendance, milestone, anniversary, and class participation data, or missing fields are marked `Unknown`.
- Coaches can submit observations or nominations.
- Staff can submit stories or testimonials.
- AI can prepare candidate lists without deciding winners.
- A human can select Member of the Month.
- Recognition drafts can be reviewed before publishing.
- Coach follow-up reminders can be reviewed before action.
- Referral candidates can be approved before any ask is made.
- Missing measurements are marked `No measurements found`.

## Boundaries

AI may:

- Surface recognition candidates.
- Identify milestone candidates.
- Flag attendance streaks and attendance drops.
- Draft recognition content for review.
- Prepare coach reminder suggestions.
- Suggest referral candidates.
- Identify community story opportunities.

AI may not:

- Select Member of the Month.
- Publish recognition content.
- Send member outreach.
- Ask for referrals automatically.
- Decide retention actions.
- Use personal stories publicly without human approval and member consent.
- Make health promises.
- Diagnose members.
- Alter Wodify records.
