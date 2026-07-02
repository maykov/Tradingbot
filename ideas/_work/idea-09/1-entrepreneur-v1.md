# FactoryEye — Business Plan v1

## 1. Product & value proposition

FactoryEye is a turnkey AI visual-inspection product for mid-market discrete manufacturers
(50–999 employees; automotive parts, electronics assembly, appliances, packaging). We bundle
pre-configured edge cameras, lighting rigs, and a foundation vision model into a subscription that
a plant quality engineer — not a data scientist — can install and tune on a production line.

**Buyer:** Quality directors / VP of Operations at mid-market plants who currently rely on manual
inspectors or legacy rule-based machine vision (Cognex/Keyence) that requires a systems integrator
and months of setup.

**Wedge feature (Year 1):** "5-Day Line" — a single-SKU defect-detection deployment that goes from
unboxing to live pass/fail decisions on one line in under five business days, using few-shot
fine-tuning of a foundation vision model on ~50–200 customer-labeled defect images (vs. the
thousands typically needed for classical ML). No-code labeling UI lets line operators, not
engineers, correct model mistakes in production, closing the loop automatically. This collapses
the classic 3–6 month machine-vision integration into a self-service motion that a $30–60k/line/yr
subscription can justify without a capex approval cycle.

## 2. Market sizing

**TAM:** Global machine-vision market ≈ **$15.5B in 2024** (Market Research Future) to **$20.4B**
(Grand View Research), growing at 8–13% CAGR through 2030. We use **$20B** as TAM (industrial
visual inspection + machine vision, global, source: Grand View Research, Precedence Research).

**SAM (bottom-up, US mid-market discrete manufacturing):**
- US has >245,000 manufacturing establishments (Census/NAM data, cited via search).
- **Assumption:** ~35% are discrete manufacturers with QC-critical lines (auto parts, electronics,
  appliances, packaged goods) → ~86,000 establishments.
- **Assumption:** ~25% fall in the 50–999 employee "mid-market" band that is too small for
  in-house ML teams but large enough to afford $30–60k/line → ~21,500 companies.
- **Assumption:** average 3 inspection-critical lines per qualifying plant that could run
  FactoryEye.
- SAM = 21,500 companies × 3 lines × $45k/line/yr (midpoint of brief's $30–60k range) ≈ **$2.9B/yr**
  in the US alone (software+hardware subscription revenue potential).

**SOM (Year 5 target, bottom-up):**
- 1,600 customers × 3.0 avg lines/customer × $45k/line/yr = **$216M ARR**.
- 1,600 customers is ~7.4% penetration of the 21,500-company SAM in 5 years — aggressive but
  consistent with a land-and-expand PLG-plus-field-sales motion in a category with a hard, visible
  ROI (2–4% of revenue lost to scrap/escapes, per brief — **assumption**, sourced from customer
  discovery, not yet externally verified).

Sources: [Grand View Research — Machine Vision Market](https://www.grandviewresearch.com/industry-analysis/machine-vision-market),
[Precedence Research — Machine Vision Market](https://www.precedenceresearch.com/machine-vision-market),
[Market Research Future — Machine Vision Market](https://www.marketresearchfuture.com/reports/machine-vision-market-1510).

## 3. 5-year plan

| Year | Product milestone | GTM motion | Headcount (Eng / Sales / Deploy-CS / G&A) | Geography | ARR target |
|---|---|---|---|---|---|
| 1 | "5-Day Line" wedge: single-SKU defect detection, no-code labeling, edge camera kit | Founder-led sales + 5 design-partner pilots; case-study driven | 18 (10/3/3/2) | US Midwest & Southeast auto/electronics clusters | ~$1.2M (20 customers × 1.5 lines × $40k) |
| 2 | Multi-SKU changeover, SPC/analytics dashboard, alerting | Inside sales team, channel partnerships with camera/integrator resellers | 45 (20/10/10/5) | US nationwide | ~$7.6M (90 × 2.0 lines × $42k) |
| 3 | Plant-wide orchestration across lines, MES/ERP integration (SAP, Epicor), predictive scrap analytics | Field sales expansion, industry-vertical playbooks (auto, electronics) | 110 (35/30/35/10) | + Mexico (nearshoring manufacturing belt) | ~$33M (300 × 2.5 lines × $44k) |
| 4 | Cross-plant benchmarking, robotic reject-arm integration, fine-tuning marketplace for niche defect types | Enterprise/multi-site accounts, partner-led installs to scale deployment | 260 (60/70/100/30) | + Western Europe (Germany, Italy industrial base) | ~$100.8M (800 × 2.8 lines × $45k) |
| 5 | Autonomous root-cause copilot, cross-customer defect-benchmark index, localization | Multi-site enterprise expansion, self-serve add-on lines for existing accounts | 480 (90/120/220/50) | + broader EU, SE Asia support hub | **~$216M** (1,600 × 3.0 lines × $45k) |

Deployment/CS headcount dominates by Year 5 because hardware installs and per-SKU tuning are the
main scaling bottleneck (see Risk 3).

## 4. Competition & moat

**Top 3 competitors:**
1. **Instrumental** — electronics-manufacturing-focused (PCB/assembly), $80M+ raised, deep
   root-cause tooling, but priced and built for large electronics OEMs, not general mid-market
   discrete manufacturing.
2. **Elementary** — horizontal no-code vision inspection (VisionStream), used by Fortune 500
   manufacturers inspecting 1B+ parts/year; fast to train but enterprise-oriented pricing and
   sales motion, leaving the smaller mid-market underserved.
3. **Landing AI (LandingLens)** — founded by Andrew Ng; positioned as a model-building tool for
   data-science teams, not a turnkey install-in-days product for plants without ML staff.

**Moat:** (a) Vertical wedge into the 50–999-employee segment that Instrumental/Landing AI ignore
(enterprise-first) and that Elementary underserves on price/self-service; (b) hardware+software
bundle removes integration risk and financed camera hardware creates switching friction once
installed; (c) data network effect — defect images collected across similar SKUs/verticals (e.g.,
stamped metal parts, PCB solder joints) improve few-shot fine-tuning for the next similar
customer, compounding accuracy advantage and shortening future deployments; (d) per-line renewal
economics tied to a visible, quantifiable ROI (scrap reduction) create high renewal rates once a
customer sees dollars saved.

## 5. Key risks

1. **Camera-OEM commoditization risk:** Cognex, Keyence, or Basler bundle equivalent foundation-
   model inspection directly into their hardware/firmware, eliminating the standalone software
   margin FactoryEye depends on. If this happens before we build a defensible data/integration
   moat, our per-line subscription collapses to a hardware-only, low-margin business.
2. **Willingness/ability to pay:** The plan assumes plants realize enough of the "2–4% of revenue
   lost to scrap" (brief's figure, unverified — **assumption**) to justify $30–60k/line/yr, and
   that a single quality director can approve this without a multi-stakeholder capex process. If
   actual realized savings are lower, or budget authority is fragmented across plant vs.
   corporate, the SAM and per-customer pricing both shrink and the $200M target becomes
   unreachable.
3. **Deployment scalability:** The Year-5 model requires 220 deploy/CS FTEs to install and
   maintain 4,800 lines (~22 lines/FTE) while preserving the "5-day install" promise. If real
   installs require significantly more customization (lighting, camera geometry, per-SKU tuning)
   than a few-shot foundation model can generalize, cost-to-serve rises faster than revenue,
   destroying unit economics needed to fund the Year 3–5 growth headcount.
