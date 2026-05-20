# ALAT for Business Onboarding Analytics: Identifying and Engaging Non-Enrolled Corporate Customers in the Apapa Zone

**Author:** Prudence Mordi  
**Role:** Zonal Manager, Commercial Banking Division  
**Organisation:** Major Tier-1 Nigerian Commercial Bank  
**Zone:** Apapa (Branches: Orile Iganmu · Ajeromi)  
**Programme:** LBA – EMBA (UA High)

---

## Overview

This capstone analyses **103 corporate current account records** across the Apapa zone to generate a detailed breakdown of customers not enrolled in **ALAT for Business (AFB)** and build a prioritised onboarding engagement list for Relationship Managers.

**The dataset is the target population:** every one of the 103 sampled accounts has `On AFB = No` — 100% non-enrollment. The analytical task is therefore not to predict *who* is unenrolled (all are), but to profile the non-enrolled population by segment, account status, product type, and officer, so that onboarding outreach can be sequenced by commercial priority.

---

## Business Question

> Which customers are not on ALAT for Business, and how should outreach be prioritised — by product type, account status, account officer, or account vintage?

---

## Dataset

| Item | Detail |
|---|---|
| File | `dataset/AFB for non curr.csv` |
| Records | 103 accounts |
| Zone | Apapa |
| Branches | Orile Iganmu, Ajeromi |
| Source | Core Banking Platform (CRM) — SQL extract, April 2026 |
| Account opening range | August 2000 – January 2026 |
| **On AFB** | **No — 103/103 (100%)** |
| Account Status | Active: 60 (58.3%) · Dormant: 40 (38.8%) · Inactive: 2 (1.9%) |
| Product split | Corporate Current Account: 83 (80.6%) · Non-Individual: 20 (19.4%) |
| Currency | NGN (all records) |

> **Key data fact:** Because all sampled accounts are unenrolled, the `On AFB` column has no variance. Statistical tests that require two outcome levels (logistic regression, chi-squared on AFB status, t-tests by AFB group) are not applicable and are skipped gracefully in the analysis with explanatory notes.

---

## Analytical Techniques

| # | Technique | Applied to |
|---|---|---|
| 1 | **Exploratory Data Analysis** | Profile the 103 non-enrolled accounts by product, status, officer, branch, and vintage |
| 2 | **Data Visualisation** | Charts of non-enrollment composition for RM briefings and zone reporting |
| 3 | **Hypothesis Testing** | Test whether account status (Active vs. Dormant) and product type differ significantly by branch or officer |
| 4 | **Correlation Analysis** | Identify which account characteristics (age, product, status) co-vary — informs onboarding sequencing |
| 5 | **Logistic Regression** | Not estimable on this dataset (zero variance in outcome); documented with explanation |

---

## Onboarding Priority Framework

Since all accounts need onboarding, prioritisation is based on commercial value and engagement likelihood:

| Priority | Criteria | Rationale |
|---|---|---|
| **Tier 1 — Immediate** | Active accounts · Corporate product | Active accounts have live transactional relationships — easiest to convert |
| **Tier 2 — Targeted** | Active accounts · Non-Individual product | Higher-value segment but may require specialist pitch |
| **Tier 3 — Reactivation first** | Dormant / Inactive accounts | Address dormancy before onboarding to AFB |

---

## Key Facts from the Data

- **100% of sampled accounts** (n = 103) are not on ALAT for Business — the entire sample is the onboarding pipeline
- **60 active accounts** are the highest-priority conversion targets (no dormancy barrier)
- **83 corporate accounts** (80.6%) vs. **20 non-individual accounts** (19.4%)
- **2 branches** covered: Orile Iganmu and Ajeromi
- **25+ year portfolio span** (accounts opened 2000–2026) — the onboarding gap is not a new-account problem

---

## Project Structure

```
banking_portfolio_analytics.qmd     # Quarto source (R + Python dual implementation)
banking_portfolio_analytics.html    # Rendered output
dataset/
  AFB for non curr.csv              # 103 non-enrolled corporate accounts, Apapa zone
docs/                               # Supporting documentation
```

---

## Tools & Environment

| Component | Tool |
|---|---|
| Data extraction | SQL Server Management Studio 2019 |
| Analysis | Python 3.10 + R 4.3 via Quarto 1.4 |
| Python libraries | `pandas`, `numpy`, `scipy`, `scikit-learn`, `statsmodels`, `matplotlib`, `seaborn` |
| R libraries | `dplyr`, `ggplot2`, `broom`, `knitr`, `kableExtra`, `pROC`, `corrplot` |

```bash
quarto render banking_portfolio_analytics.qmd
```
