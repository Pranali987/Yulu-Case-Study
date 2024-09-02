# Yulu Hypothesis Testing - Business Case Study

## Project Overview

This project analyzes various factors influencing the demand for Yulu's shared electric cycles in the Indian market. Through hypothesis testing, the project identifies significant variables that affect the demand for electric cycles and evaluates how well these variables predict the overall demand.

## Problem Statement

Yulu, a company providing rental electric bikes, aims to understand the factors that influence the demand for their shared electric cycles in the Indian market. The primary objectives of this analysis are:
1. To identify the variables that significantly predict the demand for shared electric cycles.
2. To assess how well these variables describe the demand patterns for electric cycles.

## Tools

- **Jupyter Notebook** (for Python)
- **Python Libraries**

## Steps Involved

### 1. Data Collection
- **Dataset:** The dataset contains 10,886 entries with 12 columns, including features such as `datetime`, `season`, `holiday`, `workingday`, `weather`, `temp`, `atemp`, `humidity`, `windspeed`, `casual`, `registered`, and `count`.

### 2. Data Preprocessing
- **Handling Missing Values:** Confirmed that there are no missing values in the dataset.
- **Data Type Conversion:** Converted relevant columns like `datetime` to datetime format and categorical columns such as `season`, `holiday`, `workingday`, and `weather` to categorical data types for better analysis.
- **Data Description:** Provided a statistical summary of the dataset, analyzing the central tendencies and variability of numerical features.

### 3. Exploratory Data Analysis (EDA)
- **Univariate Analysis:** Analyzed the distribution of individual variables, identifying key patterns and outliers using visualizations like box plots and histograms.
- **Bivariate Analysis:** Examined the relationships between the target variable (`count`) and other features using scatter plots and box plots. Identified correlations between different variables.

### 4. Hypothesis Testing
1. **2-Sample T-Test:** Tested if `workingday` has a significant effect on the number of cycles rented. The null hypothesis (H₀) was that working days have no effect on bike rentals.
   
2. **ANOVA Test:** Conducted ANOVA to check if the number of cycles rented differs across various `weather` conditions and `seasons`. Due to the failure of ANOVA assumptions (normality and equal variance), the Kruskal-Wallis test was applied instead.
   
3. **Chi-Square Test:** Tested the dependency between `season` and `weather`. The null hypothesis (H₀) was that `weather` is independent of `season`.

### 5. Visualization
- **Correlation Heatmaps:** Generated heatmaps to visualize correlations between numerical features.
- **QQ Plots:** Used QQ plots to check for normality of data distributions.
- **Box Plots and Scatter Plots:** Created box plots to detect outliers and scatter plots to explore relationships between numerical variables.

### 6. Insights
- **Seasonal Demand:** More bikes are rented during summer and fall seasons compared to other seasons.
- **Holiday Effect:** Fewer bikes are rented on holidays compared to regular working days.
- **Weather Impact:** Adverse weather conditions (rain, thunderstorm, snow, fog) significantly reduce the number of bikes rented.
- **Working Day Impact:** No significant effect of working days on the number of bikes rented was found.
- **Outliers:** Detected significant outliers in variables like `humidity`, `windspeed`, `casual`, `registered`, and `count`.

### 7. Recommendations
1. **Stock Management:** Increase bike availability during summer and fall seasons to meet higher demand.
2. **Working Day Strategies:** Implement marketing strategies to attract more customers on working days, potentially by promoting Yulu bikes as an alternative mode of commute.
3. **Weather Considerations:** Monitor weather conditions closely to adjust bike availability and pricing, possibly introducing weather-based promotions.
4. **Seasonal Offers:** Focus on seasonal promotions, such as student discounts during summer, to retain and attract new customers.
5. **Meteorological Integration:** Utilize meteorological data to optimize bike distribution and availability based on weather forecasts.

## Conclusion

This analysis provides Yulu with data-driven insights and recommendations to optimize their bike-sharing service, improve customer engagement, and enhance operational efficiency by considering factors like season, weather, and working days.
