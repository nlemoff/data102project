# Prediction of Energy Grid Impacts and Causal Analysis of Energy Demand and Temperature

## Overview

This repository contains the analysis and modeling code for the project **"Prediction of Relationships Between Energy Demand, Consumption, Air Temperature, and Extreme Weather Events"**. The project focuses on two primary goals:

1. **Predicting Energy Grid Impacts** during extreme weather events using Generalized Linear Models (GLMs) and non-parametric methods.
2. **Establishing a Causal Relationship** between increased electricity demand and average air temperature in California.

---

## Research Questions

1. **How can we predict impacts to the energy grid during extreme weather events?**
   - Models were developed to identify "impacted" days (defined as days where energy demand exceeds the 90th percentile).

2. **What is the causal effect of increased electricity demand on average air temperature?**
   - An instrumental variable approach was used to identify causal relationships, accounting for confounding factors like seasonality and economic activity.

---

## Methodology

### Data Overview

- **Climate Data:** Hourly weather observations aggregated to daily averages for Alameda County.
- **Energy Data:** Monthly energy demand and CO2 emissions from the EIA database.
- **Preprocessing:** Heat index calculation, feature engineering (e.g., binary heatwave indicators), and data aggregation.

### Modeling Techniques

1. **Prediction Models**
   - Logistic Regression (GLM)
   - K-Nearest Neighbors (KNN)
   - Decision Tree

2. **Causal Analysis**
   - Instrumental variable regression using temperature extremes as the instrument for energy demand.

### Evaluation Metrics

- Accuracy, Precision, Recall, F1 Score, and AUC for prediction models.
- Coefficients and R² for causal inference regression.

---

## Key Results

- **Prediction Models:**
  - Logistic Regression achieved the highest AUC (0.954) and accuracy (92%).
  - KNN had the highest recall (56%).
  - Decision Tree had the lowest recall (37%) and showed signs of overfitting.

- **Causal Analysis:**
  - A causal coefficient of **0.1811 metric tons of CO2 per megawatt-hour** of electricity demand was identified.
  - Temperature extremes proved to be a robust instrument for modeling energy demand.

---

## Limitations and Future Work

### Limitations

- Limited data granularity (e.g., monthly energy and emissions data).
- Geographic and temporal aggregation reduced the specificity of results.
- Assumptions of uniform energy efficiency and proportional emissions may introduce bias.

### Future Work

- Incorporate higher-resolution and geospatially specific datasets.
- Explore advanced models such as RNNs for capturing temporal dependencies.
- Investigate regional variations and expand analysis beyond a single state.

---

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Required libraries: pandas, numpy, sklearn, statsmodels, matplotlib, seaborn

### Authors

Nicholas Lemoff
Keita Tanabe
Areeya Tipyasothi
Erica Ying
