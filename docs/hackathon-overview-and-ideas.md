# eMerge AI Hackathon 2026 — Overview & Ideas

_Prepared: 2026-10-15 (updated the same day to add aviation MRO ideas)_
_Event page: https://luma.com/aihackathon26_

## Event summary

| Item | Detail |
|---|---|
| Date | Saturday, October 17, 2026 |
| Hours | 8:00 AM – 8:00 PM ET |
| Venue | The LAB Miami, 2750 NW 3rd Ave #24, Miami, FL 33127 (Wynwood) |
| Organizers | Miami AI Hub, powered by eMerge Americas |
| Registration | Host approval required; capacity limited |
| Team size | Solo or up to 5 people |
| Food | Breakfast, lunch, dinner, and snacks provided |

### Schedule

| Time | Item |
|---|---|
| 8:00 AM | Check-in and breakfast |
| 8:30 AM | Opening remarks |
| 9:00 AM | Hacking begins |
| 6:00 PM | Submissions close |
| 6:30 PM | Finalist pitches |
| 7:30 PM | Winners announced |
| 8:00 PM | Wrap-up |

### Rules that matter

- Problem sets are released on Oct 15 through the hackathon dashboard. This doc is based on the public track summaries, so check the full briefs.
- **All project code must be written during the 9:00 AM – 6:00 PM window.** You can't bring existing code or boilerplate. Research, data exploration, and specs are fine beforehand.
- A submission needs a **working demo**, a **public repository**, and a **short pitch deck**.
- Teams keep their IP.

## Tracks

1. **Enterprise AI (supported by Archie):** agents, copilots, and automation for business workflows, knowledge discovery, decision-making, sales, or customer experience.
2. **Healthcare (supported by Sylvester Comprehensive Cancer Center):** cancer care challenges across lifestyle medicine, survivorship, precision medicine, and drug discovery, using open datasets.
3. **Education (supported by Millennium):** build the Miami-Dade School Navigator. It should be a trusted, map-based platform that lets families explore and compare school options from infancy through 12th grade.

## Prizes ($7,000 total)

- **Track prizes:** $1,000 to the first-place team in each track ($3,000 total).
- **Best use of Archie, across all tracks:** $2,500 / $1,000 / $500. These are **separate from and stackable with** the track prizes.
- Every member of a 1st/2nd/3rd-place team in each track gets tickets to the Miami AI Summit and eMerge Americas, plus investor introductions.
- **Perks:** free Archie access on event day, and $200 in Devin (Cognition) credits for up to 200 hackers.

### Strategic takeaway

The Archie prize pool ($4,000) is larger than all track first prizes combined, and it stacks with them. **Optimize for a strong track entry that also clearly showcases Archie.**

## About Archie

Archie is Archie Labs' "idea-to-application" platform. Archie Labs grew out of 8base. Archie turns a prompt into a project blueprint covering functional requirements, UX architecture, wireframes, and technical architecture. 8base can then generate an app foundation from those specs: data model, test data, backend functions, and a GraphQL API.

**How to use it:** spend the first ~45 minutes producing a real spec in Archie, then build from it. In the pitch, show the Archie-generated spec and explain how it drove the build. This matches a spec-driven, plan-first workflow.

## My unfair advantage: aviation maintenance (MRO)

I spent about 20 years at Trax (trax.aero), an enterprise aircraft-maintenance system used by airlines and repair shops. It covers:
- materials management (inventory, purchasing)
- engineering setup
- planning and work orders
- financials
- defect-report tracking
- integrations with financial systems (SAP) and flight-ops systems (Sabre)

**Why this matters here:**
- **The Enterprise track fits perfectly.** Aviation MRO is a textbook enterprise workflow problem: heavily regulated, document-heavy, integration-heavy, and expensive when it goes wrong (AOG, aircraft on ground).
- **Very few competitors will know this domain.** Most Enterprise entries will be generic sales or support copilots. A credible MRO entry stands out right away.
- **It plays well locally.** South Florida is a major aviation and MRO hub, so the judges and investors in the room will recognize the problem.
- **It makes Archie shine.** A spec written with real domain depth (ATA chapters, MEL deferrals, AD applicability, task cards) will produce a much better Archie blueprint than a generic idea will. That helps in the Archie prize judging.
- **Open data exists.** Public FAA data can be explored before Saturday:
  - the Service Difficulty Reporting System (SDRS), which holds real-world defect reports
  - Airworthiness Directives (ADs)
  - the aircraft registry

## Ideas

### Enterprise AI — aviation MRO (new top tier)

**A. Defect / tech-log copilot ⭐ (recommended)**
- Input: a free-text pilot or mechanic write-up.
- The AI does the following:
  - Classifies the write-up to an **ATA chapter**.
  - Flags whether the item may be **MEL-deferrable**. This is advisory only, and a human signs off.
  - Detects **repeat or chronic defects** on the same tail number or system.
  - Suggests troubleshooting steps and likely parts, based on similar historical reports.
- **Demo data:** the public FAA SDRS records, so the demo uses real defect narratives.
- **Pitch:** fewer repeat defects, faster dispatch decisions, less AOG time.
- **Scope:** fits in 9 hours, with a strong visual demo of a write-up going in and a classified, cross-referenced result coming out.

**B. AD/SB applicability agent**
- Ingests a new Airworthiness Directive or Service Bulletin.
- Parses its applicability rules (aircraft type, serial-number ranges, part numbers, compliance deadlines).
- Matches those rules against a sample fleet and component configuration.
- Drafts the resulting compliance tasks and work-package items, citing the exact AD paragraph behind each one.
- **Differentiator:** transparent reasoning that shows why each tail is or isn't affected.

**C. AOG parts-sourcing copilot**
- Trigger: an aircraft goes AOG for a part.
- The agent then does the following:
  - Checks inventory across stations.
  - Checks interchangeable and alternate part numbers.
  - Checks open purchase orders and repair orders.
  - Drafts RFQs to vendors.
  - Ranks the options by time-to-aircraft and cost.
- This draws directly on materials-management and purchasing domain knowledge.

**D. Work-package planning assistant**
- Given due tasks (checks, ADs, deferred defects) and a hangar slot, the assistant proposes a bundled work package.
- It estimates labor hours and flags parts or tooling shortfalls.
- It's a stronger idea but has more moving parts, so it's harder to finish in 9 hours.

### Enterprise AI — other

**E. Integration-mapping copilot**
- Input: two API specs or sample payloads (for example, an MRO system and SAP, or a legacy CRM and a new platform).
- It proposes field mappings with confidence scores.
- It generates transform code and tests.
- It flags fields it can't map.
- This draws on integration experience at both Trax (SAP/Sabre) and Soleo (Workato → ESP).

**F. Florida condo compliance copilot**
- Answers questions over a building's governing documents, inspection reports, and reserve studies.
- Tracks deadlines under Florida's post-Surfside condo laws.
- Has strong local resonance. All code would be written fresh at the event.

### Healthcare

**G. Cancer financial-toxicity navigator**
- The user enters a diagnosis, insurance type, and location.
- An agent surfaces relevant assistance programs and foundation funds, plus plain-language next steps.
- This builds on TailorMed / financial-assistance experience. Source the data from open, public information.

**H. Clinical trial matcher**
- Uses the ClinicalTrials.gov v2 API.
- An LLM parses free-text eligibility criteria into structured rules.
- It matches those rules against a patient profile and filters to trials in South Florida.
- **Differentiator:** transparent eligibility parsing that shows which criteria matched, which failed, and which are uncertain.

### Education (most constrained: everyone builds the same product)

**I. Miami-Dade School Navigator, made distinctive by:**
- **Trust:** every claim cites its data source.
- **Multilingual:** English, Spanish, and Haitian Creole.
- **Natural-language search,** e.g. "STEM magnet near 33137 with bus service, grades 6–8."
- **Side-by-side comparison** of schools.

## Recommendation

- **Primary:** Enterprise track, **idea A (defect / tech-log copilot)**, built from an Archie-generated spec and using real FAA SDRS data. This is where 20 years of domain expertise matters most. It competes for both the Enterprise track prize and the Archie prizes, and the Enterprise track is the one Archie sponsors.
- **Alternates:** idea B (AD applicability agent) if it demos better on paper; idea G or H in Healthcare if the released Enterprise brief turns out to be very narrow.
- **Pitch angle:** "I spent 20 years building aircraft-maintenance software. Here's the problem every airline still has, and here's what AI can now do about it."

## Prep checklist (before Saturday)

- [ ] Confirm registration approval on Luma
- [ ] Read the full problem sets on the hackathon dashboard (released Oct 15) and confirm that an aviation/MRO idea fits the Enterprise brief
- [ ] Download and explore the FAA SDRS data and a handful of ADs, without writing code
- [ ] Draft the Archie prompt and spec outline for the chosen idea (ATA classification, MEL logic, repeat-defect rules)
- [ ] Pick a stack that's fast for a greenfield web app (Grails is likely too heavy for 9 hours)
- [ ] Line up LLM API keys and a deploy target (e.g. Vercel or Cloud Run)
- [ ] Redeem Devin credits when details arrive
- [ ] Outline the pitch deck: problem → demo → how Archie drove the build → impact (AOG hours or cost saved)
- [ ] Pack laptop, charger, and power strip

## Sources

- [eMerge AI Hackathon 2026 · Luma](https://luma.com/aihackathon26)
- [Archie Labs on G2](https://www.g2.com/sellers/archie-labs)
- [8base / Archie on Toolradar](https://toolradar.com/tools/8base)
- [Trax](https://www.trax.aero)
