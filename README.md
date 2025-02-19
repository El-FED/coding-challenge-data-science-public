# Data Science Coding Challenge

## Ski Ticket Sales Forecasting Challenge

## Overview

This project forecasts ski ticket sales for the 2022/2023 season using historical data from 2016 to 2022, including the 2020-2021 season, which was impacted by COVID-19. The model was built using Facebook Prophet, a tool designed to capture seasonality and trends in time series data.

## Data Processing

- The dataset was cleaned and formatted for Prophet.
- Only December to April data was used to reflect the ski season.
- The 2020-2021 season was retained, potentially introducing anomalies.
- A floor value of 1 was set to prevent negative predictions.

## Forecasting Model

- **Model Used**: Prophet
- **Why Prophet?**
  - Effectively captures yearly seasonality.
  - Works well with limited external data.
  - Provides confidence intervals to assess forecast reliability.
- The model was trained on all available seasons, including 2020-2021.
- Forecasts were generated for December 10, 2022, to April 15, 2023.

## Key Insights

- The model follows historical sales trends, peaking in January-February and declining in April.
- The forecast is aligned with past seasons but includes some uncertainty.
- Retaining the 2020-2021 season may have introduced anomalies affecting accuracy.

## Next Steps

1. **Improve Accuracy**
   - Incorporate weather, snowfall, and economic data.
   - Fine-tune Prophet’s changepoint detection.

2. **Compare Models**
   - Evaluate alternatives like XGBoost or SARIMAX.
   - Test additional feature engineering techniques.

3. **Refine Data Preprocessing**
   - Test a version without the 2020-2021 season to assess its impact.
   - Compare results between models trained with and without COVID-19 data.

## Conclusion

The forecast reasonably follows historical seasonality, but accuracy could improve with additional external data and refined tuning. Further validation and alternative model testing could enhance future predictions.
