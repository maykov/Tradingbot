# ClearBorder — Finance Review v1

## 1. Financial Model (5-Year)

**Assumptions** (all labeled; overrides entrepreneur's implicit escalating margin — see note below):
- Fully-loaded comp (**assumption**): Eng/Product $180k; Trade/Compliance (licensed brokers + analysts — COGS labor) $130k; GTM $160k; G&A $150k. Headcount by year from entrepreneur Sec. 3.
- **Gross margin held to 45%→60%, not the ~80%+ the entrepreneur's plan implies.** Licensed-broker human sign-off (their own Risk #1) is a per-filing, revenue-proportional cost — this is a services-with-software-leverage business, not pure SaaS, until/unless regulators accept AI-only filing. COGS = Trade/Compliance labor + non-labor (cloud/AI inference, ABI/API connectivity, data) plugged to hit the assumed margin.
- R&D = (Eng+Product labor) × 1.15 (tools/infra, **assumption**). S&M = GTM labor × 1.30 (programs/marketing, **assumption**). G&A = G&A labor × 1.5 + a $0.3M/new-jurisdiction step-cost (legal, broker-license applications, bonds, **assumption**): Canada (Y2), UK+Germany+Netherlands (Y3, ×3), Mexico+broader EU (Y4, ×2), APAC (Y5).
- ARR ≈ revenue recognized in the year booked (simplifying **assumption**).

| Year | ARR ($M) | Growth % | GM % | COGS ($M) | S&M ($M) | R&D ($M) | G&A ($M) | EBITDA ($M) | Cash Burn ($M) | Cumulative Capital Req. ($M) |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 1.0 | n/a | 45% | 0.55 | 0.62 | 1.66 | 0.53 | **-2.36** | 2.36 | 2.4 |
| 2 | 12.0 | 1,100% | 48% | 6.24 | 2.50 | 4.14 | 0.98 | **-1.85** | 1.85 | 4.2 |
| 3 | 49.0 | 308% | 52% | 23.52 | 7.28 | 8.28 | 3.15 | **+6.77** | 0 | 4.2 |
| 4 | 126.0 | 157% | 56% | 55.44 | 15.60 | 15.11 | 4.43 | **+35.4** | 0 | 4.2 |
| 5 | 202.1 | 60% | 60% | 80.84 | 23.92 | 21.74 | 7.05 | **+68.6** | 0 | 4.2 |

Arithmetic: e.g. Y3 EBITDA = 49.0 − 23.52 − 8.28 − 7.28 − 3.15 = 6.77. Cumulative capital required = running sum of burn years (Y1+Y2 = 4.2M), then flat since EBITDA turns positive.

**This P&L-only figure ($4.2M) is not credible as the real capital need** — see Sec. 3 for the actual recommended raise. Two reasons: (1) Sec. 4 shows the headcount plan implies ARR/employee ratios (up to ~$594k by Y5) far above realistic for a human-in-the-loop compliance business, meaning true opex is understated; (2) customs brokers often front duties/taxes to authorities on behalf of importers before client reimbursement, or must carry continuous surety bonds scaled to entered value — a **working-capital driver the entrepreneur's plan never mentions**, potentially dwarfing the P&L burn at $200M ARR scale.

## 2. Unit Economics

- **CAC (Y5)** = S&M÷net-new customers = $23.92M ÷ (4,700−3,000) = $23.92M ÷ 1,700 = **$14,071**.
- **LTV** = ACV × GM ÷ annual churn = $43,000 × 0.60 ÷ 0.15 = $25,800 ÷ 0.15 = **$172,000** (churn 15%/yr, i.e. 6.7-yr average lifetime — **assumption**, justified by the broker-of-record lock-in the entrepreneur claims in Sec. 4, but the entrepreneur gives no retention data to verify it).
- **LTV:CAC ≈ 12.2:1**; **payback** = CAC ÷ monthly gross profit = $14,071 ÷ (($43,000/12)×0.60) = $14,071 ÷ $2,150 = **6.5 months**.
- **These numbers are implausibly good and are a red flag, not a strength.** Best-in-class enterprise SaaS runs 3–5:1 LTV:CAC and 12–18-month payback; ClearBorder's own Risk #3 (Sec. 5) says customs filings are liability-sensitive and switching is trust-gated — that profile implies a *longer*, costlier sales cycle (compliance review, champion-building), not a faster one. A more defensible CAC given that dynamic is 2–3x higher (~$30–40k), which still clears a healthy ~5:1 ratio but roughly doubles the required S&M budget baked into Sec. 1 — reinforcing that the model is underfunded on GTM.
- **NRR**: not stated anywhere in Sec. 3; ACV is shown escalating $20k→$43k blended across cohorts, but new-logo mix vs. within-account expansion isn't decomposed, so NRR can't be backed out of the given data. **Assumption: 110%** (modest upsell from duty-optimization/FTA features). This is unverified and materially changes how many *gross* bookings are needed to net 4,700 logos.
- **Is $43k blended ACV achievable?** It directly **contradicts** the entrepreneur's own Sec. 2 SAM math: "blended addressable spend per customer... $15,000/yr" (**assumption**, their words). $43,000 ÷ $15,000 = **2.87x** their own market-sizing assumption. If real winning accounts pay ~3x the SAM's per-customer figure, ClearBorder is selling to a narrower, more enterprise/competitive slice than the 150,000-account mid-market pool Sec. 2 sizes — likely fewer than 4,700 reachable logos exist in that slice within 5 years, or the SAM itself needs re-sizing upward. Either way, Sec. 2 and Sec. 3 don't reconcile.

## 3. Funding Plan

| Round | Amount | Target Valuation (pre/post) | Dilution | Must Prove |
|---|---|---|---|---|
| Seed | $5M | $20M / $25M | ~20% | AI classification accuracy vs. licensed brokers (>95% agreement); 20 design partners live; US broker partnership signed |
| Series A | $18M | $70M / $88M | ~20% | $1M→$12M ARR (50→400 customers); CBP ABI filing live in production; first repeat/upsell evidence |
| Series B | $45M | $220M / $265M | ~17% | $49M ARR; UK/EU licensing secured or near-certain; real (not modeled) CAC payback <12 months |
| Series C | $85M | $600M / $685M | ~12% | $126M ARR; 5+ jurisdictions operating; credible EBITDA-breakeven path; duty-float/working-capital facility in place |

**Total primary capital ≈ $153M**, against ~46% combined founder/early-holder retention through Series C. This is **far larger than the $4.2M the P&L model above implies is needed** — the gap is intentional: it funds (a) the headcount shortfall identified in Sec. 1/4, (b) land-grab GTM overspend to actually hit 4,700 logos, and (c) working-capital/bonding buffer the entrepreneur's plan omits. If the entrepreneur's own numbers were taken at face value, this raise would be unjustifiably large — that mismatch is itself worth surfacing to them.

## 4. Sanity Checks

1. **Revenue/employee is not credible for this business model.** ARR ÷ headcount (Sec. 3 figures): Y1 $67k, Y2 $267k, Y3 $446k, Y4 $573k, **Y5 $594k**. Elite pure-software companies top out around $300–450k/employee at scale; ClearBorder has a licensed-human-review requirement baked into its own Risk #1 that should push this *lower*, not higher. The plan is under-hired relative to its ARR target — most acutely Trade/Compliance and GTM in Y3–Y5.
2. **Implied early profitability contradicts the stated land-grab strategy.** Even under conservative 45–60% (not 80%+) gross margins, Sec. 3's headcount plan turns EBITDA-positive by Y3. A company simultaneously claiming aggressive multi-country expansion (Sec. 3, Y3–Y5) and hitting profitability that fast is internally inconsistent — real companies in this mode overspend on trust-building and compliance staffing, not underspend.
3. **ACV contradicts market sizing.** Sec. 2's SAM assumption ($15k/customer) vs. Sec. 3's Y5 ACV ($43k) — a 2.87x gap, never reconciled (detailed in Sec. 2 above).
4. **Funnel math is never shown.** Sec. 3 needs 1,700 net-new logos in Y5 alone (4,700−3,000) off 115 GTM heads, with GTM headcount growing 12→35→75→115 (Y2–Y5) — no pipeline, conversion rate, or sales-cycle-length assumption appears anywhere, despite Sec. 5 Risk #3 calling this a trust-gated, liability-sensitive sale. A rep-ramp (6–12 months to full productivity) isn't reflected either; new reps are assumed instantly productive in the same year they're hired.
5. **Multi-jurisdiction licensing is compressed with no dedicated timeline or budget.** Sec. 3 puts UK, Germany, and Netherlands entry in the same year (Y3) as a 2.4x headcount jump (45→110) and a GTM-motion pivot. Sec. 5 Risk #1 calls licensing "the single riskiest assumption... a binary, external, slow-moving gate we don't control," yet Sec. 3's ARR ramp proceeds as if licensing lands on schedule regardless, with no jurisdiction-by-jurisdiction sequencing or contingency.
6. **Trade/Compliance-to-customer ratio (Sec. 3) stabilizes at ~52–56 customers/staffer from Y3 on** — plausible only if human review is thin/exception-based rather than per-filing, which is exactly the unresolved regulatory question in Risk #1. The whole cost model's credibility rides on an outcome the entrepreneur admits they don't control.
7. **No working-capital/duty-float or bonding plan.** Customs brokerage typically involves fronting duties or carrying bonds scaled to entered value — absent entirely from Sec. 1–3, and likely the largest true capital driver at $200M+ ARR scale.
