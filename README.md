# GROUNDED FITNESS ACADIANA — MARKETING OS
### `GROUND_MARKETING_OS` | Active Build | Lafayette, Louisiana

---

## WHAT THIS IS

A structured marketing operating system for Grounded Fitness Acadiana — a community gym in Lafayette, Louisiana co-owned by Tyler and Brooke Hebert.

This repo contains the brand standards, content systems, automation workflows, and PAW marketing agent prompts that power Grounded's social media presence and content operation.

It is **not** a generic social media tool. It is purpose-built for one brand with a specific voice, a specific community, and specific platforms.

---

## CURRENT BUILD STATUS

| Layer | Status | Notes |
|-------|--------|-------|
| Brand voice & standards | ✅ Complete | See `00_FOUNDATION/ANCHOR.md` |
| Content category system | ✅ Complete | 5 categories, PAW prompts written |
| PAW agent prompt library | ✅ Complete | See `03_AGENTS/` |
| Photo content engine | ✅ Operational | Manual workflow, no automation yet |
| Daily posting cadence | ✅ Defined | IG + FB, 5-7x/week |
| n8n automation workflows | 🔴 Not yet built | Blocked pending scope decision |
| Postiz integration | 🔴 Not yet built | Missing: account IDs, review gate |
| Auto-publishing | 🔴 Out of scope | See `SCOPE_BOUNDARIES.md` |

---

## PLATFORMS (CONFIRMED — per `ANCHOR.md`)

- **Instagram** — primary, daily
- **Facebook** — mirrored from Instagram
- **YouTube** — video content only, separate workflow (not yet built)

**Not in scope:** TikTok, Twitter/X (may be revisited — see `06_ROADMAP/`)

---

## FOLDER STRUCTURE

```
GROUND_MARKETING_OS/
│
├── 00_FOUNDATION/
│   ├── ANCHOR.md              # Brand truth, platform decisions, owner info
│   ├── SCOPE_BOUNDARIES.md    # What is/isn't automated, what requires human review
│   └── AI_RULES.md            # Rules all PAW agents must follow
│
├── 01_BRAND/
│   ├── voice-and-tone.md      # Brand voice rules, clichés to avoid, examples
│   ├── hashtag-system.md      # Anchor tags, rotation sets, never-use list
│   └── posting-cadence.md     # Day-by-day category guide
│
├── 02_CONTENT/
│   ├── photo-content-engine.md   # 5 category system + sort guide
│   ├── categories/
│   │   ├── 01_the-floor.md       # Action shots, classes, workouts
│   │   ├── 02_member-spotlights.md
│   │   ├── 03_the-space.md       # Facility, equipment, vibe shots
│   │   ├── 04_events-challenges.md
│   │   └── 05_mindset-culture.md
│   └── caption-formulas.md       # Per-category caption structures
│
├── 03_AGENTS/
│   ├── PAW_AGENT_MASTER.md    # Master prompt with all brand rules
│   ├── prompts/
│   │   ├── the-floor.prompt
│   │   ├── member-spotlight.prompt
│   │   ├── the-space.prompt
│   │   ├── events-challenges.prompt
│   │   └── mindset-culture.prompt
│   └── batch-session-guide.md # How to run a week of content in 30 min
│
├── 04_WORKFLOWS/
│   ├── manual-posting-sop.md  # Current human workflow (Tyler/Brooke)
│   └── n8n/
│       └── social-auto-draft.json   # 🔴 PARKED — not deployable yet
│                                    # Wrong Drive folder ID
│                                    # Wrong Postiz account IDs
│                                    # Missing human review gate
│                                    # See _grounded_adaptation_notes inside
│
├── 05_CREDENTIALS/
│   └── .env.example           # Required env vars (values NOT committed)
│                              # POSTIZ_IG_ACCOUNT_ID=
│                              # POSTIZ_FB_ACCOUNT_ID=
│                              # GOOGLE_DRIVE_FOLDER_ID=
│                              # OPENAI_API_KEY=
│
├── 06_ROADMAP/
│   ├── option-c-build-plan.md # When ready: full automation build spec
│   └── scope-decisions-log.md # Record of what changed and when
│
└── README.md                  # This file
```

---

## BRAND VOICE (QUICK REFERENCE)

**Sound like:** A coach who knows your name. Warm, direct, Louisiana-rooted.

**Never sound like:** A fitness influencer. A brand deck. A gym chain.

**Banned phrases:** "beast mode," "crush your goals," "grind," "no days off," "rise and grind," "level up," "hustle"

**Always true:** Community over performance. Real names. Real moments. Acadiana-proud.

**Platforms format:** Caption under 150 words (spotlights up to 200). Line breaks for mobile. Hashtags always separated at bottom.

**Hashtag anchors (always):** `#GroundedFitnessAcadiana` `#Lafayette` `#AcadianaFitness`

---

## CONTENT OPERATION — HOW IT RUNS TODAY

### Manual Workflow (current)
1. Tyler or Brooke selects a photo from the library
2. Photo is sorted into one of 5 content categories
3. A 2–3 sentence photo description is written
4. Description is dropped into the matching PAW agent prompt
5. Agent returns a ready-to-post caption
6. Tyler or Brooke does a 10-second review and approves
7. Post is manually scheduled or published to Instagram + Facebook

### Batch Session (recommended weekly)
- Pick 7 photos on Sunday or Monday
- Write all 7 descriptions at once
- Run all 7 PAW prompts in sequence
- Full week of content in ~30 minutes
- Schedule via native Instagram/Facebook tools until Postiz is connected

---

## AUTOMATION — WHAT'S BLOCKED AND WHY

The `04_WORKFLOWS/n8n/social-auto-draft.json` file exists but is **not deployable**.

Current blockers:
1. **Scope** — Auto-publishing without human review is explicitly out of scope per `SCOPE_BOUNDARIES.md`
2. **Drive folder ID** — Still points to original client's folder. Grounded's folder ID must be confirmed and swapped in.
3. **Postiz account IDs** — File contains original client's TikTok/Twitter/multi-Instagram IDs. Grounded uses Instagram + Facebook only. Real IDs needed.
4. **No review gate** — `AI_RULES.md` requires human approval before any post goes live. This step is not yet designed into the workflow.

### To Unblock (Option C build)
When ready, update `SCOPE_BOUNDARIES.md` to reflect automation decision, then:

```
□ Confirm Grounded's Google Drive folder ID
□ Get Grounded's Postiz account IDs (Instagram, Facebook)
□ Confirm OpenAI API key in Postiz or n8n
□ Design draft/review step (Slack notification? Email? Manual Postiz queue?)
□ Update SCOPE_BOUNDARIES.md with new decision
□ Rebuild workflow from scratch with correct IDs + review gate
□ Test with 1 post before activating full schedule
```

---

## PAW AGENT RULES (ALL AGENTS MUST FOLLOW)

These are non-negotiable for any AI agent generating Grounded content:

1. **No post goes live without human approval.** Draft only. Always.
2. **Follow the brand voice document.** Check it before generating. No exceptions.
3. **Never invent member details.** If information isn't provided, ask — don't fabricate.
4. **Platform-specific formatting.** IG captions and FB captions may differ in length.
5. **Hashtag block always at the bottom**, separated from caption by a line break.
6. **One version, not options.** Execute the best version. Tyler/Brooke will redirect if needed.
7. **No generic fitness copy.** If it could appear on any gym's Instagram, rewrite it.

---

## OWNERS

| Person | Role |
|--------|------|
| Tyler Hebert | Co-owner, content strategy, PAW operator |
| Brooke Hebert | Co-owner, content creation, voice authority |

**Brand decisions:** Tyler and Brooke both have veto authority over any content before it publishes.

---

## RELATED SYSTEMS

- **OM Venture OS** (`henrytylerhebert-eng/OM-Venture-OS`) — Opportunity Machine's venture operating system. Separate brand, separate system, separate repo.
- **Keepers Marketing OS** — STR platform client, separate engagement.
- **PAW (Marketing Agent Framework)** — shared agent infrastructure used across all Tyler's marketing OS builds.

---

_This README reflects the build state as of June 2026._
_Update this file when scope decisions change or automation is activated._
