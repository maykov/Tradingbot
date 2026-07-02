# Idea 02 — ClearPath Health

## 1. Executive Summary

ClearPath is an AI agent platform that automates prior authorization for hospital systems, specialty clinics, and MSOs — assembling verbatim, provenance-linked clinical evidence from the EHR, routing it through sanctioned payer rails, and having a licensed clinician attest before submission. The buyer is revenue-cycle and utilization-management leadership at high-PA-volume providers (oncology, imaging, cardiology), starting with MA/Medicaid-heavy systems in FL, AZ, and TX. The "why now" is CMS-0057-F's Prior Authorization API mandate (Jan 1, 2027), which forces Medicare Advantage, Medicaid managed care, and exchange payers to expose usable ePA APIs — a beachhead the product now targets honestly rather than assuming commercial ERISA plans are in scope. The path to Year-5 ARR runs from $2M (Y1, copilot-mode design partners) to $160M (Y5, 300 customers, blended $533K ACV), re-accelerating in Y2–Y3 as automation replaces labor-heavy copilot mode once payer APIs land. Verdict: conditional GO — the three Fatal legal defects from v1 are cured, unit economics remain strong (7.7:1 LTV:CAC), but the plan now depends on a single load-bearing control (clinician attestation) and an external regulatory timeline it does not control.

## 2. Product & Value Proposition

ClearPath assembles clinical evidence from the EHR (Epic, Cerner, athenahealth), matches it against payer medical-necessity policy, and submits prior-authorization requests through sanctioned channels — X12 278 via clearinghouses (Availity, Change/Optum), Da Vinci FHIR ePA where payers have shipped it, and "copilot mode" (ClearPath assembles the packet; the customer's own staff reviews and submits under their own credentials) everywhere else. Every evidence element is a verbatim, provenance-linked citation to the chart; a licensed clinician at the customer attests to each submission before it leaves. Appeals are auto-drafted with citations when claims are denied. The product is explicitly no longer "denial-proof" — it is positioned as "complete-and-accurate first submission," sold on time saved and completeness, never on approval rates. Full automation unlocks payer-by-payer as that payer's API goes live under the CMS-0057-F mandate.

## 3. Addressable Market

| Metric | Value | Basis |
|---|---|---|
| TAM | $40B/yr | Midpoint of $35–55.8B US prior-auth administrative spend (AMA 2025 survey; CAQH/AHIP via AMA/IDC) — unchanged v1→v2 |
| SAM | ~$10B (near-term), expanding toward $24B | 60% of TAM is provider-side automatable labor ($24B); v2 cuts this to the ~40% of a typical system's PA mix that is mandate-covered (MA, Medicaid MCO, QHP) — **assumption** |
| SOM (Y5) | ~$160M ARR | 300 customers (down from 400 in v1) × $533K blended ACV (**assumption**: copilot-mode ACVs ~$300K, full-automation ~$600K) ≈ 1.6% of near-term SAM |

Key assumptions: ~2,600 serviceable accounts nationally (600 multi-hospital systems + 2,000 large specialty/MSO groups, both **assumption**); SAM expands as commercial/ERISA payers voluntarily extend the same API infrastructure they build for CMS-0057-F compliance (treated as upside, not thesis).

## 4. 5-Year Plan

| Year | Product Milestones | GTM | Headcount (Eng/Clin-Prod/Sales/CS/Compliance-Ops/G&A = Total) | ARR |
|---|---|---|---|---|
| 1 | Copilot mode + clinician attestation; X12 278 rail; Epic + Cerner FHIR; FTO + UR-licensure survey; compliance officer hired | 5 MA/Medicaid-heavy design partners (FL/AZ/TX); AEs hired mid-year | 10/3/2/2/2/3 = 22 | $2M |
| 2 | First payer-API automations as CMS-0057-F APIs land (Jan 2027); appeals drafting with attestation; SOC 2 II + HITRUST started | Direct sales off Y1 references; MA/Medicaid segment focus | 20/7/8/8/8/9 = 60 | $7M |
| 3 | 8 specialties; automation >50% of volume; de-identified benchmarking product | Land-and-expand; clearinghouse channel partnerships | 35/12/22/25/20/16 = 130 | $28M |
| 4 | 12+ specialties; commercial/ERISA expansion in copilot mode + early voluntary commercial APIs; pre-submission denial-risk scoring (decision support only) | Enterprise + mid-market dual motion | 60/20/45/60/45/30 = 260 | $75M |
| 5 | Full specialty coverage; point-of-care PA via ambient-documentation integrations | National; MSO/PE roll-up channel; payer auto-approval partnerships | 90/28/70/110/80/52 = 430 | **$160M** |

Path to $200M ARR extends into Year 6 via the commercial/ERISA book, contingent on ASO administrators voluntarily extending APIs built for CMS compliance.

## 5. Financial Model

| Year | ARR | Growth % | GM % | COGS | S&M | R&D | G&A | EBITDA | Cash Burn | Cumulative Capital Required |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | $2M | — | 55% | $0.9M | $1.7M | $1.7M | $1.2M | ($3.5M) | ($3.5M) | $3.5M |
| 2 | $7M | 250% | 62% | $2.7M | $4.9M | $3.9M | $2.1M | ($6.6M) | ($6.6M) | $10.1M |
| 3 | $28M | 300% | 68% | $9.0M | $14.0M | $7.8M | $5.0M | ($7.8M) | ($7.8M) | $17.9M |
| 4 | $75M | 168% | 72% | $21.0M | $33.8M | $15.0M | $10.5M | ($5.3M) | ($5.3M) | $23.2M (peak) |
| 5 | $160M | 113% | 75% | $40.0M | $64.0M | $28.8M | $19.2M | +$8.0M | +$8.0M | $15.2M net |

**Unit economics:** Blended CAC ≈ $400K; blended LTV ≈ $3.07M (8yr life × 72% GM × $533K ACV) → **LTV:CAC 7.7:1**; payback ≈ 1.04 years. Copilot-only cohorts are markedly weaker — $300K ACV → LTV $1.68M, **4.2:1**, 1.9-year payback — and the model depends on those customers upgrading to ~$600K full-automation ACVs once a payer's API goes live; upgrade rate should be a tracked board metric.

**Cost of legal mitigations (cumulative, Y1–Y5):** ~$21.7M compliance-ops payroll, ~$4.8M specialty liability insurance (1.75% of revenue), ~$1.8M for compliance officer/counsel/FTO/licensure survey/HITRUST — roughly **$28M direct**, plus **$106M of cumulative ARR foregone** (v1's $378M cumulative ARR vs. v2's $272M) from killing scraping and "denial-proof" positioning.

**Funding plan:** Modeled P&L burn peaks at $23.2M (end of Y4), but realistic total capital required — accounting for round-sizing buffers, 60–90-day hospital AR timing, copilot-mode margin risk, and the compliance build — is **~$140–150M**, up from v1's ~$123M. Finance recommends sizing rounds to $150M with the Series B tranche gated on demonstrated copilot-to-automation conversion ≥40% within 12 months of a payer's API going live.

## 6. Legal Risk Assessment

| # | Risk | Severity | Status (v2) | Mitigation |
|---|---|---|---|---|
| L1 | CMS mandate excludes ERISA commercial plans — original "why now" mismatch | Fatal (v1) | Mitigated | Beachhead re-aimed at MA/Medicaid/QHP payers actually bound by CMS-0057-F; commercial treated as upside |
| L2 | CPOM/UR licensure exposure | Serious | Mitigated | Clinician attestation + Year-1 state-by-state licensure survey, completed before multi-state GTM |
| L3 | Portal scraping breaches ToS, risks CFAA claims | Serious/Fatal Yrs 1–2 | Resolved | Scraping eliminated; X12 278 clearinghouse rail + copilot mode (customer submits under own credentials) |
| L4 | Patient-harm liability exceeds SaaS caps/E&O coverage | Serious | Mitigated | Specialty managed-care E&O from Y1 (1.5–2% of revenue); attestation shifts standard-of-care locus to provider |
| L5 | "Denial-proof" design creates False Claims Act exposure | Fatal (v1) | Mitigated | Reframed to "complete-and-accurate"; provenance-linked citations, clinician attestation, Y1 compliance officer; win-rate guarantee killed |
| L6 | Data-flywheel moat has no legal protection | Serious | Mitigated | FTO analysis + provisional patents in Y1; moat conceded to be commercially weaker |
| L7 | BAA chains block cross-customer model training | Serious | Mitigated | Per-customer adaptation; flywheel rebuilt on non-PHI payer-knowledge artifacts |
| L8 | State consumer-health-data laws (e.g., WA MHMDA) | Manageable | Resolved | Staffed and priced into compliance headcount |
| L9 | Epic/Cerner vendor gatekeeping | Serious | Mitigated | Multi-rail design (FHIR + clearinghouse) so no single vendor approval is load-bearing |
| L10 | Payers can countermeasure an approval-maximizing agent | Serious | **Still open** — entrepreneur's rebuttal evaluated and rejected in part | Rate-limit terms negotiated into payer connectivity agreements; structural incentive conflict remains and now flows through payer-owned rails (see N3) |
| L11 | Enterprise buyers demand indemnification, inverting SaaS liability caps | Manageable | Resolved | Accepted as cost of doing business, priced in |
| N1 | Medicaid/MA program-integrity regime (new) | Serious, new | Open | Beachhead trades ERISA exposure for the most heavily policed payer segment (FL/TX active Medicaid fraud enforcement); requires Medicaid-specific compliance program |
| N2 | Attestation is now the single load-bearing control (new) | Serious, new | Open | UX must force genuine engagement (surface contradicting evidence, audit sampling, dwell-time monitoring); contracts must obligate real review |
| N3 | Payer-owned clearinghouse rail dependency (new) | Manageable, new | Open | Multi-rail redundancy should be contractual, not aspirational |

## 7. Debate Log

v1's thesis assumed CMS's 2026–2027 interoperability mandate would force broad payer API access and pitched a "denial-proof submission" product sized at $200M Year-5 ARR (400 customers × $500K ACV) funded by ~$123M. Legal flagged three Fatal defects: the mandate actually excludes ERISA self-funded commercial plans — the dominant payer type for large hospital systems — making the "why now" a mismatch (L1); "denial-proof" positioning was a textbook False Claims Act magnet (L5); and the Year 1–2 roadmap structurally depended on portal scraping before APIs existed, risking CFAA and ToS claims (L3). Finance separately found the plan's 6x revenue-per-employee efficiency gain unexplained and undersized compliance-ops relative to auth volume.

Entrepreneur v2 responded by re-aiming Years 1–3 at the MA/Medicaid/QHP beachhead the mandate actually covers (FL/AZ/TX), replacing "denial-proof" with "complete-and-accurate first submission" built on verbatim provenance-linked citations and mandatory clinician attestation, and eliminating scraping entirely in favor of X12 278 clearinghouse rails plus a new "copilot mode" where customer staff submit under their own credentials. These changes cut Year-5 ARR from $200M to $160M and pushed capital need from ~$123M to ~$150M, with headcount rising from 241 to 430 (adding a G&A/compliance column entirely absent from v1).

Legal v2 accepted that all three Fatal defects are cured and most Serious objections are Mitigated or Resolved, but rejected the entrepreneur's L10 rebuttal in part: even an honest, complete submission still raises payer medical spend by increasing approval rates, so payers retain a structural incentive to throttle or countermeasure the product regardless of intent — legal kept L10 at "Still open," not Mitigated. Legal also introduced three new risks from the pivot itself (N1–N3), most notably that clinician attestation is now a single point of failure underpinning three separate legal shields (CPOM, FCA, malpractice) simultaneously, and that the product's own "time saved" value proposition creates commercial pressure toward the rubber-stamping that would collapse it.

## 8. Verdict

**Entrepreneur:** A smaller, slower, legally honest company beats a larger fictional one — the pivot is the right trade and $160M ARR remains venture-scale.

**Finance:** Fundable with conditions — LTV:CAC of 7.7:1 and ~12.5-month payback survive the revision, but the model re-accelerates entirely on one external event (CMS-0057-F APIs shipping usably in Jan 2027) that the company does not control.

**Legal:** Structurally sound after curing all three Fatal defects, but concentrated — nearly every remaining serious risk now rests on a single control (genuine clinician attestation), the beachhead sits in the most heavily policed program-integrity environment in US healthcare, and payer countermeasure incentives remain structurally open (L10).

**Overall: GO, conditional.** The v1→v2 revision converted three potentially fatal legal defects into a monitorable risk profile without breaking unit economics, but the board should gate Series B on demonstrated copilot-to-automation conversion, require quarterly evidence that attestation is genuine (not rubber-stamped), and treat the Jan 2027 API mandate timeline as a named, tracked external dependency rather than an assumption.
