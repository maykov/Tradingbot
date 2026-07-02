# GridPilot — Business Plan v1

## 1. Product & value proposition

GridPilot is a virtual power plant (VPP) platform that aggregates commercial batteries, EV
fleet chargers, and building HVAC/BAS systems into wholesale-market bids and demand-response (DR)
programs, monetizing flexible capacity that today sits idle. **Customers:** C&I property owners
(portfolios of 0.5–10 MW flexible load), commercial EV fleet operators, and battery installers who
white-label us to their end customers; utilities are a channel/co-marketing partner, not the payer.

**Year-1 wedge feature:** a FERC Order 2222-compliant automated bidding engine that ingests live
telemetry from batteries, EV depot chargers, and building management systems and continuously
re-optimizes bids across stacked programs (ISO wholesale energy/ancillary services + utility DR)
in a single site — something incumbents (CPower, legacy DR providers) still do manually or on
multi-week settlement cycles. This "set it and forget it, get paid weekly, see your revenue-share
split live" experience is the wedge that lets us undercut integration time (target: <30 days from
signed contract to first bid) versus 3–6 months for legacy aggregators.

**Revenue model:** 20–30% share of market revenue generated per enrolled site, plus a flat
per-MW-enrolled SaaS platform fee (per seed brief).

## 2. Market sizing

**TAM (bottom-up):** DOE's Virtual Power Plant "Liftoff" analysis finds tripling US VPP capacity
by 2030 would unlock ~$10B/yr in system value and meet ~20% of peak demand [Utility Dive,
utilitydive.com/news/virtual-power-plant-vpp-doe-liftoff-tesla-voltus]. We build our own bottom-up
figure: DOE estimates ~200 GW of technical DER flexibility potential in the US by 2030
(**assumption**, extrapolated from the "triple current ~65 GW enrolled" framing in the same
report). At an **assumption** blended market value of $150k/MW-yr (capacity + energy + ancillary
service payments, benchmarked against CPower managing 5.3 GW of DER capacity nationally
[Latitude Media, latitudemedia.com/news/cpowers-new-record-year-delivers-yet-another-milestone-for-vpps]),
TAM = 200 GW × $150k/MW-yr = **$30B/yr by 2030**. This brackets the seed brief's >$20B/yr guess
and the global VPP software market forecast of $2.5B (2025) growing toward $40B by 2035 at a
~32% CAGR [openpr.com/news/4547704].

**SAM:** We exclude utility-owned/residential-only VPPs (Tesla, Sunrun-style behind-the-meter
programs) and ISOs without live FERC 2222 aggregation rules yet. **Assumption:** independent
third-party-addressable C&I + fleet flexibility is ~40% of TAM = 200 GW × 0.40 = 80 GW, valued at
the same $150k/MW-yr = **$12B/yr SAM**, concentrated in the ISOs already implementing 2222
(CAISO, PJM, ERCOT, NYISO, MISO, ISO-NE).

**SOM (year 5):** Target 3,150 MW enrolled capacity from ~1,800 customer sites averaging 1.75 MW
each (**assumption**, mix of C&I battery + EV depot + HVAC-flex sites). Revenue per MW-yr to
GridPilot: **assumption** $65,000, blending a 25% revenue share of the $150k/MW-yr wholesale/DR
value plus a ~$5–8k/MW SaaS fee — benchmarked against Voltus, which reports $35M revenue managing
7,000 MW of DERs (~$5k/MW today) [LeadIQ, leadiq.com/c/voltus-inc], adjusted up for our
higher-margin revenue-share-plus-SaaS mix versus Voltus's pure-brokerage model.
Arithmetic: 3,150 MW × $65,000/MW-yr = **$204.75M ARR**, ≈1.7% of SAM — a defensible share for a
focused new entrant across 6 ISOs in 5 years.

## 3. 5-year plan

| Year | Product milestone | GTM motion | Headcount (by fn: Eng/Data-Markets/Sales-CS/Ops-G&A) | Geography | ARR target |
|---|---|---|---|---|---|
| 1 (2027) | Launch bidding engine; ISO aggregator certification; battery+HVAC telemetry integrations | Direct pilot sales (5 anchor customers) + 2 battery-installer channel deals | 18 (9/4/3/2) | CAISO, ERCOT | $1.5M (~25 MW) |
| 2 (2028) | Add EV fleet depot module; automated settlement & revenue-share billing | Scale channel (3 installer partners); build inside sales team | 45 (20/8/12/5) | + PJM, NYISO | $12M (~200 MW) |
| 3 (2029) | Predictive multi-market bidding AI; utility white-label co-branded DR programs | Utility channel partnerships; fleet OEM integrations | 110 (42/18/38/12) | + MISO, ISO-NE; EU pilot (UK) | $42M (~700 MW) |
| 4 (2030) | Cross-ISO portfolio optimization; large-load/datacenter flexibility module | Enterprise land-and-expand; national utility MOUs | 220 (75/30/85/30) | Full US 6-ISO coverage; UK/Germany launch | $105M (~1,700 MW) |
| 5 (2031) | Autonomous multi-market orchestration; revenue-guarantee/insurance product | Scaled direct + channel; international expansion | 380 (120/45/165/50) | US nationwide + UK/EU | **$205M (~3,150 MW)** |

## 4. Competition & moat

**Top 3 competitors:**
1. **CPower** — largest incumbent DR aggregator, 5.3 GW under management [Latitude Media], deep
   utility relationships but legacy manual/batch settlement systems and slow onboarding.
2. **Voltus** — software-forward aggregator, $35M revenue on 7,000 MW managed [LeadIQ], broad
   horizontal DR/wholesale coverage but thin per-MW economics and shallow device-level telemetry
   integration (works mostly at the meter, not the asset).
3. **Leap Energy** (partnered with Enel X as of Dec 2025 [Enel North America,
   enelnorthamerica.com/about-us/newsroom/search-press/press/2025/12/leap-vpps]) — API-first
   market-access layer for OEMs/installers, strong developer experience but relies on partners for
   end-customer relationships and lacks an integrated bidding-optimization product of its own.

**Moat:** (1) **Data network effects** — every enrolled site's telemetry and settlement outcome
trains our multi-market bidding-optimization model, improving forecast accuracy and the revenue
share we can offer, which competitors with less enrolled capacity cannot match. (2) **Economic
lock-in** — revenue-share contracts with multi-year enrollment terms create high switching costs
once a site's bidding history and BMS/EMS integration are live. (3) **Registration/certification
moat** — ISO aggregator registration and asset-level telemetry certification take 6–12 months per
market; being first to certify across 6 ISOs compounds into a lead late entrants must replicate
one market at a time. (4) **Channel exclusivity** with battery installers and fleet OEMs, locking
distribution before incumbents extend deeper into asset-level integration.

## 5. Key risks

1. **FERC 2222 rollout stalls or stays patchy.** Our SAM assumes 6 ISOs have live, workable
   aggregation rules by year 3. If implementation drags (litigation, ISO tariff delays), enrolled
   capacity and thus ARR growth slow sharply — this is the single riskiest assumption underlying
   the entire plan.
2. **Wholesale/DR market value per MW stays well below $150k/yr.** Falling battery costs could
   compress capacity and energy-arbitrage prices faster than flexible-load demand (from
   AI-datacenter growth) absorbs it, shrinking our per-MW revenue and breaking year-5 unit
   economics even at full enrollment targets.
3. **Onboarding velocity fails to scale.** The wedge promise (<30-day integration) depends on
   standardized APIs across a fragmented landscape of BMS, EMS, and EV charging hardware. If
   device-level integration remains bespoke per vendor, CAC and time-to-revenue balloon, and we
   cannot reach 1,800 enrolled sites by year 5.
