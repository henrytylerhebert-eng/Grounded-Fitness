# Decisions

This file records project decisions. Keep entries short, dated, and tied to evidence when available.

## 2026-06-12: Grounded AI Is A Wodify Intelligence Layer

Decision: Grounded AI will not rebuild Wodify. It will read from Wodify exports, analyze, summarize, recommend, and draft.

Why: Wodify already owns the operational system: leads, clients, memberships, attendance, reservations, appointments, tasks, communications, automations, invoices, transactions, and reporting.

Evidence: Grounded Fitness + WodCore context export.

Status: Accepted.

## 2026-06-12: CSV Intelligence Reports Are The MVP

Decision: The MVP uses fake/sample CSV data to produce owner-readable markdown reports and draft internal communications.

MVP outputs:

- Weekly Owner Brief.
- Weekly Coach Brief.
- At-Risk Member Report.
- Member Milestone Report.
- Member of the Month Candidate Report.
- Lead Pipeline Snapshot.
- Draft internal member emails.

Why: This makes Wodify easier and more useful without connecting live APIs or writing back to Wodify.

Status: Accepted.

## 2026-06-12: Grounded Is Not Marketed As CrossFit

Decision: Public-facing and member-facing language must not market Grounded Fitness as CrossFit.

Why: Grounded's positioning is functional fitness, coaching, strength, conditioning, movement quality, community, longevity, consistency, and real-life fitness.

Status: Accepted.

## 2026-06-12: Wodify Intelligence Starts With CSV Exports

Decision: Wodify analysis begins with CSV exports, not a direct API integration.

Why: Credentials, documentation, permissions, and export schemas must be validated before any future read-only API integration.

Boundary: Write actions are locked until explicitly approved.

Status: Accepted.

## 2026-06-12: Community & Recognition Is Phase 1.5 Candidate

Decision: Community & Recognition is not MVP, but it is likely high-priority after Member Value Engine validation.

Why: Recognition, coaching follow-up, relationships, and culture create retention.

Status: Accepted.

## Decision Template

Date:

Decision:

Why:

Evidence:

Status:
