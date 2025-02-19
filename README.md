# Data Science Coding Challenge
# Ski Ticket Sales Forecasting Challenge

## Overview

This project aims to forecast ski ticket sales for the 2022/2023 season using historical data from previous ski seasons. The data spans from 2016 to 2022, including the 2020-2021 season, which was impacted by COVID-19. The forecasting model was built using Facebook Prophet, a powerful tool for time series forecasting that effectively captures seasonality and trends.

## Data Processing

- The original dataset was cleaned and formatted for Prophet.
- The ski season runs from December to April, with no ticket sales recorded in off-season months.
- The dataset includes the 2020-2021 season, meaning the model incorporates potential irregularities caused by the COVID-19 impact.
- A floor value of **1** was set to prevent negative sales predictions.

## Forecasting Model

- **Model Used**: Prophet
- **Reasoning**:
  - Prophet handles seasonality well, which is crucial given the yearly ski seasonality pattern.
  - It does not require additional exogenous variables, making it ideal for this dataset.
  - It provides uncertainty intervals, which help assess the reliability of the forecast.
- The model was trained with data from all available seasons, including the 2020-2021 period.
- Forecasts were generated for December 10, 2022, to April 15, 2023.

## Key Insights

- The model successfully captures yearly seasonality, showing an increase in sales during peak months (January-February) and a decline towards April.
- The forecasts align with past season trends but show some variation due to inherent uncertainty.
- Including the COVID-19 season in the training data may have influenced the forecast, introducing potential anomalies.

## Model Validation

- Future improvements could include more rigorous backtesting, such as cross-validation over multiple past seasons.

## Visualization

- A historical vs. forecasted sales plot was generated to compare trends.
- A confidence interval plot was created to showcase prediction uncertainty.
- Additional visualizations were included to better interpret seasonal patterns.

## Next Steps

1. **Enhancing Model Accuracy**

   - Incorporate external factors such as snowfall, weather conditions, and economic indicators.
   - Experiment with different changepoint detection settings to better capture shifts in trends.

2. **Model Comparison**

   - Evaluate alternative models like XGBoost or SARIMAX to compare performance.
   - Conduct feature engineering to explore additional relevant variables.

3. **Refine Data Preprocessing**

   - Investigate whether excluding the COVID-19 season improves accuracy.
   - Train a separate model without the 2020-2021 data and compare the results.

## Conclusion

The forecast results provide a reasonable estimate of expected ski ticket sales, aligning well with historical patterns. The model could be improved by integrating additional external data sources and refining hyperparameters. Further validation steps and model comparisons could help enhance forecast accuracy for future ski seasons.

