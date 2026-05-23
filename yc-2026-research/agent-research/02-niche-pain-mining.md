# Agent 02 — Niche Pain Mining (Boring Industry Subreddits + Forums)

**Compiled:** 2026-05-23. **For:** YC W26 / $100B Seed Group application (solo dev + agents).
**Framework applied:** Greg Isenberg "subreddits are goldmines" + "How to get AI startup ideas according to YC."
**Scope:** Real, specific, niche pain points where (a) a solo dev with agents can ship a wedge, (b) a frontier-model upgrade alone won't kill the moat, and (c) a clear buyer with budget exists today.

> Methodological note: Reddit served `403`/blocked direct site-search fetches via WebFetch and `site:reddit.com` Google queries during this research session. As a workaround, pain-point evidence was triangulated through (1) industry-press articles quoting recurring complaints, (2) industry-forum threads (Practical Machinist, AccountingWEB), (3) IdeaBrowser/IndieHackers Reddit-validated lists (Hargrave, Greensighter), and (4) vendor blogs reporting field-research time/cost metrics. URLs cited inline. Quote-level Reddit sourcing is a known gap — Agent 03 or a manual GummySearch pass should verify the top 5 with direct subreddit threads before the May 25 deadline.

---

## Section 1 — Filter criteria (applied to every pain point below)

For each candidate I scored against:

1. **Daily grind?** — recurs at least weekly per buyer (not a one-off).
2. **$50K+ annual problem?** — pain at a single buyer is large enough to support $500-$5K/mo SaaS, or a "we sell the service" $50K-$500K annual contract (per YC RFS #2 "AI-Native Service Companies").
3. **Heresy** — what cherished assumption is blocking everyone else from building it? (PG "novelty hides in dead zones around cherished mistaken assumptions.")
4. **Frontier-model kill test** — would GPT-5 / Claude 5 raw API solve it for the buyer themselves? If YES, kill (e.g. "summarize this contract" is dead).
5. **Defensibility** — is there workflow integration, distribution moat, regulatory/data moat, or a forced habit (Indie Hackers: "products that compound with proprietary data, trust, or operational depth that generic AI can't easily replicate")?
6. **Solo-dev-with-agents buildable** — wedge shippable in <90 days; no field hardware; no regulatory clearance for v1.

---

## Section 2 — Pain points captured (long list, 24 items)

### Healthcare admin (heaviest cluster)

#### P1. Prior authorization for outpatient physical therapy (and other specialty PA segments)
- **Buyer:** PT clinic owners / clinic ops directors / billing managers.
- **The pain:** Doctors juggle ~43 PA requests/week = ~12 staff-hours just on auth; each cycle costs providers $20-$30, plans $40-$50. Total US system: $350B/yr in admin waste. 24% of physicians report a PA-caused adverse event. ([Medical Economics, 2025](https://www.medicaleconomics.com/view/prior-authorization-history-burden-ai-future))
- **Validation that solo build works:** A founder in a Slack community posted $41K MRR after 14 months, solo, building exactly this for outpatient PT at Blue Cross. ([Automaiva 2026 vertical-AI](https://automaiva.com/vertical-saas-ai-agents-2026/))
- **Heresy:** "AI can't navigate payor-specific clinical-criteria PDFs reliably" — actually they can, *if* you scrape and version the criteria yourself per payor + state.
- **Frontier-model kill test:** **Survives.** GPT-5 doesn't have the payor-specific criteria, EHR connectivity, fax/portal submission, or denial-appeal templates. Workflow + integration moat.
- **Defensibility:** Clearinghouse integrations (Availity/Surescripts), payor portal scrapers, denial-pattern data, BAA + HIPAA. Distribution via state PT association partnerships.
- **Frequency:** Daily.
- **Verdict: KEEP.**

#### P2. Dental insurance verification (eligibility + benefits)
- **Buyer:** Dental practice managers (independent and small-DSO offices).
- **The pain:** Manual verification takes 8-50 hrs/week per office; 13 min each manually vs <1 min automated; costs $7.11 manually vs $1.48 automated; ~15% denial rate driven by bad verification. ([Overjet 2025 guide](https://www.overjet.com/blog/dental-insurance-verification-workflows-complete-2025-guide); [Curve Dental](https://www.curvedental.com/blog/dental-insurance-verification-guide))
- **Heresy:** "Payor portals are too fragmented; nobody can scrape all of them" — actually a small set (Delta Dental + 5 BCBS state plans + MetLife + Cigna) covers 80% of US dental volume.
- **Frontier-model kill test:** **Survives.** Requires per-payor authenticated portal access, ACORD-equivalent dental form generation, write-back into Dentrix/Eaglesoft/Open Dental, and CDT code knowledge.
- **Defensibility:** PMS integrations (Dentrix/Open Dental are the gates), payor login vaults, claim-history data feeds back into pre-emptive denial prediction.
- **Frequency:** Daily, ~50 verifications/wk/practice.
- **Verdict: KEEP.**

#### P3. Veterinary SOAP-note "pajama time"
- **Buyer:** Independent vet clinic owners / DVMs.
- **The pain:** 10-15 hrs/week of "pajama time" finishing notes at home; reclaiming 10 hrs/wk unlocks $100K+ revenue capacity per DVM at $150-$250/clinical-hr. ([PupPilot ROI analysis](https://www.puppilot.co/blog/the-100k-roi-of-an-ai-scribe-how-reclaiming-10-dvm-hours-a-week-transforms-your-clinics-finances))
- **Heresy:** "Scribe is just transcription, anyone can build it" — but vet-specific drug DB, species-specific exam templates, and PIMS write-back (ezyVet, AVImark, Cornerstone) are non-trivial.
- **Frontier-model kill test:** **At risk.** Whisper + GPT-5 transcription is essentially free. Differentiation has to be PIMS write-back + billing-code auto-attach + species pharmacology + controlled-substance log.
- **Defensibility:** Crowded (ScribbleVet, Scribenote, VetRec). Late entrant unless distribution wedge (e.g. AVMA partnership or a specific species/specialty).
- **Frequency:** Daily.
- **Verdict: PROBABLY SKIP — too crowded for a May-25 solo entry. List for awareness.**

#### P4. Medical claim denial appeal letters
- **Buyer:** Small/mid medical billing companies, RCM teams in 5-50 physician practices.
- **The pain:** $25-$50 per denied claim to rework; at 15% denials and 1,000 claims/mo a practice burns $37.5K-$75K/yr. Half of providers still review manually. ~54% of properly drafted appeals get overturned — so this is rework-with-known-ROI. ([Experian State of Claims 2025](https://www.experian.com/blogs/healthcare/healthcare-claim-denials-statistics-state-of-claims-report/); [MD Clarity appeal letters](https://www.mdclarity.com/blog/medical-appeal-letters))
- **Heresy:** "The denial reason codes are too unstructured to automate at scale" — actually CARC/RARC are a finite enum; payor-specific letter templates are scrapable.
- **Frontier-model kill test:** **Survives.** Needs CARC code mapping, payor-specific appeal portals/forms, deadline tracking, EOB/835 ingestion. None of that is in a frontier model.
- **Defensibility:** Clearinghouse integrations (Waystar/Change Healthcare/Office Ally), payor-portal submission, denial-pattern dataset compounds.
- **Frequency:** Daily.
- **Verdict: KEEP.**

#### P5. Independent insurance agency Certificate-of-Insurance (COI) issuance
- **Buyer:** Independent P&C agency owners / CSRs.
- **The pain:** 45-52 min per COI request manually; mid-agency processes 35-60/wk = **28-105+ CSR hours/wk** consumed; 3x more CSR time than policy endorsements; 5x more than billing inquiries. ([US Tech Automations 2026](https://ustechautomations.com/resources/blog/insurance-certificate-of-insurance-issuance-pain-solution-2026))
- **Heresy:** "Vertafore/Applied AMS systems already do COI" — they generate the ACORD form but everything else (request intake, holder verification, AMS logging, follow-up) is manual.
- **Frontier-model kill test:** **Survives.** Requires AMS integration (AMS360, Epic, Hawksoft), ACORD 25 generation, holder DB, regulatory rules per state.
- **Defensibility:** AMS integrations are the moat; once installed, becomes part of the agency's daily workflow.
- **Frequency:** Daily.
- **Verdict: KEEP.**

#### P6. Nursing "double-charting" / EHR flowsheet redundancy
- **Buyer:** Hospital CNO / nurse-manager (large enterprise sale — slower; **probably wrong shape for solo dev**).
- **The pain:** Acute-care nurses ask for streamlined charting 2x more than any other EHR enhancement (KLAS Arch Collaborative 2025). ([KLAS](https://klasresearch.com/archcollaborative/report/reducing-nursing-documentation-burden-2025/706))
- **Frontier-model kill test:** Survives, but Epic/Cerner are the moat-holders and the sales cycle is 18+ months.
- **Verdict: SKIP for solo W26.**

#### P7. Home-health agency referral intake from faxed PDFs
- **Buyer:** Home-health agency intake coordinators (PDPM/PDGM agencies).
- **The pain:** Faxes still dominant referral channel; intake coordinator hand-keys patient demographics, dx codes, F2F encounter notes into Axxess/HomeCare HomeBase. (Sourced from agency referral-form PDFs themselves: [MedStar fax cover](https://www.medstarhealth.org/-/media/project/mho/medstar/pdf/home-care-fax-and-referral-form.pdf))
- **Frontier-model kill test:** **Survives** — fax-to-EHR write-back, OASIS field mapping, payor verification + face-to-face documentation rules.
- **Defensibility:** Axxess/HCHB write-back integrations; OASIS rule engine.
- **Frequency:** Daily, every referral.
- **Verdict: KEEP (high heresy: "fax is dead" assumption is wrong — home health agencies receive >70% of referrals by fax).**

### Construction / contractors / trades

#### P8. Construction RFI + submittal routing for mid-size GCs
- **Buyer:** GC project managers at $10-$100M-revenue contractors.
- **The pain:** A $50M GC loses ~330+ PM/PE hrs/yr to manual RFI/submittal admin; ~800 RFIs/project × 8 hrs review = 6,000 hrs/project; each RFI ~$1,000 to respond; 35% submittal rejection rate at $805 + 2-4 weeks each. ([SubmittalLink](https://www.submittallink.com/post/hidden-costs-of-construction-admin); [ESUB on RFI cost](https://esub.com/blog/rfi-cost-construction-firm))
- **Heresy:** "Procore owns this market" — but Procore is sales-led, expensive, and bottom-quartile mid-sized GCs use it as a glorified file share. The actual *routing/triage* layer is open.
- **Frontier-model kill test:** **Survives** — needs spec-section parsing, AHJ rules, schedule-impact reasoning, integration with Procore/Buildertrend/PlanGrid.
- **Defensibility:** Spec-section dataset, project-history vector DB, e-signature flow.
- **Frequency:** Daily.
- **Verdict: KEEP.**

#### P9. HVAC quote-on-site for residential service businesses
- **Buyer:** HVAC contractor owner-operators.
- **The pain:** Tech assesses → office writes quote in Excel → owner reviews → email customer = 1-2 day turnaround at 28% close rate vs in-living-room tablet quote at 67% close rate (real r/HVAC anecdote referenced). ([BuildOps HVAC quoting](https://buildops.com/resources/hvac-quoting-software/))
- **Frontier-model kill test:** **Survives** — needs equipment catalogs, distributor pricing API (Ferguson, Johnstone), labor rate tables, financing-integration (GreenSky/Synchrony). ServiceTitan already plays here ($$$ + sales-led); huge underserved long tail of 5-15 truck shops.
- **Defensibility:** Distributor pricing feeds, tax/permit per-state, financing-partner integrations.
- **Verdict: KEEP — but tilt to <15-truck independents priced under $150/mo (under ServiceTitan's economic floor).**

#### P10. Job-shop / CNC manufacturer RFQ response
- **Buyer:** Job-shop owners (5-50 employees, often single-location).
- **The pain:** ~2.5 hr per RFQ; engineers spend 60% of time on admin not engineering; an aerospace shop's engineering team worked 60-hr weeks just to keep up; experienced quoters retiring without replacement. ([Modern Machine Shop](https://www.mmsonline.com/articles/when-it-comes-to-rfq-response-time-is-money); [StartProto](https://www.startproto.com/blog/how-ai-agents-are-revolutionizing-rfq-processing-in-manufacturing))
- **Heresy:** "You need a deep MRP integration to quote" — actually 80% of small shops still quote from a STEP/STP file + an estimator's gut feel, no MRP. So a standalone agent works.
- **Frontier-model kill test:** **Survives** — needs GD&T feature extraction from drawings, material costing (McMaster + supplier API), machine-cycle estimation, supplier lead-time data.
- **Defensibility:** Per-shop quote-history learning; Paperless Parts/Datanomix charge >$50K/yr, vast underserved market under that.
- **Verdict: KEEP.**

#### P11. Electrical/plumbing permit pulling
- **Buyer:** Small residential electrical/plumbing/HVAC contractors.
- **The pain:** Every permit = forms + plan sets + email back-and-forth, stealing billable hours and pushing finish dates. ([PermitFlow](https://www.permitflow.com/blog/electrical-permit))
- **Frontier-model kill test:** Survives but **PermitFlow already raised heavily** and Sila is in the space. Niche per-jurisdiction (e.g. SoCal counties) might work for solo dev, but distribution is hard.
- **Verdict: SKIP — established competition at PermitFlow.**

#### P12. Commercial roofing inspection report assembly
- **Buyer:** Commercial roofing contractors, third-party inspectors (TPIs).
- **The pain:** Inspector spends hours on-roof photos → back at office, hours assembling photo-annotated reports with damage descriptions. ([NRCIA template](https://www.nrcia.org/roof-inspection-report-template/))
- **Frontier-model kill test:** **Survives** — needs roof-feature object detection, NRCA terminology, IRC/IBC reference, branded PDF assembly, drone-photo geotag handling.
- **Defensibility:** Field-app + vision model + branded reports = workflow lock-in.
- **Verdict: KEEP — but consider whether agent-2 hardware (drone) creep is a problem; v1 = phone-photo only.**

### Real estate + property + finance

#### P13. Commercial real estate Offering Memorandum (OM) generation for brokers
- **Buyer:** CRE brokers (small shops, NAI/SVN-style boutique brokerages, multifamily/industrial focus).
- **The pain:** Brokerage teams spend 4-6 hrs/week on OM screening; OMs traditionally take a designer 3-5 business days; CREBuilder claims ~30 min with software. ([CREBuilder](https://www.crebuilder.com/offering-memorandum-builder); [Decobase guide](https://www.decobase.app/blog/how-to-read-a-CRE-offering-memorandum))
- **Heresy:** "Buyer-side underwriting matters more" — actually the *seller-side OM grunt work* is what burns broker time and is universally hated.
- **Frontier-model kill test:** **Survives** — needs rent-roll parsing, CoStar/Reonomy data, branded layout templates, T-12 ingestion, debt-quote pulling.
- **Defensibility:** Branded template lib per brokerage; CoStar integration; rent-roll OCR specialization.
- **Verdict: KEEP.**

#### P14. Realtor MLS listing description + remarks generation + transaction-coordination follow-ups
- **Buyer:** Solo realtors and small teams (KW/Compass/eXp solo agents).
- **The pain:** Generic but daily — MLS listing remarks, drip follow-ups, transaction milestones. Mostly **caught up by ChatGPT directly + Sierra Interactive / Follow Up Boss.**
- **Frontier-model kill test:** **FAILS** — ChatGPT alone does 80% of the value; differentiation thin.
- **Verdict: SKIP.**

#### P15. Title insurance curative work
- **Buyer:** Title agency closers, paralegal curative teams.
- **The pain:** Difficult files = 45.4 hrs avg to close (vs ~20 hrs standard); curative includes correction deeds, lien releases, affidavits, sometimes quiet-title actions. ([ALTA 2024 curative study](https://www.alta.org/media/pdf/240506-ALTA-Title-Insurance-Curative-Work-Study-Report.pdf))
- **Frontier-model kill test:** **Survives** — needs state-specific recording-office portals, lien-search workflows, e-recording (Simplifile/CSC) integration, lender-correspondence templates.
- **Defensibility:** State recording-office scrapers, lender-policy DB.
- **Verdict: KEEP.**

#### P16. Independent accounting firm: month-end close cash reconciliation
- **Buyer:** Bookkeepers + small CPA firm partners.
- **The pain:** Cash reconciliation 20-50 hrs/mo; 50% say Excel is *the* reason close is slow; 60% of finance orgs still reconcile manually; 18% of accountants admit to daily mistakes. ([Ledge.co benchmarks](https://www.ledge.co/content/month-end-close-benchmarks-for-2025); [Teampay](https://www.teampay.co/blog/problems-with-manual-reconciliation))
- **Frontier-model kill test:** **At risk for the basic match step** — frontier models can match line items via tool use. **Survives** if the product owns the workflow: Plaid + QuickBooks/NetSuite/Sage write-back, exception routing, audit trail.
- **Defensibility:** Banking + ERP integrations; CPA-firm distribution; SOC2/audit-trail.
- **Verdict: KEEP — pick a sub-niche (e.g. multi-entity SMB SaaS-revenue reconciliation on Stripe + bank + Xero).**

### Logistics / freight

#### P17. Freight broker carrier onboarding + rate-confirmation handling
- **Buyer:** 5-50 person freight brokerages.
- **The pain:** Manual onboarding 7-14 days; ~half of carriers abandon mid-process; automated path is 80% faster. Rate-con errors can cost 5-8% of profit per trip. ([Truckstop carrier packets](https://truckstop.com/blog/broker-carrier-packets/); [LoadConnect on rate-con errors](https://loadconnect.io/blog/rate-confirmation-trucking-automation))
- **Frontier-model kill test:** **Survives** — needs FMCSA SAFER scraping, COI verification, SCAC/MC#/DOT# validation, TMS integration (McLeod, Aljex, Tai), e-sign, KYB.
- **Defensibility:** TMS write-back, FMCSA monitoring data, carrier-fraud detection dataset (very hot in 2025 post double-brokering crisis).
- **Verdict: KEEP — fraud-detection angle is the wedge.**

### Public sector + small business ops

#### P18. Municipal city-clerk meeting minutes
- **Buyer:** Town/city clerks, county clerks.
- **The pain:** Manually 3-5 hrs/meeting; town clerk in Long View NC cut from 4-8 hrs to 30-60 min using ClerkMinutes. ([Smart Cities Dive on AI for clerks](https://www.smartcitiesdive.com/news/ai-municipal-clerks-speed-up-public-records-reporting/820216/); [GovTech](https://www.govtech.com/artificial-intelligence/ai-takes-the-drudgery-out-of-compiling-meeting-minutes))
- **Frontier-model kill test:** **Partially fails** — Otter/Fathom are good enough for generic transcription; differentiation needs Robert's Rules ordering, motion/vote extraction, FOIA-defensible audit trail.
- **Defensibility:** ClerkMinutes is at 400+ municipalities — established competitor. Solo-dev wedge could be **county-level clerk-of-court (different rules: pleadings, dockets, recordings)** which nobody owns.
- **Verdict: KEEP but pivot to **county clerk-of-court**, not city council.**

#### P19. Independent restaurant inventory + invoice reconciliation
- **Buyer:** Independent restaurant owner-operators (1-3 locations).
- **The pain:** 15-20 hrs/wk on manual counts; broadline + specialty + local invoices flow in daily; reconciliation drift kills food cost. ([MarketMan blog](https://www.marketman.com/blog/restaurant-vendor-management-system))
- **Frontier-model kill test:** Survives but **MarketMan + Square + Toast** sew this up; solo entry is hard.
- **Verdict: SKIP.**

#### P20. Independent pharmacy PBM/DIR reconciliation
- **Buyer:** Owner-pharmacists at independent retail pharmacies.
- **The pain:** PBM "effective rate reconciliation" claws back $1K-$10K/mo per pharmacy after-the-fact; owners can't tell which claims were under-paid without manual line-by-line audit. ([NCPA on DIR](https://www.ncpa.co/pdf/dir-faq.pdf); [Pharmacy Times white paper](https://www.pharmacytimes.com/view/white-paper-dir-fees-simply-explained))
- **Heresy:** "PBM contracts are opaque" — but 835/ERA files from PBMs are structured EDI; an audit agent can detect underpayment systematically.
- **Frontier-model kill test:** **Survives** — needs PBM-specific reconciliation rules, NCPDP transaction parsing, dispute portal automation per PBM (Caremark/ESI/OptumRx), NABP regulatory awareness.
- **Defensibility:** PMS integrations (PrimeRx, ComputerRx, RxPro, Liberty), NCPA distribution.
- **Frequency:** Daily underpayment, monthly+annual recoupment cycle.
- **Verdict: KEEP — explicitly a YC-style "data + integration" moat.**

#### P21. Optometry / optical lab order flow
- **Buyer:** Independent optometry practices.
- **The pain:** Lab orders sit in fax/email queues, get lost, come back wrong; slow turnaround on glasses; frame inventory disconnected from lab orders. ([Sightview](https://www.sightview.com/articles/optical-retail-challenges-and-how-to-solve-them); [RevolutionEHR blog](https://www.revolutionehr.com/blogs/manage-optical-orders-more-efficiently-with-revolutionehr))
- **Frontier-model kill test:** **Survives** — needs lab EDI (Essilor, VSP Optics, Walman), frame-inventory sync, insurance-benefit application to optical, Rx-to-lens-spec translation.
- **Defensibility:** Lab partner integrations, vision-plan API connections.
- **Verdict: KEEP (but check incumbent VisionWeb).**

#### P22. Small/solo law firm conflict checks + intake
- **Buyer:** 1-5 attorney shops.
- **The pain:** Intake + conflict check is unbillable, time-consuming, 25-30% miss rate on manual conflict checks. ([Smith.ai on conflicts](https://smith.ai/blog/how-to-run-a-law-firm-conflict-check); [Lawyerist intake](https://lawyerist.com/law-firm-clients/client-intake-onboarding/))
- **Frontier-model kill test:** **At risk** — basic name-matching is trivial for LLM. Differentiation = matter-history vector DB, practice-management write-back (Clio/MyCase/PracticePanther), bar-rule compliance per jurisdiction.
- **Verdict: KEEP — but only as a feature inside a broader intake-orchestrator (per #22 below) rather than standalone.**

#### P23. MSP/IT helpdesk password-reset + ticket triage
- **Buyer:** 5-50 person MSPs (ConnectWise/Autotask shops).
- **The pain:** 30-50% of helpdesk volume is password resets; triage consumes 3-5 hrs/day labor; 15-25% of tickets get misrouted, each costing 47 extra min. ([Mizo.tech](https://mizo.tech/blog/the-hidden-cost-of-manual-ticket-triage-what-ms-ps-are-really-losing/))
- **Frontier-model kill test:** **At risk** — Microsoft Copilot + Entra self-service password reset is closing the gap. **Survives** for MSPs because MSPs serve many tenants with different stacks and need a multi-tenant Copilot.
- **Defensibility:** ConnectWise/Autotask integrations, multi-tenant policy engine, M365-as-code-per-client.
- **Verdict: KEEP — frame as "Copilot-for-MSPs" not generic IT.**

#### P24. Staffing agency resume screening
- **Buyer:** Independent staffing/recruiting agencies (light industrial, healthcare, IT contract).
- **The pain:** Recruiters spend 24 hrs/wk on resumes, 80-90% don't fit; 81% recruiter burnout; time-to-fill 36 days vs 29 days in 2022. ([Vettio.com](https://vettio.com/blog/manual-screening-causes-recruiter-burnout/); [Maayu economics](https://www.maayu.ai/economics-of-a-staffing-agency))
- **Frontier-model kill test:** **FAILS at the basic-screening level.** Survives only if you own ATS write-back (Bullhorn/JobAdder) and have proprietary fit-signal data. Crowded.
- **Verdict: SKIP.**

---

## Section 3 — The TOP 15 (passed all five filters)

Ordered by solo-dev-fit + clarity-of-buyer + defensibility.

| # | Pain | Buyer | Sub-niche wedge | Frontier-kill risk | Defensibility |
|---|---|---|---|---|---|
| **1** | Outpatient-PT prior auth (P1) | PT clinic owner | Blue Cross + UHC in 3 states | Low — payor criteria DB | Clearinghouse + payor portals + denial data |
| **2** | Dental insurance verification (P2) | Independent dental practice | Open Dental + Dentrix shops | Low — payor portal logins | PMS integrations + payor login vault |
| **3** | Indie-pharmacy PBM/DIR reconciliation (P20) | Independent retail pharmacist | Caremark + ESI + OptumRx 835 reconciliation | Low — PBM EDI parsing | PMS integration + NCPA distribution |
| **4** | Independent P&C agency COI issuance (P5) | P&C agency owner/CSR | AMS360 + Hawksoft shops | Low — AMS integration | AMS integration + ACORD form library |
| **5** | Medical claim denial appeals (P4) | Mid-size billing co / RCM | CARC-code-driven appeal letters + portal submission | Low — payor portals + CARC rules | Clearinghouse + denial-pattern data |
| **6** | Home-health agency fax-referral intake (P7) | HH agency intake coordinator | Axxess + HCHB write-back | Low — fax parsing + OASIS rules | EHR write-back + OASIS rule engine |
| **7** | Job-shop CNC RFQ response (P10) | Job-shop owner/estimator | <50-employee shops with no MRP | Low — drawing analysis is multimodal but needs material costing + supplier data | Quote-history learning + supplier price feeds |
| **8** | Construction RFI/submittal routing (P8) | Mid-size GC ($10-100M) | Mid-tier GCs under Procore's price floor | Low — needs spec-section parsing | Spec dataset + Procore integration |
| **9** | Freight-broker carrier onboarding + fraud screen (P17) | 5-50 person freight broker | Anti-double-brokering wedge in 2026 | Low — FMCSA + KYB | TMS integration + carrier-fraud DB |
| **10** | CRE Offering Memorandum generation (P13) | Boutique CRE broker | Multifamily + industrial brokerages | Medium — design templates are easier now | CoStar feed + rent-roll OCR + brokerage branding |
| **11** | Title insurance curative work (P15) | Title agent / paralegal curative team | Florida + Texas (high-volume states) | Low — recording-office access + e-recording | County recording integrations + lender-correspondence DB |
| **12** | Multi-entity SMB month-end close reconciliation (P16) | Outsourced bookkeeping firm | Multi-entity SaaS clients on Stripe + Mercury + Xero | Medium — frontier tool-use can do basic match | Banking + ERP write-back + SOC2 |
| **13** | HVAC quote-in-the-living-room for sub-15-truck shops (P9) | Owner-operator HVAC contractor | Under ServiceTitan's economic floor | Low — distributor + financing integrations | Distributor pricing feeds + financing partner |
| **14** | County clerk-of-court meeting + docket minutes (P18) | County clerk-of-court | County (not city) — clerk-of-court rules | Medium — generic transcription is commoditized; rules engine is moat | Robert's Rules + docket parsing + FOIA audit trail |
| **15** | Commercial roofing inspection report assembly (P12) | Commercial roofing contractor / TPI | Phone-photo v1; NRCA terminology | Low — multimodal vision + NRCA terminology | Field-app + NRCA rules + branded PDFs |

---

## Section 4 — The "Excel runs our company" tells (per the playbook)

Spreadsheet-as-mission-critical signals encountered during research — each is a wedge in itself:

- **Accounting:** 50% of finance teams say Excel is the bottleneck for monthly close ([Ledge.co](https://www.ledge.co/content/month-end-close-benchmarks-for-2025))
- **HVAC quoting:** Office manager writes quotes in Excel after the tech leaves the customer ([BuildOps](https://buildops.com/resources/hvac-quoting-software/))
- **Construction RFI/submittal logs:** PMs maintain manual Excel logs even on Procore ([SubmittalLink](https://www.submittallink.com/post/hidden-costs-of-construction-admin))
- **AV/event production:** "Spreadsheets held together with tape" — Roy van den Broek's $15M ARR SaaS started exactly here ([Indie Hackers](https://www.indiehackers.com/post/tech/building-a-15m-arr-saas-from-a-gap-he-found-at-his-brick-and-mortar-HFriCBQLHukAmdXVEj1q))
- **Restaurant invoice reconciliation:** Daily flow of broadline + specialty + local supplier invoices into spreadsheets ([MarketMan](https://www.marketman.com/blog/restaurant-vendor-management-system))
- **Insurance COI tracking:** ~30% of mid-agencies still use Excel for COI request/renewal logs ([US Tech Automations](https://ustechautomations.com/resources/blog/insurance-certificate-of-insurance-issuance-pain-solution-2026))

---

## Section 5 — Heresies discovered (PG "novelty hides in dead zones")

The cherished assumptions blocking incumbents in 2026:

1. **"Fax is dead."** — Home health, dental insurance verification, optical lab orders, and provider-side prior auth still run on fax. A fax-to-structured-data agent that quietly bridges to modern EHR/AMS systems is huge.
2. **"Vertafore / Procore / ServiceTitan own those markets."** — They own the top decile by spend. The long tail of sub-economic-floor SMBs is wide open.
3. **"AMS / PMS / EHR integrations are too hard for a solo dev."** — Many of these systems have undocumented but stable export formats (Open Dental schema is published; QuickBooks API is stable; ConnectWise has APIs). A solo dev with agents can wrap these.
4. **"AI scribes are commoditized."** — True for the *transcription* part. False for the *post-transcription write-back + coding + payor-rules* part. Re-frame the problem from "transcribe" to "complete the documentation lifecycle."
5. **"PBM contracts are too opaque to audit."** — Wrong: 835/ERA EDI is structured and detectable.
6. **"Curative title is a paralegal job that resists software."** — Recording offices have e-recording portals, and the documents are templated; the moat is per-county configuration nobody bothered to map.
7. **"Permit pulling is solved by PermitFlow."** — It's solved for residential GCs in major metros; the trade-specific (electrical/plumbing) sub-niche in second-tier metros is underserved.
8. **"GCs all use Procore."** — Mid-tier GCs ($10-50M revenue) use Procore as glorified file storage; the *intelligence layer* on top is unbuilt.

---

## Section 6 — Frontier-model kill criterion (which 15 actually survive Claude 5 / GPT-5)

The ones that **die** under a frontier upgrade are those whose entire value is "summarize this document" or "match these line items" with no surrounding system context. The ones that **survive** in this list all share three traits:

- **External system integration** (PMS / AMS / EHR / TMS / clearinghouse / payor portal) the model doesn't have.
- **Per-buyer / per-state / per-payor configuration** the model can't memorize.
- **Workflow + write-back** — value comes from the action taken in another system, not the text generated.

All 15 in the keep-list above meet at least 2 of 3.

---

## Section 7 — Solo-dev shippable-in-90-days quick-grade

| Top 5 candidate | Day-30 wedge | Day-90 product | Distribution channel |
|---|---|---|---|
| **P1 outpatient-PT prior auth** | Single-payor (BCBS-TX) + single EHR (WebPT) + 5 design partners | Multi-payor, denial-rework loop, EMR write-back | State PT associations, billing-co partnerships |
| **P2 dental verification** | Open Dental + Delta Dental in 2 states + 10 design partners | All major payors, denial-prediction, write-back | DSO acquirers, dental podcasts, ADA channels |
| **P20 indie-pharmacy PBM reconciliation** | Caremark 835 parsing + PrimeRx integration + 5 pharmacies | Multi-PBM, dispute filing, NCPA distribution | NCPA membership channel, pharmacy buying groups |
| **P5 COI issuance** | AMS360 connector + ACORD 25 lib + 5 P&C agencies | Multi-AMS, holder DB, renewal automation | Big "I" / IIABA chapters, agency networks |
| **P10 CNC job-shop RFQ** | STEP/PDF drawing → cost estimate + 5 shops | Material costing + supplier lead-time + ERP write | r/CNC + AMT + manufacturers' association partnerships |

---

## Section 8 — Gaps & follow-ups (for downstream agents)

1. **Direct Reddit quote sourcing is incomplete.** Reddit blocked all `WebFetch` and `site:reddit.com` queries during this session. Agent 03 (if scoped to validation) or a manual GummySearch pass should retrieve direct subreddit post links for the top 5.
2. **YC RFS 2026 cross-reference.** The top 5 above all map to YC RFS items: P1/P2/P4/P5/P20 → "AI-Native Service Companies" (RFS A1-#2); P10 → "Modern Metal Mills" (RFS A2-#6); P8/P12 → "AI Guidance for Physical Work" (RFS A2-#7). Application essay should explicitly cite the matching RFS.
3. **Founder-fit screen.** User is solo dev with no stated industry background. The single most under-discussed selection criterion is **"who can you cold-DM and get a yes from for an unpaid pilot in the next 48 hours?"** — that constrains the final pick more than any of the above analysis.
4. **Founder-as-customer test (PG).** None of these are problems the founder personally has. Mitigation: pick one and *immediately* recruit a co-design partner from the buyer pool before applying.

---

## Section 9 — Sources (consolidated)

**Frameworks**
- [Greg Isenberg — find winning startup ideas from AI and data](https://www.gregisenberg.com/blog/find-winning-startup-ideas-from-ai-and-data)
- [Greg Isenberg LinkedIn pulse on Reddit goldmine](https://www.linkedin.com/pulse/greg-isenbergs-reddit-startup-idea-goldmine-method-summary-itseuwa-fs9qf)
- [IdeaBrowser](https://www.ideabrowser.com/idea-of-the-day)
- [Cluboffounders — best startup ideas hide in boring problems](https://www.cluboffounders.com/p/the-best-startup-ideas-hide-in-boring-problems)
- [Indie Hackers — Roy van den Broek $15M ARR](https://www.indiehackers.com/post/tech/building-a-15m-arr-saas-from-a-gap-he-found-at-his-brick-and-mortar-HFriCBQLHukAmdXVEj1q)
- [Automaiva — vertical-AI agents 2026](https://automaiva.com/vertical-saas-ai-agents-2026/)

**Healthcare admin**
- [Medical Economics — prior auth burden + AI](https://www.medicaleconomics.com/view/prior-authorization-history-burden-ai-future)
- [AMA prior auth survey context](https://www.ama-assn.org/press-center/ama-press-releases/physicians-concerned-ai-increases-prior-authorization-denials)
- [Overjet — dental insurance verification 2025 guide](https://www.overjet.com/blog/dental-insurance-verification-workflows-complete-2025-guide)
- [Curve Dental — verification](https://www.curvedental.com/blog/dental-insurance-verification-guide)
- [PupPilot — vet AI scribe $100K ROI](https://www.puppilot.co/blog/the-100k-roi-of-an-ai-scribe-how-reclaiming-10-dvm-hours-a-week-transforms-your-clinics-finances)
- [PupPilot — vet burnout](https://www.puppilot.co/blog/burnout-isnt-a-symptom-its-a-crisis-how-vet-automation-can-be-part-of-the-cure)
- [Experian — State of Claims 2025](https://www.experian.com/blogs/healthcare/healthcare-claim-denials-statistics-state-of-claims-report/)
- [MD Clarity — medical appeal letters](https://www.mdclarity.com/blog/medical-appeal-letters)
- [Medical billers/coders — denials](https://www.medicalbillersandcoders.com/blog/denials-in-medical-billing/)
- [KLAS — reducing nursing documentation burden 2025](https://klasresearch.com/archcollaborative/report/reducing-nursing-documentation-burden-2025/706)
- [MedStar home-health fax referral form](https://www.medstarhealth.org/-/media/project/mho/medstar/pdf/home-care-fax-and-referral-form.pdf)
- [Reveleer — AI chart abstraction](https://www.reveleer.com/resource/ai-abstraction-with-new-ai-powered-healthcare-technology)

**Pharmacy**
- [NCPA — DIR fees FAQ](https://www.ncpa.co/pdf/dir-faq.pdf)
- [Pharmacy Times — DIR white paper](https://www.pharmacytimes.com/view/white-paper-dir-fees-simply-explained)
- [Pharmacist.com — CMS eliminates retroactive DIR](https://www.pharmacist.com/Advocacy/Issues/CMS-Eliminates-Retroactive-DIR-Fees)

**Insurance**
- [US Tech Automations — COI issuance 2026](https://ustechautomations.com/resources/blog/insurance-certificate-of-insurance-issuance-pain-solution-2026)
- [myCOI — how to ask for a COI](https://mycoitracking.com/how-do-you-ask-for-a-coi/)

**Construction / trades**
- [SubmittalLink — hidden costs of construction admin](https://www.submittallink.com/post/hidden-costs-of-construction-admin)
- [SubmittalLink — RFI meaning](https://www.submittallink.com/post/rfi-meaning-in-construction)
- [ESUB — RFI cost](https://esub.com/blog/rfi-cost-construction-firm)
- [Projul — RFI management 2026](https://projul.com/blog/construction-rfi-management/)
- [BuildOps — HVAC quoting](https://buildops.com/resources/hvac-quoting-software/)
- [BuildOps — HVAC quotes guide](https://buildops.com/resources/hvac-quotes/)
- [PermitFlow — electrical permits guide](https://www.permitflow.com/blog/electrical-permit)
- [NRCIA — roof inspection report template](https://www.nrcia.org/roof-inspection-report-template/)

**Manufacturing**
- [Modern Machine Shop — RFQ time is money](https://www.mmsonline.com/articles/when-it-comes-to-rfq-response-time-is-money)
- [StartProto — AI agents for RFQ](https://www.startproto.com/blog/how-ai-agents-are-revolutionizing-rfq-processing-in-manufacturing)
- [CADDi — job-shop RFQ management](https://us.caddi.com/resources/insights/job-shop-rfq-management)

**Real estate / title / accounting**
- [CREBuilder — OM builder](https://www.crebuilder.com/offering-memorandum-builder)
- [Decobase — reading an OM](https://www.decobase.app/blog/how-to-read-a-CRE-offering-memorandum)
- [ALTA — curative work study 2024](https://www.alta.org/media/pdf/240506-ALTA-Title-Insurance-Curative-Work-Study-Report.pdf)
- [Ledge.co — month-end close benchmarks 2025](https://www.ledge.co/content/month-end-close-benchmarks-for-2025)
- [Teampay — manual reconciliation fails](https://www.teampay.co/blog/problems-with-manual-reconciliation)
- [Parseur — automate tax season](https://parseur.com/use-case/automate-tax-season)
- [Baker Tilly — 2025 income tax provision pain](https://www.bakertilly.com/insights/top-10-pain-points-for-the-2025-year-end-income-tax-provision)
- [AccountingWEB — SAGE 50 outdated 2025](https://www.accountingweb.co.uk/any-answers/why-sage-50-is-still-so-outdated-in-2025)

**Logistics**
- [Truckstop — broker carrier packets](https://truckstop.com/blog/broker-carrier-packets/)
- [DAT — carrier onboarding best practices](https://www.dat.com/resources/carrier-onboarding-guide)
- [LoadConnect — rate confirmation automation](https://loadconnect.io/blog/rate-confirmation-trucking-automation)

**Public sector**
- [Smart Cities Dive — AI for municipal clerks](https://www.smartcitiesdive.com/news/ai-municipal-clerks-speed-up-public-records-reporting/820216/)
- [GovTech — AI meeting minutes drudgery](https://www.govtech.com/artificial-intelligence/ai-takes-the-drudgery-out-of-compiling-meeting-minutes)

**Optometry / restaurant / staffing / MSP**
- [Sightview — optical retail challenges](https://www.sightview.com/articles/optical-retail-challenges-and-how-to-solve-them)
- [RevolutionEHR — managing optical orders](https://www.revolutionehr.com/blogs/manage-optical-orders-more-efficiently-with-revolutionehr)
- [MarketMan — restaurant vendor management](https://www.marketman.com/blog/restaurant-vendor-management-system)
- [Vettio.com — manual screening burnout](https://vettio.com/blog/manual-screening-causes-recruiter-burnout/)
- [Maayu.ai — staffing agency economics](https://www.maayu.ai/economics-of-a-staffing-agency)
- [Mizo.tech — hidden cost of manual ticket triage](https://mizo.tech/blog/the-hidden-cost-of-manual-ticket-triage-what-ms-ps-are-really-losing/)
- [Smith.ai — law firm conflict check](https://smith.ai/blog/how-to-run-a-law-firm-conflict-check)
- [Lawyerist — client onboarding](https://lawyerist.com/law-firm-clients/client-intake-onboarding/)

— end of file —
