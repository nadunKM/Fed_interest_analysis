# Predicting Federal Interest Rates Based on Economic Factors

![](https://github.com/nadunKM/Fed_interest_analysis/blob/main/Images/Fed_interest_rates.png)

## Introduction 
This project aims to develop a model that can predict federal interest rates in the USA based on macroeconomic factors. The federal interest rate is a critical tool that drives U.S. monetary policy and affects every person's life. Interest rates play a crucial role in deciding everything from the rate of return on savings accounts to the rates of borrowing, for example, credit card debt. The federal rates depend on many factors, such as unemployment, GDP growth, and US dollar rates. However, US debt has been rising for years and has been affecting macroeconomic factors for an extended period. Therefore, I incorporated US public debt into the analysis to see if it has an effect.

![](https://github.com/nadunKM/Fed_interest_analysis/blob/main/Images/US%20Debt.png)

### Dataset
The data for this study, crucial for understanding the impact of US debt on the federal interest rates, are sourced from a reliable and widely used database: [Federal Reserve Economic Data (FRED)](https://fred.stlouisfed.org/). This database has been providing comprehensive data since the 1920s.

## Data Cleaning

[Data Cleaning Report](https://github.com/nadunKM/Fed_interest_analysis/blob/main/Data%20Wrangling.ipynb)

First, data was checked for missing, duplicated, and data types. There were no missing data, but some numeric data was recorded with string characters and converted to numeric data. Furthermore, the frequency of data was different, as data was recorded weekly, monthly, or quarterly. To be consistent, all data was converted to monthly data (the first day of each month). If the first day of the month is a holiday, the nearest data value was taken. The value of the nearest month was used for missing months in quarterly data.  The data starts on 01 - 01 - 1990 and ends on 03 - 01 - 2024.

## EDA

[EDA Cleaning Report](https://github.com/nadunKM/Fed_interest_analysis/blob/main/EDA.ipynb)

There are a few notable correlations. GDP, personal consumption expenditure, and S&P500 are highly correlated with each other and also with other variables such as bond yield, m2 money supply, our debt-to-GDP ratio, and CPI. Since GDP is already considered with the debt-to-GDP ratio, we can drop it. Personal consumption expenditure is also highly correlated with CPI and some other features. Therefore, considering all these factors, I decided to drop GDP and personal consumption expenditure and adjusted S&P500.

![](https://github.com/nadunKM/Fed_interest_analysis/blob/main/Images/heatmap.png)

