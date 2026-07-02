# InferRoute — Finance Review, Round 1

## 1. Financial Model (5-Year)

**Assumptions** (all labeled **assumption**; ARR figures taken as-is from entrepreneur Section 3):
- Revenue recognized = net platform + take-rate fees only (matches entrepreneur's ACV figures). Pass-through inference spend billed by providers directly to customers is **excluded** from revenue and COGS (agent, not principal, treatment) — this is the critical guardrail against gross-margin distortion the brief flagged.
- Fully-loaded cost/head/yr: Eng $220K, Sales&CS $200K, G&A $180K (**assumption**, US-blended senior AI-infra comp).
- R&D = Eng headcount cost × 1.15 (dev/test infra/tools). G&A = G&A headcount cost + corporate overhead ($0.5M→$3.5M, **assumption**).
- S&M modeled as % of ARR (70%→33%, **assumption**, standard enterprise-infra SaaS glidepath), **not** off the Section 3 headcount budget alone — see Sanity Check #1 for the gap this exposes.
- Gross margin ramps 65%→78% (**assumption**: caching hit-rate and support-cost scale economies); COGS = gateway hosting/compute, semantic-cache infra, support.
- Capex/working-capital treated as ~0 (**assumption**, asset-light cloud model).

| Year | ARR ($M) | Growth % | GM % | COGS ($M) | S&M ($M) | R&D ($M) | G&A ($M) | EBITDA ($M) | Cash Burn ($M) | Cumulative Capital Required ($M) |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 3.0 | n/a | 65% | 1.1 | 2.1 | 3.0 | 1.0 | -4.2 | 4.2 | 4.2 |
| 2 | 18.0 | 500% | 68% | 5.8 | 9.9 | 5.6 | 2.0 | -5.3 | 5.3 | 9.5 (peak) |
| 3 | 55.0 | 206% | 72% | 15.4 | 24.8 | 9.6 | 3.8 | +1.4 | 0 | 8.1 net |
| 4 | 120.0 | 118% | 75% | 30.0 | 45.6 | 13.9 | 6.1 | +24.4 | 0 | net cash-generative |
| 5 | 205.0 | 71% | 78% | 45.1 | 67.7 | 19.0 | 8.9 | +64.3 | 0 | net cash-generative |

Peak external operating capital need = **~$9.5M** (end of Y2). Total capital actually raised (Section 3) is far larger — sized for competitive buffer, not pure burn.

## 2. Unit Economics

Implied ACV = ARR / customers (30/150/400/700/1,000 per Section 3): $100K, $120K, $137.5K, $171.4K, $205K.
CAC = S&M spend / net-new customers (30/120/250/300/300):

- Y1: $2.1M / 30 = **$70.0K**
- Y2: $9.9M / 120 = **$82.5K**
- Y3: $24.8M / 250 = **$99.2K**
- Y4: $45.6M / 300 = **$152.0K**
- Y5: $67.7M / 300 = **$225.7K**

LTV = ACV × GM% × 7-year avg lifetime (**assumption**, conservative vs. naive 1/churn=10yrs at 90% gross retention):

- Y1: $100K×0.65×7 = **$455K** → LTV:CAC **6.5x**, payback = $70K/($100K×0.65/12) = **12.9 mo**
- Y2: $120K×0.68×7=**$571K** → **6.9x**, payback **12.1 mo**
- Y3: $137.5K×0.72×7=**$693K** → **7.0x**, payback **12.0 mo**
- Y4: $171.4K×0.75×7=**$900K** → **5.9x**, payback **14.2 mo**
- Y5: $205K×0.78×7=**$1,119K** → **5.0x**, payback **16.9 mo**

**NRR assumption: 115%** (90% gross logo retention, ~25pp expansion from growing routed volume per account) — structurally favorable because usage-based pricing means expansion is largely organic, not sales-led. **Pricing supports unit economics through Y3** (LTV:CAC peaks at 7.0x, payback ~12 months). Y4-Y5 show payback lengthening (12→17 months) and LTV:CAC compressing (7.0x→5.0x) as CAC outpaces ACV growth during the upmarket/international push — still healthy but the trend line, not the level, is the thing to watch next round.

## 3. Funding Plan

| Round | Amount | Pre/Post Val. | Dilution | Timing | Must prove |
|---|---|---|---|---|---|
| Pre-seed | $2M | $8M/$10M | 20% | Now | Team, working prototype, 2-3 design-partner LOIs |
| Seed | $8M | $24M/$32M | 25% | +6mo | 10 design partners live, wedge savings-SLA validated |
| Series A | $20M | $100M/$120M | 16.7% | End Y1 | $3M ARR hit, NRR >110%, 2+ multi-year enterprise deals, SOC2 II underway |
| Series B | $45M | $305M/$350M | 12.9% | Y2-Y3 | $18-30M ARR run-rate, EU live, S&M efficiency closing the gap flagged in §4.1, FinOps partnerships signed |
| Series C | $75M | $825M/$900M | 8.3% | Y3-Y4 | $55-90M ARR, EBITDA approaching breakeven, HIPAA/FedRAMP-ready, demonstrated resilience to hyperscaler bundling |
| Series D | $100M | $1.9B/$2.0B | 5.0% | Y4-Y5 | $120M+ ARR, 30%+ EBITDA margin trajectory, intl >30% of ARR, category leadership vs. OSS/hyperscaler validated |

**Total primary capital raised: ~$250M.** Cumulative founder/early dilution ≈ 62% by Series D (holders retain ~38%) — consistent with a 6-round path in a hot, contested category.

## 4. Sanity Checks

1. **S&M budget vs. ARR ramp (§3 headcount table).** 12 Sales&CS heads at $200K = $2.4M Y2 spend, but hitting $18M ARR (+$15M net-new) at realistic enterprise-SaaS S&M efficiency needs ~$9.9M (our model). That's a **~$7.5M gap** unaccounted for in the headcount plan — either understaffed by ~35-40 reps/marketers, or a non-headcount demand-gen budget must be added explicitly next round.

2. **Sales cycle vs. rep ramp (§3 GTM Motion, "3-person AMY sales team").** Enterprise infra deals with security review at 500-10,000-employee accounts run 3-6 month cycles. Three enterprise reps hired in Y2 cannot plausibly carry a 6x ARR multiple (Y1 $3M → Y2 $18M) without a quantified PLG contribution, which the plan never breaks out.

3. **SOM aggressiveness vs. own comparables (§2 SAM/SOM math).** 1,000 customers = 6.7% of the stated 15,000-account SAM in 5 years, benchmarked against Datadog/Snowflake — both took 8-10+ years to reach comparable penetration in categories with no free OSS incumbent (LiteLLM, Portkey's open-sourced core, §4) and no hyperscaler-native bundling threat (§5 Risk #1). This is the single most aggressive assumption in the plan.

4. **Moat contradicts self-identified top risk (§4 vs. §5).** Moat (b), "system of record for AI spend governance," is exactly the surface AWS/Azure/GCP are best positioned to bundle free to prevent InferRoute from ever becoming that system of record. The plan never reconciles this; if hyperscalers ship "good enough" governance by Y3 (when the plan's own FinOps-integration milestone lands), the Y4-Y5 ARR bridge (+$85M net-new) is the most exposed part of the curve.

5. **Pricing/volume decomposition missing (§2 TAM vs. §5 Risk #2).** Risk #2 cites >90% inference-cost decline by 2030. Since ACV tracks % of managed spend, our implied ACV growth ($100K→$205K) is a dollar figure — a >90% unit-cost decline requires ~10x volume growth just to hold spend-based ACV flat. Section 3's milestones show no such volume ramp. Ask the entrepreneur to decompose ACV growth into (routed-volume growth) × (take rate) next round.
