# Recipe Analysis

Each automation recipe is analyzed using the required decision questions:

1. Can Wodify already do this?
2. Should Wodify do this?
3. Should Grounded AI only recommend this?
4. Does this require custom development?

## Classification Buckets

### Bucket A: Use Wodify Workflow Builder

Use when Wodify already has the trigger and action logic, especially for execution tasks like email, SMS, tags, and staff tasks.

### Bucket B: Use Grounded AI Analysis And Recommendation

Use when the value is interpretation, prioritization, reporting, draft content, exception handling, or decision support.

### Bucket C: Requires Custom Development

Use only when Wodify cannot support the workflow and Grounded has explicitly approved building something custom.

## Current Wodify Library Implication

The live Wodify Library view shows that many workflows already exist as pre-built recipes. This shifts the automation strategy further toward Wodify utilization:

- Use existing `Up to Date` recipes before designing custom automation.
- Review `Update` recipes before installing new recipes.
- Treat `Install` recipes as candidates only after checking the 1-of-2 recipe limit and business priority.
- Use Grounded AI to decide what to inspect, compare, and improve.

Observed high-relevance recipes:

- Attendance Milestones.
- Client Nurture.
- Client Progressions.
- Daily Brief.
- Drop-In Management.
- Invoice Enforcement.
- Lead Nurture.
- Membership Management.
- Performance Results.
- Weekly Streaks.
- Workflow Buttons.
- Wodify Sites.

## New Lead Welcome

- Existing recipe: yes.
- Trigger logic: lead created.
- Action logic: send welcome email.
- Business purpose: immediate lead acknowledgement.
- Risks: generic copy, wrong source context, duplicate outreach.
- Opportunities: improve message quality and monitor source performance.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Yes, if consent and copy are correct.
- Should Grounded AI only recommend this? Grounded AI should recommend copy improvements and source-specific variants, not send.
- Does this require custom development? No.

Classification: Bucket A for execution; Bucket B for copy and performance analysis.

## Intro Appointment Reminder

- Existing recipe: yes.
- Trigger logic: 24 hours before appointment.
- Action logic: send SMS reminder.
- Business purpose: reduce no-shows.
- Risks: consent, appointment state accuracy, message fatigue.
- Opportunities: no-show analysis and reminder wording review.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Yes, Wodify owns appointments and communications.
- Should Grounded AI only recommend this? Yes, Grounded AI can recommend copy and timing improvements.
- Does this require custom development? No.

Classification: Bucket A for execution; Bucket B for analysis.

## Missed Class Follow-Up

- Existing recipe: yes.
- Trigger logic: client no-showed.
- Action logic: send check-in email.
- Business purpose: fast follow-up after missed class.
- Risks: guilt tone, false context, member frustration.
- Opportunities: identify when coach-led outreach is better than automation.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Sometimes. Simple no-shows can stay in Wodify; sensitive cases should be coach-led.
- Should Grounded AI only recommend this? For high-context or repeated misses, yes.
- Does this require custom development? No for basic follow-up; maybe later if Grounded wants advanced scoring unavailable in Wodify.

Classification: Bucket A for baseline no-show automation; Bucket B for prioritization.

## Membership Expiry Warning

- Existing recipe: yes.
- Trigger logic: 7 days before membership expiry.
- Action logic: send renewal email.
- Business purpose: reduce accidental churn.
- Risks: wrong membership context, hold/cancellation sensitivity, transactional tone.
- Opportunities: exception list for owner review.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Yes for standard renewals.
- Should Grounded AI only recommend this? Yes for sensitive or unusual member states.
- Does this require custom development? No.

Classification: Bucket A for standard renewal reminder; Bucket B for exception reporting.

## Re-Engagement

- Existing recipe: yes.
- Trigger logic: no attendance in 14 days.
- Action logic: send check-in and create staff task.
- Business purpose: reduce churn through timely follow-up.
- Risks: impersonal outreach, known holds/injury ignored, task overload.
- Opportunities: rank by risk, context, tenure, and prior attendance pattern.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Yes for baseline trigger execution, if configured carefully.
- Should Grounded AI only recommend this? Grounded AI should recommend priority, message angle, and exceptions.
- Does this require custom development? Not for basic workflow; custom development only if future scoring cannot be handled with exports and reports.

Classification: Bucket A for trigger/action; Bucket B for intelligence layer.

## Attendance Milestones

- Existing library recipe: yes.
- Observed status: Functional Fitness is Up to Date.
- Business purpose: recognize key class and appointment milestones.
- Risks: generic recognition, public recognition without consent, milestone overload.
- Opportunities: Grounded AI can use milestone outputs/signals for Member Milestone Report and Member of the Month Candidate Report.

Decision questions:

- Can Wodify already do this? Yes, the Functional Fitness recipe is observed as Up to Date.
- Should Wodify do this? Yes, Wodify owns attendance, appointment counts, and milestone automation.
- Should Grounded AI only recommend this? Yes. Grounded AI should summarize milestone candidates and draft recognition copy for review.
- Does this require custom development? No.

Classification: Bucket A for milestone execution; Bucket B for recognition intelligence.

## Client Nurture

- Existing library recipe: yes.
- Observed status: Universal and Functional Fitness show Update.
- Business purpose: enhance client engagement and retention.
- Risks: duplicate re-engagement logic, over-messaging, generic retention sequences, recipe-limit impact.
- Opportunities: Grounded AI can audit whether Client Nurture covers the desired At Risk workflow and recommend whether to update it.

Decision questions:

- Can Wodify already do this? Likely yes, but exact recipe contents require inspection.
- Should Wodify do this? Yes for execution if the recipe matches Grounded's retention workflow.
- Should Grounded AI only recommend this? Yes. Grounded AI should compare desired retention logic against the recipe and suggest edits.
- Does this require custom development? No.

Classification: Bucket A if configured in Wodify; Bucket B for audit and recommendations.

## Daily Brief

- Existing library recipe: yes.
- Observed status: Install.
- Business purpose: daily overview of key client touchpoints.
- Risks: may count against the 2-recipe limit; may duplicate the planned Grounded AI owner/coach briefs; unknown contents.
- Opportunities: inspect before building any custom daily or weekly brief.

Decision questions:

- Can Wodify already do this? Possibly. The Wodify Library includes a Daily Brief recipe.
- Should Wodify do this? Maybe. Wodify should execute it if its built-in brief satisfies the need.
- Should Grounded AI only recommend this? Yes during audit. Grounded AI should compare Wodify Daily Brief against the desired Weekly Owner Brief and Weekly Coach Brief.
- Does this require custom development? No, not before inspecting the recipe.

Classification: Bucket A if Wodify Daily Brief is sufficient; Bucket B for comparison and brief synthesis.

## Weekly Streaks

- Existing library recipe: yes.
- Observed status: Universal shows Update; Functional Fitness shows Install.
- Business purpose: celebrate attendance consistency.
- Risks: may over-celebrate or feel automated; recipe-limit impact if installing Functional Fitness version; consent and tone.
- Opportunities: strong fit for recognition, retention, and community health reporting.

Decision questions:

- Can Wodify already do this? Yes, Wodify has Weekly Streaks recipes.
- Should Wodify do this? Yes if recognition tone and frequency fit Grounded's culture.
- Should Grounded AI only recommend this? Grounded AI should recommend who appears in coach/owner briefs and draft human-reviewed recognition content.
- Does this require custom development? No.

Classification: Bucket A for streak detection/execution; Bucket B for recognition recommendations.

## Unpaid Invoice

- Existing recipe: yes.
- Trigger logic: invoice 7 days overdue.
- Action logic: send reminder email.
- Business purpose: reduce unpaid balances.
- Risks: sensitive financial communication, wrong invoice state, relationship strain.
- Opportunities: owner brief summary of unpaid invoice patterns.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Yes, Wodify owns invoices and payment records.
- Should Grounded AI only recommend this? Yes, for owner-level review and tone suggestions.
- Does this require custom development? No.

Classification: Bucket A for execution; Bucket B for owner analysis.

## Birthday

- Existing recipe: yes.
- Trigger logic: client birthday.
- Action logic: send birthday message.
- Business purpose: relationship maintenance and recognition.
- Risks: generic message, wrong profile data, shallow personalization.
- Opportunities: broader recognition calendar and member milestone prompts.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Yes for basic birthday message.
- Should Grounded AI only recommend this? Grounded AI should suggest improved copy and richer recognition opportunities.
- Does this require custom development? No.

Classification: Bucket A for birthday execution; Bucket B for recognition intelligence.

## Lead Not Contacted In X Days

- Existing recipe context: common auto-generated task trigger.
- Trigger logic: lead has not been contacted in X days.
- Action logic: create staff task.
- Business purpose: prevent lead neglect.
- Risks: task noise, poor ownership, stale lead records.
- Opportunities: lead pipeline snapshot and stale lead prioritization.

Decision questions:

- Can Wodify already do this? Yes, according to source context.
- Should Wodify do this? Yes, Wodify owns lead status, communication history, and tasks.
- Should Grounded AI only recommend this? Grounded AI should recommend priority and flag data gaps.
- Does this require custom development? No.

Classification: Bucket A for task generation; Bucket B for prioritization.

## Client Has Not Attended In X Days

- Existing recipe context: common auto-generated task trigger and re-engagement automation.
- Trigger logic: no attendance in X days.
- Action logic: create staff task or send check-in.
- Business purpose: retention intervention.
- Risks: false positives, known holds, injury, travel, life events, too many tasks.
- Opportunities: Grounded AI can combine attendance decline, tenure, membership state, and prior consistency into a coach brief.

Decision questions:

- Can Wodify already do this? Yes.
- Should Wodify do this? Yes for baseline task creation.
- Should Grounded AI only recommend this? Yes for context-aware prioritization and messaging guidance.
- Does this require custom development? No for the audit/MVP phase.

Classification: Bucket A for simple trigger; Bucket B for intelligence.
