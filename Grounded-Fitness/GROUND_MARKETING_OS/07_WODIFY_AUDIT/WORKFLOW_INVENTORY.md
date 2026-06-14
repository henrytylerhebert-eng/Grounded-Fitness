# Wodify Workflow Builder Inventory

Source context: `Grounded_Fitness_WodCore_Context.md`.

Purpose: identify automation capabilities that already exist inside Wodify before designing any custom Grounded AI automation.

## Audit Principle

Never rebuild Wodify.

Prefer:

1. Wodify execution.
2. Grounded AI analysis and recommendation.
3. Custom development only when Wodify cannot reasonably support the need.

## Confirmed Wodify Automation Structure

Wodify has a Workflow Builder for pre-configured automations.

Automation structure:

- Trigger: event or condition.
- Action: email, SMS, task creation, or tag.
- State: on/off toggle per automation.

## Confirmed Action Capabilities

Wodify Workflow Builder can execute:

- Email sends.
- SMS sends.
- Staff task creation.
- Tag actions.

Grounded AI must not execute these actions during the MVP.

## Observed Communication Layer State

Source: live Wodify Communication screens shared on June 12, 2026.

Wodify Communication includes multiple execution surfaces outside Workflow Builder:

- Marketing Emails.
- Automated Emails.
- Templates.
- Workflow Email Templates.
- In-App Chat.
- Calendar Events.
- Communication Settings.

Observed communication facts:

- Marketing Emails showed 4 visible items: 3 drafts and 1 sent email.
- The sent marketing email `We Started a` went to All Active Clients on Dec 22, 2025, with 89 delivered and 1 bounced.
- Automated Emails showed 79 records.
- Visible automated emails included anniversary, birthday, bank account verification, appointment cancellation, provider change, class cancellation, and appointment creation emails.
- General Templates showed 1 draft drag-and-drop template and 0 published templates.
- Communication Settings showed default automated email from address `info@wodifymail.com`, from name `Grounded Fitness`, and reply-to `groundedfitnessacadiana@gmail.com`.
- In-App Chat is on with 32/1000 storage used.
- Calendar Events are on for drop-ins, free trials, and free intros.
- Coach availability showed 16 ordered coach records.

Important note: these communication surfaces are Wodify-owned execution paths. Grounded AI may audit and draft, but must not send, schedule, publish, toggle, or configure communications during the MVP.

## Observed Workflow Email Templates

Source: live Wodify Workflow Email Templates screen shared on June 12, 2026.

Observed count:

- 73 workflow email templates.
- Visible templates were last edited by System User.
- Visible pages included Functional Fitness, Universal, and Jiu Jitsu template families.

Important note: template presence does not mean a workflow is active, approved, on-brand, or safe to send. It only confirms reusable email assets exist inside Wodify.

### Template Families Observed

| Family | Examples observed | Audit implication |
|---|---|---|
| Appointment | Upcoming appointment reminders for Functional Fitness, Universal, and Jiu Jitsu | Wodify likely already supports appointment reminder copy; audit timing, placeholders, and tone before use. |
| Performance / PR | Congrats on your new PR | Wodify has recognition copy for performance results; Grounded AI should only help audit or improve copy. |
| Client nurture | Movement tips, performance tips, healthy habits, motivation, restart jitters, journey framing | Strong evidence that Wodify already has retention/nurture content assets. Do not rebuild this as a custom email engine. |
| Reactivation | Reignite your fitness journey, We Miss You, How have you been | Review carefully for pressure, guilt, generic personalization, and offer accuracy. |
| Referral / advocacy | Help us spread the word, Congrats on retaining another client | Use only with explicit human approval and appropriate member context. |
| Recap | Monthly Recap | Compare against desired owner/member recap needs before designing custom recap communications. |
| Operations / request handling | We received your request, We have processed your request, Error processing your request | Confirm these are tied to Wodify Workflow Buttons or request flows before editing. |
| Membership state | Reinstated Client, Suspension Notice | Sensitive. Keep execution in Wodify and require owner review of tone and state rules. |

### Visible Template Examples

Functional Fitness / mixed-family examples observed:

- Reminder: Your Upcoming Appointment at Location Name.
- Congrats on your new PR.
- Your Upcoming Appointment at Location Name.
- Reignite Your Fitness Journey with a Free Class and More.
- 3 simple ways to get more movement in your day.
- 6 Tips to Improve Your Performance.
- Does it Ever Get Easier? A Perspective on Your Fitness Journey.
- Ever Have Those Days? Let's Turn Them Around.
- First Name, our best offer, just for you.
- How have you been, First Name?
- Ignite Your Journey.
- Life Hack: 5 quick and healthy recipes.
- Mastering the Lingo: Your Guide to Speaking the Language of Functional Fitness.
- Nurturing Your Healthy Habits: The 21/90 Rule.
- Overcoming the Restart Jitters: Your Journey Back to Fitness.
- Track Your Progress for Success.
- We Miss You, First Name.
- Your Motivation for Reaching Goals.
- Help us spread the word.
- Monthly Recap.

Universal examples observed:

- Reinstated Client.
- Suspension Notice.
- Congrats on Retaining Another Client.
- Reignite Your Fitness Journey with a Free Class and More.
- 3 simple ways to get more movement in your day.
- 6 Tips to Improve Your Performance.
- Does it Ever Get Easier? A Perspective on Your Fitness Journey.
- Error processing your request.
- Ever Have Those Days? Let's Turn Them Around.
- First Name, our best offer, just for you.
- How have you been, First Name?
- Ignite Your Journey.
- Life Hack: 5 quick and healthy recipes.
- Nurturing Your Healthy Habits: The 21/90 Rule.
- Overcoming the Restart Jitters: Your Journey Back to Fitness.
- Track Your Progress for Success.
- We have processed your request.
- We Miss You, First Name.
- We received your request.
- Your Motivation for Reaching Goals.

### Email Template Audit Rules

Before using any Wodify email template:

1. Confirm the workflow using it.
2. Confirm trigger timing and audience.
3. Confirm placeholders resolve correctly, especially `First Name` and `Location Name`.
4. Remove generic offer language unless the offer is currently approved.
5. Remove pressure, guilt, hype, or fake personalization.
6. Ensure public-facing language says functional fitness, coaching, strength, conditioning, movement quality, community, longevity, consistency, or real-life fitness.
7. Avoid CrossFit positioning and terms.
8. Require human review before any send or automation activation.

## Observed Wodify Library State

Source: live Wodify Workflow Builder screen shared on June 12, 2026.

Observed account limits:

- Recipe Used: 1.
- Recipe Limit: 2.
- Most Recent Update: Fri, Jun 12, 2026 9:37 AM.
- Next Update: Sat, Jun 13, 2026 11:37 AM.

Important note: the screen shows multiple recipes marked `Up to Date` while the billable recipe count says `1 of 2`. The exact billing/limit semantics are `Unknown` and should be confirmed inside Wodify before installing or activating additional recipes.

### Wodify Library Recipes Observed

| Recipe | Type | Description | Observed Status |
|---|---|---|---|
| Attendance Milestones | Functional Fitness | Recognize key class and appointment milestones | Up to Date |
| Attendance Milestones | Jiu-Jitsu | Recognize key class and appointment milestones | Install |
| Attendance Milestones | Universal | Recognize key class and appointment milestones | Install |
| Client Nurture | Universal | Enhance client engagement and retention | Update |
| Client Nurture | Functional Fitness | Enhance client engagement and retention | Update |
| Client Nurture | Jiu-Jitsu | Enhance client engagement and retention | Install |
| Client Progressions | Universal | Celebrate promotions and automate client progression management | Up to Date |
| Client Progressions | Functional Fitness | Celebrate promotions and automate client progression management | Up to Date |
| Client Progressions | Jiu-Jitsu | Celebrate promotions and automate client progression management | Install |
| Daily Brief | Universal | Daily overview of key client touchpoints | Install |
| Drop-In Management | Universal | Keeps drop-ins on time and turns them into fans | Up to Date |
| Facility Access | Universal | Unlock the door from your Wodify app | Install |
| Invoice Enforcement | Universal | Protect your business from non-paying clients | Update |
| Lead Nurture | Universal | Streamline the Lead to Member journey | Update |
| Lead Nurture | Functional Fitness | Streamline the Lead to Member journey | Install |
| Lead Nurture | Jiu-Jitsu | Streamline the Lead to Member journey | Install |
| Membership Management | Universal | Simplify onboarding and create upsell opportunities | Update |
| Performance Results | Functional Fitness | Celebrate personal records and automate client progression management | Up to Date |
| Performance Results | Jiu-Jitsu | Celebrate personal records and automate client progression management | Install |
| Performance Results | Universal | Celebrate personal records and automate client progression management | Install |
| Workflow Buttons | Universal | Let clients submit requests and trigger automations from the mobile app | Up to Date |
| Wodify Sites | Universal | Integrate with form submissions from your website | Install |
| Wodify Sites | Functional Fitness | Integrate with form submissions from your website | Up to Date |
| Wodify Sites | Jiu-Jitsu | Integrate with form submissions from your website | Install |
| Weekly Streaks | Universal | Celebrate attendance consistency through Weekly Streaks | Update |
| Weekly Streaks | Functional Fitness | Celebrate attendance consistency through Weekly Streaks | Install |
| Weekly Streaks | Jiu-Jitsu | Celebrate attendance consistency through Weekly Streaks | Install |
| Starter Pack | Universal | Templates to create custom recipes and test emails | Up to Date |

## Current Utilization Principle

The immediate strategy is not to build custom automation. It is to better utilize Wodify's existing library:

- Separate Wodify Workflow Builder recipes from Marketing Emails, Automated Emails, and reusable Templates.
- Audit workflow email templates before activating recipes that send them.
- Audit automated email defaults and communication settings before changing any recipe that sends email.
- Inspect recipes already marked `Up to Date`.
- Confirm which recipe is counted as the 1 active billable recipe.
- Confirm whether `Update` changes existing installed workflows or adds billable usage.
- Prioritize recipes tied directly to retention, recognition, lead conversion, and owner/coach visibility.
- Let Wodify execute automations.
- Let Grounded AI summarize, compare, recommend, and draft review-ready content.

## Existing Recipes From Source Context

### New Lead Welcome

- Trigger logic: lead created.
- Action logic: send welcome email.
- Business purpose: acknowledge new leads quickly and begin the intro path.
- Risks: generic messaging, outdated offer, wrong tone, duplicate outreach if staff already contacted the lead.
- Opportunities: Grounded AI can analyze lead source quality and draft improved welcome copy for human review.
- Classification: Bucket A, use Wodify Workflow Builder.

### Intro Appointment Reminder

- Trigger logic: 24 hours before appointment.
- Action logic: send SMS reminder.
- Business purpose: reduce no-shows and help prospects arrive prepared.
- Risks: consent issues, wrong appointment status, over-messaging, stale reminder copy.
- Opportunities: Grounded AI can review no-show patterns and recommend reminder copy improvements.
- Classification: Bucket A, use Wodify Workflow Builder.

### Missed Class Follow-Up

- Trigger logic: client no-showed.
- Action logic: send check-in email.
- Business purpose: follow up after missed reservations or attendance gaps.
- Risks: guilt-based messaging, incorrect no-show context, excessive automation, member frustration.
- Opportunities: Grounded AI can flag members where a coach-led follow-up is better than an automated email.
- Classification: Bucket A for simple no-show follow-up; Bucket B for context-aware recommendation.

### Membership Expiry Warning

- Trigger logic: 7 days before membership expiry.
- Action logic: send renewal email.
- Business purpose: reduce accidental churn and prompt renewal.
- Risks: transactional tone, wrong membership state, sending during hold or cancellation context.
- Opportunities: Grounded AI can summarize expiring memberships and recommend human review for sensitive cases.
- Classification: Bucket A for standard expiry warning; Bucket B for exception review.

### Re-Engagement

- Trigger logic: no attendance in 14 days.
- Action logic: send check-in and create staff task.
- Business purpose: prompt outreach before disengagement becomes churn.
- Risks: automated outreach may feel impersonal, attendance data may miss holds/injury/known life events, task volume may overwhelm staff.
- Opportunities: Grounded AI can rank re-engagement candidates by context and suggest coach-led follow-up.
- Classification: Bucket A for baseline automation; Bucket B for prioritization and recommendation.

Preferred signal flow:

```text
No attendance in 14 days
↓
Task created in Wodify
↓
Coach assigned in Wodify
↓
At Risk tag added in Wodify
↓
Appears in Weekly Coach Brief through Grounded AI read/analysis
```

Ownership:

- Wodify owns the trigger, task, coach assignment, and tag.
- Grounded AI reads the resulting export/API signal and includes the member in the Weekly Coach Brief.
- Grounded AI does not create the task, assign the coach, add the tag, or contact the member.

### Unpaid Invoice

- Trigger logic: invoice 7 days overdue.
- Action logic: send reminder email.
- Business purpose: recover payment and reduce administrative burden.
- Risks: sensitive financial tone, wrong invoice state, payment already resolved, member relationship strain.
- Opportunities: Grounded AI can summarize unpaid invoice patterns for owner review without contacting members.
- Classification: Bucket A for payment reminder; Bucket B for owner-level analysis.

### Birthday

- Trigger logic: client birthday.
- Action logic: send birthday message.
- Business purpose: lightweight member recognition and relationship maintenance.
- Risks: generic message, incorrect member data, over-automation.
- Opportunities: Grounded AI can suggest more human recognition moments beyond birthdays.
- Classification: Bucket A for birthday automation; Bucket B for broader recognition intelligence.

## Related Wodify Task Triggers

Common task-generating trigger conditions observed:

- Lead has not been contacted in X days.
- Membership expiring soon.
- Client has not attended in X days.
- Unpaid invoice past due date.

These should usually stay inside Wodify as task automation candidates. Grounded AI may audit, prioritize, and recommend task candidates, but must not create tasks during MVP.

## Inventory Conclusion

Wodify already owns core automation execution for common gym operations:

- Lead response.
- Appointment reminders.
- Missed class follow-up.
- Membership renewal prompts.
- Re-engagement.
- Invoice reminders.
- Birthday messages.
- Staff task generation.

Grounded AI should not duplicate these execution paths. Grounded AI should make them smarter by analyzing data, identifying gaps, drafting improved copy, surfacing exceptions, and helping staff decide what to activate inside Wodify.
