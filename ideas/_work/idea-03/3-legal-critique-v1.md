# InferRoute — Legal & Regulatory Critique v1

Reviewing the plan as counsel retained to find reasons this deal does not close. My conclusion:
InferRoute's core value proposition — sit in the critical path of every enterprise LLM call across
every provider — is also its core legal exposure. Several risks are not "manageable startup risk";
they are structural contradictions between what the product must do to have a moat and what it
must not do to survive a single major incident or a single provider ToS change.

## 1. Regulatory & Licensing

**L1 (Serious) — EU AI Act role confusion.** Section 3's Year-2 "policy engine" (PII redaction,
model allow-lists) and Year-1 "smart routing" are exactly the kind of intervention that can tip
InferRoute from neutral conduit into "provider" or co-deployer under the AI Act's Art. 3
definitions, especially once it actively decides *which* model answers a request. The plan never
addresses this classification question, yet Year-5 (Section 3) explicitly targets financial
services and healthcare verticals — the two sectors where AI Act high-risk obligations bite
hardest.

**L2 (Serious) — Sectoral outsourcing rules.** Bank customers trigger EBA/OCC critical third-party
outsourcing rules (audit rights, exit plans, concentration-risk assessments) that apply not just to
InferRoute but transitively to every LLM provider it routes to. Healthcare customers require BAAs
with InferRoute *and* whichever model providers process PHI that day — impossible to guarantee
under a dynamic router. Section 3 pushes "compliance packs" to Year 4, after the plan already
assumes Year-1–3 revenue from exactly these regulated buyers.

**L3 (Manageable, but flagged) — "FedRAMP-ready" (Section 3, Year 4) is not FedRAMP Authorized.**
Marketing this to federal-adjacent buyers without an actual ATO risks False Claims Act exposure if
any sales rep oversells it, which the plan's aggressive ACV targets incentivize.

## 2. Liability

**L4 (Fatal) — Critical-path outage liability vs. standard SaaS caps.** Section 1 defines
InferRoute as sitting "between enterprise applications and every LLM provider" with failover as a
core feature — i.e., customers will architect it as non-optional infrastructure. A gateway outage
doesn't degrade one feature; it takes down every LLM-dependent workflow at once, for every
customer, simultaneously. No SaaS-standard 12-months-fees liability cap survives contact with a
bank's outaged customer-service AI or a hospital's stalled prior-auth pipeline. The plan contains
no discussion of insurance, indemnification structure, or SLA-credit economics — this is not a
detail to fix later, it's a business-model-defining number.

**L5 (Serious) — Wrong-model routing shifts liability upstream.** "Automatic downgrade-routing…
when a request doesn't need frontier quality" (Section 1) is InferRoute's own algorithmic judgment,
made without the customer or end user in the loop. When a downgraded model produces a worse
answer that causes harm (a misclassified transaction, a bad clinical summary), the customer's
claim runs against InferRoute directly — it made the substitution decision, not the model provider,
and not the customer. This is a foreseeable, product-designed source of negligence claims, not an
edge case.

**L6 (Fatal) — Semantic-cache cross-tenant leakage.** Semantic caching (Section 1) works by
matching *meaning*, not exact keys, across requests — the entire value proposition depends on
generalizing across queries. Nothing in the plan describes strict per-tenant cache partitioning. If
similarity matching ever surfaces Tenant A's cached response (containing A's confidential data) in
response to Tenant B's semantically adjacent query, that is a simultaneous, multi-tenant data
breach triggering GDPR Art. 33/34 notifications across the entire customer base at once — the
gateway architecture converts a single bug into a mass-incident by design.

## 3. IP

**L7 (Serious) — FTO and patent risk.** No freedom-to-operate analysis appears anywhere. Portkey's
acquisition by Palo Alto Networks (Section 4) puts routing/caching IP inside a company with the
budget and incentive to assert patents against smaller gateway competitors as consolidation
continues. LLM routing and semantic-cache patents are an active filing area; InferRoute is building
the exact features being patented around it.

**L8 (Fatal) — The moat requires exactly the data pooling the liability section forbids.** Section
4 concedes routing logic "is not hard to replicate" and stakes the real moat on a "cross-customer
routing/cost model trained on aggregate telemetry… across thousands of production workloads."
That requires ingesting and cross-analyzing customer request data across tenants. But Section 5's
target verticals (financial services, healthcare) and Section 3's compliance roadmap (HIPAA, SOC2)
require strict data segregation and customer-specific confidentiality commitments. You cannot sell
regulated enterprises airtight data isolation and simultaneously build your only defensible moat on
pooling their data. One of these two claims in the plan has to be false.

**L9 (Manageable) — OSS contamination.** LiteLLM (MIT) and Portkey's now-Apache-2.0 core (Section
4) are the obvious references for "Core router" (Section 3, Year 1). No code-provenance or
clean-room process is mentioned; Apache 2.0's patent-termination clause also deserves review before
any patent strategy under L7 is finalized.

## 4. Data & Privacy

**L10 (Fatal) — The cost-savings feature is a transfer-compliance violation generator.** InferRoute
is a sub-processor sitting above a stack of sub-sub-processors (each model provider), each with its
own DPA. "Smart routing" optimizes on cost/latency — meaning an EU customer's request can be
auto-routed to a cheaper US-hosted model instance for savings. That is precisely the Schrems II
transfer-mechanism problem, and it happens automatically, at scale, as the product's central
selling point (Section 1's "guaranteed savings SLA"), not as an occasional edge case. Multi-region
deployment (Section 3, Year 3) is not a fix unless routing logic is contractually and technically
barred from crossing residency boundaries for savings — which undermines the savings pitch.

**L11 (Fatal) — Provider ToS may prohibit the business model outright.** Frontier model providers'
usage policies have historically restricted or required disclosure for resale/intermediary access.
InferRoute's entire pitch — arbitrage cost/quality across providers, including "downgrade-routing"
that steers volume away from a provider's frontier models — is adversarial to the providers it
depends on for API access. Section 5's own Risk #1 acknowledges hyperscalers may build competing
routing natively; the sharper risk is that any single provider simply amends its ToS or throttles
API keys used for cross-provider arbitrage, killing that provider's traffic for every InferRoute
customer overnight, with no contractual recourse.

**L12 (Serious) — Cached PII and erasure rights.** Semantic caching necessarily stores request/
response content, which will contain PII/PHI. GDPR Art. 17 erasure requests require identifying and
purging semantically-linked cache entries — a non-trivial technical requirement nowhere addressed
in the plan.

## 5. Structural/Commercial

**L13 (Serious) — Hyperscaler bundling is a self-admitted top risk with zero legal remedy.**
Section 5 correctly flags this as "the single riskiest assumption," but there is no contractual or
legal lever to prevent AWS/Azure/Google from bundling equivalent routing/failover/spend controls
for free — this is a business risk masquerading as manageable when it is existential and outside
counsel's or the founders' control.

## Summary Table

| # | Objection | Severity |
|---|---|---|
| L1 | EU AI Act provider/deployer role ambiguity | Serious |
| L2 | Bank/healthcare outsourcing rules apply transitively | Serious |
| L3 | "FedRAMP-ready" mislabeling risk | Manageable |
| L4 | Critical-path outage liability exceeds SaaS caps | Fatal |
| L5 | Algorithmic downgrade-routing shifts harm liability upstream | Serious |
| L6 | Semantic-cache cross-tenant leakage = simultaneous mass breach | Fatal |
| L7 | No freedom-to-operate/patent analysis; Portkey now inside PANW | Serious |
| L8 | Moat (data pooling) contradicts promised tenant isolation | Fatal |
| L9 | Unvetted OSS provenance (LiteLLM/Portkey) | Manageable |
| L10 | Cost-routing feature systematically triggers Schrems II transfer violations | Fatal |
| L11 | Business model may violate/invite termination under provider ToS | Fatal |
| L12 | Cached PII vs. GDPR erasure rights unaddressed | Serious |
| L13 | Hyperscaler bundling risk has no legal remedy | Serious |
