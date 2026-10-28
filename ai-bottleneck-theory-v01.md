# Bottleneck Migration and Value Capture in the AI Revolution

Developed from discussion materials provided by Xiaoyue Lian. This paper is a testable mechanism framework and illustrative model. Its parameters have not been estimated using firm-level panel data. It is not an industry forecast, investment return model, or prediction of startup success rates.

## 1. Core proposition

As replicable cognitive capabilities expand, economic activity becomes more visibly constrained by complementary conditions that expand more slowly: electricity and computing capacity, proprietary business knowledge, customers and distribution, authorization and acceptance, responsibility for outcomes, and the ultimate ability to pay. Removing these constraints can create value, but how much value can be retained also depends on substitutes, bargaining power, competition, property rights, and contractual arrangements.

Lower barriers to starting a business can therefore coexist with concentrated profits. The former reduces experimentation costs; the latter arises when hard-to-replace complementary assets remain controlled by a small number of actors. These outcomes are compatible, but neither is inevitable in every period.

This framework combines existing ideas about complementary assets, bottleneck constraints, transaction costs, and entrepreneurial selection. Its potential contribution is to place AI infrastructure, enterprise organization, data transactions, agent governance, and startup outcomes within one testable structure. It does not establish that the underlying economic principles are new.

## 2. Distinguish three outcomes

| Level | Question | Suitable observations | Metrics that should not substitute for them |
| --- | --- | --- | --- |
| Technical capability | Can the task be completed reliably? | Success rate and effective throughput for a fixed task, quality standard, and deadline | Token volume alone or model benchmark scores |
| Economic value | Is the result worth paying for? | Actual total cost savings, incremental revenue, customer renewals, and paid task volume | Registrations, agent calls, or funding raised |
| Value distribution | Who retains returns, and who bears risk? | Profit after upstream, delivery, and risk costs; customer surplus; founder returns after dilution | Valuation, revenue growth, or total industry demand |

Agents are not final consumers with unlimited independent budgets. Machine calls may expand dramatically, but their budgets come from businesses, households, or the public sector. Many calls may represent retries, internal coordination, or redundancy rather than additional economic value.

## 3. A minimal operational model

Use a workflow with fixed quality, deadline, and responsibility requirements as the unit of analysis—for example, one procurement transaction meeting acceptance criteria. Convert every capacity into the number of equivalent valid tasks that can be completed per month. Do not directly add GPU counts, employee counts, and identity counts.

\[
Q_t^{\max}=\min\{D_t(p),K_t,T_t\}
\]

- D_t(p): Reachable task demand that customers are willing to pay for at price p. This includes the ultimate budget constraint.
- K_t: Reliable delivery capacity meeting the required quality standard. This incorporates limits from models, computing resources, electricity, business data, personnel, and tool integration.
- T_t: The maximum task volume that customers can authorize, supervise, accept, and accommodate under the relevant responsibility arrangements. This is organizational process capacity, not an abstract “trust index.”
- Q_t^{max}: Maximum transaction volume. Actual transactions may be lower because of sales, queues, task matching, or other factors.

In the simplified scenario of delivering at this limit:

\[
\pi_t=(p_t-c_t)Q_t^{\max}-F_t=m_tQ_t^{\max}-F_t
\]

- p_t: Price per accepted result.
- c_t: Variable cost per accepted result, including model calls, retries, human review, usage-based integration or customer support, and estimable expected incident costs. Counting only token costs is insufficient.
- F_t: Fixed operating costs for the period, including fixed research and development, administration, sales, and basic operations. The boundary between F_t and c_t must remain consistent to avoid double counting.
- m_t=p_t-c_t: Contribution margin per task, before fixed costs.
- π_t: Simplified operating profit, not free cash flow or the founder’s personal income. Taxes, financing, capital expenditures, and working capital are not separately modeled.

If m is negative, delivering more increases losses. A rational business may reduce or stop delivery; available capacity does not imply that it should be used. If m is positive, break-even volume is F/m, rounded up for discrete tasks.

This is a short-run approximation with strictly complementary inputs. In some businesses, humans can substitute for automation, outsourcing can substitute for in-house production, and constraint boundaries are smoother. More detailed research should use queueing models or production functions that allow substitution. A business-level minimum function cannot be directly treated as a model of global GDP.

## 4. Simulation definitions and results

Every number in the simulator is illustrative rather than measured from the market. The price is fixed at $20 per task, and fixed costs are $2,000 per month. The baseline is D=1,000, K=600, T=300, and m=6, implying c=14. Adjusting m represents a change in delivery cost while holding price constant, so the demonstration does not separately shift the demand curve.

| Change in conditions | Maximum transaction volume | Operating profit at capacity | Interpretation |
| --- | ---: | ---: | --- |
| Baseline: D=1000, K=600, T=300, m=6 | 300 tasks/month | -$200/month | Authorization and acceptance constrain throughput |
| Increase only K from 600 to 1200 | 300 tasks/month | -$200/month | Adding non-bottleneck capacity does not increase output; profit would fall if doing so adds costs |
| Increase T to 600 from baseline | 600 tasks/month | $1,600/month | Removing the current constraint makes reliable delivery a joint bottleneck |
| Keep D=1000 and K=T=600, but reduce m to 2 | 600 tasks/month | -$800/month | More activity does not guarantee value capture |
| D=200, K=T=1500, m=6 | 200 tasks/month | -$800/month | Demand can be the constraint; computing and governance cannot substitute for willingness to pay |

These results follow mechanically from the assumptions; they do not independently validate those assumptions. Increasing T also costs money in practice. The simulator is a local sensitivity analysis that temporarily excludes the costs of governance or capacity expansion projects from scenario changes. Business decisions must deduct those incremental costs.

To evaluate whether removing a constraint is worth the investment, calculate:

\[
\Delta\pi=m\,\Delta Q-\Delta F-\Delta c\,Q_{new}
\]

Here, m is the original contribution margin per task, and Δc is the change in variable cost per task. When several constraints bind simultaneously, they may need to be improved together before Q increases.

## 5. From business bottlenecks to industry power

In this framework, power means the ability to affect other participants’ access to critical resources, market entry, or returns. It is not equivalent to market capitalization, visibility, or technical sophistication.

The basic cycle is: changes in capability and cost → new tasks become feasible → complementary conditions become constraints → growth in deliverable results is limited → bottleneck controllers may gain bargaining power → profits attract investment, substitutes, and standardization → existing bottlenecks ease or are bypassed → new constraints emerge.

Two opposing feedback mechanisms operate:

- Concentration: Profits help controllers invest further, acquire businesses, and lock in customers, strengthening resource control.
- Diffusion: High profits attract competition, alternative architectures, and new supply. Standardization lowers switching costs and may compress existing rents.

If capacity expansion has long lead times, the two forces may alternate in dominance. If network effects and customer switching costs remain stronger, concentration may persist. It is therefore inappropriate to assume that bottlenecks will shift from chips to governance in 2027 and then to applications in 2028. Different regions, industries, and workflows can face different constraints simultaneously.

| Candidate constraint | What is controlled? | How to observe whether it constrains growth | Why it may not generate lasting profits |
| --- | --- | --- | --- |
| Computing, electricity, and manufacturing | Deliverable capacity, access, and supply chains | Queue times, utilization, order fulfillment, and effective computing costs | New supply, substitutes, capital costs, and cycles |
| Business knowledge and data | Access to high-quality data with valid usage rights and ongoing updates | Differences in task completion with and without the data | Substitutability, stale static data, and buyer bargaining power |
| Customers, workflows, and distribution | Access to budgets and the ability to embed in processes | Paid conversion, retention, sales cycles, and migration costs | Distribution fees, platform bundling, and product commoditization |
| Authorization, acceptance, and accountability | Enforceable permissions, traceable responsibility, and acceptable residual risk | Pilot-to-production conversion, authorization delays, and human review time | Existing security platforms may cover the need; standards may be implemented for free |
| Final demand | Actual budgets and the value of results | Renewals, cancellations, additional tasks, and net benefits | Temporary subsidies and experimental budgets may disappear |

A key limitation: solving a bottleneck and collecting bottleneck rents are different things. An open standard may create substantial social value without giving any one company exclusive charging rights. Conversely, high fees do not automatically imply high net social value.

## 6. Implications for data revenue sharing and agent trust infrastructure

micro1’s enterprise data acquisition program suggests that operational knowledge may have commercial value. A procurement commitment alone does not establish that every data seller is underpaid. Assessments should compare substitutability, update frequency, training effects, licensing scope, and competitive spillovers.

Revenue sharing is one possible risk-and-return arrangement, not the only reasonable one. Alternatives include one-time licenses, annual subscriptions, minimum guarantees plus revenue shares, shares of clearly defined product revenue pools, and milestone payments. Revenue sharing need not trace exactly which training record was “used” in each inference; contracts can define an auditable revenue base. Provenance, permissions, and audits help, but tagging data does not automatically solve training-contribution attribution or ensure enforceable rights.

For an agent trust startup, a reasonable entry hypothesis is that cross-system or cross-organization authorization and responsibility handoffs contain friction that existing products do not adequately address, and customers will pay to reduce it. This is more testable than “every agent needs an ID, so an independent identity company must win.”

For example, choose a procurement workflow spanning companies and test whether the solution can:

1. Clearly express who authorizes which agent, what it may do, and its spending and time limits.
2. Revoke or narrow authorization promptly and enforce the changes in existing systems.
3. Preserve inspectable records from authorization through action to acceptance.
4. Reduce the time needed to enter production or the cost of manual verification.
5. Retain renewals when existing identity or security vendors offer similar capabilities.

Cryptographic proofs or identity labels do not by themselves determine legal responsibility, nor do they require platforms to accept an independent certification authority. Interoperability advantages must be demonstrated in a specific workflow.

## 7. Startup entry and viability: avoid unverified industry percentages

Combining company counts from different periods, regions, or funding stages with unrelated exit counts does not produce a credible success rate. Companies that have not exited may still be young, independently operating, or missing from available records. Acquisitions may represent high returns, distressed sales, or acquihires.

Start with a cohort sharing a founding period, business category, and region. Observe it for at least five years and define “effective” in advance:

- Customer effectiveness: The company continuously solves a problem, with repeat purchases or renewals.
- Business viability: The company can operate independently after reasonable delivery and organizational costs.
- Shareholder effectiveness: Actual returns after dilution and liquidation preferences meet a defined threshold.
- Social effectiveness: Technology, talent, or institutional practices generate observable spillovers even if the company exits or closes.

These dimensions are not interchangeable. Historically important companies need not generate high founder returns; small profitable companies are not failures.

At the observation cutoff, classify companies into mutually exclusive states: acquired, closed, independently operating and sustainable, independently operating but not yet sustainable, or unknown. Account for right censoring among surviving firms and use competing-risks methods for exits. Without data, mark estimates as pending rather than supplying precise-looking figures such as 1%–5% or 85%–90%.

Mechanistically, lower entry costs increase the number of experiments N. If the number of sustainable businesses S grows more slowly, the ratio S/N falls even while S rises in absolute terms. S is not a predetermined set of historical winner slots: new markets, differentiation, and lower costs can expand it.

| Does the business provide lasting customer value? | Can it retain sufficient returns? | Possible paths, not probability forecasts |
| --- | --- | --- |
| Yes | Yes | Independent operation, expansion, or a voluntary strategic transaction |
| Yes | No | Renegotiate distribution or pricing, reduce costs, pivot, or be integrated; closure remains possible |
| Not yet demonstrated | Temporarily supported by capital or distribution | Continue validation, or become dependent on financing and subsidies |
| No | No | Pivot, narrow the scope, or stop operating |

## 8. Why credentials, communication skills, and networks are insufficient

These advantages can reduce search, fundraising, recruiting, and customer access costs. They do not automatically create paying demand, reliable products, industry knowledge, or bargaining power. An advantage within a particular environment should be measured as lower costs of accessing customers, teams, funding, and experimentation—not as a guarantee that a particular group will win.

Career decisions must also compare compensation, learning opportunities, visas, cash reserves, family constraints, and the option to start a business later. Startup failure costs are not universally close to zero. Joining an established organization can provide access to data, customer experience, and delivery capabilities that are difficult to obtain at school.

A reasonable strategy is to acquire information first: test real paid tasks with limited time and money, and define conditions for further investment. Examples include repeat use and renewals, declining human intervention as volume grows, and positive contribution margin after acquisition and delivery costs. This does not require raising funding before starting a business, nor does it imply that young people must become founders.

## 9. Conditional scenarios for 2027–2028

Do not assign “high-confidence probabilities” without calibrated data. These are conditional scenarios, not a timetable.

| Scenario | Conditions to observe | Model implication | Key question for independent startups |
| --- | --- | --- | --- |
| Continued platform concentration | Effective capacity remains scarce, platforms control distribution, and cross-platform migration is costly | Bottleneck controllers retain greater bargaining power | Can the startup provide a missing capability that platforms cannot easily bundle? |
| Application value diffuses | Reliable delivery costs fall, willingness to pay expands, and integration becomes easier | Smaller teams can operate independently | Are customer relationships, workflow integration, and differentiation sustainable? |
| Platforms absorb governance demand | Authorization and audits become more important, but native platform features are sufficient | Governance becomes more important without necessarily raising independent vendors’ profits | Is cross-organization, cross-vendor demand real? |
| Insufficient paying demand | Calls grow but renewals are weak, net benefits are low, and experimental budgets shrink | D becomes the constraint, potentially affecting both hardware and applications | Does the business create billable results rather than merely more activity? |

These scenarios can coexist across market segments.

## 10. Testing the model and identifying weakening evidence

| Testable proposition | Data to collect | Supporting evidence | Contradictory or weakening evidence |
| --- | --- | --- | --- |
| Authorization and acceptance are the current bottleneck in a workflow | Operational capacity, approval time, and paid tasks passing acceptance | With similar capability and demand, removing approval constraints substantially increases valid transactions | Shorter approvals do not increase valid transactions; failures primarily reflect quality problems or insufficient budgets |
| Better foundation models do not guarantee higher application profits | Calling costs, labor costs, prices, retention, and profits within the same firms | Price cuts, competition, or platform fees offset cost reductions | Application profits expand broadly and persistently, with control of complementary assets failing to explain differences |
| Neutral trust services have independent purchasing value | Paid pilots, renewals, budget ownership, and platform alternative quotes | Customers continue paying for cross-organization capabilities despite native alternatives | Customers use only free tools or bundled platform features |
| Easier startup entry can coexist with profit concentration | New entrants, operating profit concentration, and the absolute number of sustainable firms over the same period | Entry rises while profit concentration increases | Entry, sustainable firm counts, and returns consistently diffuse together |
| Improvements in complementary conditions help realize AI value | Acceptance, review, incidents, and net benefits across phased deployments or comparable teams | Holding tasks and quality fixed, improvements generate net benefits | No net benefit remains after integration, review, and risk costs |

An initial empirical study could phase deployment within one vertical workflow, predefine tasks and cost accounting, and include a comparable manual or existing-process group. Treat model calls as inputs, not outcomes. For rare incidents, a short period with zero incidents does not establish zero risk.

## 11. Evidence audit and corrections to the source materials

The entries below translate the evidence assessments recorded in the original draft; they do not represent a new verification of the sources.

| Material | Verification status recorded in this draft | What it may support | What it does not establish |
| --- | --- | --- | --- |
| Microsoft voluntary exit offer dated 2026-10-26 | Official announcement confirmed eligibility for selected teams in four countries at level 70 and below; Reuters separately reported approximately 60,000 eligible employees | The organization is adjusting resource allocation | That 60,000 people have been laid off; that eligible roles have been replaced by AI; or that personnel savings correspond directly to GPU investment |
| Approximately $190 billion in Microsoft capital expenditure | User materials mixed fiscal and calendar years; the Reuters report consulted stated $175 billion for calendar 2026 | Figures require reconciliation using consistent dates and definitions | Mixed-basis amounts cannot be inserted into the model to infer causality |
| micro1 data program | Official announcement dated 2026-10-09 committed $1 billion over the next 12 months to acquiring or licensing data for reinforcement learning environments | Enterprise operational data is attracting commercial procurement interest | That the full $1 billion has been spent, or that contract terms, seller returns, or market fairness have been established |
| Gartner strategic trends for 2027 | Official article listed AI agent identity and provided a forecast of security incidents in 2028 | An analyst firm considers governance worthy of attention | That forecast incidents have already occurred or that independent identity companies will necessarily profit |
| Agent identity market | Official Microsoft Entra Agent ID documentation already described identity, authorization, and responsible-owner mechanisms | There is demand and existing competition | That trust infrastructure is an empty market or large platforms cannot provide cross-platform capabilities |
| a16z article dated 2026-10-23 | The user supplied the text, without reproducible charts or underlying series | Its GPU rental, industrial supply chain, and cybersecurity indicators are research leads | Permanent industry-wide demand, equivalence between rent increases and profits, or disproof of historical depreciation assumptions |
| Advantages of young founders | Historical NBER/Census research found that founders of high-growth firms are not generally very young and that industry experience matters | A few young billionaires cannot establish startup base rates | That historical samples determine the age distribution of AI founders in 2026, or that young founders cannot succeed |
| AI startup effectiveness and failure rates | Source materials lacked a reproducible common cohort, denominator, observation period, and exit definition | These remain research questions | Previously quoted precise percentages cannot be treated as known parameters |

Additional corrections to the reasoning:

- Accounting depreciation and market prices for rental services are different. Higher rental prices alone do not prove longer economic life or profitable investment.
- Institutional forecasts, company-reported indicators, and independently audited results have different evidentiary strength.
- Automated computation, search, and decision systems predate this AI wave. It is inaccurate to say that cognition is only now being automated for the first time.
- Mean employment outcomes, median income, variance, and wealth concentration are distinct. Layoffs and success stories alone do not establish how all of them are changing.
- Businesses can profit while renting models. Sustainable returns depend on customers, products, and contracts, not ownership of every layer of production.
- Valuation, financing, contractual commitments, revenue, and actual cash flow must be distinguished.

## 12. Sources

The following sources were searched or read for the original draft. The model and causal propositions are proposed by this paper; these sources should not be understood as validating the entire framework.

1. Microsoft, Amy Coleman, “Introducing a Voluntary Exit Offer,” 2026-10-26.
   https://blogs.microsoft.com/blog/2026/10/26/introducing-a-voluntary-exit-offer/
2. Reuters, “Microsoft offers buyouts to around 60,000 employees to contain costs,” 2026-10-26.
   https://www.reuters.com/technology/microsoft-is-offering-buyouts-around-60000-employees-business-insider-reports-2026-10-26/
3. micro1, Ali Ansari, “micro1 announces commitment to spend $1B on enterprise data acquisition over the next 12 months,” 2026-10-09.
   https://www.micro1.ai/blog/micro1-commits-1b-to-enterprise-data-acquisition
4. Gartner, “Top Strategic Technology Trends for 2027.” Treated here as an institutional forecast.
   https://www.gartner.com/en/articles/top-technology-trends-2027
5. Microsoft Learn, “Agent identities in Microsoft Entra Agent ID.”
   https://learn.microsoft.com/en-us/entra/agent-id/agent-identities
6. IEA, “Key Questions on Energy and AI,” executive summary. Referenced for physical supply, financing, and complementary constraints; future demand figures are forecasts.
   https://www.iea.org/reports/key-questions-on-energy-and-ai/executive-summary
7. Azoulay, Jones, Kim & Miranda, “Age and High-Growth Entrepreneurship,” NBER Working Paper 24489, 2018. Historical sample; not directly extrapolated to AI startup base rates in 2026.
   https://www.nber.org/papers/w24489
   https://www.census.gov/library/working-papers/2018/adrm/ces-wp-18-23.html
8. Brynjolfsson, Li & Raymond, “Generative AI at Work,” Quarterly Journal of Economics, 2025. An empirical study in one customer-support setting, not representative of all cognitive labor.
   https://doi.org/10.1093/qje/qjae044
9. Moses Sternstein, a16z, “Charts of the Week: Attention is All You Need,” 2026-10-23. Read in the text supplied by the user; cited charts were not independently reproduced.
   https://www.a16z.news/p/charts-of-the-week-attention-is-all

## 13. Minimum data needed for the next version

Choose one workflow and record the following weekly: fixed task definitions; paying demand; available delivery capacity; authorization and acceptance capacity; actual delivery and success rates; unit prices; model, retry, human review, sales, and integration costs; fixed costs; customer retention; incidents and disputes; and platform alternatives. Only with these data is it appropriate to estimate bottlenecks, compare architectures, calculate returns on governance investment, and gradually extend the model to industry-level analysis.

## 14. Institutional ownership and the distribution of AI returns

Bottleneck control explains only part of value distribution. Ownership and financing determine who has claims on the resulting cash flows; pension mandates, fund fees, benefit rules, and fiscal arrangements influence whether those returns reach households. Labor-market exposure and investment exposure may overlap, but investment participation is not automatically an effective hedge against lost wages.

The companion study, [Pension Capital, Sovereign Investors, and AI Value Capture](pension-capital-and-ai.md), compares the United States, Canada, the United Kingdom, the European Union, Japan, and Singapore. It distinguishes commitments from deployment, venture allocations from total AI exposure, and sovereign assets from individual pension entitlements. These institutional routes extend the framework rather than validate its causal claims.
