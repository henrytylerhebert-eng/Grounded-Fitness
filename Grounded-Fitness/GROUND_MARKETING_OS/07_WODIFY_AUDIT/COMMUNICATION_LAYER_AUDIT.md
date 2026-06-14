# Wodify Communication Layer Audit

Source context: live Wodify Communication screens shared on June 12, 2026.

Purpose: document Wodify's communication surfaces before any Grounded AI communication, email, or automation decisions.

## Audit Boundary

This is an inventory document only.

Do not:

- Send marketing emails.
- Send automated emails.
- Change communication settings.
- Create, publish, or schedule templates.
- Change chat or calendar-event settings.
- Alter coach availability.
- Connect Grounded AI to Wodify Communication.

Grounded AI may draft and recommend. Wodify remains the execution system.

## Communication Modules Observed

The Communication navigation includes:

- Tasks.
- Inbox.
- Announcements.
- Marketing Emails.
- Automated Emails.
- Templates.
- Settings.

There is 1 visible inbox indicator.

## Communication Settings Observed

### Automated Email Defaults

| Setting | Observed value | Audit note |
|---|---|---|
| Default from email | `info@wodifymail.com` | Wodify-managed send address. Confirm deliverability/domain expectations before branded campaigns. |
| Default from name | `Grounded Fitness` | Short brand name; confirm whether member-facing communications should use `Grounded Fitness Acadiana`. |
| Reply to | `groundedfitnessacadiana@gmail.com` | Matches observed environment property; confirm this inbox is monitored. |

### In-App Chat

Observed state:

- In-App Chat is on.
- Storage: 32/1000 conversations.
- 1-on-1, group, and segment chats automatically delete after 365 inactive days.
- Class chats automatically delete after 90 inactive days.

Audit note: Grounded AI should not read, summarize, send, or automate chat without explicit future approval and privacy review.

### Calendar Events

Observed state:

- Calendar event functionality is on.
- Calendar events allow clients and leads to receive events for drop-ins, free trials, and free intros.

Audit note: Wodify already supports calendar-event delivery for key lead/client appointment contexts. Do not build calendar notification logic in Grounded AI.

### Coach Availability

Observed state:

- Coach availability table shows 16 ordered coach records with availability checkboxes.

Audit note: coach routing and availability are Wodify configuration concerns. Grounded AI may recommend follow-up ownership in reports, but must not change coach availability or assignment settings.

## Marketing Emails Observed

The Marketing Emails screen describes mass emails as a way to target groups of clients and leads.

Observed counts and records:

- Scheduled: 0.
- Drafts: 3.
- Total visible marketing email items: 4.
- One sent marketing email, `We Started a`, was sent to All Active Clients on Dec 22, 2025.
- Observed delivery result for that sent email: 89 delivered, 1 bounced.
- Three visible drafts:
  - `(new email) 01/16/2026 08:54:05`.
  - `(new email) 01/16/2026 11:47:50`.
  - `(new email) 04/23/2025 06:07:27`, recipients: Coaches.

Audit notes:

- Marketing Emails are a Wodify-owned broadcast channel, not a Grounded AI execution channel.
- Grounded AI may draft campaign copy or analyze past results only after approved exports/screenshots.
- Grounded AI must not create, schedule, send, archive, or delete marketing emails.
- The sent result is a real observed metric, but no campaign outcome, revenue, retention, or engagement conclusion should be claimed from it.

## Automated Emails Observed

The Automated Emails screen describes emails that Wodify sends to clients and employees.

Observed count:

- 79 automated email records.
- Visible page range: 1 to 20 of 79 records.

Visible records included:

| Name | Description | Observed active status |
|---|---|---|
| Anniversary Email | Congratulate your Client on key membership anniversary dates | `5 of 5` variants active/available |
| Bank Account Unverified | Notify the Client when their bank account requires verification | Toggle visible |
| Birthday Email | Wish your Clients a Happy Birthday | Toggle visible |
| Canceled Appointment - Client | Email the Client when provider is not available for appointment | Toggle visible |
| Canceled Appointment - Provider | Email provider when unavailable for appointment | Toggle visible |
| Canceled Appointment (Recurring) - Client | Notify the Client when recurring appointment is cancelled | Toggle visible |
| Canceled Appointment (Recurring) - Provider | Notify providers when recurring appointment is cancelled | Toggle visible |
| Canceled Class Automatically - Coaches | Alert staff when a class is auto-cancelled for low reservations | Toggle visible |
| Canceled Class Manually - Coaches | Alert staff when a class is manually cancelled | Toggle visible |
| Canceled Class was Reinstated - Coaches | Notify staff that a cancelled class is back on schedule | Toggle visible |
| Canceled Recurring Class Manually - Coaches | Notify staff when recurring classes are deleted | Toggle visible |
| Changed Provider - Client | Notify Client when appointment provider changes | Toggle visible |
| Changed Provider - new Provider | Notify new provider of appointment after change | Toggle visible |
| Changed Provider - old Provider | Notify old provider they no longer have appointment | Toggle visible |
| Changed Provider (Recurring) - Client | Notify Client when provider changes for recurring appointment | Toggle visible |
| Changed Provider (Recurring) - new Provider | Notify new provider of recurring appointment | Toggle visible |
| Changed Provider (Recurring) - old Provider | Notify old provider they no longer have recurring appointment | Toggle visible |
| Created Appointment - Provider | Notify providers of a new appointment booking | Toggle visible |
| Created Appointment - Client | Notify the Client of a new appointment booking | Toggle visible |
| Created Appointment (Recurring) - Client | Notify the Client when a new recurring appointment is booked | Toggle visible |

Audit notes:

- Wodify already owns many transactional and operational emails.
- Grounded AI must not duplicate appointment, cancellation, provider-change, birthday, anniversary, bank-account, or class-cancellation emails.
- Some automated emails involve payment, scheduling, and staff operations; these are sensitive and should stay inside Wodify.
- A tone audit may be useful, but execution should remain in Wodify.

## Reusable Templates Observed

The Templates screen includes:

- Drag & Drop Emails.
- Saved Rows.
- Rich Text Emails.
- Template Library.
- Create Template.

Observed state:

- Published: 0.
- Drafts: 1.
- One draft drag-and-drop template: `(new template) 06/06/2026 18:28:15`.
- The draft is attributed to Tyler Hebert.
- Tag state: No tag.

Audit notes:

- General Templates are separate from Workflow Email Templates.
- Grounded AI may draft copy or structure for human review.
- Grounded AI must not create or publish templates in Wodify during MVP.
- Before any template is used, confirm owner, purpose, audience, brand fit, and whether it is connected to Marketing Emails, Automated Emails, or Workflow Builder.

## Communication Layer Conclusions

Wodify already owns communication execution across:

- Broadcast marketing emails.
- Transactional automated emails.
- Workflow email templates.
- Reusable email templates.
- In-app chat.
- Calendar-event delivery.
- Reply/from settings.
- Coach availability routing.

Grounded AI should not become a communication platform.

Near-term Grounded AI role:

1. Inventory communication surfaces.
2. Flag duplicate or risky communication paths.
3. Draft human-reviewed copy.
4. Audit tone, placeholders, offers, and brand language.
5. Summarize observed results only when source evidence exists.

Do not send, schedule, publish, toggle, or configure Wodify communications.
