# ClearPath Health — Finance Review v1

## 1. Financial Model (5-Year)

**Assumptions** (all labeled **assumption**; ARR/customer counts taken from entrepreneur §3):
- ACV **$500K** (entrepreneur's own example: 80K auths × $5 + $100K platform fee).
- Customers implied by ARR/ACV: Y1=6, Y2=30, Y3=100, Y4=220, Y5=400 — matches entrepreneur's Y1 "6-10 design partners" and Y5 "400 customers."
- Gross margin ramps 65%→78% (services-heavy: manual-review safety net, EHR/payer integration maintenance, LLM inference cost per auth **assumption**).
- S&M 70%→40% of revenue (typical enterprise-SaaS land-grab curve, healthcare cycles keep it elevated longer than horizontal SaaS).
- R&D 60%→18% of revenue.
- G&A 25%→10% of revenue (includes legal/compliance/HR/exec — **not broken out in the entrepreneur's headcount table**, see §4).
- Cash burn ≈ EBITDA (no capex/working-capital adjustment; hospital AR runs 60-90 days, so real burn is understated by an **assumption** 10-15%).

| Year | ARR | Growth % | Gross Margin % | COGS | S&M | R&D | G&A | EBITDA | Cash Burn | Cumulative Capital Required |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | $3M | — | 65% | $1.05M | $2.10M | $1.80M | $0.75M | ($2.70M) | ($2.70M) | $2.7M |
| 2 | $15M | 400% (15/3−1) | 70% | $4.50M | $9.00M | $6.75M | $3.00M | ($8.25M) | ($8.25M) | $11.0M |
| 3 | $50M | 233% (50/15−1) | 74% | $13.0M | $25.0M | $15.0M | $7.5M | ($10.5M) | ($10.5M) | $21.5M |
| 4 | $110M | 120% (110/50−1) | 76% | $26.4M | $49.5M | $24.2M | $13.2M | ($3.3M) | ($3.3M) | $24.8M (peak) |
| 5 | $200M | 82% (200/110−1) | 78% | $44.0M | $80.0M | $36.0M | $20.0M | $20.0M | +$20.0M | $4.8M net (24.8−20) |

**Peak modeled operating burn ≈ $25M**, hit at end of Y4, before Y5 turns cash-generative. This is the P&L-only number; §3 explains why actual capital raised is much larger.

**Cross-check against the entrepreneur's literal headcount cost** (Eng/CP $220K/$200K, Sales $220K, CS $150K, Compliance-Ops $130K fully loaded, all **assumption**): total headcount cost only reaches $47.3M by Y5 against $200M ARR — an implied ~59% EBITDA margin. That is not credible for a 5-year-old company still expanding specialties and running human-in-the-loop review on every submission (their own Y1 milestone). **This mismatch is the core red flag in §4**: either headcount is understaffed for the ARR target, or the ARR target overshoots what this headcount can sell/service.

## 2. Unit Economics

- **CAC** = S&M spend ÷ net-new customers that year: Y2 $9.0M/24=$375K; Y3 $25.0M/70=$357K; Y4 $49.5M/120=$412.5K; Y5 $80.0M/180=$444K. Blended **CAC ≈ $400K**.
- **LTV** = ACV × gross margin × average lifespan. **Assumption:** 8-year average enterprise lifespan (92% gross logo retention → 1/0.08=12.5yr, discounted to 8yr for platform/payer-mandate risk), blended GM 75%. LTV = $500K × 0.75 × 8 = **$3.0M**.
- **LTV:CAC = $3.0M / $0.4M = 7.5:1** — well above the 3:1 SaaS health threshold.
- **Payback period** = CAC ÷ (ACV × GM) = $400K / ($500K×0.75=$375K) = **1.07 years (~13 months)** — inside the 12-18-month enterprise-SaaS benchmark.
- **NRR assumption: 115%**, driven by the entrepreneur's own Y3-Y4 "land-and-expand into new specialties" motion (§3 GTM). Not independently verified by the entrepreneur; no cohort data exists yet.
- **Does pricing support this?** Yes, on paper — $5/auth + $100K platform clears a healthy payback. But CAC here assumes deals close within the same fiscal year sales headcount is added. Hospital enterprise sales cycles run 9-18 months including security/legal review; if true cycle length pushes CAC realization out 6-12 months, cash-CAC effectively doubles and payback stretches past 24 months, which would strain the funding plan in §3.

## 3. Funding Plan

| Round | Amount | Pre/Post-Money | Dilution | Must prove to raise next round |
|---|---|---|---|---|
| Pre-seed | $2M | $8M / $10M | 20% | Clinical-evidence-matching accuracy on retrospective charts; 2-3 LOIs |
| Seed | $8M | $24M / $32M | 25% | Epic + 5-payer ePA integration live; 6 paying design partners (Y1 target) |
| Series A | $18M | $72M / $90M | 20% | $3M ARR achieved, ≥85% auto-submission approval accuracy, first Y1 renewals |
| Series B | $35M | $185M / $220M | 16% | $15M ARR (Y2), NRR data ≥110%, enterprise sales team producing repeatable logos |
| Series C | $60M | $440M / $500M | 12% | $50M ARR (Y3), national footprint, payer-partnership proof (mirrors Cohere "Align") |
| **Total raised** | **$123M** | | **~68% cumulative founder/employee dilution** | funds Y4-Y5 scale to $200M ARR |

**Reconciliation with §1:** modeled operating burn peaks at ~$25M, but rounds total $123M. This gap is intentional and standard: (a) each round is sized to 18-24 months of runway plus a raise-ahead buffer, not to the exact modeled deficit; (b) healthcare-specific costs are underrepresented in a %-of-revenue model — SOC 2/HITRUST, state licensure, malpractice-adjacent liability insurance, EHR-vendor certification fees; (c) §4's sales-cycle risk means real burn plausibly runs 1.5-2x the model. **A CFO should treat $120-130M, not $25M, as the realistic total capital required to reach $200M ARR.**

## 4. Sanity Checks

1. **Headcount-to-ARR growth mismatch (biggest concern).** ARR grows **67x** (Y1 $3M → Y5 $200M, entrepreneur §3) while total headcount grows only **11x** (22→241, entrepreneur §3 table). Revenue/employee goes from $136K (Y1: $3M/22) to $830K (Y5: $200M/241), a 6x efficiency gain in five years for a business whose Y1 milestone explicitly includes a "manual-review safety net on every auto-submission." Y5 milestones (§3) add specialties and point-of-care PA rather than removing human review — nothing in the plan explains where the 6x labor-efficiency gain comes from.
2. **Y1→Y2 logo velocity vs. sales-cycle length.** Entrepreneur's GTM (§3) says the enterprise sales team is "stood up" in Year 2, not Year 1, yet Y2 requires 24 net-new logos (30−6) off a reference base of just 6 live pilots that only launched in Y1. Hospital enterprise sales cycles commonly run 9-18 months including security/legal review (**assumption**, industry norm); a team hired at the start of Y2 mostly can't close before late Y2/Y3, so 24 closings in Y2 is not well supported by the GTM narrative as written.
3. **Y2→Y3 AE productivity.** 70 net-new logos (100−30) on 20 reps (up from 8, §3 headcount) = 3.5 logos/rep/year at $500K ACV — above typical 2-4 logos/year enterprise-health-IT AE productivity (**assumption**), and reps hired mid-year need 6-9 months to ramp, making this tighter still.
4. **Compliance-Ops staffing vs. clinical-liability risk.** Entrepreneur's own Risk #2 (§5) flags clinical-accuracy liability as potentially fatal to enterprise sales, yet Compliance-Ops headcount is only 2→4→8→14→20 (§3) while auth volume implied by ARR grows from ~48K/yr (6 cust × 8K, back-solved) to ~32M/yr (400 cust × 80K) — a >600x volume increase against a 10x headcount increase in the exact function meant to catch wrong submissions.
5. **SOM vs. specialty/payer coverage timing.** SOM math (§2) requires 400 customers (15% of ~2,600 accounts) by Y5, but full national payer coverage and 15+ specialties don't land until Y5 itself (§3 Product Milestones) — the footprint that's supposed to justify large-system procurement arrives the same year the customer count target is due, not ahead of it.
6. **No G&A/compliance-exec line in the headcount table.** §3's headcount columns (Eng/Clinical-Product/Sales/CS/Compliance-Ops) omit legal, finance, HR, and executive staff entirely — a material gap for a company whose top risk is regulatory/liability exposure.

*(~1,480 words)*
