---
layout: page
title: Blood Pressure Prediction
description: How is smoking associated with blood pressure, and what do we need to predict blood pressure?
img: assets/img/heart.jpeg
importance: 3
category: Data Analysis
---

## Background and goal

Hypertension is one of the most common health conditions faced by Americans. Nearly half of American adults have hypertension, and about 20% of them are unaware of their condition. Hypertension can lead to many health problems, such as heart attacks and strokes. Previous studies have shown that smoking can cause an increase in blood pressure while there is evidence that the average blood pressure of nonsmokers is higher than that of smokers. In addition to smoking, studies have found that obesity, sleep deprivation, or increasing age are all associated with an increased risk of hypertension, and that blood pressure varies by gender.

However, large-scale population-based studies involving multiple predictors are limited, and few studies have been conducted on the US population. 
Therefore, this study aims to examine the relationship between smoking and blood pressure and to find out which variables are the best options for predicting blood pressure among a representative sample in America. The findings will inform hypertension prevention strategies.

## Methodology 

The study utilizes survey data from the National Center for Health Statistics (NCHS), targeting the civilian non-institutionalized U.S. population aged 17 and above.

Initially, two multiple linear regression models were built on a training dataset. Model 1 included all variables except ID, with blood pressure as the dependent variable. Model 2 focused on predetermined predictors (age, BMI, sleeping hours, gender, and smoking) based on prior studies.

<br />

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        <figure class="text-center">
            {% include figure.html path="assets/img/s1.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
            <figcaption class="caption">
                The two initialized models
            </figcaption>
        </figure>
    </div>
</div>

<br />

### VIF Testing, Stepwise selection, and Lasso shrinkage

The Variance Inflation Factor (VIF) was calculated to detect multicollinearity. High VIFs were observed in BMI, weight, and height in Model 1, leading to the exclusion of weight and height. Both stepwise and Lasso selections were then employed, with Model 1 undergoing variable selection due to its numerous predictors.

<br />

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        <figure class="text-center">
            {% include figure.html path="assets/img/s2.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
            <figcaption class="caption">
                VIF Testing
            </figcaption>
        </figure>
    </div>
</div>

<br />

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        <figure class="text-center">
            {% include figure.html path="assets/img/s3.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
            <figcaption class="caption">
                Stepwise selection and Lasso shrinkage
            </figcaption>
        </figure>
    </div>
</div>

<br />

### Model diagnostic check

We then perform a model diagnostic check to see if our model meets the MLR assumptions: linearity, normality, constant variance, and independence. Box-Cox transformation was considered but discarded due to complexity and interpretability issues. Influential points were assessed using Cook's distance, revealing outliers and leverage points. These data points were retained for realism.

### Model selection

Following a rigorous cross-validation process, Model 2 was excluded due to its inferior predictive performance. Notably, the incorporation of smoking as a predictor in Model 1 significantly increased prediction error and adversely affected cross-validation performance. Therefore, smoking was eliminated as a predictor in the final model selection.

<br />

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        <figure class="text-center">
            {% include figure.html path="assets/img/s4.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
            <figcaption class="caption">
                Model validation of Model 2
            </figcaption>
        </figure>
    </div>
</div>

<br />

We were then left with two models to consider: Model 1, which exhibited more stable prediction performance, and Model 3, characterized by a lower prediction error. To facilitate an informed decision between these two models, we employed three key statistical criteria: the Akaike Information Criterion (AIC), the Bayesian Information Criterion (BIC), and the adjusted R-squared value. The ideal model would demonstrate lower AIC and BIC values, indicative of better fit and parsimony, alongside a higher adjusted R-squared value, suggesting improved explanatory power.

Upon comparative analysis, Model 1 emerged as the superior option. It outperformed Model 3 in terms of AIC and BIC values, and its comprehensive nature made it more realistic and applicable. While Model 3, with age as its sole predictor, showed a lower prediction error, relying solely on age for predicting blood pressure was deemed overly simplistic and not reflective of the multifaceted nature of blood pressure variability.

To enhance the robustness of Model 1, we proceeded with model shrinkage techniques, specifically ridge regression and lasso regression. This approach aimed to reduce overfitting and improve the model’s generalizability. Consequently, we developed three variations of the final model for further evaluation:

* The Ridge Regression Model: Applying ridge regression to minimize overfitting while maintaining all predictors.
* The Lasso Regression Model: Utilizing lasso regression for both variable selection and regularization, providing a more parsimonious model.
* The Original Model (Pre-Shrinkage): Retained for comparison against the ridge and lasso variants.

Model 1, after undergoing shrinkage modifications, was selected as the final model for predicting blood pressure. This model strikes a balance between predictive accuracy, generalizability, and the incorporation of a multifactorial understanding of blood pressure determinants.

<br />

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        <figure class="text-center">
            {% include figure.html path="assets/img/s5.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
            <figcaption class="caption">
                The final model: Model 1 with stepwise selection
            </figcaption>
        </figure>
    </div>
</div>

<br />


## Results

Despite some studies indicating that smoking raises blood pressure, our analysis found lower average blood pressure among smokers. Thus, advising hypertensive patients who smoke to quit may not be beneficial. The primary predictors of blood pressure identified are poverty, age, BMI, sleep quality, and gender, with blood pressure increasing with age and BMI. Men generally have higher blood pressure, and poor sleep quality correlates with lower blood pressure, although underlying factors may influence this.
Regular blood pressure monitoring is recommended, especially for older and obese individuals, with a focus on men. Public education on proper blood pressure measurement and its importance is crucial.

It is important to note that while smoking is associated with blood pressure, it is not a strong predictor in our model. The complexity it adds reduces the model's stability across different data sets. Thus, effective prediction of blood pressure involves considering a range of factors, with smoking being a less significant predictor in our study.

You can also check a powerpoint presentation for this project <a href="/assets/pdf/final.pdf" target="_blank">here</a>.
