# Plane Crash Fatalities Analysis

## Overview
This project analyses **plane crash fatalities** over the past century (1918-2022) using data from [Kaggle](https://www.kaggle.com/code/abeperez/exploring-trends-on-passenger-airline-crashes). The aim is to explore factors affecting plane crash outcomes, focusing on fatalities, flight type, crash causes, and regional effects.

## Research Questions
The analysis seeks to answer the following:

1. **Flight Type & Fatalities:** Is there a significant difference in the number of fatalities between the most frequent two flight types?
2. **Flight Type & Proportion of Fatal Flights:** Do different flight types vary in their likelihood of resulting in fatalities?
3. **Crash Cause & Fatalities:** Does the cause of the crash significantly affect the likelihood of fatalities?
4. **Region & Fatalities:** How does the region affect the number of fatalities in plane crashes?

## Data Preparation
- **Dataset:** Cleaned by removing missing values and selecting relevant columns.
- **Derived Variables:** Created a binary indicator (`has_fatalities`) to track whether a crash led to fatalities.
- **Sampling:** A random subset of 1000 records was taken for computational efficiency.

## Key Findings

### 1. Flight Type & Fatalities
- A **t-test** revealed that **Commercial flights** tend to have significantly higher fatalities than **Operational flights**.
- **P-value:** 9.4e-08 → Strong statistical significance.
- **Confidence Interval:** Does not include 0, reinforcing a meaningful difference.
- **Visuals:** A **boxplot** showed greater variability in Commercial flight fatalities, with notable outliers.

### 2. Flight Type & Proportion of Fatal Flights
- A **proportion test** found no statistically significant difference in the likelihood of a crash resulting in fatalities between **Commercial** and **Operational flights**.
- **P-value:** 1 → We fail to reject the null hypothesis.
- **Conclusion:** The number of fatalities may differ, but the probability of a flight resulting in fatalities is similar between the two flight types.

### 3. Crash Cause & Fatalities
- **ANOVA test** showed that **crash cause significantly affects the occurrence of fatalities**.
- **P-value:** Very low, indicating strong statistical significance.
- **F-value:** 9.712 → Crash cause plays a substantial role in determining fatalities.
- **Visuals:**
  - **Bar plot**: Highlights the most fatal crash causes (e.g., terrorism has the highest fatality rate).
  - **Mosaic plot**: Shows how different crash causes correlate with fatality likelihood.

### 4. Region & Fatalities
- **Linear regression** was used to examine the effect of **region** on the number of fatalities.
- **Findings:**
  - **Low R-squared**: Indicates **region is not a strong predictor** of fatalities.
  - **F-statistic:** 1.456 → Weak explanatory power.
  - **Bar plot:** Displays regions with the highest total fatalities.
- **Conclusion:** Other factors likely play a more significant role than geographic location in determining crash fatalities.

## Technologies Used
- **Language:** R
- **Libraries:** dplyr, ggplot2, base R functions
- **Statistical Methods:** t-tests, proportion tests, ANOVA, linear regression
- **Data Visualisation:** Boxplots, bar plots, mosaic plots
