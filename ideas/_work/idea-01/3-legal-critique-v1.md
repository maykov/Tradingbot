# SentinelAML — Legal & Regulatory Critique v1

Reviewing the Entrepreneur's plan (`1-entrepreneur-v1.md`) against BSA/AML, model-risk, privacy,
IP, and vendor-risk law. My job is to find why this fails, not to balance the ledger.

## 1. Regulatory & Licensing

**L1 (Fatal).** The entrepreneur's own Section 5, Risk 1 admits the entire thesis depends on
examiners "blessing" ML-driven alert suppression. That is not a risk to monitor — it is the
product. SR 11-7 (and OCC/FDIC/Fed model-risk guidance) puts validation and ultimate
responsibility on the *bank*, not SentinelAML, so every deployment requires the client's own
independent model validation function to re-bless the model annually. There is no path to
"weeks not months" pilots (Section 1) once a real BSA officer has to defend suppressed alerts to
an examiner who can issue a MRA/MRIA. This collapses the wedge's core speed advantage.

**L2 (Serious).** Auto-drafted SAR narratives (Section 1, Section 3 Year 1) run into 31
U.S.C. §5318(g)(2) SAR confidentiality: SARs and underlying information cannot be disclosed
outside narrow statutory channels. Staging draft narratives and evidence citations in a
vendor-hosted system, and using them across model training, risks a confidentiality breach
before the SAR is even filed — a compliance failure of the exact kind the product is sold to
prevent.

**L3 (Serious).** The Year 2-3 UK/EU expansion (Section 3) assumes the "examiner-tested SAR
narrative... built with input from former OCC/FinCEN examiners" moat (Section 4b) travels
internationally. It does not — UK/EU AML regimes (MLR 2017, AMLD/AMLA, FCA/NCA reporting) have
different narrative standards and examiners. The stated moat is jurisdiction-locked, undermining
the international leg of the 5-year plan.

## 2. Liability

**L4 (Fatal).** If a bank misses a SAR because SentinelAML's model suppressed or deprioritized
an alert, and that omission surfaces in an enforcement action (consent order, CMP, criminal
referral — see the scale of the 2024 TD Bank AML case), the bank will pursue SentinelAML for
negligence, breach of contract, and indemnification. Enforcement penalties at this customer tier
run into the tens or hundreds of millions; the plan's own ACVs are $150k-$1M. No SaaS-scale
company can insure or reserve against liability that is 100-1000x its contract value, and the
plan contains zero discussion of E&O coverage, reserves, or indemnification structure.

**L5 (Manageable, but flagged).** A 14-person Year 1 company (Section 3) selling into $1B-$50B
banks' BSA-critical function will struggle to obtain affordable, adequate tech E&O/cyber
coverage at all; underwriters price AML-adjacent tools as high-severity. This is solvable with
capital but is unbudgeted.

**L6 (Fatal).** Year 4's "agentic investigation workflows (auto-close low-risk alerts under model
governance)" (Section 3) has the model — not a qualified compliance officer — disposing of BSA
alerts without human review. FinCEN guidance places SAR determination responsibility on the
institution's compliance function; a fully automated close of what should have been a SAR is the
single most litigation- and enforcement-prone feature on the entire roadmap, and it is scheduled
as a headline milestone, not a cautious pilot.

## 3. IP

**L7 (Serious).** Moat (a) — "proprietary labeled-alert dataset... that compounds model accuracy"
(Section 4) — assumes SentinelAML owns or can reuse each bank's disposition history. Bank
contracts routinely restrict vendor reuse of customer financial data beyond the single client's
engagement, and GLBA/BSA confidentiality constraints (see L9 below) cut against cross-customer
pooling. The moat as described is likely not legally available to build.

**L8 (Serious).** No freedom-to-operate analysis or patent strategy appears anywhere in the plan.
Explainable ML for transaction-monitoring alert scoring is a crowded prior-art space (Actimize,
SAS, Featurespace, Unit21, Hawk AI, Napier AI — the plan's own named competitors, Section 4).
Moat (b) ("regulatory trust... built with former OCC/FinCEN examiners") is not IP at all — it is
reputation and hires, which Napier and Hawk AI are already replicating. There is no legally
defensible, ownable moat identified in the plan.

## 4. Data & Privacy

**L9 (Fatal).** The compounding-data moat (Section 4a) and the Year 5 "real-time
cross-institution risk network (consortium data-sharing)" (Section 3) require pooling multiple
banks' customer and alert-disposition data. This runs directly into GLBA Safeguards Rule limits
on data use, BSA/SAR confidentiality (§5318(g)(2) again — disposition data is often SAR-adjacent),
and each bank's own data-processing agreements. Absent a 314(b)-style safe harbor (which covers
only suspected-crime information sharing between institutions, not general model training) or
bank-by-bank consent, this flagship Year 5 product cannot legally be built as described — and
consent-by-consent negotiation defeats the network-effect economics the plan relies on.

**L10 (Serious).** If SentinelAML's risk scores influence account or transaction decisions about
individuals, FCRA "consumer reporting agency" exposure is plausible and entirely unaddressed.

**L11 (Manageable).** GDPR Art. 22 (automated decision-making) and cross-border transfer rules
apply once UK/EU customers onboard (Year 2-3, Section 3); no DPA/data-residency/transfer
mechanism is mentioned. Solvable with standard vendor tooling, but currently a gap.

## 5. Structural / Commercial Legal Risk

**L12 (Serious).** The 2023 Interagency Guidance on Third-Party Relationships requires banks to
conduct heavy due diligence, ongoing monitoring, and contract for audit/termination/business-
continuity rights before outsourcing a BSA-critical function like transaction monitoring. This
directly extends the sales-cycle risk the entrepreneur already flags as Key Risk 2 (Section 5) —
and, separately, service providers to banks can themselves be examined by federal regulators
under the Bank Service Company Act (12 U.S.C. §1867(c)). A 14-38 person company (Years 1-2
headcount, Section 3) is not built to withstand direct regulator examination across dozens of
bank clients simultaneously.

**L13 (Fatal).** Standard SaaS liability caps (fees paid) are the only liability structure
consistent with the plan's ACV economics ($150k-$1M, Section 2), but bank legal/vendor-risk teams
negotiating a BSA-critical tool will demand indemnification and high/uncapped liability for
regulatory losses traceable to vendor failure (see L4). SentinelAML cannot both win these deals
at the stated price point *and* accept caps that make the tail risk survivable — the commercial
model and the liability reality are in direct conflict, and the plan resolves neither.

**L14 (Serious).** The overlay wedge (Section 1) depends on sitting beside incumbent rules
engines (Actimize/SAS) with no committed data/API access agreement disclosed. Incumbents commonly
restrict integration access to block exactly this kind of overlay competitor; this is a platform-
dependence risk the plan does not name even though it names the incumbents as competitors
(Section 4.1).

## Summary Table

| # | Objection | Category | Severity |
|---|---|---|---|
| L1 | Wedge assumes examiner acceptance of ML alert suppression — self-identified existential risk | Regulatory | Fatal |
| L2 | Auto-drafted SAR narratives risk breaching SAR confidentiality (§5318(g)(2)) | Regulatory | Serious |
| L3 | US-built SAR/examiner moat doesn't transfer to UK/EU expansion | Regulatory | Serious |
| L4 | Vendor liability exposure (enforcement actions) vastly exceeds contract value; no insurance/indemnity plan | Liability | Fatal |
| L5 | Adequate E&O/cyber coverage likely unaffordable at Year-1 scale | Liability | Manageable |
| L6 | Auto-closing BSA alerts without human review (Yr 4) is a litigation/enforcement magnet | Liability | Fatal |
| L7 | Cross-customer data moat likely blocked by bank data-use restrictions | IP | Serious |
| L8 | No FTO analysis; crowded prior art; "moat" is reputation, not IP | IP | Serious |
| L9 | Cross-institution data pooling/consortium (Yr 5) conflicts with GLBA/SAR confidentiality | Data/Privacy | Fatal |
| L10 | Possible unaddressed FCRA "consumer reporting agency" exposure | Data/Privacy | Serious |
| L11 | GDPR Art. 22 / transfer-mechanism gap for EU expansion | Data/Privacy | Manageable |
| L12 | Interagency third-party risk guidance + Bank Service Company Act exam exposure understaffed | Commercial | Serious |
| L13 | Liability caps needed to close deals are incompatible with real tail risk | Commercial | Fatal |
| L14 | No committed data/API access from incumbents the wedge depends on | Commercial | Serious |
