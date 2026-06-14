# Scope Boundaries

## In Scope For Initial Build

The initial build is the foundation for the Member Value Engine.

Included:

- Grounded-specific positioning rules.
- Member Value Engine workflow definition.
- Domain objects.
- Manual validation assumptions.
- AI boundaries.
- Human review rules.
- MVP acceptance criteria.
- Backlog for build cycle 1.

## Out Of Scope For Initial Build

Do not build:

- Local Authority Engine.
- Lead Nurture Engine.
- New Member Success Engine.
- Coaching Standards Engine.
- Referral Engine.
- Exit Intelligence Engine.
- Member Success Framework.
- Community Partnership Engine.
- Executive Weekly Brief.
- Grounded Knowledge Base.
- Community & Recognition Engine automation.
- Production Gmail integration.
- Production Wodify integration.
- Website or blog publishing system.
- Canva production workflow.
- Instagram automation.
- Facebook automation.
- YouTube automation.
- Google Business Profile automation.
- Financial analysis.
- Automatic email sending.
- Automatic lead or member outreach.
- Any tooling that alters Wodify records.
- Direct Wodify API integration.
- Real member-data fixtures.
- Automatic recognition publishing.
- Automatic referral requests.
- Automatic coach outreach.

## Manual First Rule

The first version should run manually with clear inputs, outputs, review steps, and tracking. Only after the workflow proves useful should the repo introduce automation.

## Claims Boundary

Do not claim success without measurement.

If attendance or engagement data is missing, say `No measurements found`.

If a source cannot be verified, say `Unknown`.

## Health And Fitness Boundary

Grounded content may encourage consistency, coaching conversations, practical preparation, strength, and real-life fitness.

Grounded content may not promise:

- Weight loss.
- Injury prevention.
- Disease treatment.
- Guaranteed health outcomes.
- Guaranteed performance outcomes.

## Brand Boundary

Grounded may be described as a functional fitness gym.

Grounded may not be marketed as CrossFit.

## Source Of Truth Boundary

Wodify is the source of truth for active members, attendance, member status, membership type, lead status, and class participation.

Gmail is the source of truth for weekly programming emails.

Human approval is the source of truth for final content, member communication, publishing, and business decisions.

## Data Privacy Boundary

Do not commit real member data.

All real exports must stay outside git.

Use fake sample data for testing.

Remove, hash, or mask member identifiers when possible.

AI may flag risk, but AI may not decide action.

AI may not send outreach automatically.

## Recognition Boundary

AI may prepare recognition candidates, milestone reminders, referral candidates, and community story opportunities.

AI may not select Member of the Month, publish recognition content, ask for referrals automatically, or use personal stories publicly without human approval and member consent.

## Roadmap Boundary

Future roadmap modules may influence naming, records, and data design.

They may not expand the initial MVP.

The current MVP remains:

Weekly Programming Email -> Wodify Segmentation -> Member Value Emails
