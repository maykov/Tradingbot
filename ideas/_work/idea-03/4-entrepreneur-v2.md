# InferRoute — Entrepreneur Response v2

## 1. Responses to Legal Objections

### Fatals

**L4 — Critical-path outage liability (CHANGE).** We re-architect into a split control/data plane.
The data plane (routing proxy) ships as a customer-deployed component (VPC/on-prem, stateless,
horizontally scaled in the customer's own infra) with **fail-open passthrough**: if InferRoute
logic fails, traffic passes directly to the customer's default provider unmodified. InferRoute's
hosted control plane (policies, analytics) can be down without blocking a single inference call.
Contractually: standard 12-month fee cap holds because the customer runs the data plane; we add
tech E&O/cyber insurance ($10M limit Y1, scaling; **assumption** ~$150-300K/yr premium) and
SLA-credit remedies scoped to the control plane. Outage liability becomes an availability-zone
problem in the customer's own cloud, not a mass simultaneous outage of our SaaS.

**L6 — Semantic-cache cross-tenant leakage (CHANGE).** Caching is **hard-partitioned per tenant by
design**: per-tenant embedding namespaces, per-tenant encryption keys, and — because the data plane
is customer-deployed (L4 fix) — the cache physically lives in the customer's VPC. Cross-tenant
similarity matching is architecturally impossible, not policy-prevented. Cache hit-rates come from
within-tenant repetition (support bots, RAG pipelines repeat heavily), which is where the empirical
savings are anyway. This slightly lowers the cache-savings ceiling; the savings SLA is recalibrated
on within-tenant hit-rates only.

**L8 — Moat requires forbidden data pooling (CHANGE — moat redefined).** We drop the
cross-customer telemetry model trained on customer content. The revised moat: (a) a
**public-workload router model** trained on our own continuous benchmarking of every
provider/model against open eval suites and synthetic task batteries — our data, no customer
content, refreshed daily as providers ship updates; (b) customers may **opt in** to contribute
schema-free aggregate metadata only (model ID, latency, cost, task-category tag, thumbs-up rate —
no prompts, no completions), with regulated customers defaulted out; (c) workflow lock-in: budgets,
approval chains, and finance reporting run through InferRoute (unchanged). Isolation promises and
the moat no longer conflict; the moat is somewhat weaker and we say so — defensibility now leans
more on (c) plus compliance depth (see L2).

**L10 — Schrems II / cross-border routing (CHANGE).** **Residency is a hard constraint, not a
preference,** in the routing optimizer from day one: every request carries a data-residency tag,
and the optimizer selects the cheapest model *within* the permitted region/transfer-mechanism set
(EU requests route among EU-hosted endpoints — Azure EU, Bedrock eu-central, Mistral, etc.).
Savings SLAs for EU customers are quoted within-region; the pitch narrows but survives, because
intra-EU price dispersion across providers still exists (**assumption**). Cross-region routing
requires an explicit customer-signed transfer basis (SCCs/DPF) configured per route. The
customer-deployed data plane (L4) also keeps request content in the customer's region by default.

**L11 — Provider ToS termination (CHANGE + partial rebuttal).** We adopt a strict **BYOK
(bring-your-own-key) model**: customers hold direct contracts and API keys with each provider;
InferRoute is deployed software that the *customer* uses to allocate *its own* traffic across *its
own* accounts. We never resell tokens, never pool keys, never sit as merchant of record — so
reseller/intermediary ToS clauses don't attach, and no provider can cut off "InferRoute traffic"
without cutting off its own direct enterprise customers. Rebuttal portion: this is the established,
unchallenged operating model of LiteLLM and Portkey's enterprise deployments today. Residual risk
(a provider bans third-party gateways outright) would hit the whole category and its own customers'
tooling choices — commercially self-defeating; we accept it as monitored risk.

### Serious

**L1 — AI Act role (CHANGE).** Routing policies are **customer-authored**: the customer defines
model equivalence classes and constraints; InferRoute executes them and logs every decision. We
position as tooling to the deployer, not provider/co-deployer; we retain EU AI Act counsel in Y1
(budgeted $250K, **assumption**) and ship decision-log/transparency artifacts as a feature.
**L2 — Sectoral outsourcing (CHANGE).** Compliance packs move from Y4 to Y2; regulated customers
get **pinned static model lists** (no dynamic routing outside a pre-approved, BAA/outsourcing-
diligenced provider set), sub-processor transparency, audit rights, and exit plans as standard
contract exhibits. Regulated-vertical revenue is no longer assumed before these exist.
**L5 — Downgrade-routing liability (CHANGE).** Downgrade-routing only occurs within
customer-defined equivalence classes, backed by shadow-eval evidence the customer reviews and
approves. The substitution decision is contractually the customer's policy; we supply the evidence
and the audit log. Default mode ships conservative (no downgrade without explicit policy).
**L7 — FTO (CHANGE).** FTO analysis on routing/semantic-caching claims budgeted in Y1 ($150K,
**assumption**) before feature-naming and patent filings; monitor PANW/Portkey portfolio.
**L12 — Cached PII/erasure (CHANGE).** Cache design adds: configurable short TTLs (default 24h),
PII-detected requests excluded from cache by default, and an erasure API that purges by tenant,
user-ID tag, and semantic neighborhood. Customer-VPC cache placement makes the customer the
storage controller.
**L3 (CHANGE):** all "FedRAMP-ready" language removed until an actual ATO path is funded.
**L9 (CHANGE):** clean-room policy plus OSS-provenance scanning (no LiteLLM/Portkey code) from
first commit. **L13:** acknowledged — it is a business risk; see finance response #2 below.

## 2. Responses to Finance Sanity Checks

**#1 S&M gap ($7.5M).** Accepted. Revised plan adds an explicit non-headcount demand-gen budget
($1M Y1 → $8M Y5) and raises Sales/CS headcount (see table). The revised, lower ARR ramp also
shrinks the required net-new bookings.

**#2 (their #3) SOM vs. Datadog/Snowflake benchmarks.** Accepted. Datadog/Snowflake took 8-10
years against no free OSS incumbent; we face LiteLLM plus hyperscaler bundling. Year-5 revised to
**800 customers (5.3% of the 15,000-account SAM) at $180K blended ACV = $144M ARR**. That is the
honest number; $200M by Y5 required believing we out-execute the best infra companies ever built
while fighting free alternatives.

**#3 (their #4) Moat vs. hyperscaler bundling.** Reconciled by repositioning: we concede the
single-cloud governance surface to hyperscalers and stake the moat on **cross-provider
neutrality** — AWS will never be the trusted system of record for a customer's Azure/OpenAI/
Anthropic spend, exactly as CloudWatch never displaced Datadog for multi-cloud observability.
The L8/L2 pivot (isolation-first, compliance-deep gateway for regulated enterprises) additionally
targets the segment hyperscaler bundles serve worst.

**#4 (their #5) ACV decomposition under >90% price decline.** ACV = platform fee + (routed spend ×
take rate). Y5 blended $180K = **$105K platform fee + ($3M avg managed spend × 2.5% take rate =
$75K)**. Holding $3M managed spend per account while unit prices fall ~90% requires ~10-20x token
volume per account over 5 years — plausible only because agentic workloads multiply tokens per
task (**assumption**, the load-bearing one). Hedge: the platform fee (58% of Y5 ACV) is
volume-insensitive, and take rate is modeled compressing 3.5% → 2.5%. If volume grows only 5x,
usage revenue halves and Y5 ARR ≈ $114M.

**#2 (their #2) Sales cycle vs. rep ramp.** Y2 target cut to $11M; Y2 sales team is 8 quota
reps + PLG self-serve tier explicitly modeled at 20% of new bookings (**assumption**).

## 3. Revised 5-Year Plan

| Year | Product Milestones | GTM | Headcount (Eng/S&M+CS/G&A) | Geography | Demand-gen $ | ARR |
|---|---|---|---|---|---|---|
| 1 | Customer-VPC data plane w/ fail-open; per-tenant cache; residency-constrained router; spend console; SOC2-I; FTO + AI Act counsel | Founder-led; 10 design partners | 14/5/4 (23) | US | $1M | $2M |
| 2 | Policy engine; pinned-model regulated mode + BAA program; self-serve tier; SOC2-II | 8 reps + PLG (20% of bookings) | 24/20/7 (51) | US+UK | $3M | $11M |
| 3 | EU region + residency packs; FinOps integrations; eval-evidence workflow for downgrade policies | Enterprise AEs; SI partners | 40/38/13 (91) | +EU | $5M | $36M |
| 4 | Benchmark-trained router v2; fin-services & healthcare compliance packs GA | Land-and-expand; analyst relations | 55/60/20 (135) | +APAC | $7M | $81M |
| 5 | Agentic-workload cost governance; opt-in telemetry network | Global enterprise + renewals engine | 70/85/28 (183) | US/EU/APAC | $8M | **$144M** |

Customers: 25 / 100 / 280 / 520 / 800. Blended ACV: $80K / $110K / $130K / $155K / $180K.
$200M ARR lands in **Year 6-7** on this curve (NRR 115% + ~250 adds/yr), not Year 5.

## 4. Revised Market Sizing — Deltas Only

- TAM/SAM unchanged ($3.3B / $2.25B/yr).
- **SOM: $200M → $144M** (800 × $180K; penetration 6.7% → 5.3% of SAM accounts).
- ACV now decomposed (platform fee + take rate × managed spend) per finance #4; usage take rate
  modeled compressing 3.5% → 2.5%.
- EU savings-SLA revenue haircut ~10% of EU usage revenue (**assumption**) from residency-
  constrained routing (L10).

## 5. Changelog

1. Architecture: customer-VPC, fail-open data plane; per-tenant cache — resolves L4, L6, and most
   of L12; converts liability profile to deployed-software norms.
2. Commercial model: strict BYOK, no token resale — resolves L11.
3. Moat rebuilt on own benchmarking data + opt-in metadata + workflow lock-in — resolves L8;
   moat honestly weaker, compensated by compliance-depth positioning.
4. Residency-constrained routing from day one — resolves L10; EU savings pitch narrowed.
5. Regulated-vertical compliance moved Y4 → Y2; customer-authored routing policies — addresses
   L1, L2, L5.
6. Y5 ARR cut $205M → $144M; S&M budget and rep count raised; PLG contribution quantified; ACV
   decomposed — addresses all five finance flags. $200M is a Year-6/7 outcome, stated plainly.
