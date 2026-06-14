# Member Value Engine Specification

## Purpose

The Member Value Engine helps the owner and staff understand member engagement signals from Wodify exports and draft human-reviewed member communications.

It is an intelligence layer on top of Wodify. It does not replace Wodify member records, attendance tracking, tasks, communications, or automations.

## MVP Workflow

Wodify Fake/Sample CSV Exports -> Grounded AI Intelligence Layer -> Reports And Drafts -> Human Review

Steps:

1. Load fake/sample Wodify CSV exports.
2. Identify available and missing fields.
3. Summarize member engagement signals.
4. Generate owner-readable markdown reports.
5. Separate facts from inferred recommendations.
6. Draft internal member emails for review.
7. Require human review before communication.

## Segments

- Consistent: 4+ visits per week.
- Active: 2-3 visits per week.
- At Risk: 0-1 visits per week or attendance decline.
- New: first 90 days.

## Draft Requirements

Each draft must:

- Be tailored by segment.
- Use coaching language.
- Be simple and relational.
- Reflect the week's programming themes.
- Avoid hype.
- Avoid guilt.
- Avoid CrossFit branding.
- Avoid health promises.

## Acceptance Criteria

The MVP works when:

1. Fake/sample CSV data can be analyzed.
2. Weekly Owner Brief is produced.
3. Weekly Coach Brief is produced.
4. At-Risk Member Report is produced.
5. Member Milestone Report is produced.
6. Member of the Month Candidate Report is produced.
7. Lead Pipeline Snapshot is produced.
8. Draft internal member emails are produced.
9. Missing data is clearly identified.
10. Facts are separated from inferred recommendations.
11. No Wodify write action occurs.
12. Human review is required before member communication.

## Non-Requirements

The MVP does not require:

- A web app.
- A database.
- Production Gmail integration.
- Production Wodify API integration.
- Automated sending.
- Wodify writes.
- Wodify task creation.
- Wodify communication sending.
- Public content publishing.
- Lead nurture.
- Social automation.
