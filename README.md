# 🐴 SME Risk Intelligence & Machine Learning Early-Warning System

## Overview

An end-to-end **SME Risk Intelligence and Financial Distress Early-Warning System** developed using Python, statistical risk analytics and machine learning.

The project analyses **1,000 synthetic SMEs** across five major risk dimensions:

- Financial Risk
- Operational Risk
- Fraud Risk
- Compliance Risk
- Insurance Risk

It combines a traditional risk-scoring framework with machine-learning models to identify businesses requiring additional risk review.

---

## 🎯 Project Objective

Small and medium-sized businesses face multiple interconnected risks, including:

- excessive debt
- weak liquidity
- high operating costs
- operational disruption
- fraud
- regulatory non-compliance
- inadequate insurance protection

The objective of this project is to demonstrate how **risk analytics and machine learning can be combined to identify, rank and monitor SME risk exposure.**

The system answers three key questions:

> **Which businesses are most at risk?**

> **Why are they at risk?**

> **Which businesses should management prioritise for further review?**

---

# 📊 Portfolio Overview

| Metric | Result |
|---|---:|
| SMEs analysed | **1,000** |
| Variables after feature engineering | **55** |
| ML features | **22** |
| Training observations | **800** |
| Testing observations | **200** |
| Average overall risk | **40.96** |
| Median overall risk | **40.71** |
| Maximum overall risk | **68.15** |
| High/Critical ML alerts | **162 (16.2%)** |

---

# ⚠️ Traditional Risk Classification

The traditional risk framework produced the following portfolio distribution:

| Risk Category | SMEs | Percentage |
|---|---:|---:|
| LOW | 120 | 12.0% |
| MODERATE | 685 | 68.5% |
| HIGH | 118 | 11.8% |
| CRITICAL REVIEW | 77 | 7.7% |

The analysis shows that although most businesses fall within the moderate category, a meaningful proportion require enhanced monitoring or review.

---

# 📈 Average Risk by Dimension

| Risk Dimension | Average Score |
|---|---:|
| Financial | **50.96** |
| Operational | **46.97** |
| Insurance | **43.38** |
| Fraud | **31.88** |
| Compliance | **21.41** |

Financial risk represents the highest average risk dimension in the portfolio.

---

# 💰 Financial Risk Analysis

Three major financial indicators were analysed:

### Debt-to-Revenue

- Mean: **2.77x**
- Median: **1.15x**
- Maximum: **37.25x**

### Expense Ratio

- Mean: **1.37x**
- Median: **0.73x**
- Maximum: **41.46x**

### Cash Coverage

- Mean: **0.99 months**
- Median: **0.45 months**
- Maximum: **58.71 months**

Financial risk-driver analysis showed:

| Driver | Correlation with Financial Risk |
|---|---:|
| Expense Ratio | **0.491** |
| Debt/Revenue | **0.376** |
| Cash Coverage | **-0.313** |

This indicates that higher expense burdens and leverage are associated with higher financial risk, while stronger cash coverage is associated with lower risk.

---

# 🤖 Machine Learning

A financial distress target was created and two classification models were developed:

1. Logistic Regression
2. Random Forest

The dataset was split into:

- **80% training**
- **20% testing**

The distress target contained:

- 819 non-distressed observations
- 181 distressed observations

---

# 🧠 Model Performance

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 0.895 | **0.930** |
| Precision | 0.653 | **0.844** |
| Recall | **0.889** | 0.750 |
| F1 Score | 0.753 | **0.794** |
| ROC-AUC | 0.961 | **0.963** |

### Interpretation

Random Forest produced the stronger overall performance based on accuracy, precision, F1 and ROC-AUC.

Logistic Regression achieved higher recall.

This is important from a risk-management perspective because:

> A model with higher recall may be preferable when failing to identify a genuinely distressed business is more costly than generating additional false alerts.

---

# 🚨 Early-Warning System

The Random Forest distress probabilities were converted into five operational warning levels.

| Warning Level | SMEs | Percentage |
|---|---:|---:|
| LOW | 553 | 55.3% |
| WATCH | 234 | 23.4% |
| ELEVATED | 51 | 5.1% |
| HIGH | 119 | 11.9% |
| CRITICAL | 43 | 4.3% |

### Priority Portfolio

**162 SMEs (16.2%)** were classified as HIGH or CRITICAL and therefore represent the highest-priority group for further assessment.

---

# 🔥 Top Predicted Distress Businesses

| Business | RF Distress Probability | Warning |
|---|---:|---|
| SME_0089 | 91.35% | CRITICAL |
| SME_0905 | 90.87% | CRITICAL |
| SME_0881 | 90.33% | CRITICAL |
| SME_0683 | 90.25% | CRITICAL |
| SME_0498 | 89.87% | CRITICAL |
| SME_0179 | 89.74% | CRITICAL |
| SME_0875 | 89.56% | CRITICAL |
| SME_0347 | 87.53% | CRITICAL |
| SME_0117 | 87.49% | CRITICAL |
| SME_0071 | 87.03% | CRITICAL |

---

# 🔎 Model Feature Importance

The strongest Random Forest predictors were:

| Rank | Feature | Importance |
|---:|---|---:|
| 1 | expenses_monthly | 0.2974 |
| 2 | revenue_monthly | 0.2742 |
| 3 | total_debt | 0.0868 |
| 4 | cash_balance | 0.0671 |
| 5 | accounts_payable | 0.0334 |
| 6 | insurance_coverage_ratio | 0.0330 |
| 7 | accounts_receivable | 0.0309 |
| 8 | stock_loss_rate | 0.0299 |
| 9 | customer_concentration | 0.0280 |
| 10 | employee_turnover | 0.0267 |

The results indicate that the model relies heavily on indicators of business cash generation, expenditure pressure, leverage and liquidity.

---

# 🏢 SME_0071 Case Study

One of the highest-risk businesses identified by the traditional framework was **SME_0071**.

### Traditional Risk

**Overall Risk Score:** 68.15

**Classification:** CRITICAL REVIEW

| Dimension | Score |
|---|---:|
| Financial | **97.42** |
| Insurance | **85.92** |
| Operational | **56.51** |
| Fraud | **49.50** |
| Compliance | **42.00** |

### Financial Position

| Indicator | Value |
|---|---:|
| Revenue | $5,407.86 |
| Expenses | $43,951.79 |
| Cash Balance | $2,836.08 |
| Total Debt | $117,836.24 |
| Debt/Revenue | **21.79x** |
| Expense Ratio | **8.13x** |
| Cash Coverage | **0.06 months** |

### Machine-Learning Assessment

| Model | Distress Probability |
|---|---:|
| Logistic Regression | **99.31%** |
| Random Forest | **87.03%** |

**Early Warning:** CRITICAL

---

# 🛡️ Key Risk Findings

SME_0071 demonstrated several important vulnerabilities:

- High debt relative to revenue
- Expenses substantially exceeding revenue
- Extremely weak liquidity
- High customer concentration
- High employee turnover
- Fraud incidents
- Tax compliance issues
- Low insurance coverage
- No business-interruption cover
- No liability cover

---

# 💡 Recommended Risk Actions

The framework generates management recommendations rather than simply assigning a score.

Key actions include:

1. Review debt structure and consider restructuring.
2. Reduce unnecessary operating expenses.
3. Establish a minimum cash-buffer target.
4. Improve cash-flow forecasting.
5. Diversify the customer base.
6. Investigate employee turnover.
7. Investigate fraud incidents.
8. Strengthen internal controls.
9. Introduce regular cash reconciliations.
10. Implement segregation of duties.
11. Establish a tax-compliance calendar.
12. Maintain a central compliance document register.
13. Review insurance sums insured.
14. Assess business-interruption insurance.
15. Assess appropriate liability protection.

---

# 📊 Project Visualisations

The repository contains analytical charts covering:

- Portfolio risk distribution
- Average risk by dimension
- Top 10 highest-risk SMEs
- Overall risk distribution
- Financial risk drivers
- Financial risk sensitivity
- Machine-learning feature importance
- Model comparison
- ROC curves
- Logistic Regression confusion matrix
- Random Forest confusion matrix
- ML risk dashboard

---

# 🗂️ Repository Structure

```text
SME-Risk-Intelligence/
│
├── README.md
├── requirements.txt
│
├── data/
│   └── synthetic_sme_data.csv
│
├── charts/
│   ├── portfolio_risk_distribution.png
│   ├── average_risk_by_dimension.png
│   ├── top10_highest_risk.png
│   ├── overall_risk_distribution.png
│   ├── financial_risk_drivers.png
│   ├── financial_risk_sensitivity.png
│   ├── ml_feature_importance.png
│   ├── ml_model_comparison.png
│   ├── ml_roc_curve.png
│   ├── confusion_matrix_logistic.png
│   ├── confusion_matrix_random_forest.png
│   └── ml_risk_dashboard.png
│
├── notebooks/
│
└── reports/
    └── SME_Risk_Intelligence_FULL_Report.pdf
