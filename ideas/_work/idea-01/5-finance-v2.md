# SentinelAML — Finance Review v2

The revised plan (entrepreneur v2 §2-3) adopted my S&M envelope, cut Year-5 ARR to $134M, and
absorbed the attorney's mitigations. This re-run prices those mitigations and restates capital.

## 1. Financial model v2 (5-year)

**Assumptions** (ARR/headcount rows are the entrepreneur's, v2 §3):
- Gross margin 50%→72% (entrepreneur v2 §2.6 — single-tenant, in-tenant deployment; below my v1
  55%→78%). COGS = ARR × (1−GM).
- S&M = new ARR × efficiency ratio 1.8x→0.7x (my v1 envelope, adopted by entrepreneur §2.1).
- R&D = (Eng + Comp/ML) FTEs × $230k loaded (**assumption**): Y1 12, Y2 24, Y3 39, Y4 57, Y5 75.
- G&A = base $0.8M floor rising to 7% of ARR (**assumption**), plus E&O and FTO items below;
  Y4 includes ~$1.8M UK/EU entity/licensing/localization setup (**assumption**).
- Cash burn ≈ −EBITDA.

| Year | ARR | Growth % | GM % | COGS | S&M | R&D | G&A | EBITDA | Burn | Cum. Capital |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | $0.6M | — | 50% | $0.30M | $1.08M | $2.76M | $1.20M | **−$4.74M** | $4.74M | $4.74M |
| 2 | $4.5M | 650% | 58% | $1.89M | $5.46M | $5.52M | $1.50M | **−$9.87M** | $9.87M | $14.61M |
| 3 | $18M | 300% | 64% | $6.48M | $14.85M | $8.97M | $2.70M | **−$15.00M** | $15.00M | $29.61M |
| 4 | $54M | 200% | 68% | $17.28M | $32.40M | $13.11M | $5.90M | **−$14.69M** | $14.69M | $44.30M |
| 5 | $134M | 148% | 72% | $37.52M | $56.00M | $17.25M | $9.40M | **+$13.83M** | $0 | $44.30M (peak) |

Arithmetic samples: Y4 S&M = new ARR ($54M−$18M=$36M) × 0.9 = $32.4M; Y5 EBITDA =
134−37.52−56.00−17.25−9.40 = +$13.83M.

**Cost of the legal mitigations (cumulative, 5 years, ≈$27.5M):**
- Compliance/audit function from Year 1 (L12): 2/4/7/10/12 FTEs = 35 FTE-years × $230k =
  **$8.05M** (inside R&D/Comp-ML line).
- E&O/cyber (L4/L5): $0.25M Y1 rising to ~$1.3M Y5 (~1% of ARR, **assumption**) = **~$3.3M** (in G&A).
- FTO review + defensive filings (L8): **$0.3M** (in G&A, Y1-2).
- Single-tenant/in-tenant architecture (L9/L2): GM ramp 50→72% vs my v1 55→78%; extra COGS =
  5pts×$0.6M + 7×$4.5M + 8×$18M + 8×$54M + 6×$134M ≈ **$14.2M** — the single most expensive
  mitigation.
- UK/EU deferral to Y4 + licensing/entities (L3/L11): **~$1.8M** setup in Y4; the larger cost is
  revenue timing, already embedded in the lower ARR ramp.

**Total capital required: peak cumulative burn ≈ $44.3M** (end of Year 4; Year 5 self-funds), up
$8.7M from my v1 $35.6M — legal mitigations plus slower ramp, partly offset by lower S&M on a
smaller ARR base. With a ~45% runway buffer (**assumption**), **recommended raise ≈ $65M**
(pre-seed through Series C), confirming the entrepreneur's $65-70M estimate (v2 §2.6). Series C
sizing moves from $15M to ~$22M; earlier rounds broadly as my v1 plan.

## 2. Unit economics v2 (changes only)

- **CAC (Y5):** $56.0M ÷ 160 new logos = **$350k** (was $327k — slower cycles, smaller base).
- **LTV:** $420k ACV × 0.72 GM × 8-yr life = **$2.42M** (was $2.50M — GM compression). Lifetime
  assumption unchanged; the switch to per-customer models (v2 §1, L9 fix) arguably *strengthens*
  retention — tuning resets to zero on churn — partially replacing the lost pooled-data moat.
- **LTV:CAC = $2.42M ÷ $350k ≈ 6.9:1** (was 7.6:1). Still well above 3:1.
- **Payback:** $350k ÷ ($420k × 0.72 = $302k) = **1.16 yrs ≈ 14 months** (was 12.6). Acceptable.
- **NRR 110%** remains an unvalidated **assumption**, but the module roadmap (crypto/VASP,
  sanctions, 314(b), one-click disposition) gives it plausible carriers. Condition: prove ≥105%
  on the Year-2 cohort before Series B.
- Pipeline math now stated and coherent: 160 closes ÷ 20% win rate = 800 qualified opps
  (v2 §2.4) ≈ 27% of the 2,950 US-CA SAM touched in one year — aggressive but arithmetically
  consistent with 32 AEs at 5 deals/AE.

## 3. Verdict

**Fundable with conditions.**

Three driving numbers:
1. **$44.3M peak capital → $134M ARR** = **$3.02 of Year-5 ARR per dollar of peak burn** —
   top-quartile capital efficiency for enterprise SaaS; the raise ($65M) is easily financeable
   against this curve.
2. **LTV:CAC 6.9:1 with 14-month payback** — unit economics survive the legal mitigations with
   room to absorb further CAC slippage (breakeven vs. the 3:1 floor is CAC ≈ $807k, 2.3x modeled).
3. **Year-5 exit velocity: $134M ARR growing ~48%** — at an 8-10x forward-ARR multiple
   (**assumption**, regtech comps), that is a **$1.3-2.0B outcome**, roughly 20-30x on ~$65M
   invested at blended entry prices.

On missing the $200M target: yes, $134M is below brief. It does not matter. The honest number
still supports a venture-scale outcome — $200M becomes a Year-6/7 milestone on the same curve
(134 × 1.48 ≈ $198M in Year 6), and I will fund a credible $134M plan over a fictitious $200M one
every time. The v1 plan bought its extra $66M with an S&M budget that didn't exist and a
consortium product the attorney showed was illegal to build.

**Conditions precedent:** (1) Year-1 pilots must instrument inference-cost-per-transaction and
demonstrate a path to ≥58% GM by Year 2 — single-tenant economics are the model's soft spot;
(2) NRR ≥105% on the Year-2 cohort before Series B; (3) sales-cycle evidence at seed: the four
design partners must convert to paid inside two quarters, else the 20%-win-rate/5-deals-per-AE
engine is overstated and the curve shifts right again.
