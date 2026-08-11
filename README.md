# SME Risk Intelligence & Early Warning System

## Overview

A Python-based risk analytics system designed to assess
financial, operational, fraud, compliance and insurance
risks across 1,000 synthetic SMEs.

## What the Project Does

- Calculates financial risk
- Calculates operational risk
- Calculates fraud risk
- Calculates compliance risk
- Calculates insurance risk
- Produces an overall risk score
- Classifies businesses by risk level
- Identifies major risk drivers
- Performs financial stress testing
- Generates management recommendations

## Risk Dimensions

### Financial Risk
- Debt-to-revenue
- Expense ratio
- Cash coverage

### Operational Risk
- Operational incidents
- Stock losses
- Customer concentration
- Employee turnover
- Supplier exposure

### Fraud Risk
- Fraud incidents
- Cash discrepancies
- Segregation of duties
- Internal audit frequency

### Compliance Risk
- Compliance breaches
- Expired licences
- Missing documents
- Tax compliance

### Insurance Risk
- Insurance coverage
- Business interruption coverage
- Liability coverage

## Portfolio Results

Total SMEs: 1,000

| Risk Category | SMEs | Percentage |
|---|---:|---:|
| Low | 120 | 12.0% |
| Moderate | 685 | 68.5% |
| High | 118 | 11.8% |
| Critical Review | 77 | 7.7% |

Average Overall Risk: 40.96

Median Overall Risk: 40.71

Maximum Overall Risk: 68.15

## Average Risk by Dimension

| Dimension | Average Score |
|---|---:|
| Financial | 50.96 |
| Operational | 46.97 |
| Fraud | 31.88 |
| Compliance | 21.41 |
| Insurance | 43.38 |

## Financial Risk Drivers

Correlation with financial risk:

- Debt-to-Revenue: 0.376
- Expense Ratio: 0.491
- Cash Coverage: -0.313

Higher debt and expenses are associated with higher
financial risk, while stronger cash coverage is associated
with lower financial risk.

## Stress Testing

Example: SME_0071

| Scenario | Estimated Financial Risk |
|---|---:|
| Stress | 99.22 |
| Current | 97.71 |
| Improvement | 95.35 |

## Example High-Risk Business

Business: SME_0071

Overall Risk Score: 68.15

Classification: CRITICAL REVIEW

Top risk dimensions:

- Financial: 97.42
- Insurance: 85.92
- Operational: 56.51

Key findings include high debt, excessive expenses, weak
liquidity, fraud exposure, tax compliance issues and
inadequate insurance protection.

## Technology

- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab
- GitHub

## Skills Demonstrated

- Risk Analytics
- Financial Analysis
- Data Analysis
- Statistical Analysis
- Risk Scoring
- Stress Testing
- Data Visualization
- Python Programming
- Business Intelligence

## Project Structure

SME-Risk-Intelligence/

data/
notebooks/
charts/
reports/
README.md
requirements.txt

## Limitations

The dataset is synthetic and is intended for educational
and portfolio demonstration purposes.

The risk scores are analytical indicators and should not be
treated as regulated credit ratings or investment advice.

## Future Development

- Machine learning early-warning model
- Probability of default modelling
- Interactive Power BI dashboard
- Automated PDF reports
- SHAP explainability
- Scenario simulation
- API deployment
- Automated risk alerts

## Author

Munashe Sylvester Khembo

BSc Honours Actuarial Science

Interests: Risk Analytics | Actuarial Science | Data Analytics
| Insurance | Financial Risk | Business Intelligence

## Disclaimer

This project is for educational and portfolio demonstration
purposes only.