# InferRoute — Business Plan v1

## 1. Product & Value Proposition

InferRoute is an inference gateway that sits between enterprise applications and every LLM
provider (OpenAI, Anthropic, Google, Azure, Bedrock, open-weight endpoints). It gives platform and
AI-engineering teams one control plane for: smart routing (cost/latency/quality-aware model
selection per request), semantic caching, automatic failover across providers, per-team/per-app
spend budgets and policy enforcement (PII redaction, model allow-lists, rate limits), and unified
spend analytics for finance.

**Customer:** platform engineering and AI infrastructure teams at mid-to-large enterprises
(500-10,000+ employees) running production LLM workloads across ≥2 providers, with finance/FinOps
as a secondary buyer once spend crosses ~$500K/yr.

**Year-1 wedge feature:** a "spend-governance" console purpose-built for the CFO/FinOps
conversation — real-time cost attribution by team/app/model, budget alerts, and automatic
downgrade-routing (route to a cheaper model when a request doesn't need frontier quality) with a
guaranteed savings SLA. This is the fastest path to a signed contract because it pays for itself in
under 90 days, unlike pure developer-tooling gateways (LiteLLM, OpenRouter) that sell on
convenience, not cost recovery.

## 2. Market Sizing

**TAM (bottom-up):** Menlo Ventures estimates enterprise generative-AI spend at $37B in 2025, up
from $11.5B in 2024 (Menlo Ventures, "2025 State of Generative AI in the Enterprise"). Extending
that trajectory at a decelerating ~45% CAGR (**assumption**, off-peak vs. the 2024→2025 spike)
implies global enterprise LLM inference spend of roughly **$110B/yr by 2029**. Applying the
brief's 2–5% gateway-layer capture rate, we use 3% (**assumption**, midpoint) →
**TAM ≈ $3.3B/yr** in addressable inference-gateway revenue.

**SAM (bottom-up):** Target accounts are mid-to-large enterprises with active multi-provider LLM
deployments and >$100K/yr inference spend. We estimate **~15,000 such companies globally**
(**assumption**, sized by analogy to Datadog's ~30,000 total customers, of which roughly half are
enterprise-tier accounts with production cloud infrastructure spend at this scale — Datadog Q1
2026 investor materials). At an average achievable blended ACV of **$150K** (platform fee +
usage-based take rate), SAM = 15,000 × $150K = **$2.25B/yr**.

**SOM (Year 5 target):** 1,000 paying customers × $200K average ACV = **$200M ARR**. This is ~6.7%
of SAM accounts and ~9% of SAM dollars after 5 years — comparable to category leaders (Datadog,
Snowflake) reaching similar penetration rates within a comparable window of category emergence.

## 3. 5-Year Plan

| Year | Product Milestones | GTM Motion | Headcount (Eng / Sales & CS / G&A) | Geography | Target ARR |
|---|---|---|---|---|---|
| 1 | Core router + failover + semantic cache; spend-governance console (wedge); SOC2 Type I | Founder-led sales, 10 design partners → paying pilots | 12 / 4 / 3 (19 total) | US only | $3M |
| 2 | Policy engine (PII, allow-lists), self-serve tier, Bedrock/Azure/Vertex native connectors; SOC2 Type II | Inbound PLG + 3-person AMY sales team; first channel partner (cloud marketplace listing) | 22 / 12 / 6 (40) | US + UK | $18M |
| 3 | Multi-region deployment, on-prem/VPC option, FinOps integrations (Cloudability, ServiceNow), model-quality eval suite | Mid-market segment + enterprise AE team; partner with SIs | 38 / 28 / 12 (78) | + EU (Germany, France) | $55M |
| 4 | Autonomous routing (RL-based cost/quality optimizer), industry compliance packs (HIPAA, FedRAMP-ready) | Enterprise land-and-expand, exec sponsorship program, analyst relations (Gartner) | 55 / 50 / 20 (125) | + APAC (Singapore, Japan) | $120M |
| 5 | Full agentic-workload routing (multi-step/tool-call cost governance), marketplace for custom routing policies | Global enterprise motion, renewal/expansion engine, 2 industry verticals (fin. services, healthcare) | 75 / 75 / 30 (180) | US, EU, APAC, LatAm pilot | **$205M** |

Customer count trajectory: ~30 (Y1) → 150 (Y2) → 400 (Y3) → 700 (Y4) → 1,000 (Y5); blended ACV
rises from ~$80K (Y1, early/small accounts) to ~$200K (Y5, enterprise-weighted mix).

## 4. Competition & Moat

**Top 3 competitors:**
1. **Portkey** — enterprise-focused gateway with guardrails/observability; acquired by Palo Alto
   Networks in 2026, signaling gateway consolidation into security platforms, and open-sourced its
   core gateway (Apache 2.0) in March 2026, pressuring paid tiers (awesomeagents.ai, "Best LLM
   Gateways 2026").
2. **LiteLLM** — free, MIT-licensed, 140+ provider support, the default self-hosted choice for
   engineering teams that don't want to pay for routing (klymentiev.com, "LLM Gateway 2026").
3. **OpenRouter** — largest model catalog (400+ models, 60+ providers), pay-as-you-go, strong with
   individual developers and startups but weak on enterprise governance/compliance
   (openrouter.ai/blog, "LLM Gateway: What It Is and How to Choose One").

**Moat:** the core routing logic is not hard to replicate (LiteLLM proves this). Defensibility has
to come from three compounding layers: (a) a **cross-customer routing/cost model** trained on
aggregate telemetry (which model performs best per task type per $ across thousands of production
workloads) that improves with scale and can't be replicated by a single company's self-hosted
instance; (b) becoming the **system of record for AI spend governance** — once budgets, approval
workflows, and finance reporting are wired through InferRoute, ripping it out is a finance-process
change, not just a code change; (c) compliance certifications and audit trails (SOC2, HIPAA,
FedRAMP-ready) that OSS alternatives can't offer turnkey, targeting the regulated mid-to-large
enterprise segment OpenRouter/LiteLLM under-serve.

## 5. Key Risks

1. **Hyperscaler bundling.** If AWS Bedrock, Azure AI Foundry, or Google Vertex ship "good enough"
   native multi-model routing, failover, and spend controls for free as a retention play, the
   independent gateway layer gets squeezed to just cross-cloud arbitrage — a much smaller wedge.
   This is the single riskiest assumption: it assumes hyperscalers stay motivated to keep customers
   multi-cloud rather than lock them in natively.
2. **Inference cost collapse.** Gartner projects >90% cost decline for trillion-parameter-model
   inference by 2030 (Gartner, March 2026 press release). If the % of managed-spend revenue model
   shrinks faster than usage volume grows, ARR compresses unless we shift decisively to seat/platform
   pricing — a pricing-model risk baked into our TAM math.
3. **Open-source commoditization.** LiteLLM is free and Portkey open-sourced its gateway core in
   2026; if governance/security features reach OSS parity, enterprises self-host instead of paying,
   collapsing willingness-to-pay for anything beyond consulting/support.

**Sources:** Menlo Ventures 2025 State of Generative AI in the Enterprise; Gartner press releases
(Mar. 2026 inference cost forecast; May 2026 worldwide AI spending forecast); awesomeagents.ai,
openrouter.ai/blog, klymentiev.com (LLM gateway competitive landscape, 2026).
