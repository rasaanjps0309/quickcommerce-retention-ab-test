# QuickBasket A/B Experiment  
### Free Delivery on Second Order — Impact on Week-1 Retention

---

## Overview

This project evaluates a product intervention designed to improve early user retention in a quick-commerce grocery platform.

The experiment tests whether **removing friction (free delivery on second order)** can increase repeat behavior during the most critical lifecycle window — **Day 0–7 after first purchase**.

---

## Business Context

QuickBasket is a quick-commerce platform operating across major Indian metros, offering 10–20 minute grocery delivery.

- Strong acquisition
- High activation (~63%)
- Weak retention (majority drop after first order)

---

## Problem Statement

Users place their first order but do not return for a second order within 7 days.

This prevents habit formation and limits long-term revenue.

---

## Hypothesis

Reducing friction in the second order (via free delivery) will improve Week-1 retention without impacting unit economics.

---

## Experiment Design

- Sample Size: 2,362 users  
- Split: 50% Control / 50% Treatment  
- Duration: 14 days  
- Trigger: Day 3 after first order  

### Variants:
- Control: No intervention  
- Treatment: Free delivery on second order (valid till Day 7)

---

## Results

- 7-day Return Rate:
  - Control: 35.8%  
  - Treatment: 42.2%  
  - Lift: **+6.4 percentage points**

- Statistically significant (p = 0.0008)

- Week-2 retention also improved → indicates habit formation

---

## Key Insights

- Reducing friction improves retention more effectively than discounts  
- Early retention (Day 0–7) is highly sensitive to intervention  
- Users continue behavior beyond incentive → habit formation  
- No negative impact on AOV or cancellations  

---

## Recommendation

Ship free delivery intervention to all new users.

---

## Impact

- +500 to 800 retained users/month  
- ₹8L – ₹13L revenue uplift  
- Low implementation cost  

---

## Tech Stack

- SQL (PostgreSQL)  
- Python (pandas, numpy, scipy)  
- Jupyter Notebook  

---

## Project Structure 
notebook/
quickbasket_ab_test_free_delivery_w1_retention.ipynb


Payel Saha 
