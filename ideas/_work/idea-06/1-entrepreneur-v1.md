# AgentLens — Business Plan v1
**Entrepreneur:** maykov@gmail.com | 2026-07-02

## 1. Product & value proposition

AgentLens is observability, evaluation, and guardrails for production AI agents. It gives AI
engineering teams the equivalent of Datadog + Sentry + a compliance audit trail, but built
agent-native: full execution traces (every LLM call, tool call, retrieval, and reasoning step),
one-click replay of any failure, continuous automated evals against production traffic, real-time
safety/guardrail monitors (PII leakage, unsafe tool calls, prompt injection, runaway cost loops),
and incident alerting routed to Slack/PagerDuty.

**Customer:** AI engineering and platform teams at companies shipping agentic products —
initially mid-market SaaS and fintech/healthtech companies with agents already in customer-facing
production, expanding to enterprise platform teams.

**Year-1 wedge feature:** a framework-agnostic auto-instrumentation SDK (LangChain, LangGraph,
OpenAI/Anthropic Agents SDKs, CrewAI, or raw custom code) that ships in under 10 minutes and
immediately surfaces "silent failure" detection — infinite tool-call loops, hallucinated tool
arguments, and cost spikes — with one-click replay to the exact failing step. This targets the
acute, current pain (agents fail invisibly until a customer complains) rather than the full
evaluation/compliance suite, which we build out in years 2–3.

## 2. Market sizing

**TAM (top-down, cited):** The LLM Observability Platform market is valued at $2.69B in 2026,
growing to $9.26B by 2030 at a 36.2% CAGR (Research and Markets, "Large Language Model (LLM)
Observability Platform Market Report 2026"). We treat **$9B by 2030** as TAM.

**TAM (bottom-up cross-check, assumption):** ~500,000 organizations globally run engineering
teams capable of shipping software products (assumption). Gartner projects 40% of enterprise
applications will embed task-specific agents by end of 2026 (Gartner, cited via industry press);
extrapolating that penetration to ~10% of *all* software-shipping organizations by 2030 (assumption,
conservative vs. Gartner's enterprise-app number) gives 50,000 organizations running agents in
production. At a blended $40k/yr willingness-to-pay for dedicated agent observability
(assumption, anchored to LangSmith's $2.50–5.00/1,000-trace pricing plus per-seat fees —
pecollective.com "LangSmith Pricing 2026"), TAM ≈ 50,000 × $40k = **$2.0B**. This is
consistent-order-of-magnitude with the top-down $2.69–9.26B range; we use $2–3B as the
working TAM.

**SAM (assumption):** Restrict to English-language markets (US, UK, EU, Canada, Australia) and to
companies with agents already customer-facing or in internal high-stakes workflows (fintech,
healthtech, dev tools, e-commerce, customer support) — the verticals where agent incidents are
costly enough to buy dedicated tooling. Assumption: 15,000 such organizations reachable via
self-serve + outbound sales within 5 years, at a blended ACV of $50k (mixing self-serve ~$15k,
mid-market ~$50k, enterprise ~$150k+ tiers). SAM = 15,000 × $50k = **$750M**.

**SOM (Year 5 target):** 4,000 customers × $50k average blended ACV = **$200M ARR**, i.e., ~27%
penetration of SAM — aggressive but plausible for a category leader established in year 1–2,
comparable to LangSmith/Datadog's agent-observability land grab happening now (2026 competitive
snapshot below).

## 3. 5-year plan

| Year | Product milestones | GTM motion | Headcount (by fn) | Geo | Target ARR (arithmetic) |
|---|---|---|---|---|---|
| 1 (FY26-27) | GA: auto-instrumentation SDK, tracing, replay, wedge failure-detection | PLG self-serve + 20 hand-held design partners; dev communities, OSS releases | 12: 7 eng, 2 DevRel, 1 sales, 1 CS, 1 G&A | US only | **$2M** (~150 customers × ~$13k avg) |
| 2 | Continuous eval pipelines, safety/guardrail monitors, SOC2 Type I | Add outbound SDR, enterprise tier, cloud marketplace (AWS/Azure) listings | 35: 18 eng, 5 DevRel, 6 sales, 4 CS, 2 G&A | US + UK | **$12M** (300 customers × $40k avg) |
| 3 | Anomaly detection, cost governance, multi-agent tracing, EU AI Act audit-log features | Enterprise AEs, SI/consultancy channel partners, vertical packages (fintech/health) | 90: 45 eng, 8 DevRel, 22 sales, 12 CS, 3 G&A | + EU, Singapore | **$45M** (900 customers × $50k avg) |
| 4 | Predictive incident prevention, autonomous guardrail remediation, industry benchmarks | Land-and-expand into named enterprise accounts, SI co-sell | 160: 75 eng, 10 DevRel, 45 sales, 25 CS, 5 G&A | + Japan, India | **$110M** (1,800 customers × $61k avg) |
| 5 | Full agent-governance suite (audit + compliance + cost + safety) as system of record | Platform/ecosystem plays, partner certification program | 260: 110 eng, 12 DevRel, 80 sales, 45 CS, 13 G&A | Global (15+ countries) | **$200M** (4,000 customers × $50k avg) |

Note: blended ACV dips in year 5 despite enterprise mix growth because the self-serve/PLG base
scales fastest in customer count — enterprise tier (~10% of accounts) carries $150k+ ACV and
funds the disproportionate sales/CS headcount.

## 4. Competition & moat

**Top 3 competitors:**
1. **LangSmith (LangChain)** — deepest integration with the LangChain/LangGraph ecosystem and
   strong developer experience, but trace-volume pricing ($2.50–5.00/1,000 traces) penalizes
   complex multi-step agents, and teams "consistently underestimate trace volume by 3-5x"
   (pydantic.dev / inference.net pricing analyses, 2026). Weak outside the LangChain ecosystem.
2. **Arize AI (Phoenix)** — strong ML-monitoring heritage and enterprise-scale dashboards, an
   evaluation-first product with open-source Phoenix as a wedge, but "built-in metric coverage for
   LLM-specific use cases is limited compared to evaluation-first platforms" and setup complexity
   is high (Confident AI, "Best AI Observability Tools 2026").
3. **Datadog (Agent Observability)** — massive existing distribution inside companies already
   paying for APM, but its AI features are a bolted-on tab on a general observability platform
   rather than agent-native tooling ("traditional APM platforms like Datadog... adding AI tabs to
   their dashboards" vs. AI-native platforms — Braintrust/Confident AI competitive analyses, 2026).

**Moat:** (1) framework-agnostic instrumentation that avoids LangSmith's ecosystem lock-in and
Datadog's generic-APM shallowness; (2) a proprietary cross-customer failure-taxonomy dataset —
every replayed failure trains our anomaly/guardrail models, so detection accuracy compounds with
scale, a data network effect competitors without our customer base can't replicate quickly; (3)
once compliance and audit-trail workflows (SOC2, EU AI Act logging) live in AgentLens, switching
cost rises sharply — same lock-in dynamic that made Datadog and Sentry sticky; (4) selling into a
new, less price-sensitive budget line (Risk/Compliance, not just engineering) as agent incidents
become a board-level concern.

## 5. Key risks

1. **Agents actually scale into high-volume, budget-owning production workloads.** Adoption data
   is mixed: 80% of enterprises report *at least one* agent in production, but only ~31–51% run
   agents fully in production (2026 adoption surveys, digitalapplied.com / agenticaiinstitute.org).
   If most deployments stay small-scale pilots, the dedicated-tooling budget line never forms.
   **This is the single riskiest assumption** — the whole $200M plan assumes agent production
   traffic (and therefore failure/cost/safety pain) grows 5-10x from today, not that it plateaus.
2. **Foundation-model and framework vendors don't commoditize core tracing/evals for free.**
   OpenAI, Anthropic, and LangChain all have the distribution to bundle "good enough" observability
   into their SDKs at zero marginal cost, compressing our pricing power to the guardrail/compliance
   layer only.
3. **Willingness to pay for dedicated safety/compliance tooling holds** as regulation (EU AI Act,
   sector-specific rules) materializes on our assumed timeline; if enforcement stalls, the
   compliance-budget expansion in years 3-5 (SAM growth beyond pure dev-tool spend) doesn't
   materialize and ARR plateaus well short of $200M.

Sources: Research and Markets "LLM Observability Platform Market Report 2026"; pecollective.com
and inference.net LangSmith pricing analyses (2026); Confident AI and Braintrust competitive
comparisons (2026); digitalapplied.com and agenticaiinstitute.org enterprise agent adoption
surveys (2026). Figures not attributed to a source are labeled assumption above.
