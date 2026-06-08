# Marketing A/B Testing — Ad Campaign Effectiveness Analysis

## Business Problem
An e-commerce company ran an ad campaign and wanted to know:
**Did the ads significantly increase user conversion rates compared to a control group (PSA)?**

## Dataset
- Source: Kaggle — Marketing A/B Testing Dataset
- 588,101 users split into two groups:
  - `ad` (Treatment): 564,577 users who saw the advertisement
  - `psa` (Control): 23,524 users who saw a public service announcement

## Methodology
1. Exploratory Data Analysis — conversion rates by group, sample size check
2. Normality check — Shapiro-Wilk test on sampled data
3. Sample size & statistical power validation (80% power, α = 0.05)
4. Two-proportion Z-test (appropriate for binary conversion data)
5. Confidence interval estimation

## Results

| Group | Conversion Rate | 95% Confidence Interval |
|-------|----------------|--------------------------|
| Ad (Treatment) | 2.55% | 2.51% – 2.60% |
| PSA (Control) | 1.79% | 1.62% – 1.95% |

- **Z-statistic: 7.37**
- **P-value: < 0.0001**
- **Decision: Reject H₀**

## Business Recommendation
The ad campaign produced a statistically significant lift of **~0.77 percentage points** in 
conversion rate (2.55% vs 1.79%), with p < 0.0001 — far below the 0.05 threshold. 
The confidence intervals do not overlap, further confirming the effect is real and not 
due to chance. **Recommendation: continue and scale the ad campaign.**

## Tools
Python, Pandas, NumPy, SciPy, Statsmodels, Matplotlib, Seaborn, Jupyter Notebook
