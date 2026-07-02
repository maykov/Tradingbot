# InferRoute — Legal Review v2 (Round 2)

The v2 re-architecture (customer-VPC fail-open data plane, per-tenant caching, BYOK, residency-
constrained routing, moat without customer-content pooling) is a genuine structural response, not
cosmetic redlining. It converts InferRoute's liability profile from "hosted critical-path SaaS" to
"deployed software plus hosted control plane" — a materially better legal posture. It also
introduces new problems of its own (Section 2). No objection I ranked Fatal remains open.

## 1. Objection-by-Objection Status

**L1 — AI Act role. MITIGATED.** Customer-authored routing policies plus decision logs support the
"tooling to the deployer" position (v2 §1, L1). But positioning is argument, not safe harbor: the
"benchmark-trained router v2" (v2 §3, Y4) makes model-selection recommendations that customers
will rubber-stamp, and regulators look at substance over contract labels. Retaining AI Act counsel
in Y1 is the right hedge; classification risk persists until guidance matures.

**L2 — Sectoral outsourcing. MITIGATED.** Pinned static model lists for regulated customers,
compliance packs pulled to Y2, audit rights and exit plans as standard exhibits (v2 §1, L2) are the
correct mechanics, and regulated revenue is no longer assumed before they exist. Residual: BAA
coverage across the pinned provider set depends on providers signing downstream BAAs on the
customer's terms — outside InferRoute's control.

**L3 — FedRAMP language. RESOLVED.** Removed outright.

**L4 — Critical-path outage liability. MITIGATED (Fatal → Manageable).** The customer-VPC,
stateless, fail-open data plane (v2 §1, L4) genuinely eliminates the mass-simultaneous-outage
scenario, and the 12-month cap is defensible for deployed software the customer operates. Residuals:
(a) a bad *update* pushed to 800 data planes recreates correlated failure — see N2; (b) the $10M
E&O limit and premium are unvalidated assumptions; (c) fail-open creates a new exposure — see N1.

**L5 — Downgrade-routing liability. MITIGATED.** Substitution now occurs only within
customer-approved equivalence classes with a conservative default (v2 §1, L5). Liability shifts to
the customer's policy choice — but InferRoute supplies the shadow-eval evidence the customer relies
on. Negligent-evidence claims (our benchmarks said the cheap model was equivalent; it wasn't)
replace negligent-routing claims. Smaller, insurable, but not zero.

**L6 — Cross-tenant cache leakage. RESOLVED.** Per-tenant namespaces, per-tenant keys, and physical
cache placement in the customer's VPC (v2 §1, L6) make cross-tenant matching architecturally
impossible rather than policy-prevented. This is the correct fix; the honest savings-SLA
recalibration confirms they understood the tradeoff.

**L7 — FTO/patent risk. STILL OPEN.** Budgeting $150K for an FTO analysis (v2 §1, L7) is process,
not resolution. The risk is unchanged until the analysis returns clean — and PANW/Portkey's
portfolio incentives are unaffected by InferRoute's budget line. Severity remains Serious.

**L8 — Moat vs. isolation contradiction. RESOLVED (legally).** Dropping the customer-content-trained
model in favor of own-benchmark data, opt-in metadata-only telemetry with regulated customers
defaulted out, and workflow lock-in (v2 §1, L8) removes the legal contradiction. The plan concedes
the moat is weaker — that is now a commercial question for the finance reviewer, not a legal defect.
One caveat feeds N3 below.

**L9 — OSS contamination. RESOLVED.** Clean-room policy and provenance scanning from first commit.

**L10 — Schrems II. MITIGATED.** Residency as a hard optimizer constraint, within-region savings
SLAs, and explicit SCC/DPF configuration for any cross-region route (v2 §1, L10) is the right
design. Residuals: "EU-hosted endpoint" of a US-parent provider does not fully neutralize Schrems
II/CLOUD Act arguments — EU customers' DPO reviews will still probe this; and the constraint is a
design commitment that must survive every future optimizer change. Enforceable by architecture
review, hence Mitigated, not Resolved.

**L11 — Provider ToS. MITIGATED; rebuttal largely accepted on the merits.** BYOK is the correct
structural answer: with customers holding their own provider contracts and keys, reseller/
intermediary clauses do not attach, and a provider cannot terminate "InferRoute traffic" without
terminating its own enterprise customers. The LiteLLM/Portkey precedent is real evidence that the
deployed-gateway category is tolerated; I accept that a category-wide ban is commercially
self-defeating and properly treated as monitored risk. Two residuals keep this above Resolved:
(a) providers can still amend ToS to restrict *automated steering/arbitrage* short of banning
gateways; (b) the continuous benchmarking that now powers the moat has its own ToS exposure (N3).

**L12 — Cached PII/erasure. MITIGATED.** Short TTLs, PII-exclusion defaults, erasure API, and
customer-as-storage-controller (v2 §1, L12) address the frame. Residual: PII detection is
probabilistic (missed PII gets cached anyway) and "semantic neighborhood" purges are hard to prove
complete to a regulator. Acceptable engineering risk.

**L13 — Hyperscaler bundling. STILL OPEN.** Correctly acknowledged as a business risk with no legal
remedy (v2 §1, L13; §2 #3). The cross-provider-neutrality repositioning is a sensible commercial
answer, but nothing legal has changed. Remains Serious, owned by the business.

## 2. New Issues Introduced by v2

**N1 (Serious) — Fail-open bypasses the compliance controls.** When the data plane fails open,
traffic passes "unmodified" (v2 §1, L4) — meaning PII redaction, model allow-lists, and residency
constraints silently stop enforcing. For a bank, a fail-open compliance control is arguably a
design defect. Fix: per-policy-class fail-closed configuration (compliance-critical routes block;
cost-optimization routes pass through), documented and customer-elected in the order form.

**N2 (Serious) — Deployed-software obligations across 800 VPCs.** Customer-VPC deployment creates
version sprawl, a duty of prompt CVE disclosure and patching, correlated-failure risk from pushed
updates, and support access into customer environments (security questionnaires, background
checks, access logging). Contracts need clear update/patch SLAs, customer patching obligations,
and access-scoping terms. Manageable but must be in the Y1 contract templates, not discovered at
first enterprise redline.

**N3 (Manageable) — Benchmarking the providers may itself breach provider ToS.** The new moat runs
"continuous benchmarking of every provider/model" (v2 §1, L8). Several provider terms restrict
using outputs to develop competing products or publishing benchmark results without consent.
Internal routing use is defensible; publishing comparative results or marketing the router model
needs ToS review per provider.

**N4 (Manageable) — Insurance assumptions unvalidated.** $10M tech E&O at $150–300K/yr is asserted,
not quoted. Cyber markets price semantic-caching AI intermediaries conservatively; get binding
quotes before the number appears in any board deck.

## 3. Residual-Risk Summary (for the Board)

The v2 architecture removes the plan's legally fatal defects: no cross-tenant cache, no
customer-content data pooling, no token resale, no unconstrained cross-border routing, and no
hosted single point of failure in the inference path. What remains is a normal-for-category risk
book: an unperformed FTO analysis against a well-funded acquirer of a direct competitor (L7), an
unhedgeable hyperscaler bundling risk (L13), AI Act classification uncertainty pending guidance
(L1), and two self-inflicted items from the re-architecture — fail-open mode must not be allowed
to bypass compliance controls (N1), and deployed-software patching/support obligations must be
contractually engineered in Year 1 (N2). Conditioned on the FTO analysis returning clean, binding
insurance quotes, and fail-closed policy options shipping in v1 contracts, this plan is legally
financeable.

## 4. Status Table

| # | Objection | Original Severity | Status |
|---|---|---|---|
| L1 | AI Act role ambiguity | Serious | Mitigated |
| L2 | Sectoral outsourcing rules | Serious | Mitigated |
| L3 | FedRAMP mislabeling | Manageable | Resolved |
| L4 | Critical-path outage liability | Fatal | Mitigated |
| L5 | Downgrade-routing liability | Serious | Mitigated |
| L6 | Cross-tenant cache leakage | Fatal | Resolved |
| L7 | FTO/patent risk | Serious | Still open |
| L8 | Moat vs. isolation contradiction | Fatal | Resolved |
| L9 | OSS contamination | Manageable | Resolved |
| L10 | Schrems II cross-border routing | Fatal | Mitigated |
| L11 | Provider ToS termination | Fatal | Mitigated |
| L12 | Cached PII / erasure | Serious | Mitigated |
| L13 | Hyperscaler bundling | Serious | Still open |
| N1 | Fail-open bypasses compliance controls | Serious (new) | Open |
| N2 | Deployed-software support/patch obligations | Serious (new) | Open |
| N3 | Benchmarking may breach provider ToS | Manageable (new) | Open |
| N4 | Insurance assumptions unvalidated | Manageable (new) | Open |
