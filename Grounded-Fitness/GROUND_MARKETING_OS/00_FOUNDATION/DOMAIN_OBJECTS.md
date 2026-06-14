# Domain Objects

These are the core objects for the initial Member Value Engine. They are operating objects first, not database tables.

Future modules should influence the vocabulary here, but they should not expand the initial MVP. Keep the current workflow small while preserving room for future records.

## Weekly Programming Email

The source message that describes upcoming training. Future assumption: arrives through Gmail.

Key fields:

- Week start date.
- Programming source.
- Training themes.
- Notable workout types.
- Coaching notes.
- Member-facing opportunities.

## Training Theme

A plain-language interpretation of the week's programming.

Examples:

- Strength focus.
- Conditioning focus.
- Skill practice.
- Recovery and consistency.
- Longevity and real-life capacity.
- Community workout or partner emphasis.

## Wodify Attendance Export

The source attendance data used for segmentation. Future assumption: comes from Wodify export or integration.

Key fields expected:

- Member name.
- Member email.
- Attendance dates.
- Class count in the recent window.
- Last attended date.
- Member status.
- Membership type.
- Lead status if available.
- Class participation.

## Member Segment

A group of members with similar attendance or engagement context.

Initial manual segments:

- Consistent: members attending 4+ times per week.
- Active: members attending 2-3 times per week.
- At Risk: members attending 0-1 times per week or showing attendance decline.
- New: members in their first 90 days.

Segment rules should be based on Wodify attendance data. If Wodify data is missing or insufficient, mark the segment as `Unknown`.

## Member Email Draft

An internal draft written for a segment. It must feel like coaching, not marketing.

Required qualities:

- Useful.
- Human.
- Low-pressure.
- Specific to the week's training themes.
- Free of health promises.
- Free of CrossFit positioning.

## Human Review

The required approval step before any member-facing message is sent.

Review checks:

- Accuracy.
- Tone.
- Segment fit.
- No unsupported claims.
- No accidental shame or pressure.
- No prohibited positioning.

## Send Record

The manual record that a reviewed email was sent.

Minimum fields:

- Date sent.
- Segment.
- Subject line.
- Reviewer.
- Sender.
- Notes.

## Measurement Record

The basic tracking record used after sending.

Minimum fields:

- Segment.
- Email sent date.
- Open or engagement data if available.
- Attendance change if available.
- Qualitative member replies.
- Staff observations.

If data is missing, record `No measurements found`.

## Future Record Vocabulary

These records are architectural placeholders only. Do not build them into the MVP until the relevant future module is activated.

### Core Member Record

Future source: Wodify.

Potential use: shared member identity across attendance, retention, recognition, referral, and communication workflows.

### Attendance Record

Future source: Wodify.

Potential use: attendance frequency, decline, missed weeks, class utilization, streaks, and retention signals.

### Coach Record

Future source: Wodify exports, staff-maintained lists, or future internal records.

Potential use: coach standards, class trends, member feedback, coach follow-up, and recognition workflows.

### Milestone Record

Future source: Wodify attendance and manually confirmed achievements.

Potential use: 25, 50, 100, 250, and 500 visit recognition, benchmark tracking, and anniversary triggers.

### Recognition Record

Future source: Wodify signals, coach nominations, staff nominations, and human approval.

Potential use: Member of the Month, coach recognition, community stories, and recognition history.

### Referral Record

Future source: Wodify lead source data, staff notes, and future referral tracking.

Potential use: referral candidates, ambassador program, referral conversion, and referral retention.

### Content Record

Future source: human-approved stories, public posts, website stories, email features, and knowledge base entries.

Potential use: public content, member education, local authority, and coach onboarding.

### Communication Record

Future source: manually tracked sends, reviewed drafts, future email tooling, and human approval.

Potential use: member emails, coach follow-ups, referral requests, recognition drafts, and executive briefs.
