# Assumptions

This file lists assumptions that must be validated before architecture, automation, or production integrations.

## Business Assumptions

- Grounded Fitness Acadiana wants member communication to feel like coaching, not marketing.
- The weekly programming email contains enough context to extract useful training themes.
- Members benefit from short, practical explanations of the week's training focus.
- Attendance-based segments can help staff send more relevant member emails.
- Staff review is required before any member-facing email is sent.

## Data Assumptions

- Wodify can provide attendance data in a usable format.
- Wodify attendance data includes member names, emails, attendance dates, last attended dates, member status, membership type, lead status, and class participation.
- Segment definitions can begin manually before automated rules are built.
- Email engagement data may be available later, but is not required to validate the first manual workflow.

## Integration Assumptions

Future integrations:

- Gmail will be the source for weekly programming emails.
- Wodify will be the source for attendance and member segmentation.
- Website/blog will support future authority content.
- Canva will support future creative production.
- Instagram, Facebook, YouTube, and Google Business Profile will support future distribution.

No production integrations are approved in the initial build.

## Workflow Assumptions

- A human can review the weekly programming email and approve extracted themes.
- A human can export or provide Wodify attendance data for the test cycle.
- A human can approve member email drafts before sending.
- A human can record basic follow-up metrics after emails are sent.

## Validation Questions

1. Does the weekly programming email reliably arrive on a predictable schedule?
2. Does the programming email contain enough coaching context for member-facing themes?
3. What Wodify export format is available?
4. Which attendance window best predicts a useful member segment?
5. Can Wodify reliably identify members attending 4+ times per week?
6. Can Wodify reliably identify members attending 2-3 times per week?
7. Can Wodify reliably identify members attending 0-1 times per week or showing attendance decline?
8. Can Wodify reliably identify members in their first 90 days?
9. Who reviews and approves member emails?
10. Who sends the emails?
11. What engagement and attendance metrics can be tracked without new integrations?
12. Do members respond positively to coaching-led segment emails?

## Unknowns

- Exact Gmail source and format: Unknown.
- Exact Wodify export fields: Unknown.
- Email sending platform for manual MVP: Unknown.
- Current baseline attendance by segment: No measurements found.
- Current baseline email engagement: No measurements found.
