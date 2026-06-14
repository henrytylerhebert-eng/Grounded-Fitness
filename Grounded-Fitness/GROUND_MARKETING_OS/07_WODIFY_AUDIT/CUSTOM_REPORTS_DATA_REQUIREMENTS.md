# Custom Reports Data Requirements

Source context: live Wodify Custom Reports dashboard editor screen shared on June 12, 2026.

Purpose: define the data needed to build the Grounded Weekly Command Report inside Wodify Custom Reports.

Important privacy note: observed report rows include real member names and emails in Wodify. Do not copy full member lists or raw personal data into this repository.

## Current Screen State

Observed state:

- Dashboard title: `Master Dash`.
- Initial dashboard build was saved by Tyler after Computer Use-assisted setup.
- The dashboard now includes two existing Wodify Reporting cards:
  - `Attendances`.
  - `Coaches Classes, Filtered by Class Date`.
- Wodify prompts: create a new question or browse collections for an existing one.
- Primary visible action: Add a chart.
- Shared Reports tab is active.
- Data last updated: 06/11/2026 09:01 PM.
- Next refresh: 06/12/2026 09:01 PM.
- Follow-up Computer Use inspection opened an existing Wodify Reporting question: `Active Clients with Memberships and more than 15 days since Log In`.
- That question lives under `Sample Questions to Get Started!` and uses the `Clients` source table in the `Custom Reporting` database.

Implication: the first useful live dashboard layer exists. Next, create higher-signal Wodify Reporting questions/cards and place them onto the dashboard.

## Saved Cards Observed

### Active Clients with Memberships and more than 15 days since Log In

Observed card type: table.

Observed source: `Custom Reporting` database / `Clients` table.

Observed row count note: showing 28 rows.

Observed filters: 3 filters are applied, but the exact filter definitions were not opened.

Observed fields:

- Client ID.
- Client Name.
- Max Role Name.
- Client Active.
- Client Suspended.
- Member Since Date.
- Years As Member.
- Last Class Sign In.
- Email.
- Membership Status.

Use this card for:

- Active client roster baseline.
- Member inactivity review.
- At-risk member watch list.
- Membership status review.
- Newer-member support review using `Member Since Date` and `Years As Member`.

Limitations:

- The card is filtered to clients more than 15 days since log-in, so it is not a complete active-client roster.
- Exact filter logic is not yet documented.
- It includes personal contact data; use it for analysis, not repository storage.
- It does not show lead source, appointment history, reservations, no-shows, payments, or task follow-up.
- It should be copied into `Master Dash` only after deciding whether the dashboard should show raw member rows or a summarized owner-action version.

### Attendances

Observed card type: table.

Observed row count note: showing first 2,000 rows.

Observed fields:

- Customer ID.
- Client ID.
- Lead ID.
- Client Name.
- Attendance Type.
- Drop In Value.
- Class ID.
- Class Name.

Observed sample values show attendance records for clients and class names such as Functional Fitness, BootCamp, Barbell Club, and legacy CrossFit-labeled classes.

Use this card for:

- Raw attendance source review.
- Client attendance history.
- Class participation source data.
- First-pass validation for at-risk and member-engagement questions.

Limitations:

- The saved view is too raw for owner action.
- Last attendance date is not yet summarized.
- Days since last attendance is not yet calculated.
- Attendance decline is not yet calculated.
- Member status, membership type, and join date are not visible in this raw attendance card; they are available in the observed active-client membership question above.

### Coaches Classes, Filtered by Class Date

Observed card type: table.

Observed row count note: 106 rows.

Observed fields:

- Coach Name.
- Class.
- Program.

Observed sample values show coach/class/program records, including Functional Fitness program rows.

Use this card for:

- Coach schedule visibility.
- Class-health source review.
- Class/program labeling checks.
- Future class utilization reporting.

Limitations:

- Reservations, attendance count, no-show count, and capacity are not visible in the observed card.
- Coach performance should not be inferred from this card.
- Program labels may need brand cleanup review where legacy language appears.

## Dashboard Tabs

Use dashboard tabs to keep the report readable.

Recommended tabs:

1. Owner Snapshot.
2. Member Risk.
3. New Members.
4. Leads.
5. Classes.
6. Recognition.
7. Revenue Risk.

Start with tabs 1 through 4. Classes, Recognition, and Revenue Risk can follow once the core member/lead data works.

## Source Data Objects Needed

These are conceptual Wodify data objects. Exact Wodify Custom Reporting model names are `Unknown` until confirmed in Databases or Models.

| Data object | Why needed | Minimum fields |
|---|---|---|
| Clients / Members | Active client roster and member status | Confirmed source table: `Clients`; observed fields include client ID, name, email, active/suspended status, member since date, last class sign-in, membership status |
| Attendance | Attendance frequency, decline, last visit, class history | Partially confirmed via `Attendances`; observed fields include client ID, lead ID, client name, attendance type, class ID, class name; attendance date still needs confirmation |
| Memberships | plan type, active status, expiration, holds, cancellations | Partially confirmed through client membership fields; expiration, holds, cancellations, and plan name still need confirmation |
| Leads | lead pipeline and follow-up | lead ID, name, source, created date, status, assigned staff |
| Appointments / Intros | intro booking and attendance | lead/client ID, appointment date, appointment status, provider/coach |
| Classes | class health and schedule utilization | class ID, date, time, program/type, coach, capacity |
| Reservations / No-shows | reservations, attendance, no-show rate | class ID, client ID, reservation status, attendance/no-show status |
| Coaches / Staff | ownership and follow-up routing | coach/staff ID, name, role, active status |
| Payments / Invoices | failed payments and revenue risk | client ID, invoice/payment status, amount, due date |
| Milestones / Performance | recognition candidates | client ID, milestone type, date, count/result |
| Tasks | existing Wodify follow-up work | task ID, client/lead ID, assignee, status, due date |
| Tags | at-risk, lead, member, or workflow labels | client/lead ID, tag name, tag date |

If any object is missing from Custom Reports, mark that object `Unknown` and do not invent the metric.

## First Questions To Build

Build these Wodify Reporting questions before designing the visual dashboard.

### Q1: Active Client Roster

Purpose: baseline source for most member reports.

Data needed:

- Client/member.
- Membership.
- Status.

Fields:

- Client name.
- Client profile link or ID.
- Status.
- Membership type.
- Join date.
- Last attendance date if available.
- Total attendance count if available.

Filter:

- Status equals active.

Sort:

- Client name ascending.

Dashboard use:

- Bookmark/source table.
- Base question for at-risk and new member cards.

### Q2: No Attendance In 14 Days

Purpose: identify members needing coach-led attention.

Data needed:

- Active client roster.
- Attendance.

Fields:

- Client name.
- Membership type.
- Last attendance date.
- Days since last attendance.
- Attendance last 30 days.
- Assigned coach if available.

Filter:

- Status equals active.
- Days since last attendance is 14 or greater.

Chart/card:

- Table.
- Optional count card: Active clients with no attendance in 14+ days.

Evidence rule:

- If last attendance date cannot be calculated, show `Unknown`.

### Q3: Attendance Drop Watch

Purpose: find members whose behavior changed before they disappear.

Data needed:

- Active client roster.
- Attendance.

Fields/calculations:

- Attendance last 30 days.
- Attendance previous 30 days.
- Attendance change.
- Attendance change percentage.
- Last attendance date.

Filter:

- Status equals active.
- Previous 30-day attendance greater than 0.
- Current 30-day attendance is lower than previous 30-day attendance.

Priority flag:

- High concern if attendance is down 50% or more.

Chart/card:

- Table sorted by biggest decline.

Evidence rule:

- If Custom Reports cannot compare rolling 30-day windows, create a simpler current-month versus prior-month version.

### Q4: New Member 90-Day Watch

Purpose: protect the first 90 days.

Data needed:

- Clients/members.
- Memberships.
- Attendance.

Fields:

- Client name.
- Join date.
- Days since join.
- First attendance date.
- Last attendance date.
- Total visits.
- Visits last 7 days.
- Visits last 30 days.
- Membership type.

Filter:

- Status equals active.
- Days since join is 90 or less.

Flags:

- No first visit.
- Fewer than 3 visits in first 14 days.
- No visit in last 7 days.

Chart/card:

- Table.
- Count card: New members needing check-in.

### Q5: Lead Pipeline Health

Purpose: prevent leads from going stale.

Data needed:

- Leads.
- Appointments/intros.
- Client conversion if available.
- Tasks/contact history if available.

Fields:

- Lead name.
- Lead source.
- Created date.
- Days since created.
- Lead status.
- Assigned staff.
- Intro booked date.
- Intro status.
- Converted to client yes/no if available.
- Last contact date if available.

Views:

- New leads this week.
- Leads older than 7 days with no intro booked.
- Intro booked but not attended.
- Intro attended but not converted.
- Leads with no recent contact.

Chart/card:

- Funnel if conversion statuses are available.
- Table if funnel fields are not available.

Evidence rule:

- If conversion status is unavailable, use `No measurements found` for conversion rate.

### Q6: Class Utilization

Purpose: see class demand and weak class times.

Data needed:

- Classes.
- Reservations.
- Attendance.
- Coaches.

Fields:

- Class date.
- Class time.
- Class name/program.
- Coach.
- Reservations.
- Attended count.
- No-show count.
- Capacity if available.
- Utilization percentage if available.

Views:

- Attendance by class time.
- Lowest attended recurring classes.
- Highest attended recurring classes.
- No-show-heavy classes.

Chart/card:

- Bar chart by time of day.
- Table by class time.

Evidence rule:

- Do not use this alone to judge coach performance.

### Q7: Recognition Candidates

Purpose: find members worth celebrating.

Data needed:

- Clients/members.
- Attendance.
- Milestones/performance if available.
- Birthdays/anniversaries if available.

Fields:

- Client name.
- Total visits.
- Upcoming birthday.
- Membership anniversary.
- Attendance streak.
- Return-after-absence flag.
- Recent PR/milestone if available.

Views:

- Visit milestones.
- Weekly streaks.
- Birthdays this month.
- Anniversaries this month.
- Returned after 14+ day absence.

Chart/card:

- Table.

Human rule:

- Public recognition requires owner approval and member consent.

### Q8: Revenue And Membership Risk

Purpose: owner review of payment and membership issues.

Data needed:

- Memberships.
- Payments/invoices.
- Clients/members.

Fields:

- Client name.
- Membership type.
- Membership status.
- Expiration date.
- Failed payment status.
- Past due amount if available.
- Hold/freeze status.
- Cancellation status.

Views:

- Failed payments.
- Memberships expiring in 30 days.
- Holds/freezes.
- Suspensions/cancellations.

Chart/card:

- Count cards for owner snapshot.
- Table for review.

Evidence rule:

- Financial communication stays inside Wodify.

## Owner Snapshot Cards

Once the questions exist, add these cards to the Owner Snapshot tab:

| Card | Depends on | Card type |
|---|---|---|
| Active clients | Q1 | Count |
| At-risk 14+ days | Q2 | Count |
| Attendance-drop watch | Q3 | Count |
| New members under 90 days | Q4 | Count |
| New members needing check-in | Q4 | Count |
| New leads this week | Q5 | Count |
| Stale leads | Q5 | Count |
| Classes under target attendance | Q6 | Count |
| Recognition candidates | Q7 | Count |
| Failed payments / revenue risk | Q8 | Count |

## Filters And Parameters

Add dashboard filters only after the base questions work.

Recommended filters:

- Date range.
- Program/type.
- Location if available.
- Coach/staff.
- Membership type.
- Lead source.
- Client status.

Avoid over-filtering the first version. Too many controls can hide the operating signal.

## Data Quality Checks

Before using the dashboard operationally, confirm:

1. Active client count matches Wodify's known active client roster.
2. Last attendance dates look plausible.
3. New member join dates look correct.
4. Lead counts match Wodify leads for the same period.
5. Class attendance counts match Standard Reports or expected class counts.
6. Failed payment counts match Financial views if included.
7. Refresh time is understood.

If any check fails, mark the affected card `Unknown` until fixed.

## Build Sequence In Wodify

Completed:

1. Add existing `Attendances` card to Master Dash.
2. Add existing `Coaches Classes, Filtered by Class Date` card to Master Dash.
3. Save the dashboard changes.

Next:

1. Create Q1 Active Client Roster.
2. Create Q2 No Attendance In 14 Days.
3. Add Q1 and Q2 to Master Dash.
4. Add the Owner Snapshot count cards for active clients and at-risk clients.
5. Create Q4 New Member 90-Day Watch.
6. Create Q5 Lead Pipeline Health.
7. Add Member Risk, New Members, and Leads tabs.
8. Add Q3 Attendance Drop Watch.
9. Create or refine Q6 Class Utilization beyond the existing coach/class table.
10. Add Q7 Recognition Candidates.
11. Add Q8 Revenue And Membership Risk.

This creates value quickly while avoiding a giant dashboard build that never becomes useful.

## Grounded AI Use

Grounded AI can read exported/copy-pasted report outputs and produce:

- Owner brief.
- Coach brief.
- Lead follow-up list.
- New member check-in list.
- Recognition shortlist.
- Missing-data list.

Grounded AI cannot:

- Create the Wodify chart by itself unless a human is supervising the UI.
- Save dashboard changes without approval.
- Send messages.
- Update Wodify records.
- Decide action without human review.
