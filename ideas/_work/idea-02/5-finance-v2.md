# ClearPath Health — Finance Review v2

## 1. Financial Model v2 (5-Year)

**Revised assumptions** (ARR/headcount from entrepreneur v2 §3; everything else **assumption** unless arithmetic shown):
- Revenue = ARR (consistent with v1 model). Blended ACV **$533K** (entrepreneur v2 §4).
- Gross margin now starts lower — 55%→75% — because copilot mode is labor-heavy in Y1–Y2 and converts to API automation only after CMS-0057-F APIs land Jan 2027 (v2 §2.1).
- G&A now includes the legal-mitigation load (below), so it runs hotter than v1: 60%→12% of revenue.
- Sanity anchor: total cost per year ≈ headcount × $190K fully loaded × 1.2 for non-people (**assumption**). Y2: 60×0.19×1.2=$13.7M vs modeled $13.6M; Y5: 430×0.19×1.2=$98M vs modeled $152M — Y5 model is deliberately richer (inference, insurance, channel fees), so costs are not understated.

| Year | ARR | Growth % | GM % | COGS | S&M | R&D | G&A | EBITDA | Cash Burn | Cumulative Capital Required |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | $2M | — | 55% | $0.9M | $1.7M | $1.7M | $1.2M | ($3.5M) | ($3.5M) | $3.5M |
| 2 | $7M | 250% (7/2−1) | 62% | $2.7M | $4.9M | $3.9M | $2.1M | ($6.6M) | ($6.6M) | $10.1M |
| 3 | $28M | 300% (28/7−1) | 68% | $9.0M | $14.0M | $7.8M | $5.0M | ($7.8M) | ($7.8M) | $17.9M |
| 4 | $75M | 168% (75/28−1) | 72% | $21.0M | $33.8M | $15.0M | $10.5M | ($5.3M) | ($5.3M) | $23.2M (peak) |
| 5 | $160M | 113% (160/75−1) | 75% | $40.0M | $64.0M | $28.8M | $19.2M | +$8.0M | +$8.0M | $15.2M net (23.2−8) |

**Cost of the legal mitigations, quantified (cumulative, Y1–Y5):**
- Compliance-Ops payroll: head-years 2+8+20+45+80=155 × $140K loaded (**assumption**) ≈ **$21.7M**.
- Specialty liability insurance at 1.75% of revenue (midpoint of entrepreneur's 1.5–2%, v2 §1/L4): cumulative revenue 2+7+28+75+160=$272M × 1.75% ≈ **$4.8M**.
- Y1 compliance officer + regulatory counsel ($250K+$300K **assumption**), FTO + 50-state UR licensure survey (~$450K one-time **assumption**), HITRUST/SOC 2 (~$200K/yr from Y2 = $800K): ≈ **$1.8M**.
- **Direct mitigation cost ≈ $28M over five years**, plus the larger G&A column (3→52 heads vs zero in v1).
- **Revenue cost of the mitigations:** cumulative ARR falls from v1's $378M (3+15+50+110+200) to $272M — **$106M of cumulative ARR foregone**, including the $40M Y5 haircut. This dwarfs the direct cost and is the honest price of removing scraping and "denial-proof."

**Total capital required (restated):** modeled P&L burn peaks at only $23.2M, but — same reconciliation as v1 — runway buffers, cash-vs-ARR timing on 60–90-day hospital AR, copilot-mode gross-margin risk, and the compliance build put realistic capital at **$140–150M**. The entrepreneur's ~$150M (v2 §2.7) is the right planning number; I would size rounds to $150M with the Series B tranche gated on measured API-automation conversion.

## 2. Unit Economics v2 (deltas only)

- **CAC** = S&M ÷ net-new logos (logos back-solved as ARR/$533K: 4, 13, 53, 141, 300; net-new 9, 40, 88, 159 — close to entrepreneur's 18/60 logo counts): Y2 $4.9M/12=$408K; Y3 $14.0M/42=$333K; Y5 $64M/159=$403K. **Blended CAC ≈ $400K — unchanged from v1.**
- **Blended LTV** = $533K × 72% GM × 8yr = **$3.07M → LTV:CAC 7.7:1**; payback = $400K/($533K×0.72=$384K) = **1.04 yr**. Still healthy.
- **New wrinkle — copilot cohorts:** at $300K ACV and ~70% GM, LTV = $300K×0.70×8 = $1.68M → **4.2:1** and payback = $400K/$210K = **1.9 yr**. Copilot-mode customers are marginal standalone economics; the model works only if they upgrade to $600K automation ACVs when payer APIs go live. Track upgrade rate as a board metric.
- **Revenue-per-employee concern: substantially resolved.** $91K (Y1: $2M/22) → $372K (Y5: $160M/430) is a 4.1x gain with a *dated, external* driver (Jan 2027 API mandate) instead of the unexplained 6x. $372K/head at Y5 is low-normal for health-IT with human attestation in the loop — believable, and it costs margin, which the 75% Y5 GM already reflects.
- NRR 115% assumption unchanged; the copilot→automation upgrade motion actually strengthens the expansion case.

## 3. Verdict

**Fundable with conditions.**

The three numbers driving the verdict:
1. **~$150M capital to reach $160M ARR** — capital efficiency of ~$1.07 ARR per $1 raised (160/150). Thin but acceptable for regulated healthcare; v1's implied 1.6x (200/125) was fiction once compliance was priced in.
2. **Blended LTV:CAC 7.7:1, payback ~12.5 months** — genuinely strong unit economics survive the revision; copilot cohorts at 4.2:1 are the watch item.
3. **Y3 growth of 300% (28/7−1)** — the entire model re-accelerates on one external event: CMS-0057-F APIs shipping usably in Jan 2027. The entrepreneur's own v1 Risk #1 (payers slow-walking APIs) is now the load-bearing wall of the financial plan.

**Is sub-$200M still venture-scale?** Yes. $160M ARR growing 113% with 75% GM supports an 8–12x ARR multiple (**assumption**, current health-IT comps) = **$1.3–1.9B outcome**. Against ~$150M raised and ~70–75% cumulative dilution, a Series C entering near $500M–600M post still underwrites 2.5–4x, and a credible Y6 path to $200M+ via the commercial/ERISA book (v2 §3) preserves upside. This is a smaller, slower, real company instead of a larger fictional one — the correct trade.

**Conditions:** (a) Series B tranched on demonstrated copilot→automation conversion ≥40% within 12 months of a payer's API going live; (b) attestation workflow and liability insurance economics validated in the first five signed contracts (does clinician sign-off throttle throughput below the $300K-ACV service level?); (c) quarterly reporting on payer-API availability vs. the Jan 2027 assumption, with a pre-agreed cost-cut plan if the mandate slips.

*(~960 words)*
