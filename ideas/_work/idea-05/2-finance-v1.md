# GridPilot — Finance Review v1

## 1. Financial model (5-year)

**Revenue quality callout:** the entrepreneur's "ARR" is ~90% revenue-share on volatile wholesale/DR
prices, not subscription ARR. Splitting at the stated ~$5–8k/MW SaaS fee (midpoint **assumption**
$6.5k/MW): Y1 SaaS-ARR = 25MW×$6.5k=$0.16M (11% of "ARR"); Y5 SaaS-ARR = 3,150MW×$6.5k=$20.5M
(10% of "ARR"). The other ~90% moves with power prices, weather, and capacity-auction outcomes —
it should be modeled as revenue, not booked/valued like SaaS ARR.

**Assumptions:** fully-loaded cost/head — Eng+Data-Markets $210k, Sales-CS $190k (+25% non-headcount
S&M loading for marketing/channel/travel), Ops-G&A $170k (+25% loading). Gross margin ramps 35%→55%
(Y1→Y5) reflecting heavy settlement/telemetry/ISO-ops COGS versus a normal SaaS COGS profile — VPP
revenue-share businesses (Voltus, CPower) run thinner GM than pure software. AR/working capital:
60-day ISO/utility settlement lag (**assumption**) on revenue-share revenue only.

| Year | ARR | Rev growth % | GM % (assumption) | COGS | S&M | R&D | G&A | EBITDA | Cash burn (incl. WC) | Cumulative capital required |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | $1.5M | n/a | 35% | $1.0M | $0.7M | $2.6M | $0.4M | ‑$3.2M | $3.4M | $3.4M |
| 2 | $12M | 700% | 40% | $7.2M | $2.9M | $5.6M | $1.1M | ‑$4.7M | $6.3M | $9.7M |
| 3 | $42M | 250% | 45% | $23.1M | $9.0M | $12.0M | $2.6M | ‑$4.7M | $9.1M | $18.8M |
| 4 | $105M | 150% | 50% | $52.5M | $20.2M | $21.0M | $6.4M | +$4.9M | $4.3M* | $23.1M (peak) |
| 5 | $205M | 95% | 45%** | $92.3M | $39.2M | $33.0M | $10.0M | +$30.6M | ‑$15.7M | $7.4M |

*Y4 still burns cash despite positive EBITDA because AR grows $9.3M as revenue-share receivables
build — a classic growth-stage cash trap in a receivables-heavy model.
**GM dips vs. Y4 trend because I hold the ramp at 45% cap for revenue-share COGS (settlement,
market-ops) that doesn't scale as cleanly as SaaS COGS — flag, not a typo.

Peak cumulative capital required ≈ **$23.1M** (end of Y4), before the business turns net
cash-generative in Y5. With a 40–50% contingency buffer for revenue-share volatility, slower ISO
entry, or CAC overruns (see §2/§4), the bottoms-up minimum raise is **~$30–35M** — far below what a
"$200M ARR in 5 years" venture narrative typically raises (~$130M+ across 4 priced rounds). That
gap is itself a finding: either this is a genuinely capital-efficient, asset-light business (good),
or the headcount/GTM plan is too lean to hit the MW ramp (see §4).

## 2. Unit economics

**CAC (derived from S&M ÷ net-new sites, not asserted):** sites = MW ÷ 1.75MW/site.
- Y2: $2.9M S&M ÷ 100 net-new sites = **$29k/site**
- Y3: $9.0M ÷ 286 = **$32k/site**
- Y4: $20.2M ÷ 571 = **$35k/site**
- Y5: $39.2M ÷ 829 = **$47k/site**

CAC is *rising*, not falling, even as headcount and channel partnerships scale — inconsistent with
the "land-and-expand," channel-leverage story in the entrepreneur's §3/§4.

**LTV (assumption: 5-yr avg contract life, 90% annual retention given claimed multi-year
lock-in):** revenue/site/yr = $65k/MW × 1.75MW = $113.75k. At 50% blended GM, gross profit/site/yr
= $56.9k. LTV (5yr, undiscounted) = $56.9k × 5 = **$284.5k**. Churn-based perpetuity check:
$56.9k ÷ (1‑0.90) = $569k — I use the conservative $284.5k.

**LTV:CAC / payback:**
- Y4: $284.5k ÷ $35k = **8.1x**; payback = $35k ÷ $56.9k/yr = **7.4 months**
- Y5: $284.5k ÷ $47k = **6.0x**; payback = **9.9 months**

Both clear the >3x / <12mo SaaS bar today, but the *trend* (CAC up, LTV:CAC down) is the wrong
direction for a plan claiming GTM leverage by Y5, and both ratios rest entirely on the $65k/MW figure.

**Does $65k/MW-yr hold across ISOs?** No — it can't be a single blended constant. ERCOT is an
energy-only market (no capacity payments, higher price volatility); PJM, NYISO, ISO-NE and MISO run
capacity markets (structurally different, often higher, floor-priced revenue); CAISO uses resource
adequacy. A single $65k/MW figure applied uniformly across CAISO, ERCOT, PJM, NYISO, MISO, ISO-NE
(§3's 6-market footprint) is a **flagged assumption**, not a market-validated number — it needs
per-ISO decomposition before it can support a $205M ARR target.

## 3. Funding plan

Sized to the bottoms-up peak need (~$23M, §1) plus buffer, not to a generic Seed→D template:

| Round | Amount | Pre-money | Dilution | Must prove |
|---|---|---|---|---|
| Seed/A (pre-launch) | $10M | $25M | ~29% | FERC 2222 registration in CAISO+ERCOT; bidding engine live; 5 anchor customers signed; <30-day integration demonstrated |
| B (mid-Y2) | $15M | $70M | ~18% | $12M ARR at ~$60k/MW; PJM+NYISO registration; CAC trend flat-or-down; revenue-share settlement/billing process proven reliable |
| C (Y3) | $20M equity + $15M venture debt/receivables facility | $180M | ~10% | $42M ARR; 6-ISO trajectory on track; CAC reversal; GM >45%; receivables facility specifically funds the AR build (§1), not equity-diluted |
| D (Y4, opportunistic) | $20M | $450M | ~4% | EBITDA-positive; UK/EU expansion capital; buffer against revenue-share volatility, not survival capital |

Total: ~$65M equity + $15M debt = **$80M**, roughly 2.5–3.5x the bottoms-up minimum — appropriate
buffer given how fragile the $65k/MW and enrollment-velocity assumptions are (§4), but the fund
should recognize most of Rounds C/D as optionality capital, not burn-rate necessity.

## 4. Sanity checks

1. **$65k/MW-yr doesn't arithmetically follow from §2's own inputs.** 25% revenue share × $150k/MW
   + $5–8k SaaS = $37.5k–$45.5k/MW, not $65k. To reach $65k with an $8k SaaS fee requires a 38%
   effective revenue share — above the stated "20–30% share" band in the seed brief and §1. Either
   the share is understated or $65k is inflated ~40-70%; this single number drives the entire $205M
   Y5 ARR figure.

2. **Enrollment velocity vs. hiring plan is inconsistent with "long C&I sales cycles."** §5 risk #3
   admits onboarding/CAC risk from bespoke integrations, yet §3's Sales-CS headcount (which also
   covers customer success, not just BD) must deliver net-new sites at 5.0–8.3 sites/head/yr
   (§2 math). If even half those heads are CS/renewal rather than quota-carrying BD, actual new-logo
   velocity is ~10–17 sites per BD rep per year — nearly one signed enterprise C&I site per month,
   which contradicts the "long sales cycle" framing used to justify the 30-day-integration wedge.

3. **ISO market-entry timeline collides with the MW ramp in Year 3.** §4's own moat claim #3 says
   ISO aggregator certification takes "6–12 months per market." §3 has GridPilot entering MISO,
   ISO-NE, *and* a UK pilot simultaneously in Year 3 while also tripling enrolled MW (200→700MW).
   Three new-market certifications in one year, each taking up to a year, is not consistent with
   also hitting a 3.5x capacity ramp in the same year — the plan needs a lagged revenue ramp per
   new-ISO cohort (first bids realistically land ~Q3–Q4 of the entry year at earliest).

4. **Revenue-share volatility is invisible in the ARR presentation.** §2/§3 present $65k/MW and ARR
   targets as smooth, SaaS-like numbers. Real wholesale/capacity prices are volatile — e.g., PJM's
   capacity auction cleared multiples higher year-over-year in the 2025/26 cycle — meaning realized
   revenue-share could plausibly swing ±30–50% around the $65k/MW assumption in either direction,
   which should be shown as a range, not a point estimate, in any board-facing model.

5. **CAC is rising while the narrative claims GTM leverage** (§2) — directly contradicts §3's
   "scale channel," "land-and-expand," and "utility MOU" GTM claims for Years 3–5.

6. **Minor: per-MW ARR is inconsistent Y1–Y4 ($60k) vs. Y5 ($65k)** in the entrepreneur's own table
   (§3) — small next to #1, but signals the model wasn't stress-tested year-by-year.
