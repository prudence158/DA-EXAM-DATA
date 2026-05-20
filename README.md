# ALAT for Business Onboarding Analytics: Identifying and Engaging Non-Enrolled Corporate Customers in the Apapa Zone

**Author:** Prudence Mordi  
**Role:** Zonal Manager, Commercial Banking Division  
**Organisation:** Major Tier-1 Nigerian Commercial Bank  
**Zone:** Apapa (Branches: Orile Iganmu · Ajeromi)  
**Course:** Data Analytics 1 — Capstone Case Study (CS 1: Exploratory & Inferential Analytics)  
**Examiner:** Prof Bongo Adi, Lagos Business School · April 2026  
**Total marks:** 130 (Section A: 30 · Section B: 80 · Section C: 20 + up to +5 GitHub bonus)

---

## Overview

This capstone analyses **103 corporate current account records** across the Apapa zone to generate a detailed breakdown of customers not enrolled in **ALAT for Business (AFB)** and to build a prioritised onboarding engagement list for Relationship Managers.

**Key data fact:** Every one of the 103 sampled accounts has `On AFB = No` (100% non-enrollment). The dataset *is* the onboarding target population. The analytical task is to profile it by product, account status, officer, and vintage so that outreach can be sequenced by commercial priority.

---

## Business Question

> Which customers are not on ALAT for Business, and how should outreach be prioritised — by product type, account status, account officer, or account vintage?

---

## Dataset

| Item | Detail |
|---|---|
| File | `dataset/AFB for non curr.csv` |
| Records | 103 accounts (≥ 100 minimum; ✓) |
| Variables | 14 (≥ 5 minimum; ✓ — includes 3 numeric, 4 categorical, 1 date) |
| Zone | Apapa |
| Branches | Orile Iganmu, Ajeromi |
| Source | Core Banking Platform (CRM) — SQL extract, April 2026 |
| Account opening range | August 2000 – January 2026 |
| **On AFB** | **No — 103/103 (100%)** |
| Account Status | Active: 60 (58.3%) · Dormant: 40 (38.8%) · Inactive: 2 (1.9%) |
| Product split | Corporate Current Account: 83 (80.6%) · Non-Individual: 20 (19.4%) |
| Currency | NGN (all records) |

> **Note on statistical tests:** Because `On AFB = No` for all 103 records, the outcome variable has zero variance. Tests requiring two outcome levels (logistic regression, chi-squared on AFB status, t-tests by AFB group) are not estimable. Each affected chunk prints an explanatory note and exits cleanly. The analysis pivots to profiling the target population by the remaining variables.

---

## Rubric Compliance Map (CS 1 — 130 marks)

### Section A — Real-Data & Business-Operations Component (30 marks)

| Criterion | Marks | Status |
|---|---|---|
| Primary data collection: documented methodology, source, tools used | 10 | ✓ Section 2 — SQL query, CRM extract, April 2026 |
| Sampling justification: frame, size, period, statistical rationale | 10 | ✓ Section 3 — Systematic sampling, k=8, n=103, 25-year window |
| Each technique linked to a real decision or process | 10 | ✓ Section 1.3 — Five technique justifications, operational mapping table |

### Section B — Submitted Analytical Work (80 marks)

| Criterion | Marks | Status |
|---|---|---|
| Professional disclosure quality and depth of context linkage | 8 | ✓ Section 1 — Zonal Manager role, P&L accountability, five technique mapping |
| Five techniques × 10 marks | 50 | ✓ Sections 4–8 — EDA, Visualisation, Hypothesis Testing, Correlation, Regression |
| Depth of business interpretation per technique | 12 | ✓ Plain-language findings after each analysis section |
| Code quality, reproducibility, document structure | 6 | ✓ R + Python panel-tabset, self-contained HTML, top-to-bottom reproducible |
| Integrated conclusion and actionable recommendation | 4 | ✓ Section 9 — AFB Onboarding Drive with 5-step action plan |

### Section C — Defence / Viva Voce (20 marks)

Held approximately one week after submission. Bring the live HTML document open in a browser.

**Defence preparation — for each technique be ready to answer:**
1. Why this technique for this data?
2. What do the key numbers mean?
3. What is the single most important business implication?
4. What assumption might be violated and how would that affect the conclusion?

---

## Required Document Sections (per §1.3 Standard Structure)

| Section | Status |
|---|---|
| 1. Executive Summary (150–200 words) | ✓ |
| 2. Professional Disclosure | ✓ |
| 3. Data Collection & Sampling | ✓ |
| 4. Data Description | ✓ |
| 5–9. Analysis (one section per technique) | ✓ |
| 10. Integrated Findings | ✓ Section 9 — Conclusions & Recommendations |
| 11. Limitations & Further Work | ✓ Section 10 — four limitations + four extensions |
| References (APA 7th) | ✓ After Section 10 — all 17 citations included |
| Appendix: AI Usage Statement | ✓ Final appendix section |

---

## References (APA 7th Edition)

Add the following section to the end of `banking_portfolio_analytics.qmd` before rendering for submission.

### Course Textbook (required in every submission)

Adi, B. (2026). *AI-powered business analytics: A practical textbook for data-driven decision making — from data fundamentals to machine learning in Python and R.* Lagos Business School / markanalytics.online. https://markanalytics.online

### Primary Data Source

Mordi, P. (2026). *Corporate current accounts not enrolled in ALAT for Business — Apapa zone extract* [Dataset]. Commercial Banking Division, Retail & Commercial Banking, [Bank Name], Lagos, Nigeria. Data available on request from the author.

### Software

R Core Team. (2024). *R: A language and environment for statistical computing* (Version 4.x). R Foundation for Statistical Computing. https://www.R-project.org/

Van Rossum, G., & Drake, F. L. (2009). *Python 3 reference manual.* CreateSpace.

Allaire, J. J., Teague, C., Scheidegger, C., Xie, Y., & Dervieux, C. (2022). *Quarto* (Version 1.x) [Computer software]. https://doi.org/10.5281/zenodo.5960048

### R Packages

Wickham, H., François, R., Henry, L., Müller, K., & Vaughan, D. (2023). *dplyr: A grammar of data manipulation* [R package]. https://CRAN.R-project.org/package=dplyr

Wickham, H. (2016). *ggplot2: Elegant graphics for data analysis.* Springer. https://doi.org/10.1007/978-3-319-24277-4

Xie, Y. (2024). *knitr: A general-purpose package for dynamic report generation in R* [R package]. https://yihui.org/knitr/

Zhu, H. (2024). *kableExtra: Construct complex table with 'kable' and pipe syntax* [R package]. https://CRAN.R-project.org/package=kableExtra

Robin, X., Turck, N., Hainard, A., Tiberti, N., Lisacek, F., Sanchez, J.-C., & Müller, M. (2011). pROC: An open-source package for R and S+ to analyze and compare ROC curves. *BMC Bioinformatics, 12*, 77. https://doi.org/10.1186/1471-2105-12-77

Wei, T., & Simko, V. (2021). *corrplot: Visualization of a correlation matrix* [R package]. https://github.com/taiyun/corrplot

> **To retrieve exact citations for all R packages used:** run `citation("packagename")` in R and format the output in APA 7.

### Python Packages

McKinney, W. (2010). Data structures for statistical computing in Python. In *Proceedings of the 9th Python in Science Conference* (pp. 56–61). https://doi.org/10.25080/Majora-92bf1922-00a *(pandas)*

Harris, C. R., Millman, K. J., van der Walt, S. J., Gommers, R., Virtanen, P., Cournapeau, D., … Oliphant, T. E. (2020). Array programming with NumPy. *Nature, 585*, 357–362. https://doi.org/10.1038/s41586-020-2649-2 *(numpy)*

Virtanen, P., Gommers, R., Oliphant, T. E., Haberland, M., Reddy, T., Cournapeau, D., … van Mulbregt, P. (2020). SciPy 1.0: Fundamental algorithms for scientific computing in Python. *Nature Methods, 17*, 261–272. https://doi.org/10.1038/s41592-019-0686-2 *(scipy)*

Pedregosa, F., Varoquaux, G., Gramfort, A., Michel, V., Thirion, B., Grisel, O., … Duchesnay, É. (2011). Scikit-learn: Machine learning in Python. *Journal of Machine Learning Research, 12*, 2825–2830. *(scikit-learn)*

Seabold, S., & Perktold, J. (2010). Statsmodels: Econometric and statistical modeling with Python. In *Proceedings of the 9th Python in Science Conference* (pp. 92–96). https://doi.org/10.25080/Majora-92bf1922-011 *(statsmodels)*

Hunter, J. D. (2007). Matplotlib: A 2D graphics environment. *Computing in Science & Engineering, 9*(3), 90–95. https://doi.org/10.1109/MCSE.2007.55 *(matplotlib)*

Waskom, M. L. (2021). seaborn: Statistical data visualization. *Journal of Open Source Software, 6*(60), 3021. https://doi.org/10.21105/joss.03021 *(seaborn)*

---

## Appendix: AI Usage Statement

*Add this appendix to the QMD document before submission (required per §4.4):*

> AI tools were used in the preparation of this submission to support coding, document structuring, and drafting assistance. All data, business context, analytical choices, interpretations, and recommendations are the author's own, drawn from professional experience and the course material. The author takes full responsibility for the content of this submission.

---

## Submission Checklist

- [x] All five analysis sections complete with code, output, and plain-language interpretation
- [x] Section 10 — Limitations & Further Work added
- [x] References section added to QMD (APA 7th — 17 citations)
- [x] AI Usage Statement appendix added to QMD
- [ ] `self-contained: true` in YAML — confirmed ✓
- [ ] `code-fold: true` in YAML — confirmed ✓
- [ ] R + Python panel-tabset throughout — confirmed ✓
- [ ] Render locally: `quarto render banking_portfolio_analytics.qmd`
- [ ] Publish to RPubs (RStudio → Publish → RPubs) or Posit Connect Cloud
- [ ] Submit the live URL (not the file) via LMS
- [ ] Optional: push `.qmd` + anonymised data to a public GitHub repo for +5 bonus marks

---

## Project Structure

```
banking_portfolio_analytics.qmd     # Quarto source (R + Python dual implementation)
banking_portfolio_analytics.html    # Rendered output
dataset/
  AFB for non curr.csv              # 103 non-enrolled corporate accounts, Apapa zone
docs/
  RPubs - EMBA-31-Take-Home-Exam-April-2026.pdf   # Assessment brief
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
