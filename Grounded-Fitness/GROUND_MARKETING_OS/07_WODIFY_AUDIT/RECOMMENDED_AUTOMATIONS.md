# Recommended Automations

These are audit recommendations only. Do not build automation yet.

Live Wodify Library context:

- Recipe Used: 1.
- Recipe Limit: 2.
- Several relevant recipes are already `Up to Date`.
- Several relevant recipes show `Update`.
- Some attractive recipes show `Install`, but install decisions should wait until billable recipe impact is confirmed.

Live Workflow Email Templates context:

- 73 templates observed.
- Visible templates include Functional Fitness, Universal, and Jiu Jitsu families.
- Visible templates include nurture, reactivation, appointment, PR, referral, recap, request-handling, reinstatement, and suspension copy.
- Template usage, activation status, and workflow mapping are `Unknown`.

Live Wodify Communication context:

- Automated Emails showed 79 records.
- Marketing Emails showed 4 visible items: 3 drafts and 1 sent email.
- The sent marketing email showed 89 delivered and 1 bounced.
- General Templates showed 1 draft and 0 published templates.
- In-App Chat is on.
- Calendar Events are on.
- Automated email defaults use `info@wodifymail.com`, from name `Grounded Fitness`, and reply-to `groundedfitnessacadiana@gmail.com`.

Live Workato environment context:

- 11 environment properties observed.
- Several public social-link properties are generic platform URLs.
- No API clients exist yet.
- Community Library includes many connectors, including AI/model connectors, but none are approved for MVP use.

For every proposed automation, answer:

1. Can Wodify already do this?
2. Should Wodify do this?
3. Should Grounded AI only recommend this?
4. Does this require custom development?

## Recommendation 0: Communication Readiness

- Business purpose: prevent avoidable brand, placeholder, deliverability, channel-overlap, and configuration issues before activating or updating Wodify communication workflows.
- Trigger logic: before any workflow recipe install, update, or activation.
- Action logic: human reviews template copy, automated email settings, marketing email drafts, environment properties, placeholders, from/reply-to values, and offer accuracy.
- Bucket: A for Wodify communication/config ownership; B for Grounded AI audit and draft recommendations.

Answers:

1. Can Wodify already do this? Yes. Wodify already owns Marketing Emails, Automated Emails, Templates, Workflow Email Templates, In-App Chat, Calendar Events, and communication settings.
2. Should Wodify do this? Yes. Wodify should remain the place where communication settings, templates, and sends are stored and executed.
3. Should Grounded AI only recommend this? Yes. Grounded AI should audit copy, tone, brand fit, missing placeholders, channel fit, and outdated offers.
4. Does this require custom development? No.

Recommended next step: audit Wodify Communication settings, the 79 automated emails, the 73 workflow email templates, the 3 marketing email drafts, the 1 reusable template draft, and generic environment properties before recipe activation decisions.

## Recommendation 1: Lead Welcome

- Business purpose: acknowledge new leads quickly.
- Trigger logic: lead created.
- Action logic: send welcome email.
- Bucket: A for execution; B for copy review and source analysis.

Answers:

1. Can Wodify already do this? Yes.
2. Should Wodify do this? Yes.
3. Should Grounded AI only recommend this? Yes, for copy quality, source-specific context, and performance review.
4. Does this require custom development? No.

Recommended next step: audit current Wodify lead welcome copy and confirm consent/timing.

## Recommendation 2: Intro Appointment Reminder

- Business purpose: reduce intro no-shows.
- Trigger logic: 24 hours before appointment.
- Action logic: send SMS reminder.
- Bucket: A for execution; B for no-show analysis.

Answers:

1. Can Wodify already do this? Yes.
2. Should Wodify do this? Yes.
3. Should Grounded AI only recommend this? Yes, for wording and no-show trend analysis.
4. Does this require custom development? No.

Recommended next step: confirm reminder timing, consent, and message tone in Wodify.

## Recommendation 3: At-Risk Member Follow-Up

- Business purpose: reduce churn and support attendance consistency.
- Trigger logic: no attendance in 14 days.
- Action logic: Wodify creates a task, assigns a coach, and adds an At Risk tag.
- Bucket: A for simple trigger execution; B for prioritization and context.

Preferred flow:

```text
No attendance in 14 days
↓
Task created
↓
Coach assigned
↓
At Risk tag added
↓
Appears in Weekly Coach Brief
```

Answers:

1. Can Wodify already do this? Yes for no-attendance trigger, task creation, coach assignment if configured, and tag action if supported in the workflow.
2. Should Wodify do this? Yes. Wodify should execute the trigger, task, assignment, and At Risk tag because Wodify owns attendance, tasks, staff assignment, and tags.
3. Should Grounded AI only recommend this? Yes. Grounded AI should read the task/tag signal and include the member in the Weekly Coach Brief with context and suggested coach-led language.
4. Does this require custom development? No during audit/MVP.

Recommended next step: audit whether the current Wodify Workflow Builder configuration can add the At Risk tag and assign the correct coach after 14 days of no attendance. If yes, use Wodify for execution and Grounded AI for the Weekly Coach Brief.

## Recommendation 3A: Client Nurture Recipe Review

- Business purpose: better utilize Wodify's built-in client engagement and retention workflows.
- Observed library status: Client Nurture Universal shows Update; Client Nurture Functional Fitness shows Update.
- Bucket: A for Wodify execution; B for Grounded AI review.

Answers:

1. Can Wodify already do this? Likely yes. The Wodify Library explicitly includes Client Nurture for engagement and retention.
2. Should Wodify do this? Yes, if the recipe matches Grounded's retention logic and tone.
3. Should Grounded AI only recommend this? Yes. Grounded AI should audit the recipe contents, compare against desired coach-led follow-up, and draft copy improvements.
4. Does this require custom development? No.

Recommended next step: inspect Client Nurture before designing any custom retention automation.

## Recommendation 4: Missed Class Follow-Up

- Business purpose: recover no-shows and show care.
- Trigger logic: client no-showed.
- Action logic: send check-in email.
- Bucket: A for baseline execution; B for exception analysis.

Answers:

1. Can Wodify already do this? Yes.
2. Should Wodify do this? Sometimes. It should be used when tone is supportive and consent/context are clear.
3. Should Grounded AI only recommend this? Yes for repeated no-shows, sensitive cases, and draft improvements.
4. Does this require custom development? No.

Recommended next step: review current missed-class copy for guilt-based wording.

## Recommendation 5: Membership Expiry Warning

- Business purpose: reduce accidental churn.
- Trigger logic: 7 days before membership expiry.
- Action logic: send renewal email.
- Bucket: A for standard execution; B for exception review.

Answers:

1. Can Wodify already do this? Yes.
2. Should Wodify do this? Yes for standard renewal contexts.
3. Should Grounded AI only recommend this? Yes for owner review of holds, cancellations, and sensitive membership states.
4. Does this require custom development? No.

Recommended next step: confirm Wodify renewal workflow excludes inappropriate member states.

## Recommendation 6: Unpaid Invoice Reminder

- Business purpose: reduce overdue balances.
- Trigger logic: invoice 7 days overdue.
- Action logic: send reminder email.
- Bucket: A for execution; B for owner summary.

Answers:

1. Can Wodify already do this? Yes.
2. Should Wodify do this? Yes, because Wodify owns invoices and transactions.
3. Should Grounded AI only recommend this? Yes, Grounded AI should summarize patterns and suggest owner review.
4. Does this require custom development? No.

Recommended next step: keep financial communication inside Wodify and only use Grounded AI for owner-level reporting.

## Recommendation 7: Birthday Recognition

- Business purpose: member recognition.
- Trigger logic: client birthday.
- Action logic: send birthday message.
- Bucket: A for birthday execution; B for broader recognition intelligence.

Answers:

1. Can Wodify already do this? Yes.
2. Should Wodify do this? Yes for basic birthday messages.
3. Should Grounded AI only recommend this? Yes for improved copy and additional recognition opportunities.
4. Does this require custom development? No.

Recommended next step: use Grounded AI to identify recognition moments beyond birthdays, but leave execution in Wodify or human-approved channels.

## Recommendation 8: Member Milestone Recognition

- Business purpose: increase belonging and retention.
- Trigger logic: 25, 50, 100, 250, or 500 visits; 1/2/3 year anniversary.
- Action logic: Wodify Attendance Milestones can recognize key class and appointment milestones.
- Bucket: A for Attendance Milestones execution; B for Grounded AI recognition reporting.

Answers:

1. Can Wodify already do this? Yes for key class and appointment milestones; Functional Fitness Attendance Milestones is observed as Up to Date.
2. Should Wodify do this? Yes. Wodify owns class and appointment counts.
3. Should Grounded AI only recommend this? Yes during MVP. Grounded AI should produce Member Milestone Report and Member of the Month Candidate Report.
4. Does this require custom development? No.

Recommended next step: inspect Attendance Milestones configuration and map its outputs into the Grounded AI Member Milestone Report.

## Recommendation 8A: Weekly Streaks Review

- Business purpose: celebrate attendance consistency.
- Observed library status: Weekly Streaks Universal shows Update; Weekly Streaks Functional Fitness shows Install.
- Bucket: A for Wodify execution; B for Grounded AI recognition and coach brief context.

Answers:

1. Can Wodify already do this? Yes, Wodify has Weekly Streaks recipes.
2. Should Wodify do this? Yes if the tone, frequency, and recipe-limit impact fit Grounded's retention strategy.
3. Should Grounded AI only recommend this? Yes. Grounded AI should use streaks in owner/coach briefs and recognition candidate reports.
4. Does this require custom development? No.

Recommended next step: confirm whether updating Universal or installing Functional Fitness is the better path under the 2-recipe limit.

## Recommendation 9: Weekly Owner Brief

- Business purpose: make Wodify easier for leadership to interpret.
- Trigger logic: weekly reporting cadence.
- Action logic: compare Wodify Daily Brief with Grounded AI markdown report from exports.
- Bucket: B.

Answers:

1. Can Wodify already do this? Maybe. The Wodify Library includes Daily Brief Universal, but it is not installed and its contents are not confirmed.
2. Should Wodify do this? Wodify should do it if Daily Brief gives the owner enough useful operational visibility.
3. Should Grounded AI only recommend this? Yes. Grounded AI should compare the Daily Brief recipe against the desired Weekly Owner Brief.
4. Does this require custom development? No for CSV-based markdown report generation.

Recommended next step: inspect Daily Brief before building a custom owner brief workflow.

## Recommendation 10: Weekly Coach Brief

- Business purpose: help coaches know who needs attention.
- Trigger logic: weekly reporting cadence.
- Action logic: generate coach-facing markdown brief from exports.
- Bucket: B.

Answers:

1. Can Wodify already do this? Wodify has Coachboard/Kiosk and tasks, but a weekly coach brief is not confirmed.
2. Should Wodify do this? Wodify should execute tasks and hold source records.
3. Should Grounded AI only recommend this? Yes, Grounded AI should generate the brief and suggested talking points.
4. Does this require custom development? No for markdown brief from exports.

Recommended next step: include coach brief in the CSV MVP and do not automate task creation.

## Summary Matrix

| Opportunity | Bucket | Execution Owner | Grounded AI Role | Custom Dev |
|---|---|---|---|---|
| Communication readiness | A/B | Wodify | Copy/config/channel audit | No |
| Lead welcome | A/B | Wodify | Copy/source analysis | No |
| Intro reminder | A/B | Wodify | No-show analysis | No |
| Missed class follow-up | A/B | Wodify | Exception analysis | No |
| Membership expiry | A/B | Wodify | Exception analysis | No |
| Re-engagement | A/B | Wodify | Prioritization/reporting | No |
| Client Nurture | A/B | Wodify | Recipe audit/copy review | No |
| Unpaid invoice | A/B | Wodify | Owner summary | No |
| Birthday | A/B | Wodify | Recognition intelligence | No |
| Attendance milestones | A/B | Wodify | Candidate reports | No |
| Weekly streaks | A/B | Wodify if installed/updated | Recognition/brief context | No |
| Weekly Owner Brief | B | Grounded AI report | Analysis/recommendation | No |
| Weekly Coach Brief | B | Grounded AI report | Analysis/recommendation | No |

## Recipe-Limit Priority

Because the live account shows Recipe Used 1 and Recipe Limit 2, the recommended utilization order is:

1. Inspect and use recipes already marked `Up to Date`, especially Attendance Milestones, Client Progressions, Performance Results, Drop-In Management, Workflow Buttons, Wodify Sites Functional Fitness, and Starter Pack.
2. Audit Wodify Communication settings, Automated Emails, Marketing Emails, Templates, Workflow Email Templates, and environment properties before letting any recipe send member-facing messages.
3. Review `Update` recipes before installing anything new, especially Client Nurture, Lead Nurture, Invoice Enforcement, Membership Management, and Weekly Streaks Universal.
4. Only consider new installs after confirming recipe-limit impact, with Daily Brief and Weekly Streaks Functional Fitness as the most strategically relevant candidates.
5. Keep API clients at zero and community connectors disconnected during MVP.
6. Avoid any custom Grounded AI automation until the Wodify recipe library has been audited and configured.

## Final Recommendation

Do not build automation yet.

Audit Wodify Workflow Builder configuration first.

Audit Wodify Communication settings before changing or activating email workflows.

Use Wodify for execution.

Use Grounded AI for analysis, recommendations, owner briefs, coach briefs, and draft content.
