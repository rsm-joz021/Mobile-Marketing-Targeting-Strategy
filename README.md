# Mobile-Marketing-Targeting-Strategy
---

## Project Overview
This project analyzes whether **profit-based targeting** improves the performance of a mobile push notification campaign compared to sending messages to all eligible users.

Using data from a randomized mobile marketing experiment at Tuango, the analysis models customer response and demand, translates predictions into profit and ROME, and validates results using a rollout dataset.

---

## Key Results

### Modeling Approach
- **Purchase probability** is estimated using logistic regression.
- Features include RFM variables, demographics, and prior category behavior.
- Model interpretability is assessed via partial dependence plots and permutation importance.

---

### Business Metrics
Customer-level expected profit is computed as:
Expected Profit
= Purchase Probability × Expected Order Size × Price × Platform Commission
− Push Notification Cost

Performance is evaluated using:
- **Total profit**
- **Return on Marketing Expenditure (ROME)**

---

### Test Sample Results (Experimental Evaluation)
Using the randomized test sample:

- **Target-all strategy**
  - Profit: $130578
  - ROME: 3.7%

- **targeting strategy**
  - Profit: $881237
  - ROME: 56.2%

**Improvement over target-all (test sample):**
- Profit increase: $750695 (574.87% improvement rate)
- ROME increase on percentage: 52.5%

---

### Full Rollout Results Validation
Applying the same targeting rule to the full eligible population to validate our envision:

- **Target-all strategy**
  - Profit: $111712
  - ROME: 3.1%

- **targeting strategy**
  - Profit: $887423
  - ROME: 56.6%

**Improvement over target-all (full rollout):**
- Profit increase: $775711 (694.38% improvement rate)
- ROME increase on percentage: 53.5%

---

## Methods & Tools
- Logistic regression (purchase probability)
- Expected profit and ROME analysis
- Python (pandas, statsmodels, pyrsm)
