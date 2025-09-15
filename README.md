# Metropolitan Assemblies Revenue Analysis  
## Overview
This repository contains an R-based analysis of financial and demographic data for some selected  Metropolitan Municipal and District Assemblies (MMDAs) in Ghana: Accra Metropolitan Assembly (AMA), Kumasi Metropolitan Assembly (KMA), Tema Metropolitan Assembly (TMA), and Tamale Metropolitan Assembly (TaMA) and Others.

The analysis for most covers years from 2012  to 2022. It  examines relationships between population trends, revenue sources (e.g., Internally Generated Funds - IGF, District Assemblies Common Fund - DACF), expenditure patterns (recurrent and capital), and  land-based revenues (e.g., permit fees, property rates, stool lands revenue, licenses, fees)

The goal is to identify patterns, correlations, and predictive relationships using statistical methods like linear regression, quadratic regression, diagnostic tests, and data transformations. Key questions include the impact of population on revenue performance, expenditure allocation, and infrastructure delivery. Also looking at the the budget performance, and contributions to overall revenue.

## Contents  

- **Accra_MMDAs.html** –  revenue analysis across Accra-based MMDAs  
- **Accra Metropolitan Assembly (AMA).html** – Revenue trends and budget performance for AMA  
- **Kumasi Metropolitan Assembly (KMA).html** – Revenue breakdown and growth analysis for KMA  
- **Tamale Metropolitan Assembly (TaMA).html** – Revenue analysis for TaMA  
- **Tema Metropolitan Assembly (TMA).html** – Revenue analysis for TMA  
- **Revenue Analysis.html** –  revenue performance  
- **Revenue Analysis_contribution_to_revenue.html** – Contribution of key sources to total revenue  
- **Revenue Analysis_diff_betw_act_and_bud.html** – Differences between actual and budgeted revenue  
- **Revenue Analysis_Ratio btn Act and Bud.html** – Ratios of actual to budgeted revenue  
- **Revenue Analysis_rev_growth.html** – Revenue growth trends over time  






# Using the analysis of the one of them - The four Metropolitan Municipal and District Assemblies (MMDAs) in Ghana combined:
Accra Metropolitan Assembly (AMA), Kumasi Metropolitan Assembly (KMA), Tema Metropolitan Assembly (TMA), and Tamale Metropolitan Assembly (TaMA). 

**Date of Analysis**: March 6, 2025  
**Dataset**: `Cleaned_4_MMDAs_Data` (40 rows, up to 78 columns, including Population, IGF, DACF, Capital_Expenditure, Recurrent_Expenditure, and land-based revenue components).


### Sheet 1: Population and Revenue/Expenditure Relationships
1. **Population and IGF Revenue**:
   - Descriptive stats: Population (mean ~1.38M, skewed), IGF (mean ~18.5M GHS, skewed).
   - Trends: Positive linear trends; scatter plots show clusters, moderate correlation (Pearson=0.429).
   - Regression: Linear model significant (p=0.0057, R²=0.1843); quadratic slight improvement (R²=0.2156). Assumptions violated; log-log and square-root transformations improve fit.

2. **Population and DACF Revenue**:
   - Descriptive stats: DACF (mean ~4M GHS, skewed).
   - Trends: Positive relationship; histograms skewed.
   - Regression: Linear model significant (p<0.001, R²=0.4074); quadratic and transformations (log-log, square-root) improve fit. Elasticity: 1% population increase → 0.39% DACF increase.

3. **Population, Recurrent, and Capital Expenditure**:
   - Descriptive stats: Capital (mean ~11M GHS), Recurrent (mean ~11.6M GHS, 22.5% missing).
   - Trends: Positive scatters; per capita capital expenditure (mean ~14 GHS/person).
   - Regression: Multivariate linear significant (R²=0.1603–0.2628). Assumptions violated; quadratic and transformations improve models.

4. **Revenue Growth and Infrastructure Delivery (Capital Exp. Per Capita)**:
   - No significant relationship (p=0.396, R²=0.0207).

5. **Expenditure Growth and Infrastructure Delivery**:
   - No significant linear relationship.

### Sheet 2: Allocative Decision-Making, Funding, and Patterns
1. **Allocative/Funding Decisions and Revenue Patterns**:
   - Inferred from trends; no direct variables.
2. **Allocative Decisions and Expenditure Patterns**:
   - Trends: Total revenue and expenditure increase; strong correlation (Pearson=0.988).
   - Ratios: IGF to Total Expenditure plotted over years.
3. **Population Trends, Service Delivery, Revenue/Expenditure Patterns**:
   - Per capita revenues calculated; moderate correlations (e.g., Population vs. Total Revenue=0.530).
   - Regression: Significant for Total Revenue/Expenditure vs. Population (R²=0.281–0.305); Capital Exp. vs. Total Revenue significant (R²=0.450).

### Sheet 3: Land-Based Revenues and Patterns
1. **Land-Based Revenues (Permit Fees, Property Rates, Stool Lands, Licenses, Fees) and IGF**:
   - Multiple regression: Highly significant (R²=0.9942); all predictors except stool lands significant.
   - Correlations: Strong with property rates (0.944), licenses (0.917).
   - Simple regressions: All significant except stool lands.

2. **Land-Based Revenues and DACF**:
   - Multiple regression: Significant (R²=0.6447); stool lands and licenses key.
   - Correlations: Weak overall.
   - Simple regressions: Significant for licenses and fees.

3. **Land-Based Revenues and Capital Expenditure**:
   - Multiple regression: Significant (R²=0.6844); permits, property rates, licenses key.
   - Correlations: Moderate (0.35–0.57).
   - Simple regressions: Significant for property rates, licenses, fees.

4. **Land-Based Revenues and Recurrent Expenditure**:
   - Multiple regression: Highly significant (R²=0.9839); all predictors significant.
   - Correlations: Strong (0.79–0.97).
   - Simple regressions: All significant.

5. **Land-Based Revenues and Population**:
   - Multiple regression: Significant (R²=0.8938); most predictors significant except stool lands.
   - Correlations: Strong with fees (0.899), licenses (0.780).
   - Simple regressions: Significant for licenses and fees.

## Methods and Tools
- **Libraries**: `skimr`, `ggplot2`, `dplyr`, `lmtest`, `car`, `gridExtra`, `scales`, `corrplot`.
- **Techniques**:
  - Descriptive statistics (skim, histograms, density overlays).
  - Trend plots (scatter, line, bar) with LOESS/Linear smoothing.
  - Linear and quadratic regression (`lm`).
  - Diagnostic tests: Residual plots, Shapiro-Wilk (normality), Durbin-Watson (autocorrelation), Breusch-Pagan (homoscedasticity), VIF (multicollinearity).
  - Transformations: Log-log, square-root for non-normality/heteroscedasticity.
  - Correlations: Pearson tests and matrices.
- **Data Cleaning**: Growth rates via `diff`; squared terms for quadratics; per capita metrics derived.

## Key Findings
- Population positively influences IGF and DACF, but relationships are moderate and often require transformations.
- Strong links between total revenue/expenditure and population; capital expenditure tied to revenue but not growth rates.
- Land-based revenues strongly predict IGF (99% variance explained) and recurrent expenditure; weaker for DACF and capital.
- No strong evidence for revenue/expenditure growth impacting infrastructure delivery per capita.
- Models suggest population growth drives revenue needs, but allocative efficiency (e.g., IGF reliance) varies.

## Installation
- **R Version**: 4.0+ recommended.
- **Install Packages**:
  ```R
  install.packages(c("skimr", "ggplot2", "dplyr", "lmtest", "car", "gridExtra", "scales", "corrplot"))
