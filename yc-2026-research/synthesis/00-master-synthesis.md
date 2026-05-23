# Master Synthesis — YC 2026 Idea Research

**Date:** 2026-05-23. **For:** Solo dev with agent swarms. **Deadlines:** YC late S26 + Standard Capital $100B Seed Group (May 28).

## 1. The 6-Agent Convergence (what's robust)

Six independent agents, each given a different lens, all arrive at the same shape:

> **Build an AI-native service or service-tier B2B SaaS for a single boring/regulated vertical, where Excel/fax/manual labor is mission-critical today, where the moat lives in integration + per-customer data + regulatory/distribution access — not in the model itself.**

What every agent agreed on:

| Question | Convergent answer |
|---|---|
| What KIND of company? | Vertical AI-native service (RFS A1#2, A2#3) — sell finished outcomes, not seats. |
| What KIND of moat? | Workflow integration + proprietary per-customer data + distribution wedge + (ideally) regulatory or PMS/AMS/EHR/TMS integration. |
| What to AVOID? | Hardware, space, biotech, money-transmitter licensing, consumer social, "ChatGPT for X", anything where the model improving 20% closes your gap. |
| Frontier-kill test? | Model must be a swappable *component*, not a *dependency*. Value lives in actions taken in external systems. |
| Solo shape constraint? | V1 shippable in 60–90 days, revenue in 90 days, no enterprise procurement gate, no SOC2-from-day-1, no field hardware. |
| Distribution wedge? | Existing organized communities (NCPA, ADA, AVMA, state PT associations, etc.) — not cold outbound. |
| #1 founder filter? | **Who can you cold-DM and get a yes from for an unpaid pilot in 48 hours?** (Agent 2). Without this, no scoring matters. |

## 2. The Unified Scoring Rubric (combined from all 6 agents)

For any candidate idea, score across these 5 sections. Pass thresholds in parens.

### A. Founder-philosophy fit (Agent 3) — score /60
20 questions × 0–3 each. Pass at ≥45. Sections: Origin & insight, Demand & users, Vision & ambition, Defensibility & durability, Execution fit, Founder fit. (Full rubric in `agent-research/03-founder-philosophy.md`.)

### B. Failure inoculation (Agent 4) — score /35
7 sections × 0–5 each. Pass at ≥3.5 average AND ≥4 on Distribution risk AND ≥4 on Moat erosion AND pass full Tarpit Screen.

### C. Frontier-model survival (Agent 5) — score /5
Will-It-Survive-Claude-5 5-question gate. Pass at ≥4 yes:
1. Clone Test (≥2 of: data/integration/licence/distribution/brand)
2. Verifiability Test (proprietary feedback the lab can't see)
3. Component Test (works with half-quality open model)
4. Liability Test (you own the outcome, not the customer)
5. Diffusion Test (F500 won't deploy raw Claude into this in 24 months)

### D. Solo-dev feasibility (Agent 6) — score /5
1. V1 ships in ≤90 days?
2. First $1K MRR achievable in ≤120 days?
3. Distribution channel exists without enterprise procurement?
4. No regulatory clearance needed for v1 (no FDA, no SEC, no bar)?
5. Pricing model insulated from token-cost compression (outcomes/% recovered/per-event, not per-seat-flat)?

### E. Pain-point reality (Agent 2) — score /5
1. Real recurring weekly grind for the buyer?
2. $50K+/year annual problem at a single buyer?
3. Clearly named buyer persona with budget authority?
4. Current workaround is Excel/fax/manual/expensive consultant?
5. Heresy: identify the cherished assumption blocking incumbents (must be verifiable).

**Composite scoring band:**
- A≥45, B average≥3.5, C≥4, D=5, E=5 → **STRONG: apply to YC**
- A 40–44 or B 3.0–3.4 or C=3 → **MEDIUM: re-shape**
- Otherwise → **WALK AWAY**

## 3. The Top 12 Candidate Ideas (composite-scored)

All survive the inoculation checklist and Will-It-Survive-Claude-5 ≥4. Ranked by composite + solo-shape + distribution access.

| # | Idea | Buyer | RFS map | A | B | C | D | E | Notes |
|---|---|---|---|---|---|---|---|---|---|
| **1** | **Independent Pharmacy PBM/DIR Reconciliation** | Independent retail pharmacist owner-operator | A1#2 | 52 | 4.2 | 5 | 5 | 5 | Best composite. EDI structured, NCPA channel, monthly-quantified pain. |
| **2** | **AI-Native Compliance-as-a-Service for CMMC L2 (defense subs <50 ppl)** | Small DoD subcontractor CEO/CISO | A1#2 + A2#5 | 51 | 4.0 | 5 | 4 | 5 | ~80K eligible firms, none have software. ACV $40–80K. |
| **3** | **Outpatient-PT Prior Auth** | PT clinic owner / billing mgr | A1#2 | 51 | 4.1 | 5 | 5 | 5 | One solo dev already at $41K MRR — validates AND warns of competition. |
| **4** | **Independent P&C Agency COI Issuance** | P&C agency owner / CSR | A1#2 | 49 | 4.0 | 5 | 5 | 5 | AMS integration moat; Big "I" distribution channel. |
| **5** | **Medical Claim Denial Appeals** | 5–50 physician practice RCM team | A1#2 | 49 | 4.0 | 5 | 5 | 5 | 54% appeal-overturn rate = ROI-obvious sell. |
| **6** | **Dental Insurance Verification** | Independent dental practice | A1#2 | 48 | 3.9 | 5 | 5 | 5 | $7.11 → $1.48 per check; Open Dental/Dentrix gates. |
| **7** | **AI-native ERP for one niche manufacturer (craft distillery TTB or cannabis METRC)** | Independent operator | A1#11 + A1#12 | 48 | 3.7 | 5 | 4 | 4 | Regulatory reporting nightmare; small markets but high ACV. |
| **8** | **Home-Health Agency Fax-Referral Intake** | HH agency intake coordinator | A1#2 | 47 | 3.8 | 5 | 5 | 5 | "Fax is dead" heresy; OASIS rules; Axxess/HCHB write-back. |
| **9** | **Infra for Government Fraud Hunters (qui tam / whistleblower)** | OIG / qui tam law firm | A2#8 (Jared Friedman explicit) | 47 | 3.7 | 5 | 4 | 4 | YC explicitly requested; post-DOGE flow unbuilt. |
| **10** | **MCP-server / agent layer for one ugly enterprise SaaS (Epic, Veeva, NetSuite, Workday)** | Health systems / pharma / mid-market F500 | A1#12 + A1#13 | 46 | 3.6 | 5 | 4 | 4 | Pick Epic Hyperspace ops first — every health system needs it. |
| **11** | **Freight-Broker Anti-Double-Brokering Carrier Onboarding** | 5–50 person freight brokerage | A1#2 | 45 | 3.7 | 5 | 5 | 5 | Fraud angle is the wedge; FMCSA structured data; TMS write-back. |
| **12** | **Job-shop CNC RFQ Response (<50 employees, no MRP)** | Job-shop owner/estimator | A2#6 (adjacent) | 45 | 3.6 | 5 | 5 | 4 | Aging quoter retirements force the buy; Paperless Parts >$50K/yr leaves long tail. |

## 4. Honorable Mentions / Backups

- **AI-Native Agency for one specific deliverable** (e.g. SOC2 evidence as a service for AI startups, AI-native pentest agency) — RFS A2#3. High solo-fit, lowest YC-application strength (looks like a consultancy).
- **CRE Offering Memorandum generator for boutique brokerages** — survives if you own CoStar feed + rent-roll OCR. Caution: design templates getting easier.
- **Construction RFI/submittal routing for mid-tier GCs under Procore's price floor** — solid but harder distribution.
- **County clerk-of-court (not city council) docket minutes + FOIA-defensible audit trail** — small but defensible niche.

## 5. Traps (do not apply with any of these)

From Agent 1's trap list, with cross-confirmation from Agents 4 and 6:

1. **Industrial Capabilities in Space / Electronics in Space / Inference Chips / Modern Metal Mills / AI-Native Industrial Base / Counter-Swarm Defense / AI for Low-Pesticide Ag / AI-Native Discovery Engines / Autonomous Labs** — hardware/capital/multi-disciplinary. Solo-fatal.
2. **Stablecoin Financial Services / AI-Native Banking Infrastructure / AI-Native Hedge Fund** — money-transmitter / bank charter / SEC. Solo W26 fintech base rate: 0%.
3. **AI Personalized Medicine / Healthcare AI without clinical co-founder** — Olive AI ($900M+ shutdown) is the cautionary tale.
4. **AI-Native University / World Models in Storytelling** — accreditation / GPU competition.
5. **AI Personal Assistant (general) / AI-Native Discovery Engines (consumer search)** — frontier lab graveyard.
6. **"Cursor for PMs" / "ChatGPT for X" / yet-another-coding-tool** — capability arbitrage; dies on next model release.
7. **Generic developer infrastructure competing with hyperscalers** — Tune AI fate.
8. **Permit pulling for residential GCs in major metros** — PermitFlow + Sila already there.
9. **Restaurant inventory reconciliation** — MarketMan + Square + Toast sew it up.
10. **Staffing/recruiting resume screening** — frontier model commoditizes basic screening.

## 6. The Founder-Access Gate

Per Agent 2's flag (the single most under-discussed criterion):

> **The user has no stated industry background. The #1 selection filter is NOT score — it's *who you can cold-DM and get an unpaid-pilot yes from in 48 hours*. Recruit a paid co-design partner from the buyer pool BEFORE picking the idea.**

This is the Buffett "inside circle of competence" check + the YC "outsider+insider" rule + PG's "founders themselves want, themselves can build" filter. **Score #1 idea isn't #1 if you can't access the buyer.**

The Top 12 ordered by buyer-accessibility for someone with a developer background (no industry):
- **Easiest buyer access**: #11 freight broker, #10 MCP servers (dev → dev), #2 CMMC (small DoD subs are tech-friendly).
- **Medium**: #1 pharmacy via NCPA, #4 P&C agency via Big "I", #6 dental via ADA/Dentaltown.
- **Hardest**: #3 PT clinics, #5 medical billing, #8 home health — gated by HIPAA, BAAs, payor relationships.

## 7. Key Heresies (PG dead-zone gold)

Eight cherished assumptions that, if false, unlock big markets:

1. **"Fax is dead."** — Home health, dental verification, optical lab orders, provider-side prior auth all run on fax in 2026.
2. **"Vertafore / Procore / ServiceTitan / Epic own those markets."** — They own the top decile by spend; the sub-economic-floor SMB long tail is open.
3. **"AMS/PMS/EHR integrations are too hard for solo devs."** — Many have stable export formats (Open Dental schema is published; QuickBooks API is stable).
4. **"PBM contracts are too opaque to audit."** — 835/ERA EDI is structured and detectable.
5. **"AI scribes are commoditized."** — Transcription is. The post-transcription billing-code + payor-rule + EHR write-back is not.
6. **"Curative title is paralegal work that resists software."** — Recording offices have e-recording portals; the per-county configuration nobody mapped is the moat.
7. **"You need a partner-track human for professional services."** — 80% of the work is form-filling + rules application; the license is the moat.
8. **"Agencies are bespoke creative work."** — 80% of SMB agency work is templated; AI-native agency sells outcomes at 100x SaaS prices (Sequoia "Services is the New Software").

## 8. The Anthropic Analog for Solo Founders

The user wants to be "like Anthropic — broke through Big Tech monopoly." Agent 5's distilled positioning:

> Anthropic's moat is *not* the model — it's enterprise-trust positioning that OpenAI structurally can't credibly copy. Translate to solo:
>
> 1. Pick a positioning incumbents can't credibly copy (Anthropic→safety; you→regulated-vertical depth).
> 2. Co-opt frontier models as infrastructure (you're a customer, not a competitor).
> 3. Sell *outcomes*, not tokens. (Pricing-model defense.)
> 4. Exploit the diffusion gap — model capability is 18–36 months ahead of F500 deployment. You're the diffusion layer.

## 9. Application Strategy (May 25 → May 28 timeline)

Per Agent 6's reading of S26 application questions:

**Required application content:**
- 1-min founder video (no slides).
- Product demo video (working v0 is the #1 differentiator).
- Specific traction numbers — even 3 design partners + a signed LOI beats "we talked to 50 customers."
- A clear, narrow customer description.
- A heretical thesis (1–2 sentence "everyone believes X, we believe ¬X").

**The 48-hour pre-application sprint** (May 23 PM → May 25 9pm PT):
1. Hour 0–8: pick the idea (use this synthesis). Recruit 3 design partners via cold-DM. If zero yes → switch idea.
2. Hour 8–24: scrappy v0 — a working agent that does ONE step of the workflow end-to-end on real customer data.
3. Hour 24–36: get one screen-recording of v0 on real data + one verbal LOI on video.
4. Hour 36–48: founder video + application. Cite the matching YC RFS by number. Include the heretical thesis verbatim.

If you miss YC S26 late deadline, the Standard Capital $100B Seed Group (May 28 9pm PT) is the cleaner fallback — Buchheit + Caldwell, $200K uncapped SAFE, 10 companies, single interview.

## 10. What the Master Doc Doesn't Cover (Known Gaps)

Per the agents' own flagged gaps:

1. Direct Reddit subreddit quote-level sourcing for the top pain points (Reddit blocked agents in this session). A GummySearch pass should verify before May 25.
2. Founder-as-customer test (PG) — user has no stated industry. **Recruiting a paid co-design partner from the buyer pool in the next 48 hours is the gate.**
3. X.com sources from the original brief (jackmoses777 tweets) — gated by HTTP 402; relevant content cross-confirmed via screenshot for gregisenberg.

## 11. Files in this Research Pack

- `sources/00-source-inventory.md` — all input materials (YC/a16z/PG/Tan/Isenberg).
- `agent-research/01-rfs-synthesis.md` — RFS delta analysis, 16+8 ideas decomposed, top 8 with composite scoring.
- `agent-research/02-niche-pain-mining.md` — 24 pain points → top 15, with frontier-kill criteria and sources.
- `agent-research/03-founder-philosophy.md` — 20-question rubric + per-thinker score sheet.
- `agent-research/04-failure-analysis.md` — 7-section failure inoculation checklist + tarpit screen.
- `agent-research/05-moat-analysis.md` — 9-dim moat framework + Will-It-Survive-Claude-5 5-question gate.
- `agent-research/06-solo-dev-reality.md` — solo-feasible shapes, traps, Garry Tan operational playbook, YC application Q&A.
- `synthesis/00-master-synthesis.md` — this document.
- `final/00-recommendation.md` — the #1 pick + 2 backups + application strategy + odds.
