# KinCare — Business Plan v1

## 1. Product & Value Proposition

KinCare is an AI care-coordination platform for the 63 million US family caregivers managing
eldercare for a parent or relative (AARP/NAC, *Caregiving in the US 2025*). It replaces
spreadsheets, group texts, and phone tag with: (a) an AI care plan built from an intake
conversation plus ongoing signals, (b) a benefits/provider navigator that reads a family's
insurance and employer benefits to find covered services, (c) medication and appointment
orchestration with family task-sharing, and (d) a vetted marketplace (home care, meal delivery,
transportation, respite care) monetized via take rate.

**Customers:** we sell B2B2C — employers (as a voluntary/self-insured benefit) and Medicare
Advantage plans (as a supplemental benefit) pay a per-employee/per-member-per-month (PEPM) fee;
the employee/member uses the product free or low-cost, and pays only for marketplace services.

**Year-1 wedge:** "Benefits Navigator" — an AI agent that ingests a family's specific health plan
and employer benefits documents and tells them, in plain language, exactly what eldercare support
(FMLA, EAP, backup care, MA supplemental benefits, Medicaid waivers) they already have and how to
claim it within 48 hours. This is narrow enough to ship fast, has an immediate "aha" (money/time
recovered), and creates the intake data needed to power care plans and marketplace matching later.

## 2. Market Sizing

**TAM — $20B.** US eldercare coordination & navigation software and services market (seed-brief
assumption, consistent with adjacent categories: senior-care marketplace + care-management
software spend).

**SAM — bottom-up, ~$5.0B/yr:**
- *Employer channel:* ~19,000 US firms have 1,000+ employees (Census Bureau County Business
  Patterns firm-size distribution, **assumption** for exact count). At an average 3,500 employees
  per firm and a $4.00 PEPM caregiver-benefit price (in line with published PEPM tiers from
  comparable vendor Torchlight — torchlight.care/resources/faqs — **assumption** for our exact
  price point): 19,000 × 3,500 × $4 × 12 = **$3.19B/yr**.
- *Medicare Advantage channel:* ~33M MA enrollees nationally (CMS enrollment data, 2025,
  **assumption** for exact figure) at $50/member/yr of supplemental-benefit spend allocated to
  caregiver navigation (**assumption**): 33M × $50 = **$1.65B/yr**.
- SAM total ≈ $3.19B + $1.65B ≈ **$4.84B/yr**.

**SOM — Year 5 target ≈ $200M/yr (≈4% of SAM):**
- Employer: 400 enterprise clients, avg. 4,000 covered lives, $4 PEPM →
  400 × 4,000 × $4 × 12 = **$76.8M**.
- MA plans: 8 health-plan contracts covering 3M members combined, $25/member/yr →
  3,000,000 × $25 = **$75.0M**.
- Marketplace: $500M annual GMV of booked home-care/respite/transport services at a 10% take
  rate = **$50.0M**.
- Total ≈ $76.8M + $75.0M + $50.0M = **$201.8M**, i.e., ≥$200M ARR (all figures **assumption**
  extrapolations for a 5-year-out state; near-term figures grounded in cited comps).

## 3. 5-Year Plan

| Year | Product Milestones | GTM Motion | Headcount (Eng/Care Ops/Sales+CS/G&A) | Geography | ARR Target |
|---|---|---|---|---|---|
| 1 | Launch Benefits Navigator wedge; basic care plan + task-sharing; 10 employer pilots (~50k covered lives) | Direct enterprise sales to benefits consultants + 2 pilot MA plans; design-partner pricing | 12 / 6 / 6 / 4 (28) | US remote-first, HQ 1 metro | **$1.5M** |
| 2 | Full care-plan engine; medication/appointment orchestration; marketplace v1 (3 service categories, 2 metros) | Scale via benefits brokers/consultants (Mercer, WTW referral deals); first MA contract signed | 25 / 15 / 14 / 8 (62) | 8 metros, national employer sales | **$9M** |
| 3 | Marketplace expands to 8 categories nationwide; EHR/claims data integrations; proactive risk alerts | Land-and-expand in existing employer accounts; embed with 2 more MA plans; channel deal with a payroll/benefits platform | 45 / 35 / 30 / 15 (125) | National marketplace coverage; explore Canada pilot | **$32M** |
| 4 | AI care-coordinator handles multi-step tasks autonomously (scheduling, claims follow-up); provider network >5,000 vetted vendors | Enterprise sales team scales; MA channel becomes repeatable (RFP-ready); marketplace supply flywheel | 70 / 60 / 55 / 25 (210) | National + UK pilot (analogous NHS/employer market) | **$105M** |
| 5 | Platform-wide analytics for employers/plans (ROI dashboards); international product localization | 400 employer logos, 8 MA plans live, marketplace GMV ~$500M | 100 / 90 / 80 / 35 (305) | US national, UK live, Canada exploration | **$201.8M** |

## 4. Competition & Moat

**Top 3 competitors:**
1. **Cariloop** — care-coach-led navigation platform for employers; $42M raised total, most
   recently a $20M Series C (April 2024, led by ABS Capital) (abscapital.com;
   finsmes.com/2024/04/cariloop-raises-20m-in-series-c-funding.html). Human-coach-heavy model,
   which caps margin and scaling speed.
2. **Wellthy** — care concierge/coordination for employers and health plans; $75.9M raised total,
   merged with Patch Caregiving in October 2025 (cbinsights.com/company/wellthy/financials).
   Also concierge/service-heavy, consolidating for scale.
3. **Torchlight** — employer-focused caregiver benefit with tiered PEPM pricing plus 1:1 advising
   sessions (torchlight.care/resources/faqs). Narrower advising focus, less marketplace/AI
   automation.

**Moat:** Incumbents are staffed by human care coaches, which bounds gross margin (~40-55%) and
limits how many families one FTE can serve. KinCare's AI-native navigation targets a materially
better cost-to-serve, enabling either lower PEPM (win price-sensitive mid-market employers
incumbents ignore) or higher margin at the same price. Three durable advantages compound over
time: (1) **data network effect** — every navigated benefit, claim, and marketplace booking trains
better care plans and provider-matching, and MA claims integrations create a data moat rivals
without payer relationships can't replicate; (2) **two-sided marketplace lock-in** — vetted
provider supply plus recurring family demand creates switching costs on both sides; (3)
**distribution lock-in** — annual employer/MA renewal cycles plus embedded workflows (payroll,
EHR, claims) raise switching costs once integrated, similar to benefits-administration incumbents.

## 5. Key Risks

1. **Benefit-budget elasticity risk.** The plan assumes employers and MA plans will allocate new,
   incremental PEPM dollars specifically for caregiving rather than folding it into an existing
   EAP/wellness line that never gets renewed or expanded. If caregiving is treated as a
   nice-to-have that gets cut in the next benefits-budget downturn, the employer SAM ($3.19B)
   collapses.
2. **AI navigation liability/trust risk.** The wedge product gives specific guidance on benefits,
   medical, and financial matters for an elderly, often-vulnerable population. A high-profile
   error (wrong benefit info, missed medication interaction) could trigger liability exposure and
   destroy the trust the B2B2C model depends on — this is existential, not just reputational.
3. **Utilization/engagement risk.** SOM math assumes meaningful active-user rates within covered
   populations (driving both retention and marketplace GMV). If actual caregiver adoption within
   a covered employee/MA population is much lower than assumed (a chronic problem for benefit
   navigators), both the renewal case for PEPM pricing and the $50M marketplace revenue line
   break, since GMV requires real transacting users, not just covered lives.
