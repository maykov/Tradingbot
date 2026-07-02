# GridPilot — Legal & Regulatory Critique v1

*Reviewer: outside counsel, adversarial mandate. Basis: entrepreneur's plan §§1–5.*

## 1. Regulatory & licensing

**L1 (Fatal) — The core wedge feature is likely illegal in most markets as described.** §1 markets "continuously re-optimizes bids across stacked programs (ISO wholesale energy/ancillary services **+ utility DR**) in a single site" as the flagship differentiator. Order 2222 and virtually every utility DR tariff contain anti-double-dip / dual-participation prohibitions: a site cannot be paid twice for the same MW in a wholesale program and a retail/utility program without real-time, auditable de-confliction (telemetry-verified "opt-out" logic per event). The plan describes this stacking as a selling point, not a compliance-engineering problem, and budgets no legal/M&V function to build the de-confliction layer every ISO and utility will demand before certifying it. Until solved, the flagship feature cannot be sold as pitched in states where the local utility runs a competing DR tariff.

**L2 (Serious) — ERCOT is not FERC-jurisdictional; citing it as an Order-2222 market is a legal error baked into the GTM plan.** §3 lists CAISO **and ERCOT** as Year-1 (2027) launch markets under the banner of "ISO aggregator certification" for the "FERC Order 2222-compliant" bidding engine (§1). ERCOT is intrastate and outside FERC's jurisdiction — Order 2222 does not apply there. Any ERCOT DER-aggregation product must be built against ERCOT's own, separately-evolving (and non-FERC-mandated) rules, which have no guaranteed timeline or scope parity with CAISO's. Launching both markets in Year 1 under one compliance framework misstates the regulatory landscape to investors and will surprise the ops team with a second, unrelated rulemaking track.

**L3 (Serious) — Order 2222 timelines are materially later than the plan's own milestones.** §3's Year-2 (2028) milestone assumes PJM and NYISO are live; §3's Year-3 (2029) assumes MISO and ISO-NE are live. Public compliance-filing trackers show PJM's aggregation resources are not slated to participate in capacity auctions until the 2028/29 BRA (held mid-2026) with wholesale energy/AS participation lagging further, and MISO's implementation date is June 2029 — the same year the plan needs MISO revenue flowing, leaving zero buffer. §5's own Risk #1 concedes this is "the single riskiest assumption," but the ARR table (§3) treats the optimistic case as the base case rather than risk-adjusting it.

**L4 (Serious) — Market-participant/power-marketer registration and collateral are unbudgeted.** To bid energy (not just capacity/AS), GridPilot likely needs FERC market-based rate authority and must post ISO creditworthiness collateral scaled to bid volume. Nothing in the 5-year headcount table (§3, "Ops-G&A") or the revenue-share economics (§2) reserves working capital for posted collateral, which grows with enrolled MW and could be a multi-million-dollar cash drag well before ARR catches up.

**L5 (Manageable) — State PUC opt-outs.** Order 2222 lets states/utilities restrict retail-customer aggregation in some RTO footprints. This narrows SAM (§2) rather than killing the model — fixable by re-scoping TAM/SAM per state, but the plan currently treats all six ISO footprints as uniformly open.

## 2. Liability

**L6 (Serious) — Asymmetric non-performance exposure.** Capacity markets (e.g., ISO-NE Pay-for-Performance) impose penalties on underdelivery that can exceed the clearing payment itself. GridPilot, as the registered aggregator, is the ISO's counterparty of record — the ISO collects from GridPilot, not from the individual battery owner whose asset happened to be offline. §1's "20–30% share of market revenue" model describes only the upside split; nothing in §1–§3 allocates downside penalty risk back to the thousands of small site-hosts whose non-performance caused it. Unless every enrollment contract contractually passes penalties through (hard to enforce against small C&I owners with limited balance sheets), GridPilot absorbs uncapped tail risk against a capped revenue share.

**L7 (Serious) — Revenue-promise consumer-protection exposure.** §1's marketing language ("get paid weekly, see your revenue-share split live") is a revenue promise to non-sophisticated asset owners sold largely through white-label installer channels (§1, §4). Solar/storage marketing litigation (state UDAP claims, FTC scrutiny of savings guarantees) shows this fact pattern draws class actions the moment realized payouts diverge from marketed projections — a near-certainty given §5's own admission that per-MW market value is volatile.

**L8 (Manageable) — Grid-event/equipment-damage liability.** Remote dispatch of batteries/HVAC creates ordinary product-liability and negligence exposure if a control action damages equipment or causes a site outage. Addressable via standard insurance and indemnification clauses, but currently unmentioned in the plan.

## 3. IP

**L9 (Serious) — No freedom-to-operate analysis against a patent-heavy field.** §4 names CPower, Voltus, and Leap/Enel X as competitors and Tesla is called out in the market-sizing sources (§2) as a major VPP player, yet nowhere does the plan budget an FTO study. Tesla (Autobidder), AutoGrid/Uplight, and Stem hold optimization/dispatch patents in this exact space. The claimed moat of a "multi-market bidding-optimization model" (§4, moat #1) is precisely the kind of algorithm most likely to read on existing claims.

**L10 (Manageable) — "Registration/certification moat" is not IP and is overstated.** §4's moat #3 (ISO certification lead time) is a regulatory queue position, not an exclusive or legally defensible barrier — any funded competitor can run the same 6–12 month process in parallel. Framing it as a "moat" comparable to the data/lock-in moats is a diligence red flag, not a fatal defect.

## 4. Data & privacy

**L11 (Serious) — Meter/telemetry data ownership is unaddressed.** Interval meter data is typically owned/controlled by the utility and customer, not the aggregator, and requires per-utility, customer-authorized data-sharing agreements (Green Button/DGA-style rules) that vary by state. The "<30-day integration" wedge promise (§1) and the "data network effects" moat (§4, moat #1) both presuppose frictionless telemetry access that does not legally exist yet in most jurisdictions.

**L12 (Serious) — Cybersecurity/CIP exposure from remote dispatch is unbudgeted.** A platform that remotely controls distributed batteries, EV chargers, and building HVAC at grid scale is a plausible NERC CIP-adjacent attack surface; a compromise triggering coordinated device action is a reliability incident, not just a data breach. No security/compliance function appears in the Year 1–2 headcount (§3).

## 5. Structural/commercial legal risks

**L13 (Fatal) — Market-manipulation/baseline-gaming enforcement risk.** Automated, continuously re-optimizing bidding across stacked programs (§1) sits squarely in FERC's historical enforcement focus: DR "baseline manipulation" (inflating the counterfactual usage baseline to overstate delivered curtailment) is the single most litigated DR-fraud theory at FERC, with penalties including disgorgement and market-participation bans — a corporate death sentence for an aggregator whose entire business is market access. The plan has no compliance-monitoring or algorithmic-audit function anywhere in §3's headcount plan.

**L14 (Serious) — Internal inconsistency between certification timeline and Year-1 revenue.** §4 touts 6–12 month ISO certification as a competitive moat, yet §3 projects $1.5M ARR live in CAISO/ERCOT within calendar Year 1 — the certification process alone could consume most of that year.

**L15 (Serious) — Thousands of small counterparty contracts.** §3's Year-5 target of ~1,800 sites means standardized, low-touch revenue-share agreements with small owners — high aggregate enforcement/breach/bankruptcy-workout cost that scales with headcount the plan doesn't provision for (legal/collections function absent from §3's org table).

**L16 (Manageable) — Capacity-market reform risk.** §5's Risk #2 already flags falling per-MW value; ongoing capacity-auction reform proceedings (e.g., ISO-NE's 2026 reforms) could specifically restructure how aggregated/subsidized resources clear, but this is a revenue-model risk the plan already partially acknowledges and can be mitigated by diversifying across ISOs/products.

## Summary Table

| # | Objection | Category | Severity |
|---|---|---|---|
| L1 | Stacked wholesale+utility DR bidding likely violates dual-participation rules | Regulatory | Fatal |
| L2 | ERCOT wrongly treated as an Order 2222/FERC market | Regulatory | Serious |
| L3 | Order 2222 ISO timelines lag the plan's ARR milestones | Regulatory | Serious |
| L4 | Market-participant registration/collateral costs unbudgeted | Regulatory | Serious |
| L5 | State PUC opt-outs shrink addressable SAM | Regulatory | Manageable |
| L6 | Asymmetric non-performance/penalty exposure | Liability | Serious |
| L7 | Consumer-protection exposure on revenue promises | Liability | Serious |
| L8 | Grid-event/equipment-damage liability | Liability | Manageable |
| L9 | No freedom-to-operate analysis vs. patent-heavy incumbents | IP | Serious |
| L10 | "Certification moat" is not real IP protection | IP | Manageable |
| L11 | Telemetry/meter data ownership and access rights unresolved | Data/Privacy | Serious |
| L12 | No CIP/cybersecurity function for grid-connected control | Data/Privacy | Serious |
| L13 | Bidding-algorithm baseline gaming = FERC enforcement/market-ban risk | Structural | Fatal |
| L14 | Certification-time moat contradicts Year-1 revenue timeline | Structural | Serious |
| L15 | Legal/collections burden of thousands of small contracts unstaffed | Structural | Serious |
| L16 | Capacity-market reform could erode per-MW value further | Structural | Manageable |
