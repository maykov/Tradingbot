# ClearPath Health — Entrepreneur v2 (Response to Finance & Legal Review)

## 1. Responses to Legal Objections

**L1 (Fatal — ERISA gap in CMS-mandate thesis): Changed, with a partial rebuttal.**
Change: Years 1–3 now target the mandate-covered book — Medicare Advantage, Medicaid managed
care, and exchange QHPs — and we select beachhead customers by payer mix (MA/Medicaid-heavy
systems in FL, AZ, TX; safety-net and senior-focused MSOs), not by commercial volume. Commercial
ERISA volume moves to a Year 3–5 expansion, served in "copilot mode" (below). Partial rebuttal:
the national ASO administrators (UHC, Elevance, Aetna, Cigna) run one UM/PA infrastructure across
insured and self-funded books; APIs built for CMS-0057-F compliance will, in practice, be
extended to commercial lines because maintaining two intake stacks is costlier than one — but we
no longer *depend* on that, we treat it as upside. The "why now" is restated honestly: the
mandate opens the MA/Medicaid wedge; commercial follows payer economics, not law.

**L5 (Fatal — FCA exposure designed into "denial-proof" product): Changed — product reframed and
controls engineered in.**
The "denial-proof submission" positioning is dead. The product is now **"complete-and-accurate
first submission"**: (a) every evidence element in a submission is a verbatim, provenance-linked
citation to the chart — the system is architecturally incapable of asserting clinical facts
without a chart pointer; (b) a licensed clinician at the customer attests to each submission
before it leaves (this is also our L2 answer); (c) full immutable audit trail per submission;
(d) a compliance program with an FCA-trained compliance officer hired in Year 1, not Year 4;
(e) the Year-5 "appeals win-rate guarantee" is deleted — legal is right that guaranteeing
outcomes creates a gaming incentive. We sell time saved and completeness, never approval rates.

**L3 (Fatal Yrs 1–2 — portal scraping / ToS / CFAA): Changed — scraping is removed from the
roadmap entirely.**
Years 1–2 use only sanctioned channels: (a) X12 278 transactions via established clearinghouses
(Availity, Change/Optum) — the legally boring rail that already exists; (b) Da Vinci FHIR ePA
pilots with payers who ship early; (c) where a payer is portal-only, **copilot mode**: ClearPath
assembles the evidence packet and pre-fills nothing — the customer's own authorized staff member
reviews and submits through their own credentials. Slower and lower-priced, but zero
CFAA/ToS exposure. Full automation on a given payer unlocks only when that payer's API is live.
This is the single biggest driver of the reduced Y1–Y2 ARR ramp in §3.

**L2 (Serious — CPOM/UR licensure): Changed.** Clinician-attestation (L5 control (b)) keeps
medical-necessity judgment with the customer's licensed staff; ClearPath is a documentation and
transaction tool. We additionally budget a state-by-state private-review-agent licensure survey
in Year 1 and register where counsel advises even under the conservative reading. Regulatory
counsel is a named Year-1 hire (see revised G&A headcount).

**L4 (Serious — patient-harm liability): Changed.** Budgeted specialty coverage (managed-care
E&O / miscellaneous medical liability, not vanilla tech E&O) from Year 1 — modeled at 1.5–2% of
revenue (**assumption**). Clinician attestation shifts the standard-of-care locus to the
provider; our indemnity exposure is negotiated, capped where possible, and insured where not.
We accept L11 (mutual indemnification) as a cost of doing business and price it in.

**L6 (Serious — moat not legally defensible): Partially rebutted, partially changed.** Conceded:
the data flywheel is not IP. Rebuttal: our defensibility was always three-legged (Sec. 4 of v1),
and legs 2–3 — deep integration switching costs and provider-side alignment — survive. Cohere's
12M auths are *payer-side* UM decisions, not provider-side evidence-assembly data; the datasets
are not substitutes. Change: FTO analysis in Year 1; provisional patents on the
provenance-linked evidence-assembly architecture where patentable.

**L7 (Serious — BAA chains block cross-customer training): Changed.** Default architecture is
per-customer model adaptation under each BAA, with cross-customer learning only from
(a) de-identified data under HIPAA expert determination and (b) non-PHI artifacts — payer policy
libraries, denial-reason taxonomies, submission-format templates — which are not patient data at
all. The flywheel is now mostly a *payer-knowledge* flywheel, not a PHI flywheel. This is
honestly a weaker moat; §4 of v1 is amended accordingly.

**L9 (Serious — EHR gatekeeping): Changed, with rebuttal.** Rebuttal: the 21st Century Cures Act
information-blocking rules constrain Epic's ability to cut off apps performing legitimate
treatment/operations data access. Change: we still don't bet on goodwill — Year 1 ships on FHIR
APIs plus one clearinghouse rail so no single vendor approval is load-bearing, and Cerner is
pulled forward to Year 1–2.

**L10 (Serious — payer countermeasures): Rebutted with a repositioning.** A complete, verbatim-
cited, clinician-attested submission *reduces* payer review cost — it is not adversarial the way
"denial-proof" was. Post-reframe (L5), payers' rational response to clean submissions is
auto-approval, which is exactly the Cohere/Align direction. We add it as a monitored risk with
API-rate-limit terms negotiated into payer connectivity agreements, but the adversarial premise
legal critiqued has been removed at the product level.

**L8, L11 (Manageable): Accepted** — reflected in the enlarged compliance and G&A headcount below.

## 2. Responses to Finance Sanity Checks

1. **6x revenue/employee jump:** Conceded. Fixed from both ends: Y5 headcount rises 241→430
   (compliance-ops and CS now scale with auth volume) and Y5 ARR drops $200M→$160M.
   Revenue/employee goes $91K (Y1: $2M/22) → $372K (Y5: $160M/430), a 4.1x gain, of which the
   step-up is explained: copilot mode (labor-heavy) dominates Y1–Y2 and converts to API
   automation as CMS-0057-F APIs go live Jan 2027 (mid-Y2 onward). Efficiency gain is now an
   explicit function of a dated external event, not hand-waving.
2. **Y2 logo velocity vs. sales cycles:** Conceded. Y2 is now 18 customers (12 net-new), Y2 ARR
   $7M. First AEs hired mid-Y1 so Y2 closings come from a full-year-old pipeline.
3. **AE productivity:** Y3 is 42 net-new logos on ~22 reps ≈ 1.9 logos/rep/yr fully ramped —
   inside the 2–4 enterprise-health-IT norm with ramp time.
4. **Compliance-Ops vs. volume:** Compliance-Ops now 4→80 across five years and clinician
   attestation caps ClearPath's unreviewed-submission exposure at zero by design.
5. **SOM vs. coverage timing:** National payer-API coverage arrives with the 2027 mandate
   (mid-Y2), and 12+ specialties by Y4 — footprint now precedes the customer-count targets.
6. **Missing G&A line:** Added as its own column (legal, finance, HR, exec).
7. **Funding implication:** slower ramp + bigger compliance org pushes realistic total capital
   from finance's $120–130M to **~$150M** (**assumption**); we accept the extra dilution rather
   than the legal exposure.

## 3. Revised 5-Year Plan

| Year | Product Milestones | GTM | Headcount (Eng/Clin-Prod/Sales/CS/Compliance-Ops/G&A = Total) | ARR |
|---|---|---|---|---|
| 1 | Copilot mode (evidence assembly + clinician attestation); X12 278 rail; Epic FHIR + Cerner FHIR; FTO + UR-licensure survey; compliance officer hired | 5 MA/Medicaid-heavy design partners (FL/AZ/TX); AEs hired mid-year | 10/3/2/2/2/3 = 22 | $2M |
| 2 | First payer-API automations as CMS-0057-F APIs land (Jan 2027); appeals drafting w/ attestation; SOC 2 II + HITRUST started | Direct sales off Y1 references; MA/Medicaid segment focus | 20/7/8/8/8/9 = 60 | $7M |
| 3 | 8 specialties; automation rate >50% of volume; de-identified benchmarking product | Land-and-expand; clearinghouse channel partnerships | 35/12/22/25/20/16 = 130 | $28M |
| 4 | 12+ specialties; commercial/ERISA expansion in copilot mode + early voluntary commercial APIs; pre-submission denial-risk scoring (decision support only) | Enterprise + mid-market dual motion | 60/20/45/60/45/30 = 260 | $75M |
| 5 | Full specialty coverage; point-of-care PA via ambient-documentation integrations | National; MSO/PE roll-up channel; payer auto-approval partnerships | 90/28/70/110/80/52 = 430 | **$160M** |

**Year-5 ARR is $160M, not $200M.** That is the honest number after removing scraping-dependent
Y1–Y2 revenue, slowing logo velocity to defensible sales cycles, and pricing in the compliance
build. Path to $200M extends into Year 6 via the commercial/ERISA book as ASO administrators
extend APIs.

## 4. Revised Market Sizing (deltas only)

- TAM unchanged: $40B midpoint of $35–55.8B (AMA/IDC, v1 §2).
- **SAM cut:** mandate-covered payer volume (MA, Medicaid MCO, QHP) ≈ 40% of a typical system's
  PA mix (**assumption**) → near-term SAM = $24B × 40% ≈ **$10B**, expanding toward $24B as
  commercial APIs arrive voluntarily.
- **SOM:** 300 customers by Y5 (was 400) × $533K blended ACV (**assumption**; copilot-mode ACVs
  ~$300K, full-automation ~$600K) ≈ **$160M** = 1.6% of near-term SAM.

## 5. Changelog

1. Killed "denial-proof" positioning, appeals win-rate guarantee, and all portal scraping (L5, L3).
2. Re-aimed Years 1–3 at MA/Medicaid-heavy providers; ERISA commercial is upside, not thesis (L1).
3. Added clinician attestation, provenance-linked citations, Year-1 compliance officer,
   specialty liability insurance, UR licensure survey, FTO analysis (L2, L4, L5, L6).
4. Rebuilt moat around integrations + payer-knowledge flywheel; PHI flywheel dropped (L6, L7).
5. Cut Y5 ARR $200M→$160M; headcount 241→430 with G&A column; capital need ~$150M (Finance 1–7).
