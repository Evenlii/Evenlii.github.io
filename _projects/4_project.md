---
layout: page
title: Time series analysis of the U.S. unemployment rate
description: time series, data analysis, modeling, economics
img: assets/img/time0.jpeg
importance: 1
category: Data Analysis
---

The unemployment rate is a pivotal economic indicator reflecting a country's economic health. It is calculated as a percentage of unemployed individuals within the total labor force. Government policy often targets maintaining a low and stable unemployment rate to mitigate impacts on tax revenue and unemployment benefit expenditures. However, the unemployment rate often exhibits complex patterns, including seasonal variations and non-stationarity. This study examines the fluctuations in U.S. unemployment rates from 1948 to 2016 and forecasts future trends using Seasonal Autoregressive Integrated Moving Average (SARIMA) models, helping the U.S. government to assess future economic conditions and provide some effective information for policy-making. The analysis uses time-series data from the U.S. Bureau of Labor Statistics, covering monthly unemployment rates from January 1948 to November 2016. This period includes various economic cycles, providing a comprehensive dataset for robust modeling.

<br /><br />

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/time1.jpeg" title="example image" class="img-fluid rounded z-depth-1" style="max-width: 150%;"%}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/time2.jpeg" title="example image" class="img-fluid rounded z-depth-1" style="max-width: 150%;"%}
    </div>
</div>
<div class="caption">
    Fig.1 (left): U.S. Unemployment Monthly Rate from 1948 to 2016; Fig.2 (right): Sample ACF and PCAF of the U.S. Unemployment Rate Series
</div>

<br /><br />

At first glance, the process is not stationary since the mean of the series is not constant over time. According to Fig.1, the U.S. unemployment rates do fluctuate over time and overall there is a slight upward trend. Notably, during the deep recessions of the early 1980s and of 2007–2009, the U.S. unemployment rate rose sharply, reaching roughly 10%. Also, we observed that there are yearly cyclical rises and falls in the unemployment rate, indicating a potential existence of seasonality. We could confirm from the sample Autocorrelation Function (ACF) and Partial Autocorrelation Function (PCAF) analysis (Fig.2) that the original process is not stationary and differencing is needed. To account for both the non-stationary and the seasonal fluctuations, a twelfth-order difference will also be applied to the series.

The SARIMA models were chosen due to their capacity to handle both seasonal and non-seasonal elements. Two models, SARIMA(3,1,0)x(0,1,1)<sub>12</sub> and SARIMA(2,1,1)x(0,1,1)<sub>12</sub>, were considered based on the subsequent ACF and PACF analysis. To compare and select the best model, we conducted diagnostic tests, including analysis of residuals and Ljung-Box statistics. The SARIMA(2,1,1)x(0,1,1)<sub>12</sub> model demonstrated superior performance with independently distributed residuals and lower Bayesian Information Criterion (BIC) scores, indicating a better model fit.


<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/time3.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/time4.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig.3 (left): Model Diagnostic Results for SARIMA(3,1,0)x(0,1,1)12; Fig.4 (right): Model Diagnostic Results for SARIMA(2,1,1)x(0,1,1)12
</div>


The chosen SARIMA(2,1,1)x(0,1,1)12 model was then applied to forecast unemployment rates for the 10 months following December 2016. Predictions suggest a modest decline in unemployment, with rates expected to oscillate between 4% and 6%. This forecast aligns with the observed post-recession trend of decreasing unemployment rates.


<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/time5.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/time6.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig.5 (left): Monthly Unemployment Rate Forecast with SARIMA(2,1,1)x(0,1,1)12; Fig.6 (right): Raw Periodogram of the Unemployment Rate Series
</div>


The study highlights the efficacy of SARIMA models in forecasting economic indicators like unemployment rates. Our findings suggest a gradual improvement in the U.S. economy. However, it is crucial to note the inherent subjectivity in model selection and potential deviations due to unforeseen economic factors. Future studies could enrich this analysis by incorporating other economic indicators, creating a more holistic view of the economic landscape.

**Check the full report** <a href="assets/pdf/time.pdf" target="_blank">here</a>.

