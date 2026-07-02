# SentinelAML — Finance Review v1

Reviewer note: the entrepreneur's plan (§3) specifies ARR and headcount by year but never models
COGS, gross margin, opex mix, or a capital plan. This review builds that P&L on top of the
entrepreneur's ARR trajectory and headcount, using standard enterprise-SaaS benchmarks (labeled
**assumption**), then stress-tests whether the headcount plan can actually deliver that ARR.

## 1. Financial model (5-year)

**Assumptions** (all labeled; ARR and headcount rows are the entrepreneur's, from §3):
- Gross margin ramps 55%→78% (**assumption**: heavy compute/implementation cost early, typical
  for AI-native infra selling to regulated banks; COGS = ARR × (1−GM%)).
- R&D = entrepreneur's Eng + Compliance/ML headcount × **$230k fully-loaded/FTE** (assumption).
- S&M is *not* taken from the entrepreneur's GTM payroll — it is rebuilt from new-ARR-bookings ×
  a CAC-efficiency ratio (1.8x in Y1 improving to 0.70x in Y5, **assumption**, standard
  enterprise-SaaS benchmark for 12+ month bank sales cycles). See §4 for why the entrepreneur's
  GTM headcount cannot fund this.
- G&A = 15%→7% of ARR (**assumption**, opex leverage as company scales, includes bank-vendor
  compliance/audit/insurance overhead).
- Cash burn ≈ −EBITDA (**assumption**: ignores capex/working-capital timing, immaterial at this
  stage).

| Year | ARR | Growth % | GM % | COGS | S&M | R&D | G&A | EBITDA | Cash Burn | Cumulative Capital Req'd |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | $1.5M | — | 55% | $0.68M | $2.70M | $2.53M | $0.23M | **−$4.63M** | $4.63M | $4.63M |
| 2 | $9.0M | 500% | 65% | $3.15M | $10.50M | $5.75M | $1.08M | **−$11.48M** | $11.48M | $16.11M |
| 3 | $32.0M | 256% | 72% | $8.96M | $25.30M | $10.12M | $3.20M | **−$15.58M** | $15.58M | $31.69M |
| 4 | $88.0M | 175% | 76% | $21.12M | $47.60M | $16.10M | $7.04M | **−$3.86M** | $3.86M | $35.55M |
| 5 | $200.0M | 127% | 78% | $44.00M | $78.40M | $21.85M | $14.00M | **+$41.75M** | $0 | $35.55M (peak) |

Arithmetic: e.g., Y3 COGS = $32M×(1−0.72)=$8.96M; Y3 S&M = new ARR ($32M−$9M=$23M) × 1.1x =
$25.3M; Y3 EBITDA = $32.0−8.96−25.3−10.12−3.2 = −$15.58M. **Peak cumulative capital required ≈
$35.6M**, reached at end of Year 4; Year 5 turns cash-generative (+$41.75M) and repays the trough.
Adding a standard 12–18mo runway/timing buffer (**assumption**, ~40%) implies a **recommended
total raise of ~$50–55M**, not $35.6M — companies raise ahead of the trough, not to it.

## 2. Unit economics

CAC = S&M spend ÷ new logos that year (fully loaded).
- Y1: $2.70M ÷ 10 = **$270k CAC** vs. $150k ACV → CAC > ACV in Year 1 (normal for enterprise
  land, but steep).
- Y5: $78.40M ÷ 240 = **$327k CAC** vs. $400k blended ACV.

LTV (**assumptions**: 5% annual gross logo churn → 8-year effective lifetime given bank switching
costs; 110% net revenue retention from module upsell — crypto/VASP Y3, agentic workflows Y4,
embedded Y5):
LTV = ACV × GM% × lifetime = $400k × 0.78 × 8 = **$2.496M**.
**LTV:CAC = $2.496M / $327k ≈ 7.6:1** at maturity — well above the 3:1 healthy benchmark.

Payback period = CAC ÷ (ACV × GM%):
- Y5: $327k ÷ ($400k × 0.78 = $312k) = **1.05 years (~12.6 months)** — inside the <18-month
  enterprise-SaaS benchmark.
- Y1: $270k ÷ ($150k × 0.55 = $82.5k) = **3.3 years** — poor, expected pre-motion-maturity.

**Does the entrepreneur's pricing support this?** At the *modeled* CAC, yes — 7.6:1 LTV:CAC and
~12.6mo payback are strong. But this CAC is built from a CAC-efficiency benchmark, not from the
entrepreneur's actual GTM budget. Their §3 GTM payroll is far too small to buy this CAC (see §4)
— so pricing is fine, but the go-to-market spend plan needed to realize it is missing from the
entrepreneur's plan entirely, and NRR of 110% is unvalidated (no pilot data yet).

## 3. Funding plan

| Round | Amount | Pre-money → Post-money | Dilution | Must prove before next round |
|---|---|---|---|---|
| Pre-seed | $2M | $8M → $10M | 20% | Working overlay MVP, 2–3 signed design-partner LOIs, ex-examiner hires on the compliance team |
| Seed | $6M | $24M → $30M | 20% | Year-1 plan: 10 paying customers, $1.5M ARR, SOC 2 Type I, evidence the "overlay wedge" cuts sales cycle below the 12–18mo bank norm |
| Series A | $12M | $58M → $70M | 17% | Year-2: $9M ARR, full platform (not just overlay) live at ≥3 reference accounts, one signed channel/core-banking partner, GM trending to 65%+ |
| Series B | $20M | $160M → $180M | 11% | Year-3: $32M ARR, EU entities live, NRR ≥110% with real data (not assumption), CAC payback <18mo demonstrated |
| Series C | $15M | $435M → $450M | 3% | Year-4: $88M ARR, $50B+ enterprise-bank logos closed, EBITDA trending to breakeven (model shows −$3.86M) |
| Series D | Not modeled as required | — | — | Model shows Year-5 EBITDA +$41.75M; a D round would be opportunistic (M&A, faster international land) rather than survival capital |

Total primary capital raised: **$55M**, against a modeled peak burn of $35.6M — the ~$19M spread
is runway buffer, standard practice against execution slippage. Valuations above are round-number
multiples of forward ARR at each round's close (**assumption**, ~7x for A/B/C, consistent with
regtech/vertical-SaaS comps), not independently sourced.

## 4. Sanity checks

1. **GTM headcount cannot buy the CAC the model requires.** Entrepreneur §3 budgets GTM payroll
   of $420k (Y1, 2 people) up to $11.55M (Y5, 55 people at $210k/FTE). The CAC-efficiency
   benchmark in §1 requires **$2.70M of S&M in Y1 and $78.4M in Y5** — 6.4x and 6.8x the budgeted
   GTM payroll, respectively. Either the entrepreneur's headcount plan is understaffed by roughly
   that multiple, or CAC is far higher than assumed (which would break the 7.6:1 LTV:CAC in §2).
   This is the single largest hole in the plan.

2. **Year-1 timeline is internally inconsistent.** Entrepreneur §3 targets 10 signed customers and
   $1.5M ARR in Year 1, with SOC 2 Type I *also* shipping in Year 1 and a 2-person GTM team. But
   Entrepreneur §5 risk #2 states bank procurement cycles run 12–18 months even for the overlay
   motion. A startup cannot plausibly start selling before it has a working product and SOC 2
   evidence (typically 3–6 months to obtain), leaving well under 12 months of actual selling time
   in Year 1 — inside the sales cycle §5 itself flags as the risk. Closing 10 regulated-bank deals
   in that window with 2 GTM staff is optimistic; expect Year-1 ARR closer to $0.5–0.8M (3–5
   logos), pushing the whole curve right by roughly two quarters.

3. **Year-5 AE math doesn't fit inside the stated GTM headcount.** To hit 240 new logos in Year 5
   at a plausible enterprise close rate of ~5 deals/AE/year (**assumption**, standard for
   $300–500k ACV, 12+ month cycles), the company needs **~48 quota-carrying AEs**. Entrepreneur
   §3's entire Year-5 "GTM" function is 55 people — that leaves only 7 heads for marketing, SDRs,
   channel management, and sales engineering combined, which is not enough to run the
   "land-and-expand" and embedded-partnership motion §3 also describes for Year 5.

4. **SOM vs. SAM penetration is aggressive but the plan doesn't reconcile it with cycle time.**
   Entrepreneur §2 sizes SAM at ~4,100 institutions; the 500-customer Year-5 target is 12.2% share.
   Achieving that requires averaging ~48 new logos/quarter by Year 5 (240 logos ÷ 5 quarters of
   ramped selling), while §5 risk #2 admits procurement cycles of 12–18 months per account. A
   pipeline supporting 48 closes/quarter needs roughly 4–6x that many active late-stage
   opportunities in flight simultaneously — no pipeline or win-rate assumption is stated anywhere
   in §2 or §3 to support this.

5. **ACV growth (§3: $150k→$400k) moves the plan into a segment with longer, not shorter, cycles,
   right when logo velocity is asked to accelerate.** Year 4's stated GTM motion is "Enterprise AE
   segment for $50B+ banks" — larger, slower-procurement accounts — yet new logos still grow
   150→240 (Year 4→5), a 60% acceleration. Enterprise/RFP-driven deals typically lengthen cycles
   to 18–24 months, which cuts against accelerating close velocity in the same year.

6. **No COGS/infra cost appears anywhere in the entrepreneur's plan.** Real-time transaction
   scoring with an LLM-based scoring layer across 500 institutions implies material cloud/LLM
   inference spend; §1's assumed 22–45% COGS (implying $44M of infra+services cost by Year 5) is
   this reviewer's construction, not the entrepreneur's — it should be validated against actual
   inference-cost-per-transaction data from the Year-1 pilots before Series A.
