# ClearPath Health — Legal Review v2 (Response to Entrepreneur v2)

## 1. Objection-by-Objection Status

**L1 (was Fatal) — ERISA gap in mandate thesis: MITIGATED.** The MA/Medicaid/QHP beachhead (v2 §1, §4) fixes the legal mismatch: the thesis now stands on payers actually bound by CMS-0057-F, and the SAM is honestly cut to ~$10B. Not Resolved, because (a) the $75M→$160M Y4–Y5 ramp (v2 §3) still leans on commercial/ERISA expansion via *voluntary* payer API extension — the entrepreneur's "one intake stack" rebuttal is plausible payer economics but is a bet, correctly reclassified as upside; and (b) MA/Medicaid-heavy providers are thinner-margin buyers, which pressures the $533K blended ACV assumption. The legal flaw is cured; a market-risk residue remains.

**L2 (Serious) — CPOM/UR licensure: MITIGATED.** Clinician attestation plus a Year-1 licensure survey and registration where counsel advises (v2 §1) is the right structure. Residual: several states define "private review agent" broadly enough to capture entities that *prepare* medical-necessity documentation, and the attestation shield only holds if attestation is real review (see N2). Survey must be complete before multi-state GTM, not parallel to it.

**L3 (was Fatal Yrs 1–2) — Portal scraping/ToS/CFAA: RESOLVED.** Scraping is off the roadmap; X12 278 via clearinghouses is a sanctioned, decades-old rail, and copilot mode with customer staff submitting under their own credentials eliminates the CFAA/ToS theory. The exposure I identified no longer exists. Cost: the rail dependency creates N3.

**L4 (Serious) — Patient-harm liability: MITIGATED.** Specialty managed-care E&O from Year 1 and attestation shifting the standard-of-care locus (v2 §1) are correct moves. Residual: 1.5–2% of revenue is an optimistic premium **assumption** for an unproven AI clinical-documentation vendor; ClearPath will still be named in every suit regardless of attestation; and insurance transfers loss, not reputational collapse (v1 Risk #2 still stands commercially).

**L5 (was Fatal) — FCA exposure: MITIGATED, no longer Fatal.** Killing "denial-proof" and the win-rate guarantee, provenance-linked verbatim citations, clinician attestation, and a Year-1 compliance officer (v2 §1) remove the *designed-in* exposure. Two residuals keep this open at Serious: (a) **selection is assertion** — verbatim citations prevent fabrication but not cherry-picking; an agent that systematically includes supportive chart elements and omits contradicting ones still makes a materially misleading submission, and the architecture as described does not prevent that; (b) the whole shield depends on attestation being genuine (N2). A written selection-completeness policy (contradicting evidence must be surfaced to the attesting clinician) should be a product requirement.

**L6 (Serious) — Moat not legally defensible: MITIGATED.** FTO analysis and provisional filings in Year 1 address the legal exposure; the concession that the flywheel is not IP is accurate. The rebuttal that Cohere's payer-side data is not a substitute dataset is fair but narrow — Rhyme's provider-side data is. Legally cured; commercially the moat is now admitted to be weaker (v2 §1 L7 response), which is the finance team's problem, not mine.

**L7 (Serious) — BAA/training conflict: MITIGATED.** Per-customer adaptation plus a non-PHI payer-knowledge flywheel is the legally correct architecture. Residual: sophisticated systems increasingly prohibit *even de-identified* commercialization by contract, and the Y3 "de-identified benchmarking product" (v2 §3) walks straight back into that negotiation. Expect the expert-determination path to be contested account-by-account.

**L9 (Serious) — EHR gatekeeping: MITIGATED.** The information-blocking rebuttal is partially valid — the Cures Act constrains Epic's ability to block legitimate access, and OIG enforcement now has teeth — but exceptions (security, fees) give Epic ample lawful friction. The real fix is the multi-rail design (FHIR + clearinghouse) so no single approval is load-bearing. Accepted.

**L10 (Serious) — Payer countermeasures: STILL OPEN.** The rebuttal is evaluated and rejected in part. It is true that "complete-and-accurate" is less adversarial than "denial-proof," and clean submissions do cut payer review cost. But the rebuttal assumes PA friction exists to verify documentation. It also exists to *deter utilization*: a tool that raises approval rates and automates appeals raises payer medical spend even when every submission is honest. Payers therefore retain the incentive to throttle rate limits, tighten criteria, or migrate review to steps ClearPath can't automate (peer-to-peer calls). Negotiated rate-limit terms help; the incentive conflict is structural and now runs through payer-owned rails (N3). Severity remains Serious, though the *legal* attack surface is much reduced.

**L8, L11 (Manageable) — RESOLVED.** Accepted, staffed, and priced in (v2 §1, §2.7).

## 2. New Issues Introduced by the Pivot

**N1 (Serious) — Medicaid/MA program-integrity regime.** The beachhead pivot trades ERISA exposure for the most heavily policed payer segment: state False Claims Act analogs (some with lower scienter thresholds), Medicaid Fraud Control Units, RAC/UPIC audits, and MCO contract flow-down obligations. FL and TX — two of the three named beachhead states — have among the most active Medicaid fraud enforcement programs in the country. The compliance program must be Medicaid-specific from day one, not generic FCA training.

**N2 (Serious) — Attestation is now the single load-bearing control.** Clinician attestation is the answer to L2, L4, and L5 simultaneously. If it degrades into click-through rubber-stamping — which the product's own value proposition ("time saved," v2 §1 L5(e)) economically pressures it toward — all three shields fail at once, and plaintiffs will argue ClearPath *knew* review was perfunctory. Mitigation: attestation UX must force engagement (e.g., surfacing contradicting evidence, random audit sampling, dwell-time monitoring), and contracts must obligate customers to maintain genuine review.

**N3 (Manageable) — Payer-owned rail dependency.** The L3 fix routes Years 1–2 through Availity (payer-owned) and Change/Optum (UnitedHealth-owned). The countermeasure surface from L10 relocates here: rail owners can impose terms, fees, or throttling on a vendor whose product raises payer costs, and the Change Healthcare breach precedent makes single-rail dependency a BAA/business-continuity issue. Multi-rail redundancy should be contractual, not aspirational.

## 3. Residual-Risk Summary (for the Board)

The v2 plan cures all three Fatal defects: the mandate thesis now targets payers the mandate actually covers, the FCA-magnet "denial-proof" positioning is dead and replaced with a provenance-and-attestation architecture, and portal scraping is eliminated in favor of sanctioned rails. What remains is a structurally sound but concentrated risk profile: nearly every serious residual — CPOM, FCA, malpractice — now rests on a single control (genuine clinician attestation) whose integrity the product's own efficiency pitch erodes; the beachhead sits in the most aggressively policed program-integrity environment in US healthcare; and payer countermeasure incentives survive the reframe and now flow through payer-owned clearinghouse rails. None of this is fatal; all of it is monitorable. The board should require quarterly evidence that attestation is real (audit sampling metrics), a completed multi-state UR-licensure survey before national expansion, and Medicaid-specific compliance certification before the FL/TX launches.

## 4. Status Table

| # | Objection | Original Severity | v2 Status |
|---|---|---|---|
| L1 | ERISA gap in CMS-mandate thesis | Fatal | Mitigated |
| L2 | CPOM/UR licensure | Serious | Mitigated |
| L3 | Portal scraping / ToS / CFAA | Serious/Fatal (Yrs 1–2) | Resolved |
| L4 | Patient-harm liability | Serious | Mitigated |
| L5 | FCA exposure by design | Fatal | Mitigated |
| L6 | Moat not legally defensible | Serious | Mitigated |
| L7 | BAA chains vs. training flywheel | Serious | Mitigated |
| L8 | State health-data privacy laws | Manageable | Resolved |
| L9 | EHR vendor gatekeeping | Serious | Mitigated |
| L10 | Payer countermeasures | Serious | Still open |
| L11 | Liability-cap inversion | Manageable | Resolved |
| N1 | Medicaid/MA program-integrity regime | Serious (new) | Open |
| N2 | Attestation as single load-bearing control | Serious (new) | Open |
| N3 | Payer-owned clearinghouse rail dependency | Manageable (new) | Open |
