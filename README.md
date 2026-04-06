# QuickBasket — A/B Test: Free Delivery on Second Order

**Testing whether friction removal drives Week-1 retention better than discounting.**

---

## Background

Retention analysis of QuickBasket's Q1 2025 user base revealed a critical problem: 60–75% of first-time buyers never return within Week 1. The root cause is a discount expectation cliff — users acquired with ~24% first-order discounts perceive a value drop when order 2 reverts to full price, and they leave.

Survival analysis confirmed that churn risk peaks at Day 14–18, and the reorder conversion window effectively closes by Day 14.

Full diagnostic analysis: [quickcommerce-habit-formation-retention](https://github.com/rasaanjps0309/quickcommerce-habit-formation-retention)

This experiment tests a different approach: instead of discounting, **remove friction** by offering free delivery on the second order.

---

## Experiment Design

| Parameter | Detail |
|---|---|
| Objective | Increase 7-day return rate for first-time buyers |
| Control | Standard welcome discount, no structured follow-up |
| Treatment | Standard welcome discount + free delivery nudge on Day 3, valid until Day 7 |
| Primary metric | % of first-time buyers placing a second delivered order within 7 days |
| Baseline | 37% |
| MDE | 5 percentage points (37% to 42%) |
| Significance | 95% confidence, one-sided z-test |
| Power | 80% |
| Sample | 1,181 per group (2,362 total) |
| Duration | 14 days (7 days enrollment + 7 days measurement) |

---

## Results

### Primary Metric — 7-Day Return Rate

| | Control | Treatment |
|---|---|---|
| Return rate | 35.8% | 42.2% |
| Absolute lift | | +6.4 ppts |
| P-value | | 0.0008 |
| 95% CI for lift | | [+2.4%, +10.3%] |

Statistically significant. The entire confidence interval is above zero.

### Guardrails — All Passed

| Metric | Control | Treatment | Threshold | Status |
|---|---|---|---|---|
| Second order AOV | Rs.364 | Rs.354 | >= Rs.250 | Pass |
| Cancellation rate | 4.3% | 3.6% | <= 8% | Pass |
| Discount per user | Rs.4.8 | Rs.2.4 | <= control + Rs.40 | Pass |

Users did not place junk orders to exploit free delivery. Cancellation rates were healthy. Treatment users actually used less discount overall — the free delivery replaced coupon-seeking behavior.

### Secondary Metric — Does the Effect Last?

| | Control | Treatment |
|---|---|---|
| W2 return rate | 18.7% | 23.3% |
| P-value | | 0.003 |

The treatment effect sustained into Week 2 without any additional incentive. Users brought back by the free delivery nudge continued ordering on their own. This confirms the intervention is creating genuine habit momentum, not just buying a one-time transaction.

### Who Benefited Most?

| Channel | Control | Treatment | Lift |
|---|---|---|---|
| Meta ads | 30.6% | 39.6% | +9.0 ppts |
| App store | 37.8% | 45.6% | +7.8 ppts |
| Offline events | 31.0% | 38.0% | +7.0 ppts |
| Influencer | 27.4% | 34.2% | +6.7 ppts |
| Google ads | 33.6% | 40.0% | +6.4 ppts |
| Referral | 45.2% | 49.6% | +4.4 ppts |
| Organic search | 43.8% | 47.9% | +4.1 ppts |

Paid channel users — who had the lowest baseline return rates — showed the largest improvement. The intervention helps the users who need it most.

---

## Decision

### Ship to 100% of new users.

The primary metric is significant (p = 0.0008), all guardrails passed, and the effect sustains into Week 2.

### Projected Impact

| Metric | Estimate |
|---|---|
| Additional retained users per month | ~500–800 |
| Monthly revenue uplift | Rs.8–13 lakh |
| Monthly intervention cost | ~Rs.1.2 lakh |
| Net monthly impact | Rs.7–12 lakh |

### Recommended Next Steps

1. Ship free delivery nudge to all new first-time buyers across all cities and channels
2. Monitor Pune city-level performance in scaled rollout (anomalous negative result in test, likely sampling noise)
3. Design PMI Stage 2: test progressive incentives for W2 and W3 retention to push users toward the 4-week habit lock-in threshold
4. Separately test reduced first-order discount (12–15% instead of 24%) to address the discount expectation cliff at its root

---

## Tech Stack

PostgreSQL (pgAdmin) · Python (pandas, numpy, scipy) · Jupyter Notebook · Claude AI

---


**Payel Saha** 
Retention analytics, habit formation, and lifecycle strategy for consumer tech.
