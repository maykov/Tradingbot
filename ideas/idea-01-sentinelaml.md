# Idea 01 — SentinelAML

## 1. Executive Summary

SentinelAML is an AI-native transaction-monitoring decision-support platform that ranks and clusters AML alerts, pre-assembles evidence, and drafts SAR narratives for compliance teams at mid-size banks, credit unions, and fintechs. It targets BSA/AML officers at $1B–$50B institutions — large enough to need dedicated tooling but underserved by Tier-1 vendors (NICE Actimize, SAS, Oracle) and out-priced by white-glove service. The timing case rests on LLMs finally making alert triage and narrative drafting viable, regulators signaling openness to model-assisted (not model-suppressed) monitoring, and rising AML fines and personal officer liability pushing compliance budgets up. The revised path reaches $134M ARR by Year 5 (320 customers, $420k blended ACV), funded by roughly $65M of primary capital against a $44.3M peak burn, with $200M pushed to Year 6–7. Verdict: conditional GO — the plan survived a serious legal and financial stress test only by giving up its most aggressive claims (alert suppression, pooled data, $200M in 5 years), and what remains is a smaller but fundable and legally coherent business.

## 2. Product & Value Proposition

SentinelAML sits beside (not instead of) a bank's incumbent rules engine, ingesting the bank's own transaction, KYC, and alert-disposition data via warehouse/file export — no dependency on incumbent API cooperation. It re-scores and clusters alerts, assembles evidence, and drafts SAR narratives, but — after the v2 repositioning — **never suppresses or auto-closes an alert**: every alert still reaches a named human analyst. The pitch shifted from "fewer alerts" to "3–5x analyst throughput," preserving the same ROI math (analyst labor is the cost center) without triggering a suppression-model fight with examiners. Models are single-tenant and per-customer, trained only on that institution's own history inside that institution's environment. The Year-1 wedge is a drop-in triage/evidence-assembly layer sold via compliance-consultant referrals to design partners; later years add a case-management UI, crypto/VASP and sanctions modules, one-click (human-closed) disposition, and — replacing the illegal consortium concept — a 314(b) facilitation module that lets banks share suspected-crime information with each other under the statutory safe harbor, with SentinelAML as facilitator rather than data owner.

## 3. Addressable Market

| Metric | Value | Basis |
|---|---|---|
| TAM | ~$3.5B/yr | ~11,800 US banks/credit unions + global fintechs/MSBs/crypto exchanges × ~$300k midpoint ACV; consistent with third-party AML-software market estimates ($2.6–4B in 2025) |
| SAM | ~$1.23B/yr | ~4,100 mid-size ($1B–$50B asset) institutions underserved by Tier-1 vendors × $300k ACV |
| SOM (Year 5) | $134M ARR | 320 customers (10.9% of the US+Canada SAM slice, ~2,950 institutions) × $420k blended ACV incl. NRR |

**Key assumptions (v2):** SAM is US+Canada-only through Year 3 (UK/EU counted only from Year 4 entry); US+Canada is assumed to be ~72% of the full 4,100-institution SAM; win rate 20% against ~800 qualified opportunities/year by Year 5; blended ACV rises modestly from $150k (Y1) to $420k (Y5) via mix shift and 110% target NRR (unvalidated — condition precedent for Series B).

## 4. 5-Year Plan (v2, revised)

| Year | Product Milestones | GTM Motion | Headcount | Geography | Customers | ARR |
|---|---|---|---|---|---|---|
| 1 | Decision-support overlay (rank/cluster/evidence); in-tenant SAR drafting; SOC 2 Type I; E&O bound; FTO review started | Founder-led; 4 design partners via compliance-consultant referrals | 16 (Eng 8, Comp/ML 4, GTM 3, Ops 1) | US | 4 | $0.6M |
| 2 | Full monitoring engine (human-reviewed); case management; SOC 2 Type II; vendor-DD response pack | 4 AEs + SDRs; first core-banking channel deal | 42 | US | 20 | $4.5M |
| 3 | Crypto/VASP module; sanctions add-on; per-customer model-tuning suite | 10 AEs; 2–3 channel partners live | 79 | US + Canada | 65 | $18M |
| 4 | One-click disposition (human-in-loop); enterprise multi-entity; UK/EU localized module + entities | 20 AEs; enterprise segment opens; SI partnerships | 126 | +UK/EU entry | 105 | $54M |
| 5 | 314(b) facilitation module; embedded processor product; exam-readiness suite v2 | 32 AEs; land-and-expand + channel at scale | 180 | US, Canada, UK/EU | 320 | **$134M** |

## 5. Financial Model (v2)

| Year | ARR | GM% | COGS | S&M | R&D | G&A | EBITDA | Cum. Capital Req'd |
|---|---|---|---|---|---|---|---|---|
| 1 | $0.6M | 50% | $0.30M | $1.08M | $2.76M | $1.20M | −$4.74M | $4.74M |
| 2 | $4.5M | 58% | $1.89M | $5.46M | $5.52M | $1.50M | −$9.87M | $14.61M |
| 3 | $18M | 64% | $6.48M | $14.85M | $8.97M | $2.70M | −$15.00M | $29.61M |
| 4 | $54M | 68% | $17.28M | $32.40M | $13.11M | $5.90M | −$14.69M | $44.30M (peak) |
| 5 | $134M | 72% | $37.52M | $56.00M | $17.25M | $9.40M | **+$13.83M** | $44.30M |

**Unit economics (Year 5):** CAC $350k; LTV $2.42M (ACV $420k × 72% GM × 8-yr life); LTV:CAC ≈ 6.9:1; payback ≈ 14 months. Breakeven LTV:CAC (3:1) tolerates CAC slippage to ~$807k — 2.3x the modeled figure.

**Funding plan:** Peak cumulative burn ≈ $44.3M (end of Year 4); Year 5 turns cash-generative (+$13.83M). With a ~45% runway buffer, recommended total primary raise ≈ **$65M** across pre-seed through Series C (Series C sized up from v1's $15M to ~$22M to cover the higher burn). Capital efficiency: $3.02 of Year-5 ARR per dollar of peak burn — top-quartile for enterprise SaaS. At an 8–10x forward-ARR multiple, Year-5 exit value is estimated at $1.3–2.0B, roughly 20–30x on capital invested.

**Conditions precedent (finance):** (1) Year-1 pilots must validate a path to ≥58% GM by Year 2 (single-tenant COGS is the model's soft spot); (2) NRR ≥105% on the Year-2 cohort before Series B; (3) all four Year-1 design partners must convert to paid within two quarters or the 20%-win-rate/5-deals-per-AE engine is overstated.

## 6. Legal Risk Assessment (v2 status)

| # | Risk | v1 Severity | v2 Status | Mitigation |
|---|---|---|---|---|
| L1 | Examiner acceptance of ML alert suppression | Fatal | Mitigated | Repositioned to decision-support; every alert reaches a human; residual risk if reduced review time reads as de facto suppression (see N3) |
| L2 | SAR-draft confidentiality (§5318(g)(2)) | Serious | Resolved | Legal reading accepted: vendor-hosted SAR tooling within a bank's compliance function is established practice; hardened with in-tenant hosting and cross-customer training exclusion |
| L3 | US SAR/examiner moat doesn't travel to UK/EU | Serious | Mitigated | EU/UK entry deferred to Year 4, made non-load-bearing to the 5-yr plan |
| L4 | Vendor liability vastly exceeds contract value | Fatal | Mitigated | Bank retains disposition authority; standard fee-based caps with carve-outs only for IP/confidentiality/gross negligence; E&O budgeted |
| L5 | E&O/cyber coverage unaffordable at Year-1 scale | Manageable | Resolved | $250k Year-1 premium budgeted, rising with ARR |
| L6 | Year-4 agentic auto-close of alerts | Fatal | Resolved | Removed from roadmap entirely; no autonomous closure committed within the 5-year window |
| L7 | Cross-customer data moat likely illegal | Serious | Resolved | Single-tenant, per-customer models only; illegal pooled-data moat abandoned |
| L8 | No FTO analysis/patent strategy | Serious | Mitigated | FTO review + defensive filings budgeted pre-Series A; moat honestly restated as switching costs, not IP — review not yet performed |
| L9 | Cross-institution consortium data pooling (GLBA/SAR conflict) | Fatal | Resolved | Year-5 consortium cut; replaced with 314(b) facilitation module (safe-harbor sharing between banks, SentinelAML never owns data) |
| L10 | FCRA "consumer reporting agency" exposure | Serious | Mitigated | Contractual/product prohibition on credit/account-decision use; counsel boundary opinion gated pre-launch |
| L11 | GDPR Art. 22 / cross-border transfer gap | Manageable | Mitigated | Deferred with EU entry to Year 4; timing now appropriate |
| L12 | Third-party-risk guidance / Bank Service Company Act exam exposure | Serious | Mitigated | Compliance/audit function staffed from Year 1 (2 FTE) to 12 FTE by Year 5; sales-cycle assumptions lengthened accordingly |
| L13 | Liability caps vs. bank indemnity demands in direct conflict | Fatal | Mitigated | Conflict resolved by decision-support posture; residual negotiation friction on regulatory-loss indemnity remains ordinary commercial risk |
| L14 | No committed data/API access from incumbents | Serious | Resolved | Warehouse/file-based ingestion of bank-owned data; no incumbent cooperation required |
| N1 | In-tenant/single-tenant deployment burden (new) | — | Manageable | Acknowledged in GM ramp (50%→72%, below v1's 55%→78%); each model update may retrigger a tenant's SR 11-7 change validation |
| N2 | 314(b) module scope discipline (new) | — | Manageable | Needs hard product-level registration/scope guardrails to avoid recreating L9 |
| N3 | Rubber-stamp risk in "one-click disposition" (new) | — | Serious | Not yet mitigated in-plan; needs enforced review-depth telemetry and QA sampling, or L1/L4/L13 reopen together |

## 7. Debate Log

The v1 plan chased the seed brief's $200M target with an alert-*suppression* product, a cross-institution pooled-data moat, and a Year-4 fully autonomous alert auto-close feature. Legal review found five **fatal** objections: examiners were never going to bless suppressed alerts (L1); liability from a missed SAR could run 100–1000x the ACV with no insurance plan (L4); autonomous closure removed human judgment from a BSA-critical decision (L6); the pooled-data consortium moat violated GLBA/SAR confidentiality (L9); and standard SaaS liability caps were incompatible with the tail risk banks would demand indemnification against (L13). Finance separately found the plan's numbers didn't hold together on their own terms: the entrepreneur's GTM payroll could buy only a fraction of the CAC the pricing model required, Year-1 timing ignored the very procurement cycles the plan itself flagged as a risk, and Year-5 logo targets implied AE headcount the plan never budgeted.

Entrepreneur v2 resolved all five fatals with a single structural move: repositioning the product from suppression to decision-support, where a human closes every alert. That one change dissolved the SR 11-7 fight (L1) and, because SentinelAML no longer makes disposition decisions, also dissolved the liability conflict (L4, L13) and the rationale for autonomous closure (L6, removed outright). The pooled-data moat was abandoned in favor of single-tenant, per-customer models and a legally narrower 314(b) facilitation module (L9, L7). GTM was rebuilt entirely around finance's CAC-efficiency envelope rather than payroll guesswork, and Year-5 logo targets were cut to match plausible AE capacity (32 AEs, 5 deals/AE).

The honest cost of this de-risking is visible everywhere in the numbers: Year-5 ARR fell from $200M to **$134M**, Year-1 ARR from $1.5M to $0.6M, Year-5 customer count from 500 to 320, gross margin ramp from 55–78% to 50–72% (single-tenant deployment is more expensive), and the funding ask grew from $35.6M peak burn / $55M raise to $44.3M peak burn / ~$65M raise. Finance's verdict was explicit: it would "fund a credible $134M plan over a fictitious $200M one every time." Legal's residual concern is that the entire fix rests on one assumption — that a human meaningfully reviews every alert — and the new "one-click disposition" feature (N3) could erode that in practice if sales pressure turns it into rubber-stamping, which would reopen L1, L4, and L13 simultaneously.

## 8. Verdict

- **Entrepreneur:** A smaller, legally coherent $134M-ARR business beats a $200M fiction — the repositioning is a real product, not a euphemism.
- **Finance:** Fundable with conditions — $3.02 of Year-5 ARR per dollar of peak burn and 6.9:1 LTV:CAC survive the legal mitigations comfortably.
- **Legal:** All five Fatals are resolved or credibly mitigated, but the whole posture now depends on human review staying genuinely meaningful — that dependency (N3) is unmitigated today.
- **Overall: GO (conditional).** The plan is fundable and legally defensible only if the Year-1 pilots hit the GM/NRR/conversion conditions precedent and the company builds review-depth telemetry before "one-click disposition" ships, so funding should be staged accordingly rather than committed in full upfront.
