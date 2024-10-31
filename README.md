# UK Inflation Data 1989-2022
This project analyzes UK inflation data from 1989 to 2022, examining inflation by year and by quarter. Statistical tests are conducted to understand trends, normality, and relationships between inflation and time variables, with the following packages and methods used throughout.

## 1. Setup
Required Libraries
- openxlsx: For reading Excel files.
- ggplot2: For visualizing data and adding regression lines to scatter plots.

## 2. Data
The analysis uses two Excel files:
- Inflation by Year (Inflation by Year.xlsx): Contains annual inflation data.
- Inflation by Quarter (Inflation by Quarter.xlsx): Contains quarterly inflation data.

## 3. Data Analysis
The data is initially loaded and inspected for structure and completeness using the head() function to preview the first few rows. The variables extracted for analysis include Year and Inflation for yearly data, and Year, Quarter, and Inflation for quarterly data.

## 4. Statistical Tests
- t-Tests on Inflation Data:
  **Yearly Inflation Comparison:** Inflation data is divided into two halves, and a two-sample t-test is conducted to check for differences in the mean inflation rates.
  **Result:** No significant difference between the two halves; p-value > 0.05.
- Quarterly Inflation Comparison: Similarly, quarterly data is split into halves, and a two-sample t-test is conducted.
  **Result:** No significant difference between the two halves; p-value > 0.05.
  
## 5. Normality Tests
- Histogram and Q-Q Plot: Visual methods used to check the normality of inflation data by plotting histograms and Q-Q plots.
- Shapiro-Wilk Test: Applied to both yearly and quarterly data.
- Yearly Data: p-value < 0.05; data is not normally distributed.
- Quarterly Data: p-value < 0.05; data is not normally distributed.

## 6. Modeling and Regression Analysis
Simple Linear Regression Models
- Inflation by Year: A linear model with Inflation as the dependent variable and Year as the independent variable.
  Result: The year variable explains only 9% of inflation variability (Multiple R-Squared ≈ 0.09). The year is not a significant predictor of inflation.
- Inflation by Quarters:A linear model with Inflation as the dependent variable and Year as the independent variable for quarterly data.
  Result: The year variable explains only 4% of inflation variability (Multiple R-Squared ≈ 0.04). Year is not a significant predictor.
- Inflation by Quarters (Quarter as Predictor):A linear model with Inflation as the dependent variable and Quarter as a categorical predictor.
  Result: Quarter does not significantly affect inflation (Multiple R-Squared ≈ 0.00, p-value ≈ 0.9).
  
## 7. Visualizations
Scatter plots with regression lines were created using ggplot2 to illustrate the relationships, or lack thereof, between Year and Inflation.
**Results and Observations:** 
- No Significant Trends in Inflation Over Time: t-tests and regression analyses indicate no significant trends or relationships between inflation and the Year or Quarter variables.
- Non-Normal Distribution: Both the yearly and quarterly inflation data were found to deviate from normality, likely due to fluctuations and inflationary pressures in certain years.
- Low Predictive Value of Year and Quarter Variables: Regression models revealed that Year and Quarter explain very little of the variation in inflation.
