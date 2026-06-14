# CSV Schema Assumptions

These are assumptions only. Validate them against fake/sample exports first and real Wodify exports later outside git.

Grounded AI consumes exports. Wodify owns the records.

## Expected Export Families

- Leads.
- Clients.
- Drop-Ins.
- Segments.
- Progressions.
- Memberships.
- Membership Holds.
- Programs.
- Classes.
- Appointments.
- Tasks.
- Automations.
- Communications.
- Announcements.
- Marketing Emails.
- Attendance Reports.
- Revenue Reports.
- Lead Reports.
- Retention Reports.
- Performance Reports.

## Sample CSV Families

### `members.csv`

Potential fields:

- member_id
- first_name
- last_name
- email
- phone
- status
- membership_type
- join_date
- cancellation_date
- freeze_status

### `attendance.csv`

Potential fields:

- attendance_id
- member_id
- class_id
- attendance_date
- class_time
- coach_id
- attended_status

### `memberships.csv`

Potential fields:

- membership_id
- member_id
- plan_name
- plan_type
- start_date
- end_date
- status
- price
- discount

### `payments.csv`

Potential fields:

- payment_id
- member_id
- payment_date
- amount
- status
- payment_type
- discount
- failed_payment_reason

### `leads.csv`

Potential fields:

- lead_id
- name
- email
- phone
- source
- created_date
- intro_status
- conversion_status

### `classes.csv`

Potential fields:

- class_id
- class_name
- class_date
- class_time
- coach_id
- capacity
- attendance_count

### `coaches.csv`

Potential fields:

- coach_id
- coach_name
- status
- role

## Validation Rule

If a field is missing, record `Unknown`.

If a metric cannot be calculated, record `No measurements found`.

Do not infer missing Wodify fields as facts.
