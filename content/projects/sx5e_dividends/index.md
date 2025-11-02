---
title: "SX5E Dividends Forecasting"
date: 2025-08-16
draft: false
---
{{< social "github" "https://github.com/Hotstopper/sx5e_dividends" >}}

I first modelled dividends per share (DPS) for EUROSTOXX 50 companies using a simple ARIMA model that only looks at each firm’s past dividends.
{{< figure src="arima_forecast.png" alt="Forecast Percentage Error Distribution of ARIMA" caption="Forecast Percentage Error Distribution of ARIMA" >}}
The resulting distribution (above) shows that the error distribution is wide and heavy-tailed, meaning the model frequently misses by a large margin in both directions. In short, past dividends can not reliably predict prices in the future, supporting the weak efficient market hypothesis.

---

I then modelled DPS using a hybrid machine-learning model. The model starts from the market's own forecast (Dividend futures one year before) and tries to correct systematic errors using company fundamentals.

The machine-learning model (XGBoost) is trained on residuals (Actual DPS - Futures-implied DPS). Once these residuals are predicted, I run a quantile regression to get the optimal coefficients to combine futures-implied DPS and predicted residuals linearly. After that, I test the trained model on unseen data from 2023 - 2024 and the results are as follows:

{{< figure src="model_forecast.png" alt="Forecast Percentage Error Distribution of Futures & Hybrid XGBoost" caption="Forecast Percentage Error Distribution of Futures & Hybrid XGBoost" >}}

The hybrid model outperforms pure futures-implied forecasts. However, this is mostly due to the systematic underestimation of DPS based on futures. The hybrid model's coefficient for predicted residuals is near zero, while its coefficient for futures-implied DPS is greater than 1. The fact that predicted residuals were largely noise vindicates the semi-strong efficient market hypothesis, though the systematic underestimation remains to be explained.

---