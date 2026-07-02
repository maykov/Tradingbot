# CollectFlow — Business Plan v1

## 1. Product & Value Proposition

CollectFlow is an autonomous AR (accounts receivable) agent for SMB and mid-market B2B companies.
It plugs into a company's ERP/accounting system (QuickBooks, NetSuite, Xero, Sage) and payment
rails, then runs the entire dunning-to-cash lifecycle: it reads the AR aging report, personalizes
and sends reminder sequences by channel (email, SMS, portal), negotiates payment plans within
CFO-set policy guardrails (e.g., "may offer up to 3-month plans, max 5% discount for early pay"),
auto-reconciles incoming payments against open invoices, and escalates broken promises to a human
collector or agency with a full context packet.

**Customer:** CFOs, controllers, and AR/collections staff at SMB/mid-market firms ($5M–$500M
revenue) who have real B2B credit exposure (net-30/60/90 terms) but cannot afford a dedicated
collections team. Secondary channel: embedded/white-label distribution through accounting
platforms and ERPs that want an AR module without building one.

**Year 1 wedge feature:** "Autonomous Dunning Sequences" — an AI agent that takes over the single
most painful, most manual task (writing and sending reminder emails/calls at the right cadence and
tone per customer) and proves it reduces Days Sales Outstanding (DSO) within 60 days, with a
human-in-the-loop approval step for anything outside policy. This is narrow enough to ship fast,
measurable in dollars (DSO reduction, cash accelerated), and creates the trust needed to later
hand the agent authority to negotiate and reconcile autonomously.

## 2. Market Sizing

**TAM (top-down):** Global AR automation software market is estimated at $3.8B–$5.4B in 2026
across multiple research firms (Mordor Intelligence: $3.84B; Grand View Research: $5.40B), growing
~12–16% CAGR (sources: researchandmarkets.com, mordorintelligence.com, grandviewresearch.com).
Adding adjacent collections-outsourcing/agency spend (**assumption**, ~2x software TAM based on
typical software-vs-services ratios in fintech ops categories) brings a broader addressable pool
to roughly **$12–15B**, consistent with the seed brief's estimate.

**SAM (bottom-up):** The US Census/SBA reports 5.52M employer firms with 1–499 employees (SBA
Office of Advocacy, 2025, advocacy.sba.gov). **Assumption:** ~20% of these sell B2B on credit terms
(vs. cash/consumer-facing) → 5.52M × 0.20 ≈ **1.1M target firms** in the US alone. At a blended ACV
of $6,000/yr (SaaS subscription $3,600–$7,200 typical for mid-market AR tools per pricing research
on Billtrust/Versapay-class tools, lunos.ai comparison) plus a modest take-rate component, SAM =
1.1M firms × $6,000 = **$6.6B** for the US SMB/mid-market segment alone (excludes enterprise, which
HighRadius/Billtrust already own, and excludes international).

**SOM (5-year, bottom-up):** Target 1.5% of the US SAM firm count by year 5: 1.1M × 1.5% ≈ **16,500
customers**. Blended ACV of $6,000 (SaaS base) plus ~1% take-rate on accelerated collections
(**assumption**: average customer has $2M AR balance, accelerating collection of ~15% of it by 10
days generates a fee base averaging ~$3,000/customer/yr) → effective blended revenue/customer ≈
**$9,000–$12,000/yr** at scale as take-rate customers mature. 16,500 × ~$12,000 ≈ **$198M**, i.e.
the year-5 ARR target below. This is deliberately conservative on customer count (1.5% penetration
of a 1.1M-firm SAM) and reachable via embedded distribution deals rather than one-by-one SMB sales.

## 3. 5-Year Plan

| Year | Product Milestones | GTM Motion | Headcount (by function) | Geography | Target ARR |
|---|---|---|---|---|---|
| 1 | Autonomous dunning wedge; QuickBooks/NetSuite/Xero integrations; policy guardrail engine | Founder-led sales + design partners (20–30 SMBs); waitlist from AR communities | 12 total: 6 eng, 2 product/design, 2 GTM/sales, 1 CS, 1 ops/finance | US only | $1.2M |
| 2 | Add payment negotiation + auto-reconciliation; SOC 2 Type I; first embedded/white-label pilot with an accounting platform | Inside sales team + 1 embedded-distribution partner live | 32: 14 eng, 4 product, 8 sales/GTM, 4 CS, 2 ops/finance | US; begin Canada | $8M |
| 3 | Full autonomous negotiation with escalation workflows; collections-agency marketplace for hard cases; API/platform for ERPs | 2–3 embedded partnerships scaled (revenue share); outbound + PLG self-serve tier launched | 75: 28 eng, 8 product, 22 sales/GTM, 12 CS, 5 ops/finance | US, Canada, UK | $32M |
| 4 | Multi-currency/multi-entity support; credit-risk scoring add-on; SOC 2 Type II; vertical playbooks (distribution, staffing, healthcare services) | Channel-led growth (ERP marketplaces), partner-sourced becomes >50% of new ARR | 150: 50 eng, 14 product, 45 sales/GTM, 30 CS, 11 ops/finance | + EU (Ireland entity), Australia | $90M |
| 5 | Full AR platform (dunning, negotiation, reconciliation, credit scoring, dispute mgmt); enterprise mid-market tier | Land-and-expand into upper mid-market; 5+ major ERP/accounting-platform white-label deals live | 260: 85 eng, 22 product, 80 sales/GTM, 55 CS, 18 ops/finance | US, Canada, UK, EU, ANZ | **$200M** |

## 4. Competition & Moat

**Top 3 competitors:**
1. **HighRadius** — enterprise-grade AR/O2C suite, ~800 customers (P&G, Sanofi, J&J), backed by
   EQT with a reported path from $200M to $500M revenue; pricing $50k–$150k+/yr — priced out of
   true SMB and most mid-market (lunos.ai, chatfin.ai comparisons).
2. **Billtrust** — 2,400+ customers, more mid-market-accessible ($20k–$60k+/yr), strong cash
   application, but historically network/invoicing-first rather than autonomous negotiation-first.
3. **Point-solution collections tools** (e.g., Chaser, Upflow, Gaviti) — cheaper, SMB-friendly
   reminder/dunning tools but largely rules-based templating, not autonomous negotiation or
   reconciliation, and lack embedded distribution scale.

**Moat:** (a) **Data network effect** — every negotiated payment plan, dispute pattern, and
successful dunning sequence across thousands of customers trains policy models that generalize
per-industry, creating an accuracy gap incumbents' rules engines can't close quickly. (b)
**Embedded distribution** — white-label deals with accounting/ERP platforms make CollectFlow the
default AR layer for their SMB base, a channel HighRadius/Billtrust have not prioritized because
their enterprise motion doesn't need it. (c) **Trust/liability wedge** — the policy-guardrail
architecture (agent proposes, humans/CFO approve boundaries) lowers the adoption barrier that pure
"autonomous negotiation" pitches face, letting CollectFlow earn authority incrementally where
competitors ask for it all at once.

## 5. Key Risks

1. **Will SMB/mid-market finance teams actually delegate customer-facing negotiation to an AI
   agent?** If trust concerns (brand risk, customer relationship damage) cap adoption to
   "reminders only," the take-rate revenue layer collapses and the model reverts to a
   commoditized, low-ACV SaaS tool — killing the path to $200M.
2. **Embedded/white-label distribution deals may not materialize or may commoditize CollectFlow.**
   The plan assumes ERPs/accounting platforms become a >50% channel by year 4; if they instead
   build in-house AR agents (increasingly plausible as LLM tooling commoditizes) or refuse
   revenue-share terms, CAC reverts to expensive direct SMB sales, breaking the unit economics.
3. **Payment/negotiation errors carry outsized financial and compliance risk.** An agent
   mis-negotiating a payment plan, violating FDCPA-adjacent debt-collection rules, or
   mis-reconciling cash at scale could trigger customer churn, liability, or regulatory scrutiny
   fast enough to stall growth before trust (and the data moat) can compound.
