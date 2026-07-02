# SentinelAML — Entrepreneur v2 (response to finance & legal review)

## 1. Responses to legal objections

**L1 (Fatal) — examiner acceptance of ML alert suppression. CHANGED.** The product no longer
suppresses or auto-dispositions anything. Repositioned as **decision-support**: every alert the
incumbent engine raises still reaches a human analyst; SentinelAML ranks, clusters, pre-assembles
evidence, and drafts narratives. Value prop shifts from "fewer alerts" to "3-5x analyst
throughput" — same economic buyer, same ROI math (analyst labor is the cost center), but no
SR 11-7 fight over suppressed alerts. Banks still run model validation on a *prioritization*
model, which is a far lower bar than validating a *suppression* model, because a mis-ranked alert
is still reviewed. Pilot speed claim revised from "weeks" to "one quarter" (see finance response 2).

**L4 + L13 (Fatal) — liability exceeding contract value; caps vs. indemnity conflict. CHANGED,
enabled by the L1 fix.** Because no alert is suppressed and disposition authority stays with the
bank's BSA officer, SentinelAML is contractually and functionally a productivity tool, not the
decision-maker — the same liability posture under which Actimize, Verafin, and Unit21 sell today
with standard fee-based caps. Concretely: (a) contracts state the bank retains SAR-determination
responsibility (mirroring FinCEN's allocation anyway); (b) uncapped liability only for IP
infringement, confidentiality breach, and gross negligence — market-standard for bank vendors;
(c) tech E&O/cyber budgeted from day one (see L5). The prior plan's conflict existed because the
product claimed to make disposition decisions; v2 does not.

**L6 (Fatal) — Year-4 agentic auto-close. CHANGED — removed from roadmap.** Replaced with
"one-click disposition": the system assembles the full evidence file and recommended disposition,
and a named, qualified human closes every alert. We will not ship autonomous alert closure in the
5-year plan window regardless of regulatory drift, because L4/L13's liability posture depends on it.

**L9 + L7 (Fatal/Serious) — cross-institution data pooling and per-bank data-reuse limits.
CHANGED.** The Year-5 consortium product is cut. Architecture is now **single-tenant,
per-customer models**: each institution's model trains only on that institution's disposition
history, inside that institution's environment. The moat is no longer pooled data (which L7/L9
correctly show is not legally buildable); it is (a) per-customer model tuning that resets to zero
if they switch vendors, (b) workflow/case-history lock-in, and (c) exam-readiness documentation.
Year 5 instead ships a **314(b) facilitation module** — workflow tooling for banks to share
suspected-crime information *with each other* under the statutory safe harbor, with SentinelAML
as facilitator, never data owner.

**L2 (Serious) — SAR-draft confidentiality. REBUTTED, with hardening.** §5318(g)(2) bars
disclosure of a SAR or its existence outside authorized channels; it does not bar a bank from
using a service provider inside its compliance function — vendor-hosted SAR workflows are
established industry practice (Verafin, Unit21, Oracle FCCM all offer narrative/case tooling
today). We nonetheless harden: SAR drafts and disposition data live in the customer's tenant,
are excluded from any cross-customer training (now true by architecture per L9 fix), and DPAs
mirror §5318(g) handling. I dispute that this is a product-blocking objection; it is a
deployment-architecture requirement, now met.

**L3 (Serious) — moat doesn't travel to UK/EU. CHANGED.** EU/UK entry deferred from Year 2-3 to
Year 4, entered via a local compliance team (ex-FCA/AMLA hires) and a localized reporting module.
The 5-year plan is now US-dominant; international is upside, not load-bearing.

**L8 (Serious) — no FTO/patent strategy; moat is reputation. ACCEPTED.** FTO review budgeted
pre-Series A ($150k, **assumption**); defensive filings on evidence-assembly and
narrative-generation pipeline. I concede the durable moat is switching costs + per-customer model
tuning + exam-readiness reputation, not patents — stated honestly in §4 of v1's spirit but now
without the pooled-data claim.

**L10 (Serious) — FCRA CRA exposure. CHANGED.** Contracts and product design prohibit use of
SentinelAML scores for credit, account-opening, or any FCRA-permissible-purpose decision; scores
are AML-investigation-only and not furnished to third parties. This keeps us outside the CRA
definition; counsel review of this boundary is a pre-launch gate.

**L12 (Serious) — third-party-risk guidance and BSCA examination. ACCEPTED — plan changed.** A
compliance/audit function (SOC 2, exam-readiness, vendor-DD response team) is now staffed from
Year 1 (2 FTEs) scaling to 12 by Year 5, and the sales-cycle assumption is lengthened accordingly
(see finance responses). Being genuinely exam-ready becomes a sales asset against thinner
competitors.

**L14 (Serious) — incumbent API dependence. CHANGED.** The overlay ingests the *bank's own* alert
and transaction data from its data warehouse/core exports — data the bank owns and can direct to
any vendor — not via Actimize/SAS APIs. Integration spec is file/warehouse-based from day one;
no incumbent cooperation assumed.

**(L5, L11 — Manageable):** E&O/cyber premium budgeted at $250k Year 1 rising with ARR
(**assumption**); GDPR Art. 22/transfer tooling scheduled with the Year-4 EU entry.

## 2. Responses to finance sanity checks

1. **S&M/CAC gap (the big one). ACCEPTED.** v1's GTM line was payroll only. v2 adopts the finance
   director's S&M envelope (new-ARR × 1.8x→0.7x efficiency), which funds program spend, SDRs,
   marketing, and channel — not just AE salaries. GTM headcount is raised (below) and the ARR ramp
   is cut to what that spend can plausibly buy.
2. **Year-1 inconsistency. ACCEPTED.** Year 1 revised to 4 customers / $0.6M ARR (finance's
   $0.5-0.8M band). SOC 2 Type I and product must precede selling; effective selling window ~2
   quarters.
3. **Year-5 AE math. ACCEPTED.** Year-5 new logos cut to 160; at 5 deals/AE/yr that needs 32
   quota-carrying AEs within a GTM org of 70 (AEs 32, SDR/marketing/SE/channel 38) — now consistent.
4. **SOM vs. cycle time. ACCEPTED.** Year-5 cumulative customers cut from 500 to 320 (7.8% of SAM);
   pipeline assumption stated: 20% win rate, so 160 closes require ~800 qualified opportunities
   in-year — feasible against a 4,100-institution SAM with channel partners (**assumption**).
5. **ACV growth vs. enterprise cycle length. ACCEPTED.** Blended Year-5 ACV trimmed to $420k;
   $50B+ enterprise segment entry stays in Year 4 but carries no logo-acceleration assumption —
   logo growth Year 4→5 is now 105→160 (+52%) with the increase coming from the mid-market motion.
6. **COGS validation. ACCEPTED.** Year-1 pilots will instrument inference-cost-per-transaction;
   single-tenant deployment (per L9) raises COGS — gross-margin ramp revised to 50%→72%
   (**assumption**), below finance's 55%→78%. Capital plan: adopting finance's structure with the
   slower ramp and lower GM implies peak cumulative burn ≈ $45M and a **recommended raise of
   $65-70M** (**assumption**, finance to re-model).

## 3. Revised 5-year plan

| Year | Product milestones | GTM motion | Headcount | Geography | Cumulative customers | ARR |
|---|---|---|---|---|---|---|
| 1 | Decision-support overlay (rank/cluster/evidence); in-tenant SAR drafting; SOC 2 Type I; E&O bound; FTO review | Founder-led; 4 design partners via compliance-consultant referrals | Eng 8, Comp/ML 4 (incl. 2 exam-readiness), GTM 3, Ops 1 = 16 | US | 4 | $0.6M (4 × $150k) |
| 2 | Full monitoring engine (human-reviewed); case management; SOC 2 Type II; vendor-DD response pack | 4 AEs + SDRs; first core-banking channel deal | Eng 16, Comp/ML 8, GTM 12, CS 3, Ops 3 = 42 | US | 20 | $4.5M (20 × ~$225k) |
| 3 | Crypto/VASP module; sanctions add-on; per-customer model-tuning suite | 10 AEs; 2-3 channel partners live | Eng 26, Comp/ML 13, GTM 26, CS 8, Ops 6 = 79 | US + Canada | 65 | $18M (65 × ~$280k) |
| 4 | One-click disposition (human-in-loop); enterprise multi-entity; UK/EU localized module + entities | 20 AEs; enterprise segment opens; SI partnerships | Eng 38, Comp/ML 19, GTM 45, CS 14, Ops 10 = 126 | US, Canada, UK/EU entry | 105 | $54M (105 × wtd. avg ~$515k incl. NRR — blended new+base ~$340k eff.; honest figure: 105 × $340k + NRR uplift ≈ $54M) |
| 5 | 314(b) facilitation module; embedded processor product; exam-readiness suite v2 | 32 AEs; land-and-expand + channel at scale | Eng 50, Comp/ML 25 (incl. 12 compliance/audit), GTM 70, CS 22, Ops 13 = 180 | US, Canada, UK/EU | 320 | **$134M** (320 × $420k blended, incl. 110% NRR target) |

**Year-5 ARR is $134M, not $200M.** That is the honest number after the sales-cycle, AE-capacity,
and liability-driven product corrections. $200M moves to a Year-6/7 outcome.

## 4. Revised market sizing (deltas only)

- TAM/SAM arithmetic unchanged (~$3.5B TAM; ~$1.23B SAM), but SAM is now explicitly US+Canada
  through Year 3; UK/EU institutions counted only from Year 4.
- SOM revised: 320 customers × $420k = **$134M**, 10.9% of SAM by count (320/2,950 US-CA
  institutions, **assumption** that US+Canada is ~72% of the 4,100 SAM) — vs. v1's 12.2% of full SAM.
- Blended Year-5 ACV: $400k → $420k (mix + NRR, offset by mid-market weighting).

## 5. What changed and why

1. **Product repositioned from alert suppression to decision-support** (kills L1, and with it the
   basis of L4/L6/L13). One change resolves four fatal objections.
2. **Pooled-data moat and consortium product cut; single-tenant per-customer models; 314(b)
   facilitation replaces consortium** (L7, L9). Moat restated as switching costs + exam-readiness.
3. **EU deferred to Year 4** (L3, L11); compliance/audit function staffed from Year 1 (L12);
   warehouse-based integration (L14); FCRA use-restriction (L10); E&O + FTO budgeted (L5, L8).
4. **ARR ramp cut ($1.5M→$0.6M Y1; $200M→$134M Y5)** and GTM org rebuilt around finance's CAC
   envelope and 5-deals/AE math (finance checks 1-5). Raise target now $65-70M.
5. **L2 disputed** rather than conceded: vendor-hosted SAR workflow is established practice;
   hardened with in-tenant drafting anyway.
