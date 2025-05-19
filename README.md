[Click here to view the HTML report](https://karthikeyan2kk.github.io/Machine-Failure-Prediction-/)

# Predicting Torque in CNC Machines using Forward Selection and Hypothesis Testing in R

## Overview

This project involves analyzing a dataset related to CNC machining processes to understand factors affecting **Torque [Nm]**. It includes **statistical hypothesis testing**, **model selection using forward stepwise regression**, and **data visualization**. The work was completed as part of a data science module using R.

## Objectives

- Identify whether torque varies significantly between machine types (M and L)
- Check for equality of variances using an F-test
- Conduct a t-test to compare mean torque values
- Use forward stepwise regression to build a predictive model for torque
- Visualize tool wear patterns using boxplots and histograms

## Statistical Methods Used

- **F-test** to compare variances of torque across machine types
- **Two-sample t-test** (with equal variances, justified by F-test result)
- **Forward Selection** using `stepAIC()` from the `MASS` package
- **Model performance metrics**: MAE and MSE using `MLmetrics`

## Key Insights

- The variance of torque between machine types M and L was statistically equal (F-test p-value = 0.9013)
- There was no significant difference in mean torque between M and L (t-test p-value = 0.9265)
- Forward selection retained only `Rotational.speed..rpm.` as the significant predictor of torque, resulting in a high R² (~0.77)

## Tools and Libraries

- **R 4.x**
- `MASS` — for stepwise model selection
- `MLmetrics` — for model evaluation (MAE, MSE)
- `ggplot2` — for data visualization
- `base R` and `stats` — for hypothesis testing

## Files in this Repository

- `Project_presentation_R.Rmd`: Source RMarkdown script for the entire analysis
- `Project_presentation_R.html`: Rendered presentation of the RMarkdown analysis under docs folder
- `README.md`: This file
