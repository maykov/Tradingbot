# RoboCrew — Business Plan v1

## 1. Product & value proposition

RoboCrew is a robotics-as-a-service (RaaS) marketplace for mid-market warehouse operators and 3PLs. We vet and bundle third-party robot hardware (AMRs from vendors like Locus Robotics-class fleets, picking arms, sortation), finance the equipment off our customers' balance sheets, handle integration with existing WMS/WCS systems, and bill per task (per pick, per pallet move, per hour) instead of per robot.

**Customer:** operations directors and CFOs at 3PLs and mid-market distributors (50–500 employees, 50K–500K sq ft) who want automation ROI but cannot justify a $2–10M capex project, a 12-month integration timeline, or the in-house engineering team needed to run a multi-vendor robot fleet.

**Year-1 wedge feature:** a vendor-agnostic orchestration layer ("RoboCrew OS") that lets a single warehouse run AMRs and picking arms from different OEMs under one task queue, one dashboard, and one bill — deployed in under 30 days with zero upfront capex. The wedge is not the robots (commoditizing per the brief) but the *financed, unified, fast-to-deploy bundle*: we underwrite the equipment lease, integrate it, and guarantee a per-task price, so a mid-market operator can turn on automation like a utility.

## 2. Market sizing

**TAM (top-down, cited):** Global warehouse automation market = $27.4B (2026) growing to $59.5B (2030) at 18.7% CAGR — Grand View Research, *Warehouse Automation Market Size Report 2024–2030* (grandviewresearch.com). We treat $59.5B (2030) as directional TAM ceiling for hardware+software+services.

**SAM (bottom-up):**
- US third-party logistics businesses: 72,937 (IBISWorld, *Third-Party Logistics in the US*, 2024).
- **Assumption:** ~15% of these (10,940) are "mid-market" facilities (50–500 employees, 50K–500K sq ft) — big enough to need automation, too small to run an in-house robotics program.
- **Assumption:** an equal-sized pool of non-3PL mid-market distribution operators (retail, manufacturing, wholesale DCs) adds ~11,000 more facilities.
- Total addressable facilities in North America ≈ **22,000** (assumption, built from the IBISWorld base).
- **Assumption:** average addressable RaaS + financing + orchestration spend per facility = **$400K/yr** (blended AMR + picking-arm + platform fee; anchored to Locus Robotics' publicly described enterprise RaaS deals of $500K–$2M/yr at large sites, scaled down for mid-market volume — Locus Robotics RaaS overview, locusrobotics.com).
- **SAM = 22,000 facilities × $400K = $8.8B/yr.**

**SOM (year 5):** 500 customer warehouses × $400K average ARR = **$200M**, or 2.3% penetration of SAM — consistent with a services company 5 years post-launch in a market still under 20% automated.

## 3. 5-year plan

**Asset ownership & capex financing:** RoboCrew never carries robots on its own balance sheet. Equipment is purchased by a bankruptcy-remote financing SPV, capitalized with (a) OEM revenue-share/vendor financing (robot makers subsidize placement to win volume), and (b) a warehouse-equipment-backed debt facility from a specialty lender (structure modeled on equipment-as-a-service lessors). RoboCrew is the servicer/orchestrator, earning a marketplace + software margin on top of the SPV's lease payments; customers sign a per-task services contract, not a robot lease, so capex never appears on their books either.

| Year | Product milestones | GTM motion | Headcount (by function) | Geography | Target ARR |
|---|---|---|---|---|---|
| 1 | RoboCrew OS MVP: multi-vendor task orchestration, billing engine, 3 OEM integrations | Founder-led sales, 10–15 design-partner warehouses, SPV financing facility closed ($15M) | 25 (12 eng, 5 ops/deploy, 4 sales, 4 G&A) | US Midwest/Southeast logistics corridors | $3M |
| 2 | Predictive task-routing, WMS plug-ins (top 5 WMS), 6 OEM integrations | Inside sales + 3PL association channel partnerships | 70 (30 eng, 20 field ops, 12 sales, 8 G&A) | National US | $15M |
| 3 | Autonomous fleet rebalancing across facilities, self-serve ROI calculator, underwriting automation | Channel: co-sell with WMS vendors and equipment lessors; regional field ops teams | 160 (55 eng, 55 field ops, 30 sales, 20 G&A) | US + Canada; EU pilot (UK) | $50M |
| 4 | Cross-facility benchmarking/data product, dynamic per-task pricing, 12+ OEM integrations | Enterprise 3PL accounts (multi-site rollouts), EU GTM team | 280 (85 eng, 110 field ops, 55 sales, 30 G&A) | US, Canada, UK, Germany | $110M |
| 5 | RoboCrew OS as category standard; open API for OEMs to self-list | Land-and-expand into multi-site 3PL enterprise contracts; capital-markets scale-up of SPV | 420 (120 eng, 170 field ops, 90 sales, 40 G&A) | US, Canada, EU (UK/DE/NL), pilot APAC | **$200M** |

## 4. Competition & moat

1. **Locus Robotics** — the market leader in AMR RaaS, but sells single-vendor fleets directly to large enterprise DCs (Locus RaaS overview, locusrobotics.com); doesn't aggregate other OEMs or serve sub-scale mid-market accounts economically.
2. **Formic Robotics** — a RaaS/financing aggregator across industrial automation broadly, proving the "pay-per-use, we own the capex" model works, but is not warehouse-specialized and lacks a unified multi-robot orchestration layer for pick/pack workflows.
3. **Status quo system integrators** (Dematic, Honeywell Intelligrated, and regional SIs) — sell one-off, capex-heavy integration projects (12+ month timelines) with no ongoing per-task billing or multi-vendor flexibility.

**Moat:** (a) the financing relationship — once RoboCrew's SPV underwrites a facility's automation, switching means renegotiating equipment leases, a high-friction event; (b) the orchestration data asset — the more facilities and OEM combinations run through RoboCrew OS, the better our task-routing and underwriting models get, a network effect competitors starting later can't replicate quickly; (c) OEM channel lock-in — robot makers prefer a single integrated demand-aggregator over building their own financing and multi-vendor integration stacks.

## 5. Key risks

1. **Unit economics assumption:** we assume per-task margin after OEM revenue share, financing cost, and field-ops labor stays positive (~20%+ gross margin) at mid-market volumes. If mid-market facilities' task volume is too low/variable to amortize integration and financing costs, the per-task model doesn't clear — this is the single riskiest assumption, since it's unverified with only public comps, not our own operating data.
2. **Underwriting/credit risk:** the SPV financing structure assumes stable utilization and low customer churn/default. A downturn or a wave of mid-market 3PL bankruptcies could trigger defaults that freeze the debt facility, cutting off our ability to deploy new robots.
3. **Disintermediation risk:** if a major robot OEM (or Amazon-scale player) decides to offer its own financing + multi-vendor-style orchestration directly to mid-market customers, our "neutral aggregator" wedge collapses, since we own no proprietary hardware.

**Sources:** Grand View Research, *Warehouse Automation Market Size Report, 2024–2030* (grandviewresearch.com); IBISWorld, *Third-Party Logistics in the US — Number of Businesses* (ibisworld.com); Locus Robotics RaaS overview (locusrobotics.com).
