# Amazon Stage-Gate Workflow

Use this reference when the user needs a repeatable Amazon product pipeline rather than a one-off product opinion. The goal is to move from a loose market idea to a sourcing, launch, rework, or stop-loss decision through explicit gates.

This workflow is designed for small brands and lean product teams. Each gate should end with a decision, evidence quality, missing data, and the next smallest action.

## Gate Map

| Gate | Question | Main Output | Decision |
| --- | --- | --- | --- |
| 0. Intake and triage | What decision is needed now? | Decision brief | Route / clarify / reject scope |
| 1. Company fit | Does this arena fit the brand, capital, team, and supply chain? | Fit screen | Fit / weak fit / no fit |
| 2. Demand and trend | Is demand real, durable, and buyer-intent driven? | Demand note | Validate / watch / reject |
| 3. Market structure | Is the market attractive for a small brand? | Market scorecard | Enter / watch / avoid |
| 4. Competitor map | Where are the reachable openings? | Competitor gap map | Target wedge / rework / avoid |
| 5. VOC and product definition | What buyer pain should the first offer solve? | Product definition memo | Define / research more / reject |
| 6. ROI and risk | Can the product work after realistic fees, ads, returns, and inventory risk? | ROI risk memo | Go / test first / no-go |
| 7. Validation plan | What proof is needed before committing more capital? | 7-day or 30-day plan | Execute / wait / stop |

## Gate 0: Intake And Triage

Clarify the decision before analyzing data.

Capture:

- Marketplace and category.
- Product idea, market arena, or ASIN set.
- Current stage: idea, research, sourcing, pre-launch, live ASIN, rescue, or stop-loss.
- Budget, team, supplier, and launch constraints.
- Required output: market decision, product selection, launch plan, profit rescue, inventory action, or kill/continue call.

Exit criteria:

- The user has a clear decision question.
- The next gate is obvious.
- Known constraints are separated from assumptions.

## Gate 1: Company Fit

Do not evaluate a market only by demand. First check whether the user can realistically play.

Score 1-5:

| Factor | Check |
| --- | --- |
| Brand fit | Does the product reinforce a believable brand promise? |
| Supply fit | Can existing suppliers, materials, or QA capabilities support it? |
| Capital fit | Can the first test batch be funded without overexposure? |
| Team fit | Can the team handle content, support, compliance, and operations? |
| Portfolio fit | Can this become a product lane with second and third SKUs? |

Decision:

- `Fit`: continue to demand and trend validation.
- `Weak Fit`: continue only if demand and margin are unusually strong.
- `No Fit`: reject or park unless the user has a strategic reason.

## Gate 2: Demand And Trend

Validate whether demand is durable rather than a noisy keyword spike.

Look for:

- Core keyword and long-tail cluster depth.
- Stable or rising trend evidence.
- Multiple buyer scenarios, not one fragile use case.
- Search terms with purchase intent.
- Seasonality, event-driven spikes, and fad risk.

Red flags:

- Demand depends on one trend term.
- Search intent is informational rather than purchase-driven.
- Social hype is not visible in Amazon search, reviews, or rank proxies.
- Seasonal peaks would require inventory commitments the user cannot absorb.

Decision:

- `Validate`: demand is plausible enough for deeper market analysis.
- `Watch`: demand exists but timing or durability is unclear.
- `Reject`: demand is weak, shallow, or too volatile.

## Gate 3: Market Structure

Use `market-screening-framework.md` for the full market score. At this gate, decide whether the arena is worth entering before choosing a SKU.

Required checks:

- Price-band health.
- Review barrier.
- Brand concentration.
- Listing quality gaps.
- Margin potential.
- Compliance burden.
- Capital requirement.
- Product-line extensibility.

Decision:

- `Enter Market`: durable demand, reachable wedge, acceptable economics, and follow-on path.
- `Watch Market`: attractive but timing, evidence, or execution is not ready.
- `Avoid Market`: structure is unattractive for a small brand.

## Gate 4: Competitor Map

Map competitors to find an entry wedge the user can actually execute.

Compare:

- Price, rating, review count, review velocity, and seller concentration.
- Image quality, title clarity, bullets, A+ content, and mobile readability.
- Review pain points, Q&A gaps, and unmet use cases.
- Bundle, size, material, feature, packaging, or positioning gaps.
- PPC difficulty and likely CPC pressure when evidence is available.

Output:

- 3-5 competitor groups.
- The strongest competitor moat.
- The weakest credible gap.
- First wedge recommendation.
- Why the wedge can convert without copying a competitor.

## Gate 5: VOC And Product Definition

Turn buyer evidence into a product definition before supplier work.

Capture:

- Target buyer and use case.
- Purchase trigger.
- Must-have requirements.
- Differentiators.
- Non-goals.
- Claims to avoid.
- Content promise.
- Packaging, materials, size, and QA implications.

Decision:

- `Define`: enough buyer evidence exists to create a product selection memo or PRD.
- `Research More`: pain points are still vague or contradictory.
- `Reject`: no meaningful buyer problem or differentiation path exists.

## Gate 6: ROI And Risk

The product must survive realistic economics, not only optimistic sales assumptions.

Calculate or estimate:

- Selling price and target price band.
- Landed cost, FBA fee, referral fee, storage, coupon, returns, and ad spend.
- Net margin and ROI.
- Break-even ACoS.
- MOQ, lead time, cash tied in inventory, and reorder exposure.
- Compliance, defect, return, and IP risk.

Default thresholds:

- Net margin below 15% is high risk for scaling.
- Break-even ACoS below 20% requires strong organic conversion or low CPC.
- High MOQ plus uncertain demand should usually become `Test First` or `No-Go`.
- Any hard compliance, IP, or safety blocker overrides a good market score.

Decision:

- `Go`: economics and execution risk are acceptable.
- `Test First`: opportunity is plausible but one or more assumptions need proof.
- `No-Go`: margin, cash, compliance, or execution risk is too weak.

## Gate 7: Validation Plan

Convert uncertainty into a small test.

Use a 7-day plan for research uncertainty:

1. Keyword cluster and trend check.
2. Top competitor price/review/rating map.
3. Review and Q&A pain mining.
4. Supplier cost and MOQ quote.
5. FBA fee and break-even ACoS estimate.
6. Compliance and IP risk screen.
7. Decision memo with next action.

Use a 30-day plan for execution uncertainty:

1. Sample or prototype validation.
2. Listing and image concept test.
3. Small PPC or keyword validation plan.
4. Supplier and packaging confirmation.
5. ROI update with real quotes.
6. Launch readiness checklist.
7. Go / Test First / No-Go review.

## Output Pattern

When using the stage-gate workflow, output:

1. Current gate and decision.
2. Gate score or evidence quality.
3. What passed.
4. What failed or remains unknown.
5. Next gate.
6. Smallest next action.
7. Stop condition or review trigger.

## Stop Rules

Stop or downgrade the opportunity when:

- The market has no credible second or third SKU.
- The user cannot fund a test batch without material cash-flow risk.
- The category requires compliance depth the team cannot manage.
- The offer has no buyer-visible differentiation.
- The product only works under optimistic ad cost, return rate, or landed cost.
- Competitor moats require review volume, brand trust, or price aggression the user cannot match.
