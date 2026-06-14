# MVP Requirements

## MVP Direction

The MVP is an AI intelligence and accessibility layer on top of Wodify exports.

It does not rebuild Wodify.

It does not write to Wodify.

It uses fake/sample CSV data only.

## MVP Inputs

- Fake/sample Wodify client data.
- Fake/sample Wodify attendance data.
- Fake/sample Wodify lead data.
- Fake/sample Wodify class data.
- Fake/sample Wodify milestone or performance data if available.
- Fake/sample Wodify revenue data if available.

## MVP Outputs

The MVP should produce:

- Weekly Owner Brief.
- Weekly Coach Brief.
- At-Risk Member Report.
- Member Milestone Report.
- Member of the Month Candidate Report.
- Lead Pipeline Snapshot.
- Draft internal member emails.

## Acceptance Criteria

The MVP is accepted when:

- It uses fake/sample CSV data only.
- It produces owner-readable markdown reports.
- It clearly identifies missing data.
- It separates facts from inferred recommendations.
- It does not perform any Wodify write action.
- It requires human review before member communication.
- It does not send emails, SMS, chat messages, announcements, or marketing emails.
- It does not create Wodify tasks, tags, automations, or communications.
- It does not convert leads to clients.
- It does not change memberships, holds, invoices, payments, or transactions.

## Report Requirements

Every report should show:

- Source files used.
- Date range if available.
- Confirmed facts.
- Inferred recommendations.
- Confidence level.
- Missing data.
- Human review needed.

## Privacy Rules

- Never commit real member data.
- Use fake sample data only.
- Gitignore exports and private files.
- No automated outreach.
- No health promises.
- No medical advice.
- No CrossFit public branding.

## Non-Requirements

The MVP does not require:

- A database.
- A web app.
- A live Wodify connection.
- A Wodify API integration.
- A Gmail integration.
- Any writeback workflow.
- Automated communications.
- Production reports from real member data committed to git.
