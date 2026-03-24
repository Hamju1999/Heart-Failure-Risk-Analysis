# Heart-Failure Risk Prediction: A Statistical Approach

### Overview
This project focuses on identifying key predictors of heart disease using a logistic regression framework. The analysis emphasizes statistical rigor, ensuring the model meets all classical assumptions for reliable clinical prediction.

### My Technical Contributions
* **Exploratory Data Analysis (EDA):** Performed data cleaning, handled missing values, and encoded categorical variables (Sex, ChestPainType) in R.
* **Statistical Modeling:** Developed a logistic regression model to quantify the impact of risk factors.
* **Model Diagnostics:** * Conducted **Variance Inflation Factor (VIF)** analysis to check for multicollinearity.
    * Performed **Durbin-Watson** tests for autocorrelation.
    * Evaluated **Cook’s Distance** and **Leverage plots** to identify influential outliers.
* **Remediation:** Optimized model fit by applying log transformations to the `RestingBP` variable and removing high-leverage points.

### Key Results
* **Model Improvement:** Successfully reduced the **AIC from 890.6 to ~600**, indicating a significantly more parsimonious and better-fitting model.
* **Insight:** Identified Age, Cholesterol, and Sex as the most statistically significant predictors of heart disease risk in the dataset.

### Technical Stack
* **Language:** R
* **Libraries:** tidyverse, caret, car, ggplot2
