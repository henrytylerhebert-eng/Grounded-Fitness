# Automation Gap Analysis

This document identifies where Wodify Workflow Builder appears sufficient, where Grounded AI should add intelligence, and where custom development might eventually be considered.

## Confirmed Baseline

Wodify already supports automation structure:

- Trigger.
- Action.
- On/off toggle.

Wodify action types include:

- Email.
- SMS.
- Task creation.
- Tag.

The live Wodify Library also shows pre-built recipes for milestones, nurture, progressions, daily briefs, drop-ins, invoice enforcement, lead nurture, membership management, performance results, workflow buttons, website form integrations, weekly streaks, and starter templates.

The current account view shows Recipe Used 1 and Recipe Limit 2. The exact relationship between library status labels and billable recipe usage is `Unknown`.

The Workflow Email Templates screen shows 73 templates, including Functional Fitness and Universal client nurture, appointment, performance, reactivation, referral, recap, request-handling, reinstatement, and suspension templates. Template activation status and exact workflow usage are `Unknown`.

The Communication screens show additional Wodify communication execution surfaces: Marketing Emails, Automated Emails, reusable Templates, In-App Chat, Calendar Events, and Communication Settings.

Observed Communication state includes 79 automated email records, 4 visible marketing email items, 1 sent marketing email with 89 delivered and 1 bounced, 3 marketing email drafts, 1 reusable template draft, In-App Chat on, Calendar Events on, and automated email defaults configured.

The Environment Properties screen shows generic social links, Wodify internal identifiers, and formatting/link properties that may be used by recipes. These should be reviewed before workflow emails are activated or updated.

The API Clients screen shows no API clients yet. This supports the current no-live-API boundary.

## What Wodify Already Covers Well

Bucket A: Use Wodify Workflow Builder.

- Attendance milestones.
- Weekly streaks.
- Client nurture.
- Client progressions.
- Drop-in management.
- Lead nurture.
- Invoice enforcement.
- Membership management.
- Performance results.
- Workflow buttons.
- Wodify Sites form integration.
- Automated transactional emails.
- Marketing email sending.
- Reusable email templates.
- In-app chat.
- Calendar-event delivery.
- New lead welcome.
- Intro appointment reminder.
- Missed class follow-up.
- Membership expiry warning.
- Re-engagement after no attendance.
- Unpaid invoice reminder.
- Birthday message.
- Lead not contacted task.
- Membership expiring soon task.
- Client has not attended task.
- Unpaid invoice past due task.
- At Risk tag assignment after no attendance if supported by current Workflow Builder configuration.
- Workflow email template storage and reuse.

These should not be rebuilt in Grounded AI.

## Where Grounded AI Adds Value

Bucket B: Use Grounded AI analysis and recommendation.

Grounded AI should help with:

- Prioritizing which at-risk members need coach-led attention first.
- Explaining why a member was flagged.
- Separating source facts from inferred risk.
- Identifying sensitive exceptions before automated messages go out.
- Drafting more human, coach-led copy for Wodify workflows.
- Summarizing workflow performance for the owner.
- Surfacing missing data.
- Identifying recognition opportunities beyond standard birthday automation.
- Recommending which Wodify workflows should be reviewed or activated.
- Comparing lead source quality and stale lead patterns.
- Producing owner and coach briefs from Wodify exports.
- Comparing installed/up-to-date Wodify recipes against Grounded's desired operating workflows.
- Recommending which existing Wodify recipes to update, inspect, or leave alone.
- Creating a recipe-priority plan under the 2-recipe limit.
- Auditing workflow email templates for tone, placeholders, brand language, and offer accuracy before Wodify sends them.
- Auditing automated email defaults, from/reply-to settings, and communication channel overlap.
- Summarizing observed marketing email delivery results without inventing outcomes.
- Flagging generic environment properties that could leak into member-facing emails.

Grounded AI should not execute the automation.

## Potential Gaps That May Need More Evidence

These are not custom-development approvals. They are areas to validate.

### Context-Aware Re-Engagement Scoring

Question: Can Wodify segment and trigger on enough fields to distinguish true disengagement from holds, travel, injury, or known staff context?

Likely bucket now: Bucket B.

Potential future bucket: Bucket C only if export-based reports and Wodify segments cannot support the decision need.

Preferred baseline flow before any custom scoring:

```text
No attendance in 14 days
↓
Task created in Wodify
↓
Coach assigned in Wodify
↓
At Risk tag added in Wodify
↓
Appears in Weekly Coach Brief through Grounded AI
```

Gap to verify: whether Wodify can assign the correct coach and add the At Risk tag from the existing Workflow Builder configuration. If this is available, it remains Bucket A for execution and Bucket B for Grounded AI brief inclusion.

### Recognition Candidate Ranking

Question: Can Wodify automatically combine attendance milestones, anniversaries, performance signals, coach nominations, and community contribution?

Likely bucket now: Bucket B.

Potential future bucket: Bucket C only for a future dashboard if Wodify exports cannot support a usable workflow.

### Owner Weekly Brief

Question: Does Wodify Daily Brief already produce a useful owner brief across attendance, leads, revenue, recognition, and retention?

Known from source: Wodify has report collections and the live library includes a Daily Brief recipe, but the recipe contents are not confirmed.

Likely bucket now: Bucket B.

Potential future bucket: Bucket C only if automated report generation becomes necessary after CSV validation.

### Coach Brief

Question: Does Wodify Daily Brief or Client Nurture already produce coach-specific action briefs?

Known from source: Wodify has Coachboard/Kiosk, tasks, Client Nurture, and Daily Brief, but a weekly coach brief matching Grounded's desired format is not confirmed.

Likely bucket now: Bucket B.

Potential future bucket: Bucket C only if a dedicated coach-facing surface is approved.

### Workflow Performance Audit

Question: Does Wodify expose automation performance, message engagement, task completion, and conversion by workflow?

Known from source: Unknown.

Likely bucket now: Bucket B.

Potential future bucket: Bucket C only if Wodify exports/API cannot provide enough audit visibility.

### Workflow Email Template Quality

Question: Which of the 73 workflow email templates are actively used, and are they on-brand for Grounded Fitness Acadiana?

Known from source: Wodify has Functional Fitness and Universal templates for nurture, reactivation, appointments, PRs, referrals, monthly recap, request handling, reinstatement, and suspension.

Likely bucket now: Bucket B.

Potential future bucket: Bucket C is not justified. The need is template audit and copy review, not custom email infrastructure.

### Communication Channel Overlap

Question: Which messages belong in Workflow Builder, Automated Emails, Marketing Emails, Templates, In-App Chat, or Calendar Events?

Known from source: Wodify has multiple communication modules, including 79 automated emails, marketing emails, templates, in-app chat, and calendar events.

Likely bucket now: Bucket B.

Potential future bucket: Bucket C is not justified. The need is a communication map and governance rule, not custom sending infrastructure.

### Marketing Email Performance Interpretation

Question: Can Grounded AI evaluate marketing email performance?

Known from source: one visible sent marketing email showed 89 delivered and 1 bounced. No opens, clicks, conversions, revenue, retention, or replies were observed.

Likely bucket now: Bucket B for summary only.

Potential future bucket: Bucket C only if Wodify cannot export enough email performance data and a custom reporting surface is explicitly approved.

Required language: No measurements found for conversion, revenue, retention, opens, clicks, or replies unless those metrics are exported or observed.

### Environment Configuration Hygiene

Question: Are the environment properties safe and current enough for recipe activation?

Known from source: Facebook, Instagram, X, and Youtube properties currently show generic platform URLs. Internal identifiers and profile-link bases are present.

Likely bucket now: Bucket A for Wodify/Workato config cleanup; Bucket B for Grounded AI audit notes.

Potential future bucket: Bucket C is not justified.

### API And Connector Readiness

Question: Should Grounded AI connect to Workato APIs, community connectors, or AI model connectors now?

Known from source: no API clients exist. The community library includes many AI/model/data connectors, but connector availability is not approval.

Likely bucket now: Out of scope.

Potential future bucket: Bucket C only after explicit approval, least-privilege role design, credential handling, privacy review, and read-only access planning.

## Custom Development Threshold

Bucket C requires all of the following:

- Wodify cannot already execute the workflow.
- Wodify exports and Grounded AI reports cannot solve the decision need.
- The workflow has been validated manually.
- Human review rules are defined.
- Privacy and consent rules are defined.
- The user explicitly approves custom development.

No automation qualifies for Bucket C during this audit.

## Highest-Priority Utilization Gaps

These are not build tasks. They are Wodify utilization questions.

1. Which recipe currently counts as the 1 used recipe?
2. Do `Update` actions consume billable recipe capacity or only refresh installed recipes?
3. What exactly is included in Client Nurture Functional Fitness?
4. What exactly is included in Daily Brief Universal?
5. Can Attendance Milestones feed recognition workflows without custom development?
6. Can Weekly Streaks Functional Fitness be used without exceeding the recipe limit?
7. Can Lead Nurture Universal be updated instead of building any lead nurture logic in Grounded AI?
8. Can Wodify Sites Functional Fitness already cover website form submissions?
9. Which of the 73 workflow email templates are currently tied to active workflows?
10. Which templates include generic placeholders, outdated offers, or off-brand tone?
11. Which Automated Emails are active and which are default Wodify system emails?
12. Which Marketing Email drafts should be deleted, archived, finished, or ignored?
13. Is `Grounded Fitness` the correct default from name, or should it be `Grounded Fitness Acadiana`?
14. Is `groundedfitnessacadiana@gmail.com` actively monitored for replies?
15. Which environment properties are used in active recipes?
16. Should generic social links be updated before any recipe sends member-facing messages?
17. Should collaborator access be reviewed before any API or connector work?

## Key Risks

- Duplicating Wodify functionality.
- Creating a second source of truth.
- Automating sensitive member communication too early.
- Overloading staff with tasks.
- Sending generic or guilt-based messages.
- Sending Wodify templates with unresolved placeholders such as `First Name` or `Location Name`.
- Sending outdated offers or generic social links.
- Confusing Workflow Email Templates, Automated Emails, reusable Templates, and Marketing Emails.
- Interpreting delivery counts as business outcomes without evidence.
- Changing communication settings that affect operational emails.
- Ignoring Wodify consent and communication history.
- Connecting community AI tools or API clients before privacy and least-privilege review.
- Building custom software before validating Wodify Workflow Builder capabilities.

## Audit Conclusion

Most execution automation belongs in Wodify.

Most interpretation, prioritization, reporting, and drafting belongs in Grounded AI.

Custom development should be deferred.
