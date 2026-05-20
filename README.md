# ALAT for Business Onboarding Analytics

**Author:** Prudence Mordi  
**Course:** Data Analytics 1 — Capstone Case Study, Lagos Business School · April 2026

---

## Overview

This project analyses 103 corporate current account records in the Apapa zone (Orile Iganmu and Ajeromi branches) to build a prioritised onboarding engagement list for Relationship Managers targeting ALAT for Business (AFB) non-enrollment.

All 103 sampled accounts have `On AFB = No`. Because the primary outcome has zero variance, the analysis uses **Account Status** (Active vs Dormant/Inactive) as the working outcome — producing a 60/42 split that makes all five statistical techniques fully estimable.

## Business Question

> Among 103 non-enrolled accounts, which are commercially active and ready for immediate AFB onboarding, and which need account reactivation first?

## Dataset

| Item | Detail |
|---|---|
| File | `dataset/AFB for non curr.csv` |
| Records | 103 accounts |
| Source | Core Banking CRM — SQL extract, April 2026 |
| Zone | Apapa (Orile Iganmu · Ajeromi) |
| Outcome | Account Status: Active 60 · Dormant 40 · Inactive 2 |
| Product split | Corporate Current: 83 · Non-Individual: 20 |

## Analysis

Five techniques applied using R and Python in a dual-implementation Quarto document:

1. **EDA** — Profile non-enrolled accounts by product, officer, status, and vintage
2. **Visualisation** — Account status breakdowns by product type and account officer
3. **Hypothesis Testing** — Chi-squared (product type vs status); Welch's t-test (account age vs status)
4. **Correlation** — Pearson correlations between dormancy, product type, and account age
5. **Logistic Regression** — Predict dormancy probability to generate a tiered outreach call list

## Results

Accounts are segmented into three outreach tiers based on predicted dormancy probability:

- **High Priority — Outreach Now:** Active accounts → immediate AFB enrollment
- **Monitor / Reactivate First:** Borderline accounts → reactivation check before enrollment
- **Dormancy Campaign:** Dormant/Inactive accounts → reactivation campaign first

## Reproduce

```bash
quarto render banking_portfolio_analytics.qmd
```

Requires R 4.x and Python 3.10+. R packages: `dplyr`, `ggplot2`, `knitr`, `kableExtra`, `pROC`, `corrplot`. Python packages: `pandas`, `numpy`, `scipy`, `scikit-learn`, `statsmodels`, `matplotlib`, `seaborn`.

## Project Structure

```
banking_portfolio_analytics.qmd   # Quarto source (R + Python)
banking_portfolio_analytics.html  # Rendered output
dataset/
  AFB for non curr.csv            # 103 non-enrolled accounts
docs/
  RPubs - EMBA-31-Take-Home-Exam-April-2026.pdf
```
