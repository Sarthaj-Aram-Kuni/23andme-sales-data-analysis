# 23andme-sales-data-analysis
![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange)
![SciPy](https://img.shields.io/badge/SciPy-Statistical%20Testing-green)

# Project Overview
This project analyzes 50 weeks of timestamped sales data to identify trends, anomalies, and customer demographic shifts. The analysis was conducted as part of a data science take-home assignment (23andMe recruitment case study).

The primary objective was to investigate a sudden discontinuity in daily sales volume, determine its statistical significance, and assess if changing gender demographics were a contributing factor.

## Repository Structure
|File/Folder  | Description|
|---------------|-------------------------------|
data| 50 csv files of datasets

## Key Findings

### 1. Identification of Sales Surge
Visual inspection of the time-series data revealed a distinct discontinuity in sales volume.

- **Event Date:** April 29, 2013
- **Observation:** Daily sales volume shifted from a mean of **~504 units** to **~703 units**.

![Sales Trend](images/sales_trend.png)
*(Figure 1: Daily sales over 50 weeks showing the clear step-change in late April)*

### 2. Statistical Significance (A/B Testing)
To confirm this was a fundamental shift rather than random volatility, an independent two-sample t-test was performed comparing daily sales before and after April 29th.

- **Hypothesis:** $H_0$: $\mu_{before} = \mu_{after}$ vs $H_1$: $\mu_{before} \neq \mu_{after}$
- **T-Statistic:** `-45.94`
- **P-Value:** `3.49e-138`

**Conclusion:** With a p-value effectively at zero ($p < 0.05$), the increase in sales is **statistically significant**.

### 3. Gender Demographics Analysis
Investigated whether the sales spike was driven by a shift in the proportion of male vs. female customers.

-
