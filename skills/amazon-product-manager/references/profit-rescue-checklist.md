# Profit Rescue Checklist

Use this checklist when a product has a net margin below target, a high ACoS that is consuming contribution profit, or return drag that is making the unit economics unsustainable.

Work through each section in order. Stop at the first section where an action can materially move the margin before proceeding deeper.

---

## 0. Diagnose the Bottleneck First

Run this triage before touching any lever. Most margin problems have one primary driver; fixing secondary drivers without addressing the primary is waste.

| Symptom | Most likely bottleneck |
|---|---|
| Net margin is low but ACoS is in range | Price too low, COGS too high, or FBA size tier wrong |
| ACoS is high but organic rank is strong | Ad campaign structure (broad match waste, bid leakage) |
| ACoS is high and organic rank is weak | Conversion rate problem — listing, price, or reviews |
| Return rate is high | Product quality, expectation mismatch, or listing accuracy |
| Margin was fine 90 days ago but has fallen | Price erosion, rising CPC, storage fee increase, or competitor entry |
| Margin varies widely across SKUs in same ASIN | Variation profiling needed — kill or reprice losing variations |

---

## 1. Price and Revenue Levers

- [ ] **Is the current price at or above the floor needed for target net margin?**  
  Calculate: `Floor price = COGS + inbound freight + FBA fee + referral fee + ad spend per unit + return cost + target margin`  
  If current price is below floor, raise price and monitor CVR and rank impact for 14 days.

- [ ] **Is there headroom to test a price increase?**  
  Check competitor prices, BSR rank sensitivity, and review rating. A 5-10% price increase with stable rank often recovers 5-8 margin points.

- [ ] **Is there a coupon or promo that is subsidising ad-driven traffic with no payback?**  
  Remove or cap coupons on high-ACoS keywords. Coupon discount compounds on top of ad cost.

- [ ] **Is the product in a Subscribe & Save programme?**  
  S&S discount (5-10%) reduces margin on repeat orders. Verify the S&S cohort is profitable before maintaining enrollment.

---

## 2. COGS and Supply Chain Levers

- [ ] **Has COGS increased since launch without a corresponding price adjustment?**  
  Re-request factory quotes for the next order. If FOB has risen more than 10%, negotiate or re-source.

- [ ] **Is the current MOQ unnecessarily large, tying up cash and increasing storage fees?**  
  Reorder at a lower MOQ if turn rate allows. Higher cash efficiency often more than offsets a small COGS increase.

- [ ] **Is the carton size or product dimensions causing a higher FBA fee tier than necessary?**  
  Check whether reducing packaging dimensions moves the product from an oversized tier to a standard-size tier. A tier change can save $1-$4 per unit in FBA fees.

- [ ] **Is there a packaging or insert driving COGS with no conversion benefit?**  
  Remove premium packaging that buyers do not mention in reviews and does not affect listing perception.

---

## 3. FBA and Fulfillment Levers

- [ ] **Is FBA storage cost material due to slow turn or seasonal buildup?**  
  Calculate days of cover. If cover exceeds 90 days for a non-seasonal product, reduce the next inbound shipment or create a removal order for aged inventory.

- [ ] **Is there a long-term storage fee (LTS) approaching?**  
  Inventory over 365 days in FBA incurs additional charges. Plan a removal or promotional sell-down before the LTS date.

- [ ] **Is the product enrolled in FBA without checking whether multi-channel fulfillment or a 3PL is cheaper?**  
  For low-velocity or heavy products, compare total FBA cost vs. fulfillment by a 3PL on non-Amazon channels.

---

## 4. Advertising Levers (High ACoS)

- [ ] **Is the TACoS (total ACoS including organic sales) above 15%?**  
  High TACoS means ads are not building organic rank. Focus spend on 3-5 core ranking keywords, reduce broad match, and add negative keywords.

- [ ] **Are there auto-campaign search terms converting at an ACoS above break-even?**  
  Pull the search term report. Add converting terms to an exact-match manual campaign and negate them from auto. Remove or bid down non-converting terms.

- [ ] **Is the CPC rising without a corresponding rank or CVR improvement?**  
  CPC rises when competitor bids increase or keyword relevance drops. Reduce bids to a sustainable ceiling and test whether rank holds at lower spend.

- [ ] **Is the ad budget split across too many campaigns with no clear winner?**  
  Consolidate to 2-3 campaigns per ASIN: one auto, one exact/phrase manual for ranking keywords, one defensive ASIN-targeting campaign. Pause experimental campaigns until profitability is restored.

- [ ] **Is there a sponsored brand or display budget running on a loss-making ASIN?**  
  Pause all awareness spend until the ASIN is at break-even on sponsored product alone.

---

## 5. Return and Refund Levers

- [ ] **Is the return rate above 5%?**  
  Pull the return reason report. The top 3 return reasons determine the fix:
  - "Not as described" → fix listing copy or images
  - "Defective / doesn't work" → investigate QA with the factory
  - "Changed mind" → consider whether the listing over-promises
  - "Wrong item sent" → check FBA label accuracy and ASIN prep

- [ ] **Are returns creating unsellable inventory?**  
  Calculate the effective unit cost including write-off of unsellable units. If return rate is high, add a QA-fail reserve to the margin model.

- [ ] **Is the listing creating expectation mismatch?**  
  Compare the top return complaints to the listing claims in the title, bullets, and A+ content. Correct any specific claims that are driving false expectations.

---

## 6. Rescue Decision Gate

After working through the checklist, assess the rescue path:

| Outcome | Decision |
|---|---|
| At least 2 material levers identified; fix is actionable within 30 days | **Rework Offer** — execute fixes and review in 30 days |
| Levers exist but require factory rework, certification, or major listing rebuild | **Test First** — run a controlled experiment before committing to full rescue |
| No lever moves the margin above 15% under realistic assumptions | **Kill or Liquidate** — stop reordering; liquidate current stock and reallocate capital |

---

## Margin Model Snapshot

Fill in after running through the checklist:

```
Sale price:              $
Amazon referral fee:    −$
FBA fulfillment fee:    −$
COGS (FOB + freight):  −$
Inbound per unit:       −$
Ad spend per unit:      −$
Return allowance:       −$
Storage allocation:     −$
Other:                  −$
─────────────────────────
Net profit per unit:    $
Net margin:              %
```

If net margin is below 15% after all fixes, re-run the rescue decision gate.
