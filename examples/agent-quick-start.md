# Agent Quick Start

This example shows how to use `agents/product-manager-workflow-agent/AGENT.md` as a lightweight workflow wrapper around the core `amazon-product-manager` skill.

## When To Use This Agent

Use this wrapper when you want one agent entrypoint for:

- Market screening.
- Product selection.
- Launch planning.
- Profit repair.
- Inventory risk review.
- Stop-loss decisions.
- Boss/meeting-ready product memos.

For the newer integrated 000-007 stage-gate workflow, use `amazon-pm-integrated-agent`.

## Copy-Ready Prompt

```text
Act as Product Manager Workflow Agent.

Use the bundled amazon-product-manager skill to evaluate this Amazon product decision.

Marketplace:
Product/category:
Business context:
Available evidence:
Main question:

Return:
1. Decision summary
2. Current decision type
3. Known facts
4. Signal reading
5. Risks
6. Missing evidence
7. Next actions
8. Meeting-ready recommendation

Rules:
- Do not invent sales, search volume, profit, compliance, or review conclusions.
- Separate facts from interpretation.
- Make missing evidence visible.
```

## Example Input

```text
Marketplace: Amazon US
Product/category: coffee capsule holder
Business context: small brand, limited launch budget, target price $15-$35
Available evidence:
- Search demand appears stable
- Competitors include drawers, towers, wall racks, and countertop organizers
- Reviews mention flimsy structure, drawer jams, counter space, and capsule compatibility
Main question:
Should we enter, watch, avoid, or test this market first?
```

## Expected Output Shape

```text
## Decision Summary

## Current Decision Type

## Known Facts

## Signal Reading

## Risks

## Missing Evidence

| Priority | Gap | Why It Matters | Next Step |
| --- | --- | --- | --- |
| P0 |  |  |  |
| P1 |  |  |  |
| P2 |  |  |  |

## Next Actions

## Meeting-Ready Recommendation
```
