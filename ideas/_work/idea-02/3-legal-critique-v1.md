# ClearPath Health — Legal & Regulatory Critique v1

## 1. Regulatory & Licensing

**L1 (FATAL) — The "why now" is a mismatch between the mandate's scope and the target payer mix.** Sec. 1 says Year-1 integrates "the five payers covering the largest share of a typical hospital's *commercial* + Medicare Advantage mix," and the Moat section (Sec. 4, #2) bets that ePA becomes "CMS-mandated infrastructure." CMS-0057-F's Prior Authorization API mandate (compliance Jan. 1, 2027) binds MA plans, Medicaid/CHIP FFS and managed care, and ACA exchange QHPs — it does **not** reach self-funded ERISA commercial plans, which are the dominant payer type for large hospital systems. The plan's own Risk #1 frames this as payers "slow-walking compliance"; the real problem is worse — most of the commercial book is never in scope at all, no matter how compliant payers are.

**L2 (SERIOUS) — Corporate-practice-of-medicine / utilization-review licensure.** Sec. 1 describes agents that "match [evidence] against payer medical-necessity policy" and "auto-draft appeals with citations." Several states license "private review agents"/UR entities and restrict non-clinicians from making medical-necessity determinations. If ClearPath's software effectively decides what counts as sufficient clinical justification (not merely routes documents), plaintiffs' counsel and state regulators have a colorable theory that ClearPath is performing UR or CPOM-adjacent functions without licensure — a state-by-state compliance burden entirely absent from the 5-year plan (Sec. 3).

**L3 (SERIOUS, verging on FATAL for Years 1–2) — Payer portal Terms of Service and CFAA exposure.** The plan's own Risk #1 admits agents will "degrade to portal-scraping" before/absent real APIs. Payer portals' ToS routinely prohibit automated/bot access. Scraping in the face of a ToS ban risks contract termination of the hospital-customer's own portal credentials (crippling the very workflow ClearPath sells) and potential Computer Fraud and Abuse Act "exceeds authorized access" claims. Since ePA APIs are not required until Jan. 1, 2027 (L1), **the entire Year 1–2 roadmap ($3M→$15M ARR, Sec. 3) structurally depends on the riskiest, least-defensible access method.**

## 2. Liability

**L4 (SERIOUS, one incident from FATAL) — Patient-harm exposure the plan itself flags but underweights.** Sec. 5 Risk #2 concedes "one high-profile wrong submission" could be catastrophic. Standard SaaS liability caps (typically 1x fees) do nothing against a patient's direct tort suit against the hospital, which will then seek full indemnification/contribution from ClearPath. Tech E&O policies commonly exclude bodily-injury/"medical" claims, meaning ClearPath likely needs specialty coverage it hasn't budgeted for, and a single adverse outcome (delayed oncology care from a bad submission) is a wrongful-death-adjacent claim, not a capped software dispute.

**L5 (FATAL) — False Claims Act exposure is designed into the product, not incidental.** Sec. 1's "denial-proof submission" framing and "matching payer policy criteria line-by-line" describes optimizing submissions to pass payer gatekeeping rather than neutrally representing clinical fact. If the model selectively emphasizes or fabricates supporting evidence to secure approval for care later billed to Medicare/Medicaid, that is a textbook FCA "false statement material to a false claim" theory — with treble damages, per-claim penalties, qui tam relators (disgruntled UM staff, competitors), and potential exclusion from federal programs. The Year-5 "appeals win-rate guarantee program" (Sec. 3, Year 5) compounds this: guaranteeing outcomes creates a KPI that directly incentivizes gaming submissions.

## 3. IP

**L6 (SERIOUS) — The claimed moat is not legally defensible.** Sec. 4's Moat #1 ("evidence-assembly accuracy data flywheel") is an accumulated-data advantage, not IP — there is no patent, copyright, or trade secret protecting it, and incumbents Cohere Health (12M+ auths/yr) and Rhyme (4M+ auths/yr, cited in Sec. 4) already have a multi-year, multi-order-of-magnitude data head start. Nothing stops them from replicating the flywheel faster. Freedom-to-operate risk also runs the other way: this is an actively, heavily funded patent-filing category (Cohere's $90M Series C, per Sec. 4), and ClearPath has done no FTO analysis.

## 4. Data & Privacy

**L7 (SERIOUS) — BAA chain complexity is unaddressed and will slow or block the moat.** The product (Sec. 1) touches Epic/Cerner/athenahealth, payer channels, and (implicitly) LLM infrastructure — each requires a BAA, and hospital compliance teams routinely refuse BAA language permitting cross-customer reuse of PHI-derived data to train a shared model. That refusal directly guts Moat #1's flywheel: sophisticated hospital-system legal teams will not casually authorize their patients' data to also improve a competitor's ClearPath account.

**L8 (MANAGEABLE) — State health-data privacy laws add compliance surface.** Washington's My Health My Data Act and similar state consumer-health-data statutes impose consent and (for WA) private-right-of-action exposure beyond HIPAA. Addressable with counsel, but the 5-year plan's compliance-ops headcount (Sec. 3: 2→20 heads) is likely undersized for this plus L2/L7 combined.

## 5. Structural/Commercial

**L9 (SERIOUS) — EHR vendor gatekeeping is a single point of failure treated as an engineering task.** Sec. 3's Year 1 milestone ("Epic + 5-payer ePA integration") is presented as a build item, but Epic App Orchard and Cerner Code impose vendor-approval, data-use, and revenue-share terms and can revoke access unilaterally. Epic in particular has a track record of restricting third parties whose products compete with or route around Epic's own workflow tools.

**L10 (SERIOUS) — Payers have every incentive to countermeasure an adversarial optimizer.** ClearPath's product is explicitly designed to convert more submissions into approvals (Sec. 1, "denial-proof"), which is directly adverse to payer loss ratios. Payers can throttle API rate limits, amend portal ToS, or fingerprint and deny automation-pattern submissions — commercial/legal countermeasures the plan does not model as a risk to unit economics distinct from Sec. 5 Risk #3 (denial-rate compression).

**L11 (MANAGEABLE) — Contractual liability caps will be renegotiated against ClearPath, not for it.** Sophisticated hospital-system buyers will demand mutual indemnification for third-party claims (patients, regulators) arising from ClearPath's auto-submissions, inverting the standard SaaS liability-cap protection the entrepreneur's model implicitly relies on for margin predictability.

## Summary Table

| # | Objection | Severity |
|---|---|---|
| L1 | CMS ePA mandate excludes ERISA commercial plans — "why now" thesis mismatched to target payer mix | Fatal |
| L2 | Evidence-matching/appeal-drafting risks CPOM/UR licensure exposure, state-by-state | Serious |
| L3 | Pre-2027 reliance on portal scraping breaches payer ToS, risks CFAA claims and credential termination | Serious/Fatal (Yrs 1–2) |
| L4 | Patient-harm liability from wrong submissions exceeds SaaS liability caps and likely E&O coverage | Serious (one incident from Fatal) |
| L5 | "Denial-proof" submission design creates direct False Claims Act exposure, incl. qui tam risk | Fatal |
| L6 | Claimed data-flywheel moat has no legal protection; incumbents have a larger data head start | Serious |
| L7 | Multi-party BAA chains will block cross-customer model training the moat depends on | Serious |
| L8 | State consumer-health-data laws (e.g., WA MHMDA) add unbudgeted compliance surface | Manageable |
| L9 | Epic/Cerner vendor terms are a unilateral, revocable gatekeeper treated as an engineering task | Serious |
| L10 | Payers can legally/contractually countermeasure an approval-maximizing automation agent | Serious |
| L11 | Enterprise buyers will demand indemnification that flips standard SaaS liability protections | Manageable |
