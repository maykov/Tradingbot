# SentinelAML — Legal Review v2 (response to entrepreneur v2)

Reviewing `4-entrepreneur-v2.md` against my L1-L14 (`3-legal-critique-v1.md`).

## 1. Objection-by-objection status

**L1 (Fatal) — examiner acceptance of ML suppression. MITIGATED.** Repositioning to
decision-support (v2 §1, L1 response) removes the specific objection: nothing is suppressed, a
human sees every alert, and validating a prioritization model is genuinely a lower SR 11-7 bar
than validating suppression. Not fully resolved, because the economic claim ("3-5x analyst
throughput") only materializes if analysts spend materially less time on low-ranked alerts —
which examiners can characterize as de facto reduced review. See N3.

**L2 (Serious) — SAR-draft confidentiality. RESOLVED — rebuttal accepted.** Their legal reading
is correct: §5318(g)(2) restricts disclosure of a SAR or its existence, not a bank's use of
service providers acting within its compliance function; interagency guidance permits outsourcing
BSA operational functions while responsibility stays with the bank, and vendor-hosted SAR/case
tooling (Verafin, Unit21, Oracle FCCM) is established, examined practice. My v1 framing
overstated this. The in-tenant hardening and cross-customer training exclusion make it moot.
I accept the rebuttal.

**L3 (Serious) — moat doesn't travel to UK/EU. MITIGATED.** EU deferred to Year 4 and made
non-load-bearing (v2 §1 L3, §3). The problem still exists in Year 4; it just no longer threatens
the plan's spine.

**L4 (Fatal) — liability exceeding contract value. MITIGATED.** With disposition authority
contractually and functionally retained by the bank, SentinelAML's posture matches how incumbent
AML vendors sell today with fee-based caps; E&O is budgeted. Residual: contract language does not
stop a bank (or its regulator's findings) from pursuing gross-negligence claims if
mis-prioritization contributes to a missed SAR, and "gross negligence" is an uncapped carve-out
in their own term sheet (v2 §1 L4(b)). Survivable, no longer structurally fatal.

**L5 (Manageable) — E&O affordability. RESOLVED.** $250k Year-1 premium budgeted (v2 §1 L5);
adequate for the revised decision-support risk profile.

**L6 (Fatal) — agentic auto-close. RESOLVED.** Removed from the roadmap entirely, with an
explicit commitment not to ship autonomous closure in the plan window (v2 §1 L6). Replacement
("one-click disposition") raises a lesser issue — see N3.

**L7 (Serious) — cross-customer data reuse. RESOLVED.** Single-tenant, per-customer models
trained only on that institution's data, in its environment (v2 §1 L9+L7). The illegal moat is
gone; the restated moat (switching costs, exam-readiness) is legally buildable.

**L8 (Serious) — no FTO/IP strategy. MITIGATED.** FTO review budgeted pre-Series A; defensive
filings planned; moat honestly restated as non-patent. Mitigated, not resolved, because the FTO
review has not happened — the freedom-to-operate question is still an open fact.

**L9 (Fatal) — consortium data pooling. RESOLVED.** The Year-5 consortium is cut. The 314(b)
facilitation replacement is legally coherent in principle (banks share with each other under the
safe harbor; SentinelAML is facilitator, not data owner) but carries its own constraints — see N2.

**L10 (Serious) — FCRA CRA exposure. MITIGATED.** Contractual and product prohibition on
credit/account-decision use is the right design, and counsel review is gated pre-launch. Residual
because a vendor cannot fully police downstream bank use of scores, and the boundary opinion
doesn't exist yet.

**L11 (Manageable) — GDPR Art. 22 / transfers. MITIGATED.** Deferred with EU entry to Year 4
(v2 §1). Deferral is not resolution, but timing is now appropriate.

**L12 (Serious) — third-party-risk / BSCA examination. MITIGATED.** Compliance/audit function
staffed from Year 1 scaling to 12 FTE, sales cycles lengthened to match (v2 §1 L12, §3). BSCA
examination exposure is inherent and cannot be resolved, only staffed for — this is now staffed for.

**L13 (Fatal) — caps vs. indemnity conflict. MITIGATED.** The conflict existed because the
product claimed decision authority; v2's decision-support posture plus market-standard carve-outs
matches how comparable vendors actually contract with banks. Residual: sophisticated bank legal
teams will still push for regulatory-loss indemnity, and each such negotiation is margin and
cycle-time risk — but it is now ordinary commercial friction, not a structural impossibility.

**L14 (Serious) — incumbent API dependence. RESOLVED.** Warehouse/file-based ingestion of
bank-owned data requires no incumbent cooperation (v2 §1 L14). Any residual data-latency/quality
issues are commercial, not legal.

## 2. New issues introduced by v2

**N1 (Manageable) — in-tenant/single-tenant deployment burden.** Deploying models and SAR
workflows inside each customer's environment shifts patching, access-control, and
change-management duties into 320 separate tenants. Vendor personnel access for model tuning must
satisfy GLBA Safeguards and bank access policies, and every model update inside a tenant can
retrigger that bank's SR 11-7 change validation. Legally sound, operationally expensive; the
50%→72% gross-margin revision (v2 §2.6) at least acknowledges the cost.

**N2 (Manageable) — 314(b) module scope discipline.** The safe harbor covers only sharing about
suspected money laundering/terrorist financing between *registered* institutions. The module must
enforce registration checks and scope limits; any drift toward general risk-signal sharing
quietly recreates L9. Needs a hard product-level guardrail, not just policy.

**N3 (Serious) — rubber-stamp risk in "one-click disposition."** If throughput rises 3-5x with a
named human clicking through machine-assembled dispositions, examiners and plaintiffs will ask
whether human review was meaningful. A pattern of seconds-per-alert closures converts the
decision-support posture (the fix for L1/L4/L13) back into de facto automation. Mitigable with
enforced review-depth telemetry and QA sampling — neither is currently in the plan.

## 3. Residual-risk summary

The board should worry less about legal show-stoppers — all five Fatals are resolved or credibly
mitigated — and more about the fragility of the fix: the entire liability and regulatory posture
now rests on the claim that a human meaningfully decides every alert. If sales pressure or
customer behavior turns "one-click disposition" into rubber-stamping (N3), L1, L4, and L13 all
reopen at once. Secondary worries: the FTO review and FCRA boundary opinion are budgeted but not
done; BSCA examination exposure scales with every bank signed; and the honest cost of the fixes
(ARR cut to $134M, GM cut, $65-70M raise) means the legal de-risking has been paid for in
plan economics rather than eliminated.

## 4. Status table

| # | Objection | v1 Severity | v2 Status |
|---|---|---|---|
| L1 | Examiner acceptance of ML suppression | Fatal | Mitigated |
| L2 | SAR-draft confidentiality | Serious | Resolved (rebuttal accepted) |
| L3 | Moat doesn't travel to UK/EU | Serious | Mitigated |
| L4 | Liability exceeds contract value | Fatal | Mitigated |
| L5 | E&O affordability | Manageable | Resolved |
| L6 | Agentic auto-close | Fatal | Resolved |
| L7 | Cross-customer data-reuse moat | Serious | Resolved |
| L8 | No FTO/patent strategy | Serious | Mitigated |
| L9 | Consortium data pooling | Fatal | Resolved |
| L10 | FCRA CRA exposure | Serious | Mitigated |
| L11 | GDPR Art. 22 / transfers | Manageable | Mitigated |
| L12 | Third-party-risk / BSCA exams | Serious | Mitigated |
| L13 | Caps vs. indemnity conflict | Fatal | Mitigated |
| L14 | Incumbent API dependence | Serious | Resolved |
| N1 | In-tenant deployment burden | — (new) | Manageable |
| N2 | 314(b) module scope discipline | — (new) | Manageable |
| N3 | Rubber-stamp risk in one-click disposition | — (new) | Serious |
