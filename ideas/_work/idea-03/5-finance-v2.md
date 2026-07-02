# InferRoute — Finance Review, Round 2 (v2 plan)

## 1. Financial Model v2 (5-Year)

**Cost of the legal/architecture mitigations (quantified):**
- **Customer-VPC data plane engineering:** ~4 eng FTEs Y1 rising to ~8 by Y3 (**assumption**) = 4×$220K=$0.9M Y1 → ~$1.8M/yr, inside R&D. This is why Y1 ships 14 eng vs. 12 in v1.
- **Gross-margin impact:** two offsetting forces. Customer-VPC shifts data-plane compute cost to the customer (COGS down), but adds solutions-engineering for VPC onboarding (~$20K/enterprise deploy, **assumption**) and per-tenant caching forfeits cross-tenant hit-rate economies. Net: GM path **62%→75%** vs. 65%→78% in v1 — a ~3pp haircut every year (**assumption**).
- **G&A adders:** E&O/cyber insurance $200K/yr avg (their $150-300K range), AI Act counsel $250K (Y1), FTO $150K (Y1).
- **Revenue-side cost:** residency-constrained routing haircuts EU usage revenue ~10% — already inside the $144M.

**Other assumptions carried from v1:** loaded cost/head Eng $220K, S&M $200K, G&A $180K; R&D = Eng cost ×1.15; S&M = S&M headcount cost + entrepreneur's explicit demand-gen line (§3); G&A = headcount + overhead ($0.5M→$3.0M) + adders above; COGS = ARR×(1−GM).

| Year | ARR ($M) | Growth % | GM % | COGS ($M) | S&M ($M) | R&D ($M) | G&A ($M) | EBITDA ($M) | Cash Burn ($M) | Cum. Capital Req. ($M) |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 2.0 | n/a | 62% | 0.8 | 2.0 | 3.5 | 1.8 | -6.1 | 6.1 | 6.1 |
| 2 | 11.0 | 450% | 65% | 3.9 | 7.0 | 6.1 | 2.3 | -8.3 | 8.3 | 14.4 |
| 3 | 36.0 | 227% | 69% | 11.2 | 12.6 | 10.1 | 3.8 | -1.7 | 1.7 | **16.1 (peak)** |
| 4 | 81.0 | 125% | 72% | 22.7 | 19.0 | 13.9 | 6.0 | +19.4 | 0 | cash-generative |
| 5 | 144.0 | 78% | 75% | 36.0 | 25.0 | 17.7 | 8.5 | +56.8 | 0 | cash-generative |

Arithmetic samples: Y2 S&M = 20 heads×$200K + $3M demand-gen = $7.0M. Y1 G&A = 4×$180K + $0.5M overhead + $0.2M insurance + $0.25M AI Act + $0.15M FTO = $1.8M. Y5 EBITDA = 144×0.75 − 25.0 − 17.7 − 8.5 = +$56.8M.

**Restated capital required:** peak cumulative operating burn ≈ **$16M** (through Y3) — up from ~$9.5M in v1 (lower early ARR + mitigation costs), but total recommended raise **falls** from ~$250M to **~$130M** (Pre-seed $2M + Seed $8M + A $20M + B $40M + C $60M), because the plan turns EBITDA-positive in Y4 and Series D becomes optional/opportunistic rather than required. ~$114M of the $130M is competitive buffer, not modeled burn.

## 2. Unit Economics v2 — Changes Only

Net-new customers: 25 / 75 / 180 / 240 / 280. CAC = S&M ÷ net-new:
- Y1: $2.0M/25 = **$80K**; Y2: $7.0M/75 = **$93K**; Y3: $12.6M/180 = **$70K**; Y4: $19.0M/240 = **$79K**; Y5: $25.0M/280 = **$89K**.

LTV (ACV × GM × 7-yr life, unchanged method): Y5 = $180K×0.75×7 = **$945K** → LTV:CAC **10.6x**; payback = $89K/($180K×0.75/12) = **7.9 months**. Y1: $80K×0.62×7=$347K → **4.3x**, payback 17.3 mo.

The v1 deterioration (Y5 payback 17 mo) reverses — but that is because S&M is now only 17% of Y5 ARR (25/144). New-logo bookings Y5 = 280×$180K=$50.4M on $25M S&M (magic number ~2.0, with NRR 115% expansion carrying the rest: 81×1.15 + 50 ≈ 144 ✓). That efficiency is **better than Datadog at scale** — residual optimism, flagged, but the 20% PLG contribution and expansion-led model make it defensible enough to underwrite with a Series B gate rather than reject.

**ACV decomposition ask: answered.** §2/#4: $180K = $105K platform fee (58%, volume-insensitive) + $3M managed spend × 2.5% take rate = $75K; take rate compresses 3.5%→2.5%; and they state the load-bearing assumption plainly — 10-20x token volume per account offsetting >90% unit-price decline — with a quantified downside (**$114M ARR if volume only 5x**). This is exactly the decomposition requested.

## 3. Verdict

**Fundable with conditions.**

Three numbers that drive it:
1. **$144M Y5 ARR, +$56.8M EBITDA** — an EBITDA-positive, 78%-growth business at Y5 supports a $2.5-3.5B outcome (**assumption**, ~18-22x forward on decelerating growth) on ~$130M raised — a strong venture-scale return profile even without hitting $200M until Y6-7. Growth-adjusted, this beats the v1 plan, which bought $205M ARR with ~$250M and thinner credibility.
2. **$16M peak burn against a $3.3B TAM** — unusually capital-efficient for infra; the burn math no longer depends on later rounds clearing.
3. **$114M downside ARR** (5x volume case) — still fundable at Series B/C scale; the plan degrades gracefully rather than breaking.

**Hyperscaler bundling:** the repositioning (concede single-cloud governance; own cross-provider neutrality, per the Datadog-vs-CloudWatch analogy in §2/#3) is the right answer and the compliance-deep regulated segment is where hyperscaler bundles are weakest. Residual risk is multiple compression, not existence — priced into the valuation ceiling above, not a reason to pass.

**Conditions:** (a) Series A gate: evidence from design partners of per-account token-volume growth trajectory supporting the 10-20x assumption; (b) Series B gate: VPC deployment economics proven ≤$25K/onboard and ≤30 days, and Y2 magic number ≥1.0 actuals; (c) S&M budget trues up (+$5-8M/yr Y4-5) if new-logo CAC efficiency reverts to industry norms — pre-agree this in the Series C sizing.
