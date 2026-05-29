# Heart Failure Risk Analysis

## Overview

Logistic regression analysis on the Heart Failure Prediction dataset to identify
statistically significant predictors of cardiovascular disease risk. The project
emphasizes mathematical rigor - model assumptions are validated before conclusions
are drawn, and every remediation step is justified by diagnostic evidence.

## Dataset

- 918 observations, 11 attributes
- 5-source UCI aggregate: Cleveland Clinic Foundation, Hungarian Institute of
  Cardiology, Switzerland University Hospital, Long Beach VA Medical Center,
  and the Statlog project
- Source: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction/data

## My Contribution

This was a two-member project (50/50 split). My scope covered:

- Initial project setup and R Markdown structure
- Data preprocessing: categorical encoding (Sex, ChestPainType as dummy
  variables), Cholesterol zero-value handling via MICE (Multiple Imputation
  by Chained Equations with predictive mean matching) after confirming mean
  and median substitution created artificial concentration
- Logistic regression model fitting
- Full diagnostic suite: Durbin-Watson autocorrelation test, VIF
  multicollinearity check, Residuals vs. Fitted heteroscedasticity analysis,
  Cook's Distance and Leverage influential point identification
- Remediation: log transformation of RestingBP, removal of influential points
- Summary and conclusions

The teammate contributed EDA visualizations, correlation heatmap, and
future recommendations sections.

## Key Results

**Autocorrelation:** Durbin-Watson statistic = 2.057, p = 0.802 - no
significant autocorrelation in residuals.

**Multicollinearity:** All VIF values close to 1.0 (Age: 1.042, RestingBP:
1.038, Cholesterol: 1.024, Sex: 1.028, ChestPainType: 1.006) - no
multicollinearity concerns.

**Model improvement:** AIC reduced from 889.15 (original) to 600.14
(log-transformed + influential points removed), confirming substantially
improved fit and parsimony.

**Primary risk drivers:** Age (z = 6.179, p < 0.001), Sex/Male (z = 7.441,
p < 0.001), and Cholesterol (z = 3.043, p = 0.002) confirmed as the
most statistically significant predictors of cardiovascular disease risk.

## Technical Stack

- **Language:** R
- **Libraries:** tidyverse, caret, car, ggplot2, mice, lmtest, corrplot,
  gridExtra, dplyr

## Repository Structure
```
├── data/
│   └── heart.csv              # 918-observation UCI aggregate dataset
├── Project Code.Rmd           # Full analysis - preprocessing through conclusions
├── Project Markdown.html      # Rendered HTML output
├── Heart Analyze Report.pdf   # Final report
└── README.md
```

## Author

**Mohammad Hamza Piracha** |
Data Scientist & Applied AI Engineer |
[LinkedIn](https://www.linkedin.com/in/hamza-piracha) | hamzapiracha@live.com
