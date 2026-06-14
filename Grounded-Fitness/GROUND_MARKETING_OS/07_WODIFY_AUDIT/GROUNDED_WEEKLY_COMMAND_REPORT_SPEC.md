# Grounded Weekly Command Report Spec

Source context: live Wodify Custom Reports screen shared on June 12, 2026.

Purpose: define the ideal read-only owner report that helps Grounded Fitness decide who needs attention, what is working, and what to do next.

## Positioning

The Grounded Weekly Command Report is a Wodify decision-support report.

It is not:

- A replacement backend.
- A second source of truth.
- A Wodify writeback tool.
- A communication sender.
- A lead/member automation system.

Wodify remains the system of record. Grounded AI may later summarize, interpret, and turn the report into review-ready action lists.

## Observed Custom Reports Surface

Observed Wodify Custom Reports facts:

- Page: Custom Reports.
- Status: Beta.
- Tabs: Shared Reports and My Reports.
- Data last updated: 06/11/2026 09:01 PM.
- Next refresh: 06/12/2026 09:01 PM.
- Embedded reporting surface: `reporting.wodify.com`.
- Data section includes Databases and Models.
- Database observed: Custom Reporting.
- Bookmark observed: All Active Clients.
- Collections observed: personal collection, Custom Reporting Tutorials, Sample Questions to Get Started, Pre Built Dashboards from Core, and Wodify Community Library.
- `Master Dash` was saved with two initial cards:
  - `Attendances`.
  - `Coaches Classes, Filtered by Class Date`.

Audit note: the reporting refresh cadence appears daily from the observed timestamps. Treat live freshness as `Unknown` until confirmed inside Wodify documentation or settings.

Detailed data requirements for the dashboard questions/cards live in `CUSTOM_REPORTS_DATA_REQUIREMENTS.md`.

## Report Objective

Every week, the owner should be able to answer:

1. Who needs attention?
2. Which leads are slipping?
3. Which new members need support?
4. Which classes are healthy or weak?
5. Which members should be recognized?
6. Which financial or membership issues need review?
7. What should coaches do this week?

## Report Sections

### 1. Owner Snapshot

Purpose: one-screen view of the week.

Suggested cards:

- Active clients.
- New leads this week.
- Intros booked.
- New clients.
- At-risk clients.
- Members with no attendance in 14+ days.
- New members under 90 days.
- Failed payments or payment issues.
- Memberships expiring soon.
- Recognition candidates.

Evidence rule: if a metric is unavailable in Custom Reports, show `Unknown`.

### 2. At-Risk Member Watch

Purpose: identify members who may need coach-led attention.

Suggested fields:

- Client name.
- Membership status.
- Membership type.
- Primary coach or owner if available.
- Last attendance date.
- Days since last attendance.
- Attendance last 7 days.
- Attendance last 14 days.
- Attendance last 30 days.
- Attendance previous 30 days.
- Attendance change.
- New member flag.
- Hold/freeze/cancellation flag if available.
- Suggested follow-up owner.
- Notes/status from Wodify if available.

Suggested views:

- No attendance in 14+ days.
- Attendance down 50% or more from prior 30 days.
- Active member with 0 visits this week.
- New member under 90 days with no visit in 7+ days.

Grounded AI use later: summarize risk reason and draft coach talking points for review.

Grounded AI must not send the message or change the member record.

### 3. New Member 90-Day Watch

Purpose: protect the most important retention window.

Suggested fields:

- Client name.
- Join date.
- Days since join.
- First visit date.
- Total visits.
- Visits in last 7 days.
- Visits in last 30 days.
- Last attendance date.
- Intro/free trial source if available.
- Membership type.
- Coach/owner if available.
- Status.

Suggested flags:

- No first visit yet.
- Fewer than 3 visits in first 14 days.
- No attendance in last 7 days.
- Attendance declined after first month.
- Needs coach check-in.

### 4. Lead Pipeline Health

Purpose: help the owner see whether prospective members are moving.

Suggested fields:

- Lead name.
- Lead source.
- Created date.
- Status.
- Intro booked date.
- Intro attended.
- Converted to client.
- Days since created.
- Last contact date if available.
- Assigned staff member if available.

Suggested views:

- New leads this week.
- Leads not contacted.
- Leads with no intro booked.
- Intros booked but not attended.
- Intros attended but not converted.
- Stale leads older than 7, 14, and 30 days.

Evidence rule: if contact history or source is missing, record `Unknown`.

### 5. Class Health

Purpose: identify schedule strength, weak class times, and utilization patterns.

Suggested fields:

- Class date.
- Class time.
- Program/type.
- Coach.
- Reservations.
- Attendance.
- No-shows.
- Capacity if available.
- Utilization percentage if available.

Suggested views:

- Best attended classes.
- Lowest attended recurring classes.
- No-show-heavy classes.
- Class attendance by time of day.
- Attendance by coach.
- Attendance by program.

Evidence rule: do not judge coach performance from attendance alone. Use this as a schedule and demand signal.

### 6. Recognition And Community

Purpose: find moments where members should feel seen.

Suggested fields:

- Client name.
- Total visits.
- Visit milestone.
- Attendance streak.
- Birthday.
- Membership anniversary.
- Recent PR/performance result if available.
- Referral candidate if available.
- Community note if available.

Suggested views:

- Upcoming birthdays.
- Upcoming membership anniversaries.
- Attendance milestones.
- Weekly streaks.
- Return-after-absence wins.
- Consistent members.

Human rule: AI may suggest candidates and drafts, but humans decide recognition and obtain consent before public use.

### 7. Revenue And Membership Risk

Purpose: focus owner attention on operational risk without turning AI into a financial decision-maker.

Suggested fields:

- Client name.
- Membership type.
- Status.
- Expiration date.
- Failed payment flag.
- Past due amount if available.
- Suspension/hold/cancellation status.
- Renewal date.

Suggested views:

- Failed payments.
- Expiring memberships.
- Suspensions.
- Cancellations.
- Holds/freezes.
- High-value membership changes.

Evidence rule: financial communication stays inside Wodify and owner review.

### 8. Owner Action List

Purpose: convert reporting into a weekly decision checklist.

Suggested grouped actions:

- Call or text these at-risk members.
- Assign coach follow-up for these new members.
- Review these stale leads.
- Celebrate these members.
- Review these classes.
- Review these payment or membership issues.

Output should include:

- Person or item.
- Source reason.
- Recommended next step.
- Owner/coach.
- Confidence level.
- Missing data.

## Report Build Priority

Build the report in this order:

1. All Active Clients baseline.
2. At-Risk Member Watch.
3. New Member 90-Day Watch.
4. Lead Pipeline Health.
5. Owner Action List.
6. Class Health.
7. Recognition And Community.
8. Revenue And Membership Risk.

Reason: member retention and lead follow-up create the fastest operating value.

## Grounded AI Interpretation Layer

Once the Wodify report exists, Grounded AI can turn exported or copied report results into:

- Weekly owner brief.
- Weekly coach brief.
- At-risk member summary.
- New member check-in list.
- Lead follow-up list.
- Recognition candidates.
- Draft talking points.

Required language:

- Source facts.
- Inference.
- Recommended action.
- Confidence.
- Missing data.

Grounded AI may not:

- Mark a task complete.
- Assign a coach in Wodify.
- Add tags.
- Change lead status.
- Send email, SMS, chat, or announcements.
- Publish public recognition.

## Measurement Rules

Allowed measurements:

- Counts visible in Custom Reports.
- Dates visible in Custom Reports.
- Statuses visible in Custom Reports.
- Delivery metrics observed directly in Wodify.
- Exported report metrics.

Use `No measurements found` for:

- Conversion rate if lead conversion fields are unavailable.
- Revenue impact if payment or membership data is not included.
- Retention lift unless compared over time.
- Open/click/reply rates unless exported or observed.
- Coach performance unless intentionally measured with fair context.

Use `Unknown` for:

- Fields not visible.
- Refresh cadence not confirmed.
- Data model joins not confirmed.
- Report permissions not confirmed.
- Whether a metric can be exported.

## First Manual Workflow

1. Create or open the Wodify Custom Report.
2. Start from All Active Clients.
3. Add the At-Risk Member Watch table.
4. Add New Member 90-Day Watch.
5. Add Lead Pipeline Health.
6. Export or copy results.
7. Grounded AI summarizes into an owner brief.
8. Human reviews actions.
9. Owner or coach acts inside Wodify or normal communication channels.
10. Review the next week for changes.

## Acceptance Criteria

The report is useful when:

1. The owner can identify at-risk members in under five minutes.
2. New members needing support are visible.
3. Stale leads are visible.
4. Recognition opportunities are visible.
5. Every recommendation points back to a Wodify source fact.
6. Missing data is clearly marked.
7. No Wodify writes or automatic communication happen from Grounded AI.
