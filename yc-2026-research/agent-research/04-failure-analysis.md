# 04 — Failure Analysis: Why Startups Die (and How to Inoculate)

Agent #4 of 6. Compiled 2026-05-23. Deadline 2026-05-25. Founder: solo dev, building with agent swarms, applying to YC S26 / $100B Seed Group.

Goal: First-principles inventory of WHY 99%+ of startups die, mapped to **idea-stage avoidable** vs **execution-stage** causes, with a concrete inoculation checklist for the user's idea selection.

---

## 1. The Headline Numbers

### 1a. CB Insights (most recent, 2024 update, n=431 VC-backed failures since 2023)
Source: https://www.cbinsights.com/research/startup-failure-reasons-top/

| Rank | Reason | % of failures |
|---|---|---|
| 1 | **Ran out of capital** | 70% |
| 2 | **Poor product-market fit** | 43% |
| 3 | **Bad timing / macro** | 29% |
| 4 | **Unsustainable unit economics** | 19% |

Crucial reframe in the 2024 update: CB Insights explicitly calls "ran out of capital" the **final symptom, not the root cause.** Companies run out of capital BECAUSE they lacked PMF, mistimed the market, or had broken economics. Median company raised $11M before dying; median time from last raise to shutdown = 22 months.

Sector breakdown of failures: Healthcare/biotech 14%, fintech 13%, food/ag 13%.

### 1b. Wilbur Labs 2026 (n=200 founder survey)
Source: https://www.wilburlabs.com/blueprints/why-startups-fail

| Reason | % citing |
|---|---|
| Competition & market dynamics | 45% |
| Technology / product issues | 44% |
| External factors (macro, regulatory) | 31% |
| Hiring missteps | 30% |
| Running out of money | 25% (down from 38% in 2023 — capital is more abundant) |

**54% of founders said "better understanding PMF" was THE lesson from failure.**

### 1c. Original CB Insights (n=110+, 2014–2021, but most-cited)
Source: https://www.cbinsights.com/research/startup-failure-reasons-top/

1. No market need — **42%**
2. Ran out of cash — **29%**
3. Wrong team — **23%**
4. Got outcompeted — **19%**
5. Pricing/cost issues — **18%**
6. Poor product — **17%**
7. Lack of business model — 17%
8. Poor marketing — 14%
9. Ignored customers — 14%
10. Mistimed product — 13%
11. Pivot gone bad — 10%
12. Burnout / lack of passion — 8%

### 1d. MIT NANDA "State of AI in Business 2025" — enterprise AI specifically
Source: https://fortune.com/2025/08/18/mit-report-95-percent-generative-ai-pilots-at-companies-failing-cfo/

- **95% of enterprise GenAI pilots produce no measurable P&L impact.** Only ~5% see "rapid revenue acceleration."
- n=150 leader interviews, 350 employee survey, 300 deployments analyzed.
- **Build-internal succeeds ~⅓ as often as buy-from-vendor.** This is bullish for startups *selling* to enterprises, bearish for any startup whose pitch is "we'll be your in-house AI team."
- 50%+ of GenAI budgets go to sales/marketing tools, but the actual ROI hides in back-office automation.

### 1e. AI-specific failure data
- ~90% of AI startups fail within their first year (multiple sources, hackernoon graveyard piece).
- 254 VC-backed startups filed Chapter 11 in Q1 2024 alone (60% jump YoY, 7x the 2019 rate).
- CB Insights: **78% of "AI startups" launched in 2024 are essentially API wrappers** — ~12,000 companies on top of the same foundation models.
- Average AI wrapper churn: **65% within 90 days** (vs SaaS norm 35%).

### 1f. YC-specific baseline
- ~45% of YC companies reach Series A (vs 33% industry seed-stage average). [Lenny's newsletter on YC]
- **~70% of YC unicorns pivoted at least once.**
- ~10–11% of YC companies are solo-founded historically; W26 was 22 solo founders (11%).
- Solo founders are 5x less likely to get into YC vs teams, but conditional-on-funded, take companies public at ~2x rate (0.6% vs 0.3%). Selection effect: YC's solo bar is brutal.

---

## 2. Failure Causes Decomposed: Idea-Stage vs Execution-Stage

For each, I tag whether the user can avoid it **at idea-pick time (IDEA)** or only via **execution (EXEC)**. Idea-pick avoidable means the wrong idea structurally guarantees this failure mode no matter how well executed.

### 2.1 No market need / poor PMF (42–43%) — **IDEA-stage avoidable, mostly**
**Why it happens:** Founders build a model of the world that doesn't match reality. PG's 1995 art gallery startup is the canonical example. They scratch their own itch without checking whether the itch is shared, or they ride hype into a market that doesn't actually pay.

**Counter-pattern (PG, YC partners, Wilbur):**
- Find problems, don't think of ideas. Ideally your own problem, or a problem you've watched a domain expert deal with.
- "Live in the future and build what's missing" — but verify the future is here.
- Test demand BEFORE building: landing page + waitlist + pre-sells.
- 54% of failed founders said "I should have understood PMF better." Translation: they were premature on build.

**Inoculation for solo dev with agents:** Pick a problem you can articulate from lived experience (former job, your own workflow, or a domain you've shadowed for 2+ weeks). If the only reason you can give for the idea is "AI can now do X," you're an AI wrapper.

### 2.2 Ran out of cash (29–70%) — **EXEC-stage, but IDEA-stage influences runway**
**Why it happens:** Burn outpaces traction. Symptom of weak PMF, slow GTM, or hiring ahead of revenue.

**Counter-pattern:**
- Default-alive math from week 1.
- For solo-with-agents specifically: zero payroll = enormous runway advantage. Use it. But also: $200K SAFE / S26 stipends imply you need to be revenue-generating within 12–18 months for any path other than "raise again at higher valuation."

**Inoculation:** Pick an idea where revenue can start in <6 months. AI-native service businesses (YC RFS A1 #2, A2 #3) have this property — bill from day 1. Pure infrastructure plays do not.

### 2.3 Wrong team / co-founder issues (23%) — **N/A for solo, but burnout-equivalent risk**
Solo skips co-founder conflict but inherits **burnout** (8% of failures, but 54% solo burnout rate in 2025 surveys, 75% anxiety episodes — Solo Founder Index 2026).

**Inoculation:** Pick an idea you can sustain emotional engagement with for 5–10 years. Boring industries that ALSO bore you are fatal. If the domain doesn't intrinsically interest you, the dopamine collapse at month 14 ends the company.

### 2.4 Got outcompeted (19%) — **PARTIALLY IDEA-stage avoidable**
**Why it happens:** Idea was either (a) already crowded (tarpit), or (b) lacked a moat as it grew. For AI specifically: foundation model providers ate the category from below; bigger startups ate it from above with more compute and distribution.

**Counter-pattern (a16z, Marc Andreessen, YC's "7 real moats"):**
- The moat is NEVER the model. It's data, integrations, distribution, captured workflow.
- "Capability compression" — the gap between Claude tiers narrows faster than the price gap, so any moat predicated on "we use the best model" decays in 6 months.
- The Crow (YC W26) thesis: the operational knowledge of *how* to deploy agents reliably, the guardrails, the trust, and the sales motion — that's what's not copyable in a quarter.

**Inoculation:**
- Will this idea survive GPT-5/Claude-5/Gemini-3 launching with the feature built-in? If "no," kill it now.
- Does the product accumulate something with each customer that a competitor would have to re-earn? (Proprietary data, integrations, switching cost, brand, trust.)
- Is there a defensible regulated / hard-to-replicate distribution wedge (procurement contract, license, partnership) you can win?

### 2.5 Pricing / unit economics broken (18–19%) — **IDEA-stage avoidable for AI specifically**
**Why it happens for AI startups:** Flat-fee pricing + token-based COGS = inverted unit economics. One whale paste-summarizes a 500-page PDF and you lose money on them all month.

**Counter-pattern:**
- Usage-based or value-based pricing if COGS is variable.
- AI-native service companies bill on outcome (claims processed, leases drafted, calls answered) — naturally aligned with COGS.

**Inoculation:** Sketch unit economics BEFORE building. Compute COGS per transaction at three traffic levels (10x, 100x, 1000x). If margin compresses with scale, the idea is broken.

### 2.6 Poor product (17%) — **EXEC-stage**
Solo-with-agents partially mitigates this through fast iteration, but also risks shipping low-quality code wrapped in confidence. Mitigation: have real users in the loop weekly.

### 2.7 No business model (17%) — **IDEA-stage avoidable**
Tarpit idea cluster: consumer "great UX, figure out monetization later." Dalton Caldwell explicitly: "Consumer startups are the biggest tar pits."

### 2.8 Mistimed product (13–29%) — **IDEA-stage partially**
**For AI in 2026 specifically:** Models are at "good enough for many tasks but unreliable for high-stakes" stage. Building products that REQUIRE 99.9% reliability (medical, legal, financial autonomy) is too early. Building products where 90% reliability is huge improvement (admin tasks, draft generation, screening) is now.

### 2.9 Regulatory / legal — **IDEA-stage avoidable, mostly**
**Failed examples:** Babylon Health (healthcare regulation eating margins), Yara AI (shut down voluntarily because AI mental health support deemed too dangerous without regulatory framework).

**Inoculation:** Avoid HIPAA-critical or FDA-critical paths unless you have an unfair advantage. Government (YC RFS A2 #5) and stablecoins (A2 #4) are explicitly endorsed precisely because the regulatory WINDOW is open right now.

---

## 3. Specific Failed AI Companies (named postmortems, 2024–2025)

Sources: https://techstartups.com/2025/12/09/top-ai-startups-that-shut-down-in-2025-what-founders-can-learn/, https://hackernoon.com/how-not-to-die-in-2025-advice-from-the-graveyard-of-failed-ai-startups, https://www.healthcaredive.com/news/olive-ai-shuts-down/698455/

| Company | Raised | What killed it | Lesson |
|---|---|---|---|
| **Olive AI** | $902M, $4B valuation | Overpromised AI capabilities for hospital RCM, underdelivered, lost customer trust | "Don't ship marketing ahead of product." Healthcare AI requires deep clinical workflow embedding. |
| **Babylon Health** | $600M+, public via SPAC | UK NHS dependency + bad unit economics + regulatory headwinds | Asset sale to eMed. Healthcare regulation eats consumer telehealth. |
| **Builder.ai** | Microsoft-backed, ~$1.2B | Overstated AI capabilities (the "AI" was 700 engineers in India), inflated revenues, lender trust collapse | If your AI is humans, eventually the math catches up. Avoid wizard-of-oz at scale. |
| **Humane** (AI Pin) | $230M+ | Hardware that didn't beat smartphones; "bad at almost everything it does" | Hardware + AI is brutal. Need 10x not 1.1x. |
| **Noogata** | $20M+ | Enterprise pilots never scaled; sales cycles outran runway | Enterprise pilot ≠ revenue. Procurement is the bottleneck. |
| **Locale.ai** | YC-backed | Niche TAM plateaued; founder burnout after 6 years; high-touch founder-led sales never templatized | Solo/small team + high-touch sales = burnout. |
| **Subtl.ai** | YC-backed | Scattered across verticals; no repeatable sales motion; bespoke per customer | Lack of focus + custom work each customer = services masquerading as SaaS. |
| **Tune AI** | YC-backed | Competed head-on with hyperscalers (AWS/Azure/GCP) on similar features at lower prices | If your competitor is OpenAI/Azure/AWS on a core feature, you lose. |
| **Wuri** | — | AI wrapper, multiple pivots, never found PMF | Commodity wrapper + no domain wedge = die. |
| **CodeParrot** | — | Code quality not production-grade; competition from Copilot/Cursor; peaked at $1.5K MRR | Coding tools became hyper-competitive. Tarpit unless you own a specific niche. |
| **Astra** | — | Co-founder conflict + enterprise data trust issues | Trust is the moat in enterprise AI. Young startups + sensitive data = nope unless brand. |
| **Yara AI** | — | Founders concluded the domain (AI mental health) was too risky to operate ethically | Some markets are correctly avoided. |
| **Kite** | $17M+ | AI coding assistant, predates LLM era, killed by GPT/Copilot | Got outcompeted by foundation model expansion. |
| **Zymergen** | Public, $1B+ market cap at peak | Rigid AI architecture; couldn't accommodate model updates without rewrites | Architecture must assume your underlying model improves 2x/year. |
| **Aria Insights** (drones) | — | Built sophisticated tech before infrastructure (WiFi/connectivity) existed; lavish R&D before paying customers | Don't be early on hard infra. |
| **DeepGlint** | — | Computer vision focused on brick-and-mortar as market shifted to e-commerce | Watch macro market shifts. |

**Common thread:** sophisticated tech without (a) PMF or (b) defensible distribution or (c) margin stability under scale. The MIT 95% pilot-failure number maps directly here — most AI vendors die in the "Pilot → Production" gap.

---

## 4. The Solo-Founder-With-Agents Specific Failure Mode

This is the user's exact configuration. Let me analyze what kills these specifically.

### 4.1 Statistical baseline
Sources: Solo Founder Index 2026 (ShipSquad), Carta, Lenny's YC analysis

- **Solo founders 23% more likely to fail than 2–3 founder teams.** Take 3.6x longer to scale.
- **Carta:** Solo-founded share of all startups went from 23.7% (2019) → 36.3% (mid-2025). Trend strongly up.
- **AI-augmented solo founders vs non-AI solo founders:**
  - Reaching $100K ARR in 12mo: **28% vs 11%**
  - Reaching $1M ARR in 24mo: **4.2% vs 0.8%**
  - Median ARR: **$240K vs $48K**
  - Feature ship rate: 8–12/month vs 2–4/month
- **Burnout rate solo founders 2025:** 54%. **Anxiety episodes:** 75%. **Loneliness/isolation:** 62%. **Bad/very bad mental health (last 12mo):** 46%.

### 4.2 What kills solo-with-agents specifically

**(A) Distribution. By a wide margin.**
Top performers spend 40–50% of their time on marketing/sales/community. Failing solo founders spend ~10% (they're stuck building). Building is now the easy part because agents. **The differentiated work is now distribution.**

- Base44 (Maor Shlomo): solo, sold for $80M in 6 months, 300K users, $3.5M ARR. He had a *creator/audience* foundation before launch. That's the distribution wedge.
- This is the inverse-Wuri pattern: agent-built product + no distribution = death.

**(B) Enterprise procurement & trust.**
- 48% of solo founders report being **disqualified or stalled in enterprise deals because of solo-founder perception.** Procurement asks "who's your CISO? what happens if you get hit by a bus?"
- Astra example: enterprise customers won't share sensitive data with young startup.
- SOC 2 Type II, ISO 27001, GDPR — table stakes for enterprise AI sales. Each is months of work for a solo dev. Alternative: target SMB / micro-niche / PLG.

**(C) Burnout when the dopamine ends.**
Months 3–9 are the danger zone. Initial agent-magic high, then grinding distribution work with no team to share the load. 41% of solo founders burn out *despite working fewer hours* (Solo Founder Index 2026) — cognitive load, not hours, is the killer.

**(D) Context-switching cost.**
54% of solo founders cite cognitive overload across functions (eng, sales, support, finance, legal). Agents help with eng but the others still demand human time.

**(E) Acquihire trap / sub-optimal exit.**
For solo founders, the most common "success" outcome is acquihire at $5–20M (which sounds great but at a small ownership stake post-dilution is life-changing-but-not-VC-target). Pattern: if you're solo and reach $1–3M ARR, big tech will offer to buy YOU. Many take it — rationally. But it caps the upside the VC needs.

**(F) "Outsider tax" in regulated verticals.**
For B2B AI in regulated industries (healthcare, legal, finance, insurance), solo founder without domain credentials = significantly higher CAC + longer sales cycles + lower conversion. Insiders trust insiders. Mitigation: advisor/design-partner relationships with domain authority figures.

### 4.3 Base rate estimate: YC solo-founder AI-agent companies 2025–2026 outcomes

Reasoning from available data (no clean dataset, but triangulated):

- W25 + S25 + W26 batches: ~600 companies total. ~60% AI-themed (~360). ~10% solo-founded (~36 AI solo founders across three batches).
- Of these ~36, time-since-funding is 6–18 months. **Almost none are old enough to have raised Series A yet by May 2026.** Realistic Series A rate at 18 months for YC AI cohorts has been running ~25–35%. For solo: scale DOWN, because investors discount solo at Series A specifically (capital-formation risk).
- **My best estimate:**
  - Reached Series A by May 2026 (~18 months in for W25): **15–20%** of solo YC AI agents.
  - Acquihired (small-mid exit): **10–15%**.
  - Still grinding, not yet raised: **35–45%**.
  - Quietly dead / dormant: **20–30%**.
  - Pivoted significantly: **30–40%** (overlapping with above buckets).
- Harper (W25, AI insurance brokerage, $47M Series A Feb 2026) is the visible success but had multiple co-founders.
- Base44 is the visible solo success but was OUTSIDE YC.

**Takeaway:** Solo-founder + YC + AI-agent is a viable path but the visible successes have either (a) pre-existing distribution (creator/audience), (b) deep domain insider expertise, or (c) shipped fast enough to revenue before runway concerns matter. Anyone else is in the "grinding" or "quiet shutdown" bucket.

---

## 5. The Failure Inoculation Checklist

Use this for EVERY candidate idea before committing to it. Score each section 0–5. Idea must average ≥3.5 across all sections.

### 5.1 PMF risk (target: ≥4)
1. Can I name 3 specific people I'd talk to in the first week who have this problem RIGHT NOW?
2. Have I (a) personally lived this problem, OR (b) shadowed someone living it for 10+ hours?
3. Can I describe the current workaround the user employs (Excel, manual, BPO, expensive consultant)?
4. Is the workaround painful enough to be solved by a product, not just a feature?
5. Would the user pay >$50/mo (B2B) or this be worth >$10K/year (enterprise) to make the problem go away?

### 5.2 Capital / runway risk (target: ≥3.5)
1. Can I generate first revenue within 90 days of building?
2. With $200K SAFE only, am I default-alive for 18+ months?
3. If I need to raise again in 12 months, is there an obvious metric I can hit ($X ARR, Y customers) that triggers it?
4. Are my unit economics positive at 100 customers? At 1000?
5. Is my COGS variable with usage, and does my pricing match (no flat-fee + variable-token-cost mismatch)?

### 5.3 Distribution risk (target: ≥4, this is the killer)
1. Do I have an existing audience, customer access, or network in the target market? If not, what's my distribution wedge?
2. Can I personally reach 100 potential customers in week 1 (warm intros, communities I'm in, etc.)?
3. Is there a community/subreddit/Slack/conference where users congregate that I can show up in authentically?
4. Is the sales cycle <90 days (SMB / PLG) OR do I have a partner who shortens enterprise sales?
5. Is the product viral / referral-driven / SEO-discoverable, or do I have to outbound to every customer?

### 5.4 Moat erosion risk (target: ≥4) — CRITICAL FOR USER
1. If GPT-5 / Claude-5 / Gemini-3 ships next quarter with this exact feature, do I die? If yes — kill the idea.
2. If OpenAI / Anthropic launches their own "agent that does X" feature, do I die?
3. Is what I'm building ABOVE the model layer (workflow, integration, data, trust, distribution) or AT the model layer?
4. Does the product accumulate proprietary data, switching cost, or integration depth with each customer?
5. If a competent team copied my front-end in 2 weeks, what would they still be missing? (Answer should be concrete, not "execution.")

### 5.5 Solo-founder risk (target: ≥3.5)
1. Can I sustain emotional engagement with this domain for 5+ years (not just hype-cycle excitement)?
2. Is the customer/user someone I genuinely want to talk to weekly forever?
3. Can the product be built by me + agents in 60 days to a sellable v1?
4. Is the trust/credibility bar low enough that "solo founder" isn't a deal-breaker? (SMB usually yes; F500 usually no.)
5. Is there a graceful failure mode where I can wind down or sell without total wipeout (e.g., side income, advisory work, acquihire target)?

### 5.6 Regulatory / external risk (target: ≥3)
1. Am I avoiding HIPAA/FDA/SEC/bar-licensure critical paths unless I have a moat there?
2. Is the regulatory environment trending toward enabling this product or restricting it?
3. If a foundation model provider gets sued for X (copyright, hallucination, bias), do I get sued too?
4. Am I in a "permitted window" (stablecoins, AI for govt) vs a "fighting upstream" zone (autonomous medical advice)?

### 5.7 Tarpit screen (must pass all)
From Dalton Caldwell + YC + venture security tarpit lists:

- [ ] Not consumer social / friend-coordination / discovery app
- [ ] Not "Cursor for X" where X is generic (only OK if X is a specific narrow vertical with insider knowledge)
- [ ] Not "ChatGPT for X" with no defensible wedge
- [ ] Not building yet-another-better-detection-tool against entrenched incumbents (Crowdstrike, Palo Alto, Workday)
- [ ] Not "single pane of glass" for any category
- [ ] Not "executive co-pilot dashboard"
- [ ] Not building generic developer tooling competing with Cursor/Copilot
- [ ] Not pure infrastructure that requires hyperscaler-level investment
- [ ] Not consumer AI companion / chat
- [ ] Not "perfect" anything (perfect search, perfect DLP, perfect personalization)

---

## 6. Counter-Patterns: What Successful Founders Did Differently

Synthesized from CB Insights survivors, YC successes, and recent solo-founder wins.

1. **Solved their own well-understood problem** (Stripe — Collison brothers building payments because they'd built ecommerce; Airbnb — they couldn't afford rent).
2. **Picked a market with existing budget moving manually** (Harper, AI insurance brokerage — insurance brokers exist, they bill commissions; just AI-ify the existing GTM machine).
3. **Started services-first, productized later** (Brex, Segment both pivoted hard from initial concept; YC RFS A1 #2 explicitly endorses AI-native services as new shape).
4. **Got a small group of users to LOVE it before chasing scale** (paul graham: "the company that grows because it's better has a flywheel").
5. **Charged from day 1** (Base44 hit $3.5M ARR in 6 months from launch with paid users).
6. **Treated distribution as the product** (Maor Shlomo had a creator audience; Pieter Levels built in public).
7. **Picked verticals where they had unfair information advantages** (former domain workers; immigrants serving their diaspora; consultants productizing their playbooks).
8. **Avoided LLM lock-in at architecture level** (model-agnostic = survive every Anthropic/OpenAI repricing).
9. **Built infrastructure-shaped products in regulated industries** (Stripe Atlas → Stripe Treasury, etc).

---

## 7. Direct Implications for the User's S26 Decision

Given the user is:
- Solo developer, agent-augmented
- Wants resilience against next-gen Claude/GPT
- Wants real niche existing problem
- Application due May 25, 2026

**Top 5 inoculation priorities (rank-ordered):**

1. **Moat erosion / model-substitution risk** — pick an idea whose moat is data, distribution, trust, integration, or vertical workflow knowledge. NOT the model itself.
2. **Distribution wedge** — without it, solo agent-built product = dies in noise. Need either pre-existing audience, niche community access, insider domain network, or natural virality.
3. **Founder-market fit** — pick a vertical/problem you can credibly claim insider status on or genuinely care about long-term.
4. **Time-to-revenue** — services-first or transactional revenue model that bills early, validates demand, funds development.
5. **Avoid tarpit categories** — friend coordination, consumer social, generic AI assistants, perfect-X tools, Cursor-clones.

**Highest-risk patterns to AVOID for THIS founder shape:**

- Pure infrastructure plays competing with hyperscalers (Tune AI fate).
- Consumer social/discovery (Houseparty, tarpit).
- Enterprise-only AI requiring SOC2 + procurement from day 1 (Astra, Noogata fate — solo procurement disqualification).
- Healthcare AI without clinical co-founder (Olive, Babylon fate).
- Coding tools competing with Cursor/Copilot/Claude Code (Kite, CodeParrot fate).
- Anything where "the AI is the product" rather than "the AI is the enabler of a service/workflow."

**Highest-affinity patterns FOR this founder shape:**

- AI-native service company in a domain user knows (YC RFS A1 #2, A2 #3) — bills from day 1, no enterprise procurement.
- Software-for-agents (YC RFS A1 #12) — niche infra, defensible via developer mindshare, the user IS the user.
- Sell-to-Fortune-100-from-tiny-team (YC RFS A1 #13) — counterintuitively works if you find a specific F100 sponsor.
- Boring-industry verticals from Isenberg framework (r/insurance, r/realtors, r/dentistry) where the user can do 2 weeks of shadowing to establish credibility.

---

## 8. Sources

Primary:
- CB Insights "Top 9 Reasons Startups Fail" 2024 update — https://www.cbinsights.com/research/startup-failure-reasons-top/
- CB Insights "20 Reasons Startups Fail" PDF — https://s3-us-west-2.amazonaws.com/cbi-content/research-reports/The-20-Reasons-Startups-Fail.pdf
- Wilbur Labs "Why Startups Fail 2026" (200 founders) — https://www.wilburlabs.com/blueprints/why-startups-fail
- MIT NANDA "State of AI in Business 2025" (via Fortune) — https://fortune.com/2025/08/18/mit-report-95-percent-generative-ai-pilots-at-companies-failing-cfo/
- Tech Startups "Top AI Shutdowns 2025" — https://techstartups.com/2025/12/09/top-ai-startups-that-shut-down-in-2025-what-founders-can-learn/
- HackerNoon "Graveyard of Failed AI Startups" — https://hackernoon.com/how-not-to-die-in-2025-advice-from-the-graveyard-of-failed-ai-startups
- Failory Cemetery — https://www.failory.com/cemetery
- Solo Founder Index 2026 — https://shipsquad.ai/blog/solo-founder-index-2026
- Lenny's Podcast w/ Dalton Caldwell on tar pit ideas — https://www.lennysnewsletter.com/p/lessons-from-1000-yc-startups
- YC Library: Tarpit Ideas Sequel — https://www.ycombinator.com/library/LH-tarpit-ideas-the-sequel
- VentureInSecurity tarpit ideas in cybersecurity — https://ventureinsecurity.net/p/tarpit-startup-ideas-in-cybersecurity
- Olive AI shutdown — https://www.healthcaredive.com/news/olive-ai-shuts-down/698455/
- TechCrunch Harper Series A — https://techcrunch.com/2026/02/25/ai-insurance-brokerage-harper-raises-45m-series-a-and-seed/
- Marc Andreessen / Marc Love on commoditization — https://marclove.com/2025/02/10/commoditization-trap-why-model-agnostic-ai-products-will-win.html

Cross-references in inventory:
- /home/user/ChatterBot/yc-2026-research/sources/00-source-inventory.md (PG essays, YC RFS lists, Isenberg, Garry Tan)
