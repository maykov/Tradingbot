# SentinelAML — Business Plan v1

## 1. Product & value proposition
SentinelAML is an AI-native transaction-monitoring and case-management platform for banks, credit
unions, fintechs, and crypto exchanges that must run AML programs but cannot staff the analyst
armies that legacy rules engines (Actimize, SAS, Verafin) demand. We ingest transaction, KYC, and
device/network data; score alerts with explainable ML layered on top of (not replacing) existing
rules for regulatory continuity; auto-draft SAR narratives with full evidence citations; and give
investigators a case workspace that closes alerts 5-10x faster.

**Wedge for Year 1:** "False-positive triage copilot" — a drop-in layer that sits beside a bank's
incumbent rules engine (no rip-and-replace, the #1 sales objection killer), re-scores and clusters
existing alerts, and auto-drafts SAR narratives for confirmed hits. This gets a live pilot signed
in weeks instead of the 9-12 month RFP cycle a full replacement requires, and lets us prove a
25-40% reduction in analyst review time before asking for the full platform swap.

**Customer:** compliance and BSA/AML officers at $1B-$50B asset banks and credit unions, mid-size
fintechs (BaaS-sponsored programs), and crypto exchanges — institutions too large to ignore AML
risk but too small to get white-glove attention or bespoke tuning from Tier-1 vendors.

## 2. Market sizing

**TAM (bottom-up):** ~8,800 US banks and credit unions (FDIC: 4,462 insured banks; NCUA: ~4,370
credit unions as of mid-2025) [FDIC/NCUA], plus an assumption of ~3,000 fintechs/MSBs/crypto
exchanges globally that need dedicated AML tooling (**assumption**, based on BSA-registered MSB
counts and fintech-BaaS program estimates). At a blended $150k-$1M ACV (seed-brief range,
midpoint ~$300k), TAM = ~11,800 institutions × $300k ≈ **$3.5B/yr** for the US+global mid-market
segment alone. This is consistent with third-party estimates of the broader AML/transaction-
monitoring software market at $2.6B-$4B (2025) trending toward $6.8B-$10.7B by the mid-2030s at
~11% CAGR [Fortune Business Insights; Precedence Research].

**SAM (serviceable):** Mid-size institutions ($1B-$50B assets) that are big enough to have a
dedicated compliance budget but small/mid enough to be underserved by Tier-1 vendors (NICE
Actimize, SAS, Oracle) and overserved-on-price by Tier-1 pricing. **Assumption:** this is ~35% of
the 11,800-institution universe = ~4,100 institutions. SAM = 4,100 × $300k ACV ≈ **$1.23B/yr**.

**SOM (5-year target, bottom-up to plan):** Year-5 target of 500 customers (see plan below) at a
blended ACV of ~$400k (mix shifts toward larger accounts and multi-product attach by year 5) =
500 × $400k = **$200M ARR**. This is ~12% share of SAM and ~4.2% of a comparable-vendor pool where
Unit21 alone claims 200+ customers today [Unit21.ai], suggesting 500 customers by year 5 is
aggressive but not implausible for a category leader.

## 3. 5-Year Plan

| Year | Product Milestones | GTM Motion | Headcount (by function) | Geography | Target ARR |
|---|---|---|---|---|---|
| 1 | Triage-copilot wedge live; SAR auto-draft; SOC 2 Type I; 5 design partners | Founder-led sales + 2 pilots via compliance-consultant referral network | Eng 8, Compliance/ML 3, GTM 2, Ops 1 = 14 | US only | $1.5M (10 customers × ~$150k) |
| 2 | Full transaction-monitoring engine (rules + ML) replaces incumbent at pilot accounts; case-mgmt UI; SOC 2 Type II | Inside sales team; first channel deal with a core-banking/BaaS platform | Eng 18, Compliance/ML 7, GTM 8, CS 3, Ops 2 = 38 | US; start UK/EU groundwork | $9M (35 customers × ~$260k) |
| 3 | Crypto/VASP module; sanctions & KYC-refresh add-ons; multi-entity support for bank holding cos | Expand channel (2-3 core-banking partners); outbound AE team; first EU customers | Eng 30, Compliance/ML 14, GTM 20, CS 8, Ops 5 = 77 | US, UK, EU (Ireland/Germany entities) | $32M (110 customers × ~$290k) |
| 4 | Agentic investigation workflows (auto-close low-risk alerts under model governance); regulator-facing model documentation suite | Enterprise AE segment for $50B+ banks; system-integrator partnerships | Eng 48, Compliance/ML 22, GTM 38, CS 16, Ops 9 = 133 | + Canada, APAC (Singapore) | $88M (260 customers × ~$340k) |
| 5 | Real-time cross-institution risk network (consortium data-sharing, privacy-preserving); embedded card/payment-processor product | Platform land-and-expand; embedded partnerships with payment processors | Eng 65, Compliance/ML 30, GTM 55, CS 25, Ops 15 = 190 | US, UK/EU, Canada, APAC, LatAm pilot | $200M (500 customers × ~$400k) |

## 4. Competition & moat

**Top 3 competitors:**
1. **NICE Actimize / SAS / Oracle FCCM** — Tier-1 incumbents with deep bank relationships but slow
   (9-18mo) implementations, rules-only cores retrofitted with ML, and pricing/complexity that
   excludes mid-market. They defend the top 100 banks; we win where they're too expensive or slow.
2. **Unit21** — closest direct competitor, agentic AI fraud+AML platform, 200+ customers incl.
   Chime, Intuit [Unit21.ai], strong in fintech-native accounts. Better funded/earlier mover; we
   differentiate on regulated-bank depth (SAR quality, examiner-ready documentation) vs. their
   fraud-ops/fintech center of gravity.
3. **Hawk AI / Lucinity / Napier AI** — well-funded European AI-native entrants targeting the same
   mid-market wedge. Competition will be fiercest here; differentiation is US bank/credit-union
   regulatory fluency (SAR narrative quality, examiner relationships) and the incumbent-overlay
   wedge that lowers switching cost.

**Moat:** (a) proprietary labeled-alert dataset from every customer's historical disposition
history, which compounds model accuracy and is not portable if a customer churns; (b)
examiner-tested SAR narrative and model-governance documentation templates built with input from
former OCC/FinCEN examiners — regulatory trust is slow to build and sticky; (c) the overlay
wedge creates a low-friction land motion that competitors selling full rip-and-replace cannot
match, giving us a distribution-speed advantage that compounds into data-moat advantage.

## 5. Key risks (assumptions that could kill the company)

1. **Regulators don't actually accept ML-driven alert suppression.** Our entire value prop assumes
   examiners will bless a model that closes/deprioritizes alerts a rules engine would have raised.
   If FinCEN/OCC/state examiners keep effectively requiring "alert on everything, review manually,"
   false-positive reduction has no economic value and the wedge collapses into a documentation tool.
2. **Mid-market institutions won't pay $300k+ ACV without multi-year procurement cycles.** Our SOM
   math assumes we can close 500 accounts in 5 years; if bank procurement/vendor-risk review
   cycles average 12-18 months regardless of our "overlay" pitch, our sales-cycle assumption is off
   by 2-3x and we miss the ARR curve well before year 5.
3. **A Tier-1 incumbent (NICE Actimize, SAS) ships a credible AI-overlay product first.** Their
   distribution and existing contracts at our target accounts mean if they close the AI-native gap
   even partially, our core wedge (better ML on top of their engine) becomes unnecessary — we'd be
   competing on a full platform swap from day one, which is the harder, slower motion we designed
   the wedge specifically to avoid.

**Sources:** FDIC insured-institution count; NCUA Q2/Q3 2025 credit union data; Fortune Business
Insights and Precedence Research AML software market estimates; Unit21.ai product/customer pages.
Numbers not tied to a cited source are labeled **assumption**.
