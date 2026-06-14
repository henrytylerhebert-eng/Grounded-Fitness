# MVP Requirements

## MVP Definition

The Member Value Engine MVP is a repeatable weekly operating workflow, not a software product.

The MVP is successful when Grounded can run the workflow manually for a weekly programming cycle, send reviewed member emails, and record basic attendance and engagement observations.

## MVP Workflow

1. Receive weekly programming email.
2. Extract weekly training themes.
3. Segment members from Wodify attendance data.
4. Draft internal value-based member emails.
5. Human reviews.
6. Send.
7. Track attendance and engagement.

## Required Inputs

- Weekly programming email.
- Wodify attendance export or manually provided attendance data.
- Segment definitions.
- Human reviewer.
- Manual sending process.
- Basic measurement record.

## Required Outputs

- Weekly programming summary.
- Training theme notes.
- Member segment list.
- Segment-specific email drafts.
- Human review notes.
- Send record.
- Measurement record.

## Initial Segments

Use only segments that can be supported by available Wodify attendance data:

- Consistent: members attending 4+ times per week.
- Active: members attending 2-3 times per week.
- At Risk: members attending 0-1 times per week or showing attendance decline.
- New: members in their first 90 days.

If the data does not support a segment, mark it `Unknown` and do not use it.

## Acceptance Criteria

The MVP is accepted when all of the following are true:

- A weekly programming email is captured and recorded.
- The weekly programming email can be summarized.
- At least three weekly coaching themes are extracted in plain language.
- A human confirms the extracted themes are accurate.
- Wodify attendance data is provided manually or through export.
- Members can be grouped into attendance-based segments.
- Segment criteria are documented.
- Three internal emails can be drafted for the week.
- Emails are clearly tailored by segment.
- Each draft uses coaching-led language and avoids CrossFit branding.
- Each draft avoids hype, shame, gym-bro language, and health promises.
- A human reviewer approves each message before sending.
- No AI-generated message is sent automatically.
- No Wodify records are altered.
- Send date, segment, subject line, reviewer, and sender are recorded.
- Attendance or engagement follow-up is recorded after sending.
- Missing metrics are marked `No measurements found`.
- Missing source data is marked `Unknown`.
- The workflow can be repeated the following week without redesign.

## Non-Requirements

The MVP does not require:

- A web application.
- A database.
- Production Gmail integration.
- Production Wodify integration.
- Automated sending.
- Public content publishing.
- Lead nurture automation.
- Financial analysis.
- Social media scheduling.
- Canva integration.

## Success Measurement

Do not claim success until at least one manual cycle has been completed and reviewed.

Possible early measurements:

- Number of members in each segment.
- Emails sent by segment.
- Replies from members.
- Attendance changes after send.
- Staff observations.
- Review edits required.

If no measurement exists, record `No measurements found`.
