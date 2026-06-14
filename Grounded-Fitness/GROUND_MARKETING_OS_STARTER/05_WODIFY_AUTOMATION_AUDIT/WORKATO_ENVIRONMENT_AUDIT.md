# Workato Environment Audit

Source context: live Wodify Automations / Workato and Wodify Communication screens shared on June 12, 2026, plus the pasted Workato recommended-app inventory.

Purpose: document the surrounding Workato environment before any future integration decisions.

## Audit Boundary

This is an inventory and risk-control document only.

Do not:

- Create Workato API clients.
- Install community connectors.
- Connect AI model providers.
- Send real member data to third-party AI tools.
- Create, update, delete, or alter Wodify records.
- Activate or edit Wodify workflows without human approval.
- Change Wodify communication settings.
- Send, schedule, publish, or toggle Wodify communications.

Initial Grounded AI scope remains fake/sample CSV analysis only.

## Environment Properties Observed

The Environment Properties screen showed 11 properties.

| Property | Observed value | Audit note |
|---|---|---|
| Facebook Link | `https://www.facebook.com` | Generic placeholder; update before using in workflow emails. |
| Instagram Link | `https://www.instagram.com` | Generic placeholder; update before using in workflow emails. |
| `wodify_business_email` | `groundedfitnessacadiana@gmail.com` | Confirm as approved public/business reply address. |
| `wodify_client_profile_link` | `https://app.wodify.com/Admin/Main?q=ClientProfile%7CId%3D` | Useful internal deep-link base; do not expose publicly. |
| `wodify_custom_dictionary_coach` | `Coach` | Safe operational label. |
| `wodify_customer_id` | `3643` | Internal identifier; do not publish. |
| `wodify_date_format` | `%m/%d/%Y` | Safe formatting property. |
| `wodify_online_sales_portal` | `groundedfitness.wodify.com` | Confirm whether workflows should include full URL. |
| `wodify_time_format` | `%l:%M %p` | Safe formatting property. |
| X Link | `https://twitter.com` | Generic placeholder; likely remove or update before using. |
| Youtube Link | `https://www.youtube.com` | Generic placeholder; update before using in workflow emails. |

Latest activity observed:

- `wodify_client_profile_link` updated by Wodify Pro on Feb 19, 3:03 PM.
- `wodify_custom_dictionary_coach` updated by Wodify Pro on Feb 19, 3:03 PM.
- `wodify_time_format` updated by Wodify Pro on Feb 19, 3:03 PM.

## Environment Property Recommendations

Before activating or updating any recipe that pulls social/profile values:

1. Replace generic social links with approved Grounded Fitness links.
2. Confirm the business email is the preferred reply or notification address.
3. Treat `wodify_customer_id`, workspace IDs, and client profile URL bases as internal-only.
4. Keep sensitive values out of environment properties unless they use `password`, `key`, or `secret` naming and Wodify/Workato masking is confirmed.
5. Prefer consistent property naming for future custom values, such as `grounded_public_instagram_url` or `grounded_public_youtube_url`.

## Community Library Surface

The Community Library and pasted recommended-app inventory show a broad Workato connector surface.

Observed high-risk or high-relevance categories include:

- AI/model providers and tools: OpenAI, Anthropic, Google Gemini, Azure OpenAI, AWS Bedrock, Mistral AI, DeepSeek, Ollama, AI by Workato, Workato Genie, MCP, Perplexity.
- Data and search tools: Google BigQuery, Qdrant, Brave Search.
- Speech, vision, and document tools: Google Speech to Text, Google Text to Speech, Google Vision, Google Natural Language, Amazon Textract, ElevenLabs, Rossum.
- Automation and agent tools: Automation Anywhere, BotPress, Skyvern, Moveworks.
- CRM, productivity, and operations tools: Airtable, HubSpot, Salesforce, Slack, Gmail, Google Sheets, Google Drive, Jira.

Important conclusion: availability is not approval.

The connector library creates opportunity, but it also creates privacy, security, cost, and source-of-truth risk. No community connector should be installed or connected during the MVP.

## API Clients Observed

The API Clients screen showed:

- No API clients yet.
- The screen indicates a client role must be added before creating API clients.
- API clients would grant role-based endpoint access to Workato APIs.

Recommendation:

- Do not create API clients now.
- Future API access requires a role design, least-privilege review, credential storage plan, logging/audit plan, and explicit approval.
- First future API posture should be read-only.

## Workspace Admin Observed

The Workspace Admin screens showed:

- Workspace name: Grounded Fitness Acadiana.
- Workspace ID: `4786034`.
- Session timeout duration: 7 days.
- Active job execution time unit: Minutes.
- Active job execution time limit: 90 minutes.
- Access control showed 17 collaborators, including Wodify staff/system users and Tyler Hebert.

Recommendation:

- Review collaborator access before any future API or connector work.
- Confirm whether deprecated roles are expected Wodify-managed access.
- Do not publish workspace ID or collaborator details.

## Environment Audit Conclusion

The Workato environment is powerful enough to automate a lot of work, but the current Grounded AI project should stay deliberately narrow.

Near-term action should be:

1. Clean up environment properties that could appear in workflow emails.
2. Audit existing Wodify recipes, automated emails, marketing emails, templates, and communication settings.
3. Keep API clients at zero.
4. Keep community connectors disconnected.
5. Use Grounded AI only for analysis, recommendations, and draft copy from approved exports.
