# Student Loan Collections EDA (2015–2018)

**Tools:** R (tidyverse, ggplot2), Statistics (Pearson correlation, linear regression)  
**Data:** TidyTuesday (2019-11-26), originally published by the U.S. Department of Education  

## Problem

Student loan default collections rely on multiple recovery mechanisms, including rehabilitation, voluntary payments, and wage garnishment. This project explores how these mechanisms relate particularly whether higher rehabilitation activity is associated with higher voluntary repayments.

## Dataset

- **Unit of observation:** collection agency × year (aggregated totals), 2015–2018  
- **Key variables:** rehabilitation, voluntary_payments, wage_garnishments, year, agency_name  
- Monetary values were converted to **millions of dollars** for easier interpretation  

## Methods

- Removed missing values in key columns  
- Computed descriptive statistics (mean, median, SD, variance, IQR)  
- Visualized distributions using histograms and boxplots  
- Examined relationships using scatter plots with regression lines  
- Calculated Pearson correlation between rehabilitation and voluntary payments  
- Built a linear regression model: voluntary_payments ~ rehabilitation  

## Key Results

- All repayment variables show **right-skewed distributions**, indicating a small number of large values  
- Strong positive association between rehabilitation and voluntary payments  
  - **Pearson r ≈ 0.79, p < 0.001**  
- Rehabilitation is a significant predictor of voluntary payments  
  - **R² ≈ 0.63, p < 0.001**  
- Year-wise analysis shows increased variability in later years  

## Interpretation

Higher rehabilitation activity is associated with higher voluntary repayments. This may indicate that programs designed to help borrowers return to good standing are linked to improved repayment behavior.

## Limitations

- Aggregated data (agency-year), not individual borrower-level  
- No demographic or income variables available  
- Only four years of observations  
- Skewed distributions suggest additional robustness checks could improve the analysis  

## Future Improvements

- Perform Spearman correlation as a non-parametric alternative  
- Apply log transformation to reduce skewness  
- Include year as a predictor variable in regression models  
- Develop interactive dashboards to explore trends over time  

## Reproducibility

Run the provided R/Quarto script to reproduce all tables, figures, and statistical analyses.
