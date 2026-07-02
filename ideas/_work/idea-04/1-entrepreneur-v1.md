# ClearBorder — Business Plan v1

## 1. Product & Value Proposition

ClearBorder is an AI-native customs brokerage: we replace the fragmented, manual, paper-driven
customs-brokerage industry with a software platform that classifies goods (HS/HTS codes), predicts
and optimizes landed cost (duties, tariffs, fees), and files entries directly with customs
authorities — backed by our own licensed customs brokers for liability and audit sign-off.

**For whom:** mid-market importers/exporters ($5M–$500M in annual import value), cross-border
e-commerce brands, and the 3PLs/freight forwarders who serve them but lack in-house trade-compliance
depth. These customers are too small for Flexport's white-glove service and too complex for
spreadsheet-based compliance, so they overpay legacy brokers for slow, error-prone, non-transparent
filings.

**Wedge feature for Year 1:** an AI HS-classification and landed-cost prediction engine that ingests
a customer's product catalog (SKUs, descriptions, spec sheets, images) and returns defensible HS
codes, applicable duty/tariff/Section 301-style rates, and a landed-cost estimate per SKU — in
minutes instead of the multi-week manual process incumbent brokers use. This is sold standalone as
SaaS to build trust and a training-data flywheel, then upsells into full filing/brokerage once we
hold the customs-broker license and ABI (Automated Broker Interface) connectivity. The wedge is
timed to 2025–26 tariff volatility, where importers need re-classification and duty-optimization
answers weekly, not quarterly.

## 2. Market Sizing

**TAM ≈ $40B.** Global customs-brokerage services were valued at ~$29.6B in 2025, growing ~6.9%
CAGR (Mordor Intelligence / MarketsAndData estimates). Add global trade-compliance software
(~$10B, per seed-brief **assumption**, consistent with adjacent GRC/supply-chain-software sizing).
TAM = $29.6B + $10B ≈ **$40B**.

**SAM ≈ $2.25B (bottom-up, assumption-heavy).** We target mid-market importers/exporters and
cross-border e-commerce brands in the US, Canada, Mexico, UK, and EU — the geographies where
customs digitization (CBP ACE/ABI, UK CDS, EU ICS2) makes API-based filing feasible this decade.
- Estimated mid-market importers/exporters + e-comm brands in these geos: **150,000** (**assumption**,
  derived from CBP reporting ~300,000+ active US importers of record, roughly half judged
  "mid-market" by volume, scaled up ~1.6x for Canada/Mexico/UK/EU).
- Blended addressable spend per customer on brokerage + compliance software: **$15,000/yr**
  (**assumption**, based on per-filing fees plus SaaS across SKU volume).
- SAM = 150,000 × $15,000 = **$2.25B**.

**SOM (Year 5) = $202M**, i.e., ~9% of SAM and ~0.5% of TAM — see Year-5 row below for the
customer-count × ACV arithmetic. This penetration level is aggressive but comparable to what
category-definers (e.g., Flexport in freight forwarding) achieved within a mid-market slice over a
5–7 year window.

## 3. Five-Year Plan

| Year | Product Milestones | GTM Motion | Headcount (by function) | Geography | Customers | Blended ACV | ARR |
|---|---|---|---|---|---|---|---|
| 1 | AI HS-classification + landed-cost SaaS launches; acquire/partner with a licensed US customs brokerage for filing rights and CBP ABI access | Founder-led sales, 20 design partners, content/SEO around tariff volatility | 15 (Eng 6, Trade/Compliance & licensed brokers 3, Product 2, GTM 3, G&A 1) | US only | 50 | $20k | **$1.0M** |
| 2 | Full self-serve filing via ABI; duty-optimization recommendations (FTA/tariff engineering); ERP/Shopify/NetSuite integrations | Inside sales + channel partnerships with freight forwarders/3PLs; PLG signups from Year-1 SaaS wedge | 45 (Eng 15, Trade/Compliance 10, Product 5, GTM 12, G&A 3) | US + Canada | 400 | $30k | **$12.0M** |
| 3 | Multi-jurisdiction classification (EU TARIC, UK CDS); tariff-scenario simulator for supply-chain redesign; enterprise-tier audit/analytics dashboard | Outbound + embedded partnerships (become the compliance layer inside 3PL/forwarder platforms) | 110 (Eng 30, Trade/Compliance 25, Product 10, GTM 35, G&A 10) | + UK, Germany, Netherlands | 1,400 | $35k | **$49.0M** |
| 4 | Enterprise tier for large 3PLs/brands; FTA-optimization engine; AI audit layer (pre-submission error detection, à la Flexport's auditor) | Enterprise sales team, channel expansion, industry conferences | 220 (Eng 55, Trade/Compliance 55, Product 18, GTM 75, G&A 17) | + Mexico, broader EU | 3,000 | $42k | **$126.0M** |
| 5 | Global multi-jurisdiction AI brokerage; predictive tariff-change alerts; supply-chain re-routing recommendations | Full enterprise motion + self-serve long tail; APAC pilot (Singapore/Vietnam hubs) | 340 (Eng 80, Trade/Compliance 90, Product 25, GTM 115, G&A 30) | US, Canada, Mexico, UK/EU, APAC pilot | 4,700 | $43k | **$202.1M** |

Arithmetic check: Y1 50×$20k=$1.0M; Y2 400×$30k=$12.0M; Y3 1,400×$35k=$49.0M; Y4 3,000×$42k=$126.0M;
Y5 4,700×$43k=$202.1M ≥ $200M target.

## 4. Competition & Moat

**Top 3 competitors:**
1. **Flexport** — digital freight forwarder with an in-house customs brokerage and, as of 2025, an
   AI auditor that audits 100% of entries pre-submission at a 0.2% error rate, and can classify up
   to ~20,000 SKUs/month (Flexport product pages, 2025–26). Well-capitalized first mover in AI
   customs, but focused on its own freight customers, not standalone mid-market brokerage.
2. **Descartes Systems (Sphere/TRAM engine)** — incumbent trade-compliance software vendor
   expanding its proprietary AI classification engine (TRAM) into product classification, planned
   for 2026 rollout. Deep incumbency and data, but legacy UX and enterprise-only pricing/service
   model.
3. **Traditional customs brokers** (e.g., Livingston International, regional/independent brokerages)
   — thousands of small firms running manual, relationship-based workflows; this is the actual bulk
   of the TAM we are displacing, not a single competitor but a long tail with high switching
   friction and no software moat of their own.

**Defensibility:** (a) a proprietary classification/duty-optimization model trained on our own
filing outcomes, customs-authority audit results, and ruling precedents — a data flywheel that
compounds accuracy and defensibility with every filing, hard to replicate without live filing
volume; (b) we hold the actual customs-broker license and surety bonds, so switching means
re-establishing legal liability relationships, not just changing software; (c) deep ERP/3PL
integration and multi-year historical landed-cost data create workflow lock-in; (d) FTA/tariff-
engineering recommendations get more valuable as we see more of a customer's SKU/lane history,
creating account-level network effects.

## 5. Key Risks

1. **Licensing/regulatory scalability (assumption: we can operate as a licensed, AI-assisted
   customs broker across 5+ jurisdictions).** If CBP, UK HMRC, or EU customs authorities restrict
   AI-generated classifications, require human sign-off at a ratio that erases our cost advantage,
   or slow-walk broker licensing in new geographies, the unit economics and expansion timeline
   collapse. **This is the single riskiest assumption** — it is a binary, external, slow-moving
   gate we don't control.
2. **Demand durability (assumption: tariff volatility keeps driving urgent reclassification/duty-
   optimization demand).** If trade policy stabilizes or simplifies materially before Year 3, the
   acute pain that drives Year 1–2 adoption could fade faster than our SaaS-to-brokerage upsell
   motion matures.
3. **Trust-driven switching (assumption: mid-market importers will move liability-sensitive customs
   filings to a new AI-native platform).** Misclassification carries fines and seizure risk, so
   incumbents' relationship trust is sticky; if customers won't switch primary broker-of-record
   despite better tooling, we get stuck as a point-solution SaaS vendor at a fraction of the
   modeled ARR.
