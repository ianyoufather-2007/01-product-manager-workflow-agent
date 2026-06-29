# Complete Example: Market Screening with Expected Output

This file shows a full end-to-end run of the `amazon-product-manager` skill for a market screening request. All data is synthetic; no real seller, supplier, or paid-tool data is used.

---

## Input Prompt

```text
Act as Product Manager Workflow Agent.

Use the bundled amazon-product-manager skill to evaluate this Amazon product decision.

Marketplace:       Amazon US
Product/category:  ceramic matcha whisk stand
Business context:  Small brand, limited launch budget, target price $18-$28, first batch under $4,000 landed cost.
Available evidence:
  - Keyword "matcha whisk stand" shows consistent monthly searches; broader term "matcha accessories" is growing.
  - Competitors: mostly generic white/beige ceramic pieces at $10-$22; a few branded bamboo options at $25-$35.
  - Top listings have 200-800 reviews; a few newer entries have 30-80 reviews and 4.3+ ratings.
  - Common complaints: chip-prone edges, no drainage hole, wrong width for wide whisks.
  - FBA estimate: lightweight item, ~0.4 lb, standard-size tier, estimated FBA fee ~$3.40.
  - Target COGS from Alibaba RFQ: $3.50-$5.00 per unit FOB, MOQ 200 units.

Main question:
Should we enter, watch, or avoid this market?

Return:
1. Decision summary
2. Current decision type
3. Known facts
4. Signal reading
5. Risks
6. Missing evidence
7. Next actions
8. Meeting-ready recommendation
```

---

## Expected Output

### Decision Summary

**Enter Market — conditional on validating drainage hole differentiation and hitting ≤$5.20 all-in landed cost.**

The ceramic matcha whisk stand market has durable demand tied to the growing matcha ritual category, visible product gaps in the current competition, and accessible review barriers for a new entrant. Unit economics are viable if COGS stays under $5.00 and the product ships in a standard-size FBA tier.

---

### Current Decision Type

**Market Screening → Pre-selection**

The question is answered at the market level; move to pre-selection once a specific SKU is chosen.

---

### Known Facts

| # | Fact | Source |
|---|------|--------|
| 1 | "matcha whisk stand" has consistent monthly search volume; "matcha accessories" cluster is growing | Keyword research (user-provided signal) |
| 2 | Price band: $10-$35; most generic options cluster at $10-$22 | Amazon search results |
| 3 | Top competitors: 200-800 reviews; newer entrants: 30-80 reviews at 4.3+ | Amazon listings |
| 4 | Common complaints: chip-prone edges, no drainage hole, width mismatch for wide whisks | User-provided review signal |
| 5 | FBA fee estimate: ~$3.40 for standard-size | FBA calculator estimate |
| 6 | Target COGS: $3.50-$5.00 FOB, MOQ 200 units | Alibaba RFQ (estimated, not confirmed) |
| 7 | First batch cap: $4,000 landed cost | User-provided constraint |

---

### Signal Reading

**Positive signals:**

- Keyword demand is stable and tied to a wider growing category (matcha ritual / tea culture), not a single trend term — reduces fad risk.
- Review barriers are accessible: several recent entrants rank and convert with <100 reviews, suggesting the category is not fully consolidated.
- Product gap is specific and fixable: a drainage hole and wider-compatible design address the most-cited complaints without requiring new tooling beyond a minor mold change.
- Price band supports a target net margin above 25% if COGS lands at $4.50 and listing price is $24.99.

**Caution signals:**

- COGS range of $3.50–$5.00 is wide; margin math at the high end ($5.00 COGS) tightens significantly.
- Compliance: ceramic products may require lead and cadmium safety testing in some markets. Not confirmed yet.
- The differentiation angle (drainage hole, wider sizing) is easy to copy once visible to competitors.

---

### Risks

| Priority | Risk | Mitigation |
|---|---|---|
| P0 | COGS at $5.00 FOB with freight and FBA leaves margin below 20% | Require factory quote ≤$4.50 before committing to MOQ |
| P0 | No compliance confirmation for ceramic/clay products | Obtain FDA or CA Prop 65 test report before first shipment |
| P1 | Differentiation (drainage hole) is visible and copyable within 6 months | Use design, branding, and bundling (whisk + stand) to extend the moat |
| P1 | "Matcha accessories" growth is category-level; "whisk stand" specifically may plateau | Expand keyword targeting to matcha sets, matcha tools, tea ceremony accessories |
| P2 | MOQ of 200 units at $5.00 COGS + freight may approach the $4,000 cap | Negotiate a 150-unit sample run for the first batch |

---

### Missing Evidence

| Priority | Gap | Why It Matters | Next Step |
|---|---|---|---|
| P0 | Confirmed FOB price at target spec (drainage hole, wide-base mold) | Margin math depends on this number | Request 3 factory quotes with drainage-hole spec by [date + 10 days] |
| P0 | Ceramic compliance requirements (lead/cadmium, FDA, Prop 65) | Legal risk and added test cost could change the budget | Check Amazon listing policy + contact a compliance broker within 7 days |
| P1 | Landed cost with actual freight quote (sea vs air, carton dimensions) | FBA fee tier depends on packed dimensions | Get a freight estimate once factory spec is confirmed |
| P1 | Click-through and conversion rate proxy for similar ASINs | Validates whether organic ranking is achievable | Pull BSR trends and review velocity for the top 5 competitors |
| P2 | Whisk width standards (most common sizes) | Needed for mold spec | Measure 5 competitor whisks or check product descriptions |

---

### Next Actions

1. **[Day 1–3]** Request quotes from 3 Alibaba suppliers for ceramic whisk stand with drainage hole, base diameter 8–9 cm, MOQ 100–200 units. Ask for CAD or sample photos.
2. **[Day 1–5]** Check Amazon US listing policy for ceramics; contact a China-based compliance broker for Prop 65 cost estimate.
3. **[Day 3–7]** Pull BSR and review velocity for ASINs B0XXXXXX, B0YYYYYY, B0ZZZZZZ (top competitors). Calculate monthly unit sales proxy.
4. **[Day 7–10]** Compare factory quotes. If COGS ≤$4.50 FOB and compliance cost is <$500, advance to pre-selection.
5. **[Day 10]** Review decision gate: proceed to sampling or revisit market with updated data.

---

### Meeting-Ready Recommendation

> **Enter — conditional.** The ceramic matcha whisk stand market has genuine demand, a visible product gap (drainage hole, wider base), and accessible review barriers for a new entrant. Unit economics are viable at $24.99 with COGS ≤$4.50. Two blockers must clear before committing to MOQ: (1) factory quote at or below $4.50 FOB with drainage-hole spec, and (2) confirmation that compliance costs are manageable. If both clear within 10 days, advance to sampling.

---

## Notes on This Example

- Sales volumes, keyword counts, and competitor review numbers are **synthetic** — not pulled from any paid tool.
- COGS and freight figures are illustrative estimates used for margin math only.
- This example is intended to show the output structure, not to predict real market performance.
