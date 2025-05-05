# Toronto Neighbourhood Analysis: Income and High Blood Pressure (HBP)

## Overview
This project investigates the association between income levels and high blood pressure (HBP) prevalence across Toronto neighborhoods. Using public datasets from health, income, and demographic sources, we use statistical analysis and geospatial mapping to uncover socioeconomic patterns in chronic disease prevalence.


## Research Questions

- Is there a statistical relationship between income and high blood pressure?
- How does HBP prevalence vary across income quintiles?
- Do demographic variables (e.g., immigrant %, visible minority %) strengthen the model?
  

## Methodology

### Approach:
- Imported and cleaned multi-sheet Excel files with neighborhood-level data
- Created income quintiles using `pandas.qcut()`
- Merged datasets across common neighborhood codes
- Performed exploratory data analysis (EDA) using graphs and summaries
- Conducted two regression models:
  - Simple: HBP ~ Low Income (%)
  - Extended: HBP ~ Low Income (%) + Immigrant (%) + Visible Minority (%)
- Conducted geospatial analysis using `geopandas` and `contextily`


## Key Results

- **Simple Regression:** Low income (%) alone explains ~20% of variance in HBP
- **Extended Regression:**
  - Low Income (%): −1.10 (significant negative)
  - Immigrant (%): +0.31 (significant positive)
  - Visible Minority (%): Not significant
  - **R² = 63.9%**
- **Geospatial Mapping:** Choropleth map confirms clustering patterns in northwest Toronto
