# Wodify Audit

This folder documents what already exists inside Wodify, Workato, Wodify Communication, and Wodify Sites before Grounded builds or automates anything.

## Purpose

Use this folder to answer:

- What can Wodify already do?
- What should stay inside Wodify?
- Where can Grounded AI help with analysis, copy, prioritization, or review?
- What is still `Unknown`?
- Where do we have `No measurements found`?

## Current Rule

Wodify remains the source of truth and execution layer.

Grounded AI may:

- Inventory Wodify surfaces.
- Analyze exported or observed data.
- Draft review-ready copy.
- Recommend workflow priorities.
- Flag risks, placeholders, and missing evidence.

Grounded AI may not:

- Create, update, or delete Wodify records.
- Send, schedule, publish, or toggle Wodify communications.
- Install or update recipes.
- Create API clients.
- Connect community connectors.
- Connect AI model providers to Wodify.
- Use real member data outside approved exports.

## Files

- `WORKFLOW_INVENTORY.md`: observed Workflow Builder recipes, email templates, and utilization principles.
- `AUTOMATION_GAP_ANALYSIS.md`: what belongs in Wodify, what belongs in Grounded AI, and what remains unverified.
- `RECOMMENDED_AUTOMATIONS.md`: audit recommendations only, not build approvals.
- `RECIPE_ANALYSIS.md`: recipe-by-recipe Bucket A/B/C classification.
- `WORKATO_ENVIRONMENT_AUDIT.md`: environment properties, API clients, connector surface, and workspace admin notes.
- `COMMUNICATION_LAYER_AUDIT.md`: Marketing Emails, Automated Emails, Templates, settings, chat, and calendar-event observations.
- `WODIFY_SITES_BLOG_AUDIT.md`: Wodify Sites blog, public website, and personalization observations.
- `GROUNDED_WEEKLY_COMMAND_REPORT_SPEC.md`: read-only Wodify Custom Reports design for owner, coach, lead, retention, recognition, and class-health visibility.
- `CUSTOM_REPORTS_DATA_REQUIREMENTS.md`: question-by-question Wodify Custom Reports data requirements for the Master Dash build.

## Relationship To Data Intelligence

`04_DATA_INTELLIGENCE/` is for future CSV/export-based reporting.

`07_WODIFY_AUDIT/` is for source-system inventory and governance.

Do not build direct Wodify API access until credentials, permissions, role design, privacy rules, and read-only scope are explicitly approved.
