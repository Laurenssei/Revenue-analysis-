# Metropolitan Assemblies Revenue Analysis  

Full Report: View Combined Analysis (All_the_four_Metropolitan_Assemblies_(AMA,_KMA,_TMA,_TaMA),_NO_STMA_data.html)


## Overview

This project conducts a comprehensive analysis of revenue trends, expenditure patterns, and demographic influences on fiscal performance across  some selected  Metropolitan Municipal and District Assemblies (MMDAs) in Ghana. Using data from 2012–2022, the study explores relationships between population growth, internally generated funds (IGF), District Assemblies Common Fund (DACF), land-based revenues, and expenditure allocations. By applying regression models and diagnostic tests, it uncovers insights into budget performance, revenue contributions, and allocative efficiency. These findings support evidence-based policymaking for sustainable urban development, highlights the  opportunities to enhance revenue mobilization and infrastructure delivery in growing metropolitan areas and the districts.



## Objectives

- Assess the impact of population trends on IGF, DACF, and overall revenue generation.
- Evaluate relationships between land-based revenues and key expenditure categories (recurrent and capital).
- Analyze budget performance, including ratios and differences between actual and budgeted revenues.
- Identify patterns in revenue growth and their implications for allocative decision-making and service delivery.



## Dataset Summary

- **Source**: Is from the  Ghana's Metropolitan, Municipal, and District Assemblies (MMDAs), afrobarometer Ghana,  cleaned for analysis (2025) .
- **Sample Size**: 40 observations across years 2012–2022 but varies in some.
- **Key Variables**: Population estimates; revenue sources (IGF, DACF, property rates, permit fees, stool lands, licenses, fees); expenditures (recurrent, capital); budget metrics (actual vs. budgeted, growth rates, per capita values).
- **Note**: Raw data is not included due to confidentiality. Please contact the author for collaboration requests.

## Methods

- Descriptive statistics (means, correlations, histograms) and visualizations (scatter plots, trend lines, correlation matrices) for exploratory analysis.
- Linear and quadratic regression models, with transformations (log-log, square-root) to address violations of assumptions (normality, heteroscedasticity, multicollinearity).
- Diagnostic tests including Shapiro-Wilk for normality, Breusch-Pagan for heteroscedasticity, Durbin-Watson for autocorrelation, and VIF for multicollinearity.
- Per capita calculations and growth rate derivations for normalized insights; multiple regression for predictor effects.

## Key Findings
- Population growth positively correlates with IGF (R²=0.18) and DACF (R²=0.41), with elasticities indicating that a 1% population increase drives 0.39% higher DACF, though models require transformations for better fit.
- Land-based revenues strongly predict IGF (R²=0.99) and recurrent expenditure (R²=0.98), with property rates and licenses as dominant contributors, but weaker links to capital expenditure (R²=0.68).
- Total revenue and expenditure show near-perfect alignment (Pearson=0.99), yet revenue growth does not significantly impact per capita infrastructure delivery (p=0.40).
- Budget performance varies, with actual revenues often falling short of budgets, underscoring the need for improved forecasting in population-driven urban contexts.


## How to Reproduce the Analysis
### Requirements
- RStudio
- R packages: skimr, ggplot2, dplyr, lmtest, car, gridExtra, scales, corrplot

### Steps
1. Clone this repository.
2. Open the main R Markdown file  in RStudio.
3. Install required packages if not already installed (e.g., `install.packages(c("skimr", "ggplot2", "dplyr"))`).
4. Knit the R Markdown file to generate the HTML report.
Data not included due to confidentiality. Please contact me for collaboration requests.

## Repository Structure
├── All_the_four_Metropolitan_Assemblies_(AMA,_KMA,_TMA,_TaMA),_NO_STMA_data.html  # Combined analysis report  
├── Accra_Metropolitan_Assembly_(AMA).html  # AMA-specific report  
├── Kumasi_Metropolitan_Assembly_(KMA).html  # KMA-specific report  
├── Tamale_Metropolitan_Assembly_(TaMA).html  # TaMA-specific report  
├── Tema_Metropolitan_Assembly_(TMA).html  # TMA-specific report  
├── Revenue_Analysis_S1_.html  # Sheet 1:  
├── Revenue_Analysis_contribution_to__revenue.html  # Revenue contributions  
├── Revenue_Analysis_diff_betw_act_and_bud.html  # Actual vs. budgeted differences  
├── Revenue_Analysis_Ratio_btn_Act_and_Bud.html  # Actual-to-budgeted ratios  
├── Revenue_Analysis_rev_growth.html  # Revenue growth trends  
├── Accra_MMDAs.html  # Accra-based MMDAs overview  


## License / Citation
This project is for academic and research purposes. Please cite appropriately if referenced, e.g., Sei, Lawrence. (2025). Revenue Analysis of Major Metropolitan Assemblies in Ghana.


