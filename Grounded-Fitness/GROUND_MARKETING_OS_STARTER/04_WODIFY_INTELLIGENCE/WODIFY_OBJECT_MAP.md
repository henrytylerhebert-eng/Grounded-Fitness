# Wodify Object Map

Wodify owns the operational records. Grounded AI may read exports, infer patterns, recommend human-reviewed actions, and draft content. Grounded AI must not modify Wodify objects during the MVP.

## Leads

- What Wodify owns: lead identity, lead status, source, intro appointment state, conversion state, communication history, and automation state.
- What Grounded AI may read: exported lead records, source, status, dates, intro status, and conversion fields.
- What Grounded AI may infer: stale leads, source quality, conversion gaps, and follow-up opportunities.
- What Grounded AI may recommend: human-reviewed follow-up, lead source review, and pipeline cleanup questions.
- What Grounded AI must not modify: lead status, lead type, contact details, tasks, communications, tags, automations, or conversion state.

## Clients

- What Wodify owns: client identity, status, profile, communication consent, membership links, attendance history, and client history.
- What Grounded AI may read: exported client records, status, join date, contact-safe identifiers in fake/sample data, attendance summaries, and membership context.
- What Grounded AI may infer: engagement level, attendance decline, retention risk, recognition opportunities, and missing data.
- What Grounded AI may recommend: coach check-ins, recognition candidates, internal draft messages, and review questions.
- What Grounded AI must not modify: client profiles, status, consent, tags, tasks, communications, memberships, or notes.

## Drop-Ins

- What Wodify owns: drop-in identity, visit history, payment status, program/class participation, and communication history.
- What Grounded AI may read: exported drop-in records and visit context.
- What Grounded AI may infer: repeat drop-in patterns, conversion opportunities, and source quality if available.
- What Grounded AI may recommend: human-reviewed follow-up opportunities.
- What Grounded AI must not modify: drop-in records, communications, lead/client conversion, payments, or tags.

## Segments

- What Wodify owns: segment definitions, filter logic, favorites, targeting, and segment membership.
- What Grounded AI may read: exported segment names, descriptions, and membership counts if available.
- What Grounded AI may infer: operational segment purpose, overlap, missing segments, and reporting opportunities.
- What Grounded AI may recommend: segment review questions or suggested segment definitions for human review.
- What Grounded AI must not modify: segment filters, names, favorites, targeting, or membership.

## Progressions

- What Wodify owns: progression levels, colors, criteria, staff approvals, certificates, and promotion/demotion history.
- What Grounded AI may read: exported progression levels, criteria, member progression status, and near-promotion indicators if available.
- What Grounded AI may infer: milestone opportunities, recognition candidates, and coach attention needs.
- What Grounded AI may recommend: coach review, recognition, or milestone review.
- What Grounded AI must not modify: progression level, criteria, certificates, staff approval, promotion, or demotion.

## Memberships

- What Wodify owns: membership plans, access rules, pricing, start/end dates, renewal state, and member-plan relationship.
- What Grounded AI may read: exported membership type, plan status, dates, limits, and pricing fields.
- What Grounded AI may infer: plan mix, retention windows, revenue snapshot notes, and missing data.
- What Grounded AI may recommend: human-reviewed retention questions or plan-mix analysis.
- What Grounded AI must not modify: membership type, plan, pricing, renewal state, access, start/end dates, or status.

## Membership Holds

- What Wodify owns: hold type, reason, start date, end date, billing pause, and attendance pause.
- What Grounded AI may read: exported hold status, type, reason category, and dates.
- What Grounded AI may infer: hold patterns, return timing, and reactivation review opportunities.
- What Grounded AI may recommend: human-reviewed return check-in questions.
- What Grounded AI must not modify: hold creation, hold dates, hold reason, billing pause, or return status.

## Programs

- What Wodify owns: program names, color codes, access controls, publish status, secure programming setting, and active/inactive state.
- What Grounded AI may read: exported program records and participation context.
- What Grounded AI may infer: program engagement, class utilization by program, and public-content opportunities.
- What Grounded AI may recommend: owner review of program trends.
- What Grounded AI must not modify: program settings, visibility, enrollment rules, status, or colors.

## Classes

- What Wodify owns: class schedule, program link, coach assignment, capacity, attendance, and performance results.
- What Grounded AI may read: exported class records, attendance counts, coach assignments, capacity, and dates.
- What Grounded AI may infer: class utilization, high-performing classes, low-performing classes, and coach/class trends.
- What Grounded AI may recommend: owner review of schedule patterns or coach brief notes.
- What Grounded AI must not modify: schedule, capacity, coach assignment, attendance, reservations, or performance results.

## Appointments

- What Wodify owns: appointment type, duration, assigned coach, attached client/lead, status, and schedule.
- What Grounded AI may read: exported appointment records and statuses.
- What Grounded AI may infer: intro completion patterns, no-show patterns, and follow-up opportunities.
- What Grounded AI may recommend: human-reviewed follow-up questions or owner brief notes.
- What Grounded AI must not modify: appointment status, schedule, assigned coach, client link, or communications.

## Tasks

- What Wodify owns: task name, assignee, due date, status, linked record, creation source, and completion history.
- What Grounded AI may read: exported task records if available.
- What Grounded AI may infer: staff workload, open follow-ups, overdue tasks, and process gaps.
- What Grounded AI may recommend: task candidates for human review.
- What Grounded AI must not modify: task creation, assignee, due date, status, linked record, or completion state.

## Automations

- What Wodify owns: triggers, actions, on/off states, emails, SMS, task generation, tags, and workflow logic.
- What Grounded AI may read: exported or documented automation names, trigger descriptions, and status if available.
- What Grounded AI may infer: automation coverage, overlap, and gaps.
- What Grounded AI may recommend: human-reviewed automation audit questions.
- What Grounded AI must not modify: triggers, actions, on/off state, messages, task creation, tags, or workflow settings.

## Communications

- What Wodify owns: email, SMS, chat history, consent state, templates, conversation threads, and channel records.
- What Grounded AI may read: exported communication metadata or approved sample content.
- What Grounded AI may infer: communication gaps, follow-up needs, and draft context.
- What Grounded AI may recommend: review-ready message drafts or follow-up questions.
- What Grounded AI must not modify: threads, sent messages, templates, consent, channel state, or communication history.

## Announcements

- What Wodify owns: announcement content, target audience, schedule, state, and app-feed display.
- What Grounded AI may read: exported announcement metadata or approved samples.
- What Grounded AI may infer: announcement gaps, event communication opportunities, and audience fit.
- What Grounded AI may recommend: review-ready announcement drafts.
- What Grounded AI must not modify: announcement content, targeting, schedule, state, or publishing.

## Marketing Emails

- What Wodify owns: campaign content, templates, segments, send state, drafts, tags, and email history.
- What Grounded AI may read: exported campaign metadata, approved sample templates, and performance fields if available.
- What Grounded AI may infer: content opportunities, missing nurture steps, source-quality notes, and draft angles.
- What Grounded AI may recommend: review-ready email drafts and campaign questions.
- What Grounded AI must not modify: templates, drafts, segments, campaign state, sends, tags, or email history.

## Attendance Reports

- What Wodify owns: attendance records, reports by member/class/program/date range, and report outputs.
- What Grounded AI may read: exported attendance reports.
- What Grounded AI may infer: engagement, decline, missed weeks, streaks, utilization, and at-risk signals.
- What Grounded AI may recommend: owner brief notes, coach check-in candidates, and draft internal communications.
- What Grounded AI must not modify: attendance records, reservations, class records, or Wodify reports.

## Revenue Reports

- What Wodify owns: revenue, invoices, transactions, plan revenue, failed payments, discounts, and report outputs.
- What Grounded AI may read: exported revenue reports using fake/sample data in repo.
- What Grounded AI may infer: revenue snapshot, failed payment notes, plan mix, discount patterns, and missing financial fields.
- What Grounded AI may recommend: owner review questions.
- What Grounded AI must not modify: invoices, payments, transactions, discounts, memberships, reports, or accounting records.

## Lead Reports

- What Wodify owns: lead status, source, conversion, intro status, and report outputs.
- What Grounded AI may read: exported lead reports.
- What Grounded AI may infer: lead source quality, stale leads, intro conversion gaps, and pipeline bottlenecks.
- What Grounded AI may recommend: human-reviewed follow-up candidates or source review questions.
- What Grounded AI must not modify: leads, statuses, conversions, appointments, communications, tags, or reports.

## Retention Reports

- What Wodify owns: churn, at-risk member signals, inactive members, retention calculations, and report outputs.
- What Grounded AI may read: exported retention reports.
- What Grounded AI may infer: retention risks, attendance-decline patterns, hold/cancellation patterns, and missing data.
- What Grounded AI may recommend: coach-led follow-up candidates and owner brief notes.
- What Grounded AI must not modify: retention records, statuses, tasks, communications, automations, or reports.

## Performance Reports

- What Wodify owns: performance results, workout scores, leaderboard history, progressions, and report outputs.
- What Grounded AI may read: exported performance reports when available.
- What Grounded AI may infer: milestone opportunities, recognition candidates, improvement patterns, and coach brief notes.
- What Grounded AI may recommend: human-reviewed recognition or coaching opportunities.
- What Grounded AI must not modify: scores, leaderboard records, progression levels, certificates, or reports.
