# ClearPath Health — Business Plan v1

## 1. Product & Value Proposition

ClearPath is an AI agent platform that automates prior authorization (PA) end-to-end for hospital
systems, specialty clinics, and MSOs. Agents pull clinical evidence from the EHR (Epic, Cerner,
athenahealth), match it against payer medical-necessity policy, submit the request via payer
electronic-PA (ePA) APIs or portals, track status, and auto-draft appeals with citations when
denied. Customers are revenue-cycle and utilization-management leaders at hospital systems and
high-PA-volume specialty groups (oncology, radiology/imaging, cardiology, ortho/MSK) — specialties
where a single denial can delay six-figure treatment.

**Year-1 wedge:** a "denial-proof submission" agent for the three highest-friction specialties
(oncology, advanced imaging, cardiology), integrated with Epic and the five payers covering the
largest share of a typical hospital's commercial + Medicare Advantage mix. The wedge is narrow by
design — we go deep on evidence-assembly accuracy (matching payer policy criteria line-by-line)
before going broad on specialties, because a single wrong auto-submission erodes trust fast in
healthcare.

## 2. Market Sizing

**TAM:** US prior-authorization administrative spend is estimated at $35B–$55.8B/year, including
staff labor, delay-driven costs, and downstream clinical impact (AMA 2025 Prior Authorization
Physician Survey; CAQH/AHIP data cited in AMA and IDC analyses)
([AMA](https://www.ama-assn.org/practice-management/prior-authorization/fixing-prior-auth-nearly-40-prior-authorizations-week-way),
[IDC](https://www.idc.com/resource-center/blog/the-u-s-healthcare-prior-authorization-crisis-will-agentic-ai-come-to-the-rescue/)).
We take the midpoint, **$40B**, as our TAM.

**SAM (bottom-up):** Restrict to organizations with EHR-API access and PA volume dense enough to
justify software (hospital systems and large multi-specialty/MSO groups), and to the sub-set of
spend actually addressable by an automation layer (submission + appeals labor, not the clinical
delay/denial cost component). **Assumption:** ~60% of the $40B TAM is provider-side administrative
labor addressable by automation → **SAM ≈ $24B**.

**SOM (bottom-up, customer × price):**
- Target customer universe: ~600 multi-hospital health systems in the US (**assumption**, rounded
  from commonly cited AHA counts of ~6,000 hospitals organized into large- and mid-size systems)
  plus ~2,000 large specialty/MSO groups with >5,000 PAs/year — **~2,600 serviceable accounts**
  (**assumption**).
- Year-5 penetration target: 400 customers (~15% of the serviceable base) — **assumption**,
  consistent with a 5-year-old category leader in a fragmented market where incumbents (Cohere
  Health, Rhyme) already prove enterprise willingness to pay.
- Pricing: blended $2–8/auth transaction fee (seed-brief revenue model) plus a platform
  subscription. **Assumption:** average customer ACV of **$500K/yr** (e.g., a mid-size system
  running ~80,000 PAs/yr in our covered specialties × $5/auth = $400K, plus $100K platform fee).
- **SOM = 400 customers × $500K = $200M ARR in Year 5** — 0.83% of the $24B SAM, i.e. plausible
  but requires real execution, not passive market capture.

## 3. 5-Year Plan

| Year | Product Milestones | GTM Motion | Headcount (Eng / Clinical-Product / Sales / CS / Compliance-Ops) | Geography | Target ARR |
|---|---|---|---|---|---|
| 1 | Epic + 5-payer ePA integration; oncology, imaging, cardiology submission agents; manual-review safety net on every auto-submission | Design-partner pilots (6–10 systems), founder-led sales, KOL relationships with UM directors | 12 / 4 / 2 / 2 / 2 (22 total) | 2–3 US regions (Northeast, Southeast) | $3M |
| 2 | Cerner + athenahealth support; appeals-automation agent; denial-reason analytics; SOC 2 Type II | Direct enterprise sales team stood up; referenceable case studies drive inbound | 22 / 8 / 8 / 6 / 4 (48 total) | National US (10+ states) | $15M |
| 3 | 8 specialties covered; payer-side auto-approval partnerships (mirroring Cohere's "trusted provider" model); self-serve tier for mid-market MSOs | Channel partnerships with EHR marketplaces (Epic App Orchard, Cerner Code) and RCM platforms | 40 / 15 / 20 / 16 / 8 (99 total) | Full US coverage | $50M |
| 4 | Predictive "will this get denied" pre-submission scoring; value-based-care analytics add-on; expanded Medicaid MCO coverage | Land-and-expand into existing accounts (new specialties/service lines); regional payer partnerships | 65 / 22 / 38 / 32 / 14 (171 total) | US + early payer-side pilots to widen distribution | $110M |
| 5 | Full-specialty coverage (15+); real-time point-of-care PA (Dragon/ambient-note integration, mirroring Rhyme-Microsoft direction); appeals win-rate guarantee program | Enterprise + mid-market dual motion; MSO/PE roll-up channel | 90 / 28 / 55 / 48 / 20 (241 total) | National US, dominant in top 20 health-system markets | **$200M** |

## 4. Competition & Moat

**Top 3 competitors:**
1. **Cohere Health** — payer-side PA platform, processes 12M+ PA requests/yr for 600K+ providers
   through health-plan customers; raised $90M Series C (May 2025), >$200M total funding; launched
   "Align" to pre-approve trusted providers
   ([MedCity News](https://medcitynews.com/2025/05/healthcare-hospital-insurance-tech-ai/),
   [Modern Healthcare](https://www.modernhealthcare.com/health-tech/ai/mh-prior-authorization-companies-cohere-health-eliseai/)).
   Cohere sells to *payers*, not providers — different buyer, complementary rather than head-to-head,
   but its payer relationships could let it commoditize the provider-side workflow too.
2. **Rhyme (formerly PriorAuthNow)** — largest integrated PA network for providers, 4M+ auths/yr
   across 83 large health systems; October 2025 Microsoft Dragon Copilot partnership for
   point-of-care PA. Rhyme is our closest direct competitor on the provider side.
3. **Availity** — payer-owned clearinghouse (Interactive Care Reviewer) auto-approving common
   procedures for specific payers (e.g., Anthem); broad but shallow, optimized for payer
   convenience rather than provider outcomes.

**Moat:** (1) **Evidence-assembly accuracy data flywheel** — every submission/appeal outcome
(approved, denied, overturned) trains our policy-matching models on payer-specific criteria,
compounding accuracy per payer-specialty pair faster than a generalist competitor without our
volume; (2) **deep EHR + payer API integrations** are high switching-cost, high-effort to
replicate, and become CMS-mandated infrastructure (2026–2027 interoperability rules) that we build
once and lease many times; (3) **provider-side trust** — unlike Cohere (payer-aligned) or Availity
(payer-owned), we are unambiguously the provider's advocate, which matters for hospital system
procurement and for appeals aggressiveness.

## 5. Key Risks

1. **Payer API access assumption.** The plan assumes CMS's 2026–2027 electronic prior-auth
   mandates actually force payers to expose usable, reliable APIs on schedule. If payers slow-walk
   compliance or ship low-quality APIs (a realistic risk given past interoperability rule
   experience), our submission agents degrade to portal-scraping, which is fragile, breaks
   constantly, and caps our unit economics and scale — the single riskiest assumption.
2. **Clinical-accuracy liability tolerance.** The model assumes hospital systems will trust an AI
   agent to assemble and submit clinical evidence with limited human review. One high-profile
   wrong submission or missed appeal deadline causing patient harm could trigger both reputational
   collapse and regulatory/liability exposure that shuts down enterprise sales.
3. **Denial economics compress.** The plan assumes payers keep denying enough claims that
   automation ROI stays obvious. If payer denial rates fall structurally (regulatory pressure, AMA
   advocacy, or payer PR response) or payers themselves automate approvals away entirely (e.g.
   Cohere's "trusted provider" auto-approval trend), the addressable transaction volume — and our
   per-auth revenue line — shrinks faster than we can expand into new specialties or geographies.
