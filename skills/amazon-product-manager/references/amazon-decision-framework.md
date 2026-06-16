# Amazon Decision Framework

Use this reference to make Amazon product management decisions across market screening, selection, launch, growth, rescue, and stop-loss stages.

## Decision Flow

1. Define the decision: choose market, enter, source, launch, scale, optimize, rescue, liquidate, or kill.
2. If the question is earlier than a single SKU, run market screening first using `market-screening-framework.md`.
3. Identify stage: market screening, pre-selection, sampling/sourcing, pre-launch, launch, growth, maturity, decline, or stop-loss.
4. Score the opportunity using demand, competition, economics, differentiation, operations, and capital pressure.
5. Diagnose the main bottleneck: market fit, demand, listing, price, ads, margin, inventory, reviews, compliance, or supply.
6. Decide: `Enter Market`, `Watch Market`, `Avoid Market`, `Go`, `No-Go`, `Test First`, `Rework Offer`, or `Kill or Liquidate`.
7. Convert the decision into ranked actions, owner handoffs, metrics, and a review date.

## Opportunity Score

Score each factor from 1 to 5. Higher is better except where noted.

| Factor | 1 | 3 | 5 |
| --- | --- | --- | --- |
| Demand strength | Weak or unclear search demand | Some keyword and trend evidence | Strong keyword demand, stable/rising trend, clear buyer intent |
| Competition attractiveness | Head brands dominate, high reviews, strong listings | Mixed competitors and some gaps | Fragmented competitors, weak listings, visible pain points |
| Profit room | Net margin likely below 15% | Net margin around 15-25% | Net margin above 25% after ads and returns |
| Differentiation space | Commodity with no clear improvement | Some bundle/content/feature room | Clear product, offer, content, or segment gap |
| Operational feasibility | High compliance, MOQ, defect, or supply risk | Manageable execution risk | Simple sourcing, reliable supply, manageable support |
| Capital pressure | High inventory cash need or slow turn | Moderate cash cycle | Fast turn or small validation batch possible |

Recommended interpretation:

- 24-30: likely `Go` if no critical compliance or margin blocker exists.
- 18-23: usually `Test First` or `Rework Offer`.
- 12-17: usually `No-Go` unless there is a strategic reason.
- Below 12: `No-Go`.

Do not let the score replace judgment. Override the score when compliance risk, cash flow, review barriers, or margin math makes execution impractical.

## Stage Playbooks

### Market Screening

Focus on market pool, scenario cluster, keyword depth, price-band health, brand concentration, review barrier, product-line extensibility, compliance burden, capital fit, and a realistic first wedge. Use `Enter Market`, `Watch Market`, or `Avoid Market` before judging individual SKUs.

### Pre-selection

Focus on keyword demand, competitor concentration, price band, review barriers, differentiation, COGS estimate, FBA fit, and seasonality inside an already screened market. Prefer `Test First` when demand exists but margin or competitor gaps are uncertain.

### Sampling and Sourcing

Focus on supplier reliability, landed cost, MOQ, defect rate, compliance, packaging, dimensions, and whether the product can hit the target price and margin. Use `No-Go` if the unit economics only work under optimistic assumptions.

### Pre-launch

Focus on listing readiness, keyword map, hero image, bullets, A+ content, review plan, launch inventory, coupon, pricing, PPC structure, and dashboard metrics. Use `Rework Offer` when the offer is not yet strong enough for launch.

### Launch

Focus on CTR, CVR, CPC, ACoS, keyword rank movement, review velocity, stockout risk, and early return signals. Use `Test First` for controlled budget and keyword experiments.

### Growth

Focus on organic rank, TACoS, repeatable conversion gains, variation/bundle expansion, pricing power, ad portfolio structure, review moat, and inventory turn.

### Decline or Stop-loss

Focus on aged inventory, negative contribution margin, falling rank, weak review recovery, rising CPC, stock pressure, and opportunity cost. Use `Kill or Liquidate` when recovery requires more investment than the expected upside.

## Diagnostic Models

### Market Screening Diagnosis

Check macro arena, scenario clusters, keyword cluster depth, price bands, brand concentration, review barriers, margin range, compliance burden, supplier feasibility, capital requirement, and product-line extensibility. Tie recommendations to market score, first wedge, validation speed, net margin potential, and follow-on SKU path.

### Listing Diagnosis

Check title, main image, secondary images, bullets, A+ content, Q&A, reviews, rating, variation structure, keyword coverage, mobile readability, claim compliance, and competitor contrast. Tie recommendations to CTR, CVR, keyword rank, rating, and return rate.

### Launch Diagnosis

Check launch goal, ranking keywords, starting price, coupon, first inventory batch, review acquisition path, PPC campaign structure, budget cap, monitoring cadence, and rollback triggers. Tie recommendations to CTR, CVR, ACoS, rank, sell-through, and stockout risk.

### Profit Diagnosis

Check selling price, COGS, inbound freight, FBA fee, referral fee, storage fee, coupon/promo cost, ad spend, return cost, removals, and reimbursements. Tie recommendations to net margin, ROI, contribution profit, and break-even ACoS.

### Growth Diagnosis

Check ad efficiency, keyword rank, organic share, CVR, price elasticity, review moat, bundle opportunities, variation opportunities, brand store, Subscribe & Save, and off-Amazon traffic. Tie recommendations to TACoS, organic sales mix, rank, repeat purchase, and margin.

### Inventory Diagnosis

Check sell-through, days of cover, lead time, reorder point, MOQ, storage fees, aged inventory, seasonality, and cash tied in stock. Tie recommendations to stockout risk, storage cost, cash conversion cycle, and liquidation loss.

### Stop-loss Diagnosis

Check whether the issue is fixable. Fixable issues include weak creative, poor keyword structure, bad PPC segmentation, pricing mismatch, and missing A+ content. Hard blockers include unrecoverable rating damage, no margin after realistic ad spend, high defect or return rate, compliance risk, and competitor moats that cannot be challenged.

## Default Thresholds

- A market without a credible second and third product should be treated as a single-SKU bet, not a strategic product lane.
- A small brand should avoid markets where the first validation batch requires too much inventory cash or paid traffic before conversion proof.
- If keyword depth is shallow and demand depends on one trend term, use `Watch Market` or `Avoid Market` unless there is strong external evidence.
- Net margin below 15% is high risk; rework price, COGS, FBA size, ad spend, coupon, or return costs before scaling.
- Break-even ACoS below 20% means low ad tolerance; require strong organic rank, high CVR, or lower COGS before aggressive PPC.
- Head competitors with high ratings, very high review counts, and concentrated brand share increase entry difficulty.
- Strongly seasonal products require separate inventory and cash-flow analysis.
- High-return categories must include return cost and unsellable inventory in the decision.
- A product with negative contribution margin after realistic ads should not scale, even if revenue is growing.
- A launch plan without inventory coverage, keyword targets, PPC budget limits, and rollback triggers is not launch-ready.

## Output Pattern

Use this compact structure when the user asks for a decision:

1. Decision: `Go`, `No-Go`, `Test First`, `Rework Offer`, or `Kill or Liquidate`.
2. Why: 3-5 evidence bullets across demand, competition, economics, operations, and risk.
3. Score: factor table when enough evidence exists; otherwise state missing evidence.
4. Actions: ranked next moves with owner, metric, and timeline.
5. Watchouts: risks that could change the decision.
6. Review point: date, metric threshold, or trigger for revisiting the decision.
