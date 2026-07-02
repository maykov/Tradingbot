# Idea 03 — InferRoute

## 1. Executive Summary

InferRoute is an enterprise LLM inference gateway — a customer-deployed routing and spend-governance layer that sits across every model provider an enterprise uses, offering smart routing, semantic caching, failover, policy enforcement, and cost analytics. It targets platform and AI-engineering teams at mid-to-large enterprises (500–10,000+ employees) already spending $100K+/yr across ≥2 LLM providers, with FinOps/CFO as a secondary buyer. The wedge is timely: model proliferation plus intensifying CFO scrutiny of exploding AI budgets creates urgent demand for cost governance, while a customer-VPC, fail-open architecture (adopted in v2) neutralizes the outage and data-leakage risks that would otherwise disqualify the category. The path to scale runs through a revised, more defensible plan reaching $144M ARR by Year 5 (with $200M plausible in Year 6–7), turning EBITDA-positive in Year 4 on ~$130M of total capital raised. Verdict: conditional GO — the legal and financial teams converged on a fundable, structurally sound plan, but two unhedged risks (FTO/patent exposure and hyperscaler bundling) remain outside the company's control and should gate, not block, the next rounds.

## 2. Product & Value Proposition

InferRoute gives platform/AI-engineering teams one control plane across OpenAI, Anthropic, Google, Azure, Bedrock, and open-weight endpoints: cost/latency/quality-aware smart routing, semantic caching, automatic cross-provider failover, per-team/per-app spend budgets, policy enforcement (PII redaction, model allow-lists, rate limits), and unified spend analytics. The Year-1 wedge is a spend-governance console with a guaranteed savings SLA — automatic downgrade-routing to cheaper models when frontier quality isn't required — designed to pay for itself in under 90 days, differentiating from convenience-first OSS gateways (LiteLLM, OpenRouter).

Following the v2 re-architecture, the product ships as a **split control/data plane**: the routing proxy deploys inside the customer's own VPC/on-prem environment (stateless, fail-open — if InferRoute logic fails, traffic passes through unmodified to the customer's default provider), while a hosted control plane handles policy, analytics, and reporting. Caching is hard-partitioned per tenant (per-tenant embedding namespaces and encryption keys, physically located in the customer's VPC). Customers operate under a strict **BYOK (bring-your-own-key)** model — InferRoute never resells tokens or pools API keys, avoiding intermediary/reseller exposure with providers. Routing policies are customer-authored, with InferRoute executing and logging decisions rather than making autonomous model-selection calls.

## 3. Addressable Market

| Metric | Value | Basis |
|---|---|---|
| TAM | $3.3B/yr | Enterprise LLM inference spend ~$110B/yr by 2029 (Menlo Ventures trend, ~45% decelerating CAGR, **assumption**) × 3% gateway-capture rate (**assumption**, midpoint of brief's 2–5% range) |
| SAM | $2.25B/yr | ~15,000 target enterprises globally with multi-provider deployments and >$100K/yr inference spend (**assumption**, sized by analogy to Datadog's enterprise-tier base) × $150K achievable blended ACV |
| SOM (Year 5) | $144M ARR | 800 customers × $180K blended ACV = 5.3% of SAM accounts (revised down from v1's 6.7%/$200M after benchmarking against Datadog/Snowflake's 8–10-year penetration timelines in categories without a free OSS incumbent) |

Key assumptions: TAM/SAM are unchanged from v1 to v2. ACV is decomposed as $105K volume-insensitive platform fee (58%) + $75K usage take rate (2.5% of ~$3M average managed spend, compressing from 3.5%). Holding managed-spend-based revenue flat against a >90% projected inference unit-cost decline (Gartner) requires 10–20x token-volume growth per account over five years — the single most load-bearing assumption in the model, with a stated downside case of $114M ARR if volume growth is only 5x. EU usage revenue carries a further ~10% haircut from residency-constrained routing.

## 4. 5-Year Plan

| Year | Product Milestones | GTM | Headcount (Eng/S&M+CS/G&A) | Geography | ARR |
|---|---|---|---|---|---|
| 1 | Customer-VPC data plane w/ fail-open; per-tenant cache; residency-constrained router; spend console; SOC2-I; FTO + AI Act counsel engaged | Founder-led; 10 design partners | 14/5/4 (23) | US | $2M |
| 2 | Policy engine; pinned-model regulated mode + BAA program; self-serve tier; SOC2-II | 8 quota reps + PLG (20% of bookings) | 24/20/7 (51) | US + UK | $11M |
| 3 | EU region + residency packs; FinOps integrations; eval-evidence workflow for downgrade policies | Enterprise AEs; SI partners | 40/38/13 (91) | + EU | $36M |
| 4 | Benchmark-trained router v2; fin-services & healthcare compliance packs GA | Land-and-expand; analyst relations | 55/60/20 (135) | + APAC | $81M |
| 5 | Agentic-workload cost governance; opt-in telemetry network | Global enterprise + renewals engine | 70/85/28 (183) | US/EU/APAC | **$144M** |

Customer count: 25 / 100 / 280 / 520 / 800. Blended ACV: $80K / $110K / $130K / $155K / $180K. $200M ARR is now projected in Year 6–7, not Year 5.

## 5. Financial Model

| Year | ARR ($M) | Growth % | GM % | COGS ($M) | S&M ($M) | R&D ($M) | G&A ($M) | EBITDA ($M) | Cash Burn ($M) | Cum. Capital Req. ($M) |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 2.0 | n/a | 62% | 0.8 | 2.0 | 3.5 | 1.8 | -6.1 | 6.1 | 6.1 |
| 2 | 11.0 | 450% | 65% | 3.9 | 7.0 | 6.1 | 2.3 | -8.3 | 8.3 | 14.4 |
| 3 | 36.0 | 227% | 69% | 11.2 | 12.6 | 10.1 | 3.8 | -1.7 | 1.7 | **16.1 (peak)** |
| 4 | 81.0 | 125% | 72% | 22.7 | 19.0 | 13.9 | 6.0 | +19.4 | 0 | cash-generative |
| 5 | 144.0 | 78% | 75% | 36.0 | 25.0 | 17.7 | 8.5 | +56.8 | 0 | cash-generative |

**Unit economics:** Y5 CAC $89K, LTV $945K (ACV × GM × 7-yr life), LTV:CAC 10.6x, payback 7.9 months — driven by S&M falling to just 17% of Y5 ARR as 115% NRR and a 20% PLG contribution carry expansion. Magic number ~2.0 at Y5. Finance flags this efficiency as better than Datadog at scale — plausible given the model, but residual optimism to monitor.

**Funding plan:** Pre-seed $2M → Seed $8M → Series A $20M → Series B $40M → Series C $60M ≈ **$130M total raised**, down from v1's $250M because the plan turns EBITDA-positive in Year 4, making a Series D optional/opportunistic. Peak cumulative burn ≈ $16M (through Year 3), roughly $6.5M higher than v1 despite lower early ARR, reflecting the cost of VPC engineering, insurance, and compliance counsel. Finance conditions the raise on: (a) Series A — evidence of per-account token-volume trajectory supporting the 10–20x assumption; (b) Series B — VPC onboarding economics ≤$25K/≤30 days and Y2 magic number ≥1.0 actuals; (c) pre-agreed S&M true-up if CAC efficiency reverts to industry norms.

## 6. Legal Risk Assessment

| # | Risk | Severity | Status | Mitigation |
|---|---|---|---|---|
| L1 | EU AI Act provider/deployer role ambiguity | Serious | Mitigated | Customer-authored routing policies, decision logs, AI Act counsel retained Y1; classification risk persists pending regulatory guidance |
| L2 | Bank/healthcare sectoral outsourcing rules apply transitively | Serious | Mitigated | Pinned static model lists, BAA program, audit rights/exit plans as standard exhibits; compliance packs moved Y4→Y2; regulated revenue no longer assumed early |
| L3 | "FedRAMP-ready" mislabeling risk | Manageable | Resolved | Language removed entirely until an ATO path is funded |
| L4 | Critical-path outage liability exceeds SaaS caps | Fatal | Mitigated | Customer-VPC, stateless, fail-open data plane; 12-month liability cap now defensible; E&O/cyber insurance added |
| L5 | Algorithmic downgrade-routing shifts harm liability upstream | Serious | Mitigated | Substitution limited to customer-approved equivalence classes with conservative default; residual negligent-evidence exposure |
| L6 | Semantic-cache cross-tenant leakage (mass breach) | Fatal | Resolved | Per-tenant namespaces/keys, cache physically in customer VPC — architecturally, not just policy, prevented |
| **L7** | **No freedom-to-operate/patent analysis; Portkey now inside PANW** | **Serious** | **Still open** | **$150K FTO analysis budgeted Y1 but unperformed; risk unchanged until it returns clean** |
| L8 | Moat (data pooling) contradicted promised tenant isolation | Fatal | Resolved | Moat rebuilt on own benchmark data + opt-in metadata-only telemetry (regulated customers defaulted out) + workflow lock-in; moat is honestly weaker |
| L9 | Unvetted OSS provenance (LiteLLM/Portkey) | Manageable | Resolved | Clean-room policy and provenance scanning from first commit |
| L10 | Cost-routing triggers Schrems II transfer violations | Fatal | Mitigated | Residency as a hard optimizer constraint; within-region savings SLAs; explicit SCC/DPF for cross-region routes |
| L11 | Business model may violate/invite termination under provider ToS | Fatal | Mitigated | Strict BYOK — no token resale, no key pooling; reseller clauses don't attach; category precedent (LiteLLM/Portkey) supports tolerance |
| L12 | Cached PII vs. GDPR erasure rights unaddressed | Serious | Mitigated | Short TTLs, PII-exclusion defaults, erasure API, customer-as-storage-controller; probabilistic PII detection is residual risk |
| **L13** | **Hyperscaler bundling has no legal remedy** | **Serious** | **Still open** | **Acknowledged as pure business risk; cross-provider-neutrality repositioning (Datadog-vs-CloudWatch analogy) is the commercial, not legal, answer** |
| **N1** | **Fail-open bypasses compliance controls (new)** | **Serious** | **Open** | **Per-policy-class fail-closed configuration needed for compliance-critical routes; must be customer-elected in order form** |
| **N2** | **Deployed-software obligations across ~800 VPCs (new)** | **Serious** | **Open** | **Update/patch SLAs, customer patching obligations, access-scoping terms needed in Y1 contract templates** |
| N3 | Benchmarking providers may itself breach provider ToS (new) | Manageable | Open | Internal routing use is defensible; publishing/marketing benchmark results needs per-provider ToS review |
| N4 | Insurance assumptions unvalidated (new) | Manageable | Open | $10M E&O at $150–300K/yr is asserted, not quoted; obtain binding quotes before board presentation |

No Fatal objections remain open. The legal team characterizes v2 as "a genuine structural response, not cosmetic redlining."

## 7. Debate Log

V1 proposed a hosted, multi-tenant SaaS gateway targeting $205M Year-5 ARR on ~$250M raised, with a moat built on cross-customer telemetry pooling. Legal review found this architecture fatally flawed on three counts: a hosted critical-path single point of failure (L4), semantic caching that could leak Tenant A's data into Tenant B's response (L6), and a moat (L8) that directly contradicted the isolation guarantees needed to sell regulated verticals — "one of these two claims has to be false." Finance separately flagged an unfunded $7.5M S&M gap, an unrealistic 3-rep sales ramp, an aggressive SOM versus Datadog/Snowflake comparables, and an ACV growth curve that ignored the >90% projected inference cost collapse.

V2 responded with a genuine re-architecture rather than a defense. The gateway split into a customer-deployed, fail-open data plane (traffic passes through unmodified if InferRoute fails) plus a hosted control plane — resolving the outage liability and converting the product to "deployed software" norms. Caching became strictly per-tenant and physically resident in the customer's VPC, eliminating cross-tenant leakage by architecture rather than policy. The company adopted BYOK (customer-held provider keys and contracts), removing reseller/ToS termination risk. Routing became residency-constrained by default, addressing Schrems II exposure at the cost of narrowing the EU savings pitch. Most consequentially, the moat was rebuilt without customer-content pooling — shifting to proprietary benchmark data, opt-in metadata-only telemetry (regulated customers opted out by default), and workflow lock-in — with the entrepreneur candidly conceding the moat is "somewhat weaker." Financially, Year-5 ARR was cut from $205M to $144M (with $200M now a Year 6–7 outcome), demand-gen budget and headcount were raised to close the S&M gap, and ACV was decomposed into platform fee versus take-rate components with a stated downside case. The re-architecture introduced two new legal issues (fail-open bypassing compliance controls; support/patch obligations across hundreds of customer-deployed VPCs) that must be contractually engineered in Year 1.

## 8. Verdict

**Entrepreneur:** A materially more defensible plan that trades $61M of Year-5 ARR for a legally survivable architecture and an honestly weaker but real moat.

**Finance:** Fundable with conditions — $144M ARR and $56.8M EBITDA at Year 5 on $16M peak burn and ~$130M raised is capital-efficient and beats v1's growth-adjusted credibility, gated on token-volume, VPC-economics, and CAC-efficiency proof points at each round.

**Legal:** Legally financeable — every Fatal objection from v1 is Mitigated or Resolved, conditioned on a clean FTO result, binding insurance quotes, and fail-closed policy options shipping in Year 1 contracts; hyperscaler bundling and FTO/patent risk remain real and unhedgeable but are business risks, not legal blockers.

**Overall: GO (conditional).** The v2 plan resolved every structurally fatal legal defect through genuine architectural change rather than rhetoric, and the financial model is capital-efficient and EBITDA-positive by Year 4 even under a $144M (vs. $200M) Year-5 outcome — the remaining risks (FTO, hyperscaler bundling) are known, bounded, and appropriately gated to future financing rounds rather than being reasons to withhold investment now.
