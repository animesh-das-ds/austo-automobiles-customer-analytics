# Austo Automobiles — Customer Purchase Behaviour Analysis

![Course](https://img.shields.io/badge/Course-Python%20for%20Data%20Science-3776AB)
![Grade](https://img.shields.io/badge/Grade-A%20(4.0)-success)
![Type](https://img.shields.io/badge/Type-EDA%20%C2%B7%20Customer%20Analytics-blue)
![Tools](https://img.shields.io/badge/Tools-pandas%20%C2%B7%20NumPy%20%C2%B7%20Matplotlib%20%C2%B7%20Seaborn-orange)

A customer-analytics study of **who buys which car and why**, using exploratory data analysis (EDA) in Python. It answers six specific marketing questions for a car manufacturer.

---

## Business Problem

Austo Motor Company makes SUVs, Sedans and Hatchbacks. At a board meeting, concerns were raised that the **marketing strategy was not well targeted**. The data science team was asked to look at customer data and find out what really drives purchase behaviour — so marketing money could be spent where it actually works.

## Objective

Clean the customer dataset, explore it thoroughly (univariate and bivariate analysis), and answer **six targeted business questions** about gender, profession, income, loans and vehicle type.

## Data

| Attribute | Detail |
|---|---|
| Records | **1,581 customers** |
| Variables | **14** |
| Fields | age, gender, profession, marital status, education, dependents, personal loan, house loan, partner working status, salary, partner salary, total salary, vehicle make, price of purchased vehicle |

## Approach

1. **Data cleaning** — found and fixed typos in the Gender column (*"Femal"*, *"Femle"*), dropped rows with missing gender, and repaired missing `Partner_salary` values using business logic: if the partner was not working, set partner salary to 0; if the partner was working, set `partner salary = total salary − own salary`.
2. **Univariate analysis** — histograms and boxplots for every numeric column; bar charts and frequency tables for every categorical column.
3. **Bivariate analysis** — correlation heatmap and pairplot, deliberately dropping `Total_salary` to avoid redundancy (it is just salary + partner salary).
4. **Targeted question analysis** — cross-tabulations and boxplots to answer each of the six business questions.

## Key Findings

| Finding | Detail |
|---|---|
| **Age is the strongest driver of spend** | Age vs price correlation **+0.80** — the strongest relationship in the dataset. Older buyers consistently buy more expensive cars (~₹800 more per year of age). |
| **Salary matters, but less** | Salary vs price **+0.41**; salary vs age **+0.62** (career progression). |
| **Women spend more per car** | Median purchase price **₹49,000 for women vs ₹29,000 for men** — a gap of about ₹17,000. The entire female interquartile range sits above the male one. |
| **Women prefer SUVs more than men** | **52.6% of women prefer SUVs vs only 9.8% of men**. Men lean heavily toward Hatchbacks (47.1%). Sedans are equally popular with both (~43%). |
| **Personal loans drive nearly half of sales revenue** | Loan customers spent **₹26.6 million** in total, only ~6% less than cash buyers. |
| **A working partner does not change the price paid** | Median price is identical (₹32,000) in both groups. |

**Profile of the typical customer:** 78% male · 91.3% married · 62.2% postgraduates · 50.3% with a personal loan · most aged 25–38 with 2–3 dependents.

## Recommendations

1. **Target salaried professionals** with Sedan promotions and EMI/financing bundles.
2. **Focus SUV marketing on female customers** — comfort, safety and family features.
3. **Use premium packages and higher-trim models** to lift revenue from female buyers, who already spend more.
4. **Leverage personal-loan offers** for mid-range vehicles, since financing drives volume.
5. **Bundle add-ons** (accessories, extended warranty, service plans) for younger buyers of entry-level cars.
6. **Target the 30–45 age group** with premium options, and stock inventory by regional gender mix.

## Skills Demonstrated

Python (pandas, NumPy, Matplotlib, Seaborn) · data cleaning and imputation logic · univariate/bivariate EDA · correlation analysis · cross-tabulation · translating statistics into marketing recommendations.

## Repository Structure

```
├── notebooks/
│   └── austo_automobiles_eda.ipynb
├── reports/
│   └── Austo_Automobiles_Business_Report.pdf
├── screenshots/
│   ├── notebook_chart_01.png … notebook_chart_10.png
│   └── report_page_01.png … report_page_04.png
└── README.md
```

---

*PGP in Data Science & Business Analytics · Great Lakes Executive Learning / The University of Texas at Austin, McCombs School of Business. Content drawn from the project notebook, business report and course transcript.*
