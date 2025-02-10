# STAT-S 670: Exploratory Data Analysis

## Mini-Project: Life Expectancy and COVID

### Authors:
Rishikesh Kakde | Swarn Gaba | Gayatri Gattani | Gandhar Ravindra Pansare

## Executive Summary

This project explores the relationship between life expectancy and GDP per capita from 2019 to 2021 across 166 countries on five continents. Our objective is to analyze how life expectancy has changed over this period and its correlation with GDP.

Key findings:
- A positive correlation exists between GDP per capita and life expectancy in 2021.
- Life expectancy declined across all continents from 2019 to 2021, likely due to COVID-19.
- The relationship between GDP and life expectancy changes is not straightforward, showing no clear trend.
- Regional variations exist, suggesting other factors beyond GDP influence life expectancy shifts.
- Future work involves modeling these factors using variables such as continent, 2019 life expectancy, and GDP per capita.

## Data and Methodology

A researcher at a think tank seeks insights into how life expectancy evolved from pre-COVID (2019) to post-COVID (2021). Using World Bank data on life expectancy and GDP per capita, we conducted an Exploratory Data Analysis (EDA) that includes:
- Graphical visualizations
- Summary statistics
- Trend analysis

These techniques help uncover patterns and variations in life expectancy changes across different regions.

## Model Interpretation

We analyzed the change in life expectancy from 2019 to 2021 against GDP per capita in 2019 using a **loess regression model**. The model revealed a non-linear relationship:
- GDP per capita logarithm transformation provides better predictive power.
- The model explains only ~20.88% of life expectancy variation, leaving 79% unexplained.
- Regional differences exist, with better model fit in **Africa, Asia, and Oceania**, and poorer fit in **Americas and Europe**.

### Model Performance
- **Life Expectancy Change 2019-2021 vs. Life Expectancy 2019**: Weak predictor with low variance explained. Countries with higher initial life expectancy had poorer model fits.
- **Life Expectancy Change 2019-2021 vs. GDP Per Capita 2019**: Moderate explanatory power, improved by factoring in continent interactions.

### Outliers
The model does not fit well for:
- **Oman (-4.13 residual)**
- **Botswana (-3.21 residual)**

## Conclusions

### **GDP and Life Expectancy in 2021**
- Applying a logarithm to GDP Per Capita linearizes its relationship with Life Expectancy.
- A positive correlation exists, with wealthier countries showing higher life expectancy.

### **Life Expectancy Changes from 2019 to 2021**
- A global decline in life expectancy occurred, with Oman showing the largest drop.
- Oceania was an exception, showing an increase in life expectancy.

### **Relationship Between GDP and Life Expectancy Changes**
- No clear linear correlation exists.
- A **loess curve** captures the complex non-linear relationship globally and by continent.

### **Modeling Insights**
- Life Expectancy Change 2019-21 is best modeled non-linearly.
- A **two-degree loess model (span = 0.75)** effectively analyzes the relationship between GDP Per Capita and Life Expectancy Change.
- Model accuracy varies by continent, indicating that economic factors alone are insufficient to explain life expectancy trends.

### **Final Thoughts**
- **COVID-19 significantly impacted global life expectancy.**
- **GDP alone is not a strong predictor of life expectancy changes.**
- **More factors (e.g., healthcare quality, government response, social conditions) need to be considered in future analyses.**

## Technologies Used
- **R** for data analysis and visualization
- **tidyverse, arm, broom** for data manipulation and modeling
- **ggplot2** for visualizations
- **Markdown** for documentation
