# Decisions

This file records decisions for Grounded Marketing OS. Decisions should be short, dated, and tied to the New Build Launch Framework.

## 2026-06-12: Start With Member Value Engine Only

Decision: The initial build will focus only on the Member Value Engine.

Why: The most direct value is improving weekly member communication from programming and attendance context. This can be validated manually before adding integrations or broader marketing systems.

Status: Accepted.

## 2026-06-12: MVP Is An Operating Workflow, Not Software First

Decision: The MVP is a repeatable weekly operating workflow:

1. Receive weekly programming email.
2. Extract weekly training themes.
3. Segment members from Wodify attendance data.
4. Draft internal value-based member emails.
5. Human reviews.
6. Send.
7. Track attendance and engagement.

Why: Grounded needs proof that the communication workflow creates member value before investing in tooling.

Status: Accepted.

## 2026-06-12: No Production Integrations Yet

Decision: Gmail, Wodify, website/blog, Canva, Instagram, Facebook, YouTube, and Google Business Profile are documented as future integrations only.

Why: The manual workflow must be validated before API access, automation, or publishing systems are built.

Status: Accepted.

## 2026-06-12: No CrossFit Positioning

Decision: Grounded Fitness Acadiana must be described as a functional fitness gym, not a CrossFit gym.

Why: Public positioning should match the brand's required language and avoid incorrect or unwanted affiliation.

Status: Accepted.

## 2026-06-12: Wodify Audit Becomes Its Own Module

Decision: Wodify inventory and governance will live in `07_WODIFY_AUDIT/`.

Why: Wodify, Workato, Wodify Communication, and Wodify Sites already contain meaningful execution surfaces. They need to be audited before Grounded builds anything that could duplicate Wodify, create a second source of truth, or send/publish without review.

Status: Accepted.

Evidence: Live Wodify screens showed Workflow Builder recipes, Workflow Email Templates, Workato environment properties, no API clients, Communication Settings, Marketing Emails, Automated Emails, Templates, Wodify Sites blog, and website personalization.

## Decision Template

Date:

Decision:

Why:

Status:

Evidence:
