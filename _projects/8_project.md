---
layout: page
title: Gender Pay Inequality
description: Statistical Modeling, Data Analysis, Computational Social Sciences
img: assets/img/pay0.jpeg
importance: 4
category: Data Analysis
---

## Background and goal

In a world where wealth significantly influences the quality of life and access to social resources, the disparity in earnings based on gender stands as a critical issue. This report delves into the gender pay gap within the IT sector of the Eurozone, a region where this inequality is particularly pronounced. By analyzing a comprehensive dataset of IT specialists' salaries from 2020, we aim to investigate the gender disparity in male-dominated work fields and offer strategies for equity promotion. 

To support this analysis, we will use the salary dataset of IT specialists in the EU region in 2020. The data were collected from an anonymous salary survey in 2020, in which 1,253 respondents volunteered to participate.

## Initial exploratory analysis

Our initial analysis reveals a stark contrast in earnings between genders. The average gross income for female IT professionals stands at €60,000 annually, compared to €75,000 for their male counterparts. This significant difference underscores the urgency of addressing gender pay inequality. Furthermore, the pay rise distribution for women, characterized by a bimodal and right-skewed histogram, indicates that a significant proportion of female IT workers did not receive any pay rise in 2020. This trend highlights the additional challenges women face in advancing their careers within the sector.

<br />

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        <figure class="text-center">
            {% include figure.html path="assets/img/pay1.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
            <figcaption class="caption">
                
            </figcaption>
        </figure>
    </div>
</div>

<br />

<div class="row justify-content-center">
    <div class="col-sm mt-3 mt-md-0">
        <figure class="text-center">
            {% include figure.html path="assets/img/pay2.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
            <figcaption class="caption">
               
            </figcaption>
        </figure>
    </div>
</div>

<br />

## Methodology

This report will use six statistical methods to examine gender pay inequality in the IT industry in Europe. More specifically, we will focus on the average salary level of men and women, the salary increase of women, and the proportion of women in the high-income group to investigate the well-being of female IT employees in the EU. Finally, we will analyze the relationship between working experience and total annual income to analyze the reasons for women’s lower average salary level compared to men. 

*  **Confidence Intervals**: Estimating the true mean annual gross salary for males and females using bootstrap samples and a 95% confidence interval.

*  **Hypothesis test**: Investigating the true average salary of female employees in the IT sector over the Eurozone. In the confidence interval
section above, we found a range for the true average salary of female IT workers, based on which we wanted to get a more specific estimate.

*  **Maximum Likelihood Estimator**: Focusing on the annual salary increase for female employees, we hypothesize that this follows an exponential distribution.

*  **Goodness of Fit Test**: Assessing the proportion of women among high-income IT professionals, with an initial estimate of women comprising only 10% of this group.

*  **Bayesian Credible Interval**: Enhancing the reliability of our findings regarding the proportion of high-income females in the IT sector.

*  **Regression Model**: Exploring the relationship between work experience and annual gross salary to understand gender-based salary disparities.

## Key Results

Our findings confirm the severity of gender pay inequality in the IT sector. Men's average annual salaries significantly surpass those of women, with a 95% confidence interval reinforcing this disparity. Based on the sample average and the confidence interval, we have strong evidence that female
IT employees’ true yearly average wage in the EU is 60,000 euros in 2020. The exponential distribution model for female salary increases provides further insight, allowing us to calculate probabilities and percentiles for annual pay rises. 

A particularly telling result is the underrepresentation of women in high-salary positions, estimated at only 10%. Our Bayesian analysis supports this, indicating a 95% probability that the true parameter of high-earning women ranges between 3.5% and 15.4%. Additionally, our regression analysis reveals a positive correlation between work experience and salary, suggesting that the relative lack of experience among women—partly due to career interruptions for childbirth or caregiving—may contribute to their lower average salaries. For new IT employees, they are expected to earn an annual salary of 57,831 euros. People with more work experience tend to be more capable and efficient in handling things, thus making a higher salary. Based on this relationship, we speculate that the reason for the lower salary levels of women compared to men may be the lack of work experience of women. The sample points out that the average work experience of female IT employees in the EU is three years less than that of men. This may be because women are faced with childbirth or household care as they get older. Since pregnant women tend to have difficulty in mobility, they are likely to get fired, resulting in a lack of work experience. It also means that women have fewer opportunities for advancement than men, which may be one of the reasons why women make up a smaller percentage of the high-earning population. Therefore, the average salary level of women will be lower than that of men.



## Recommendation

To address these disparities, a multifaceted approach is necessary:

* **Performance-Based Evaluation**: Companies should adopt blind evaluation processes, focusing solely on employees' accomplishments without regard to gender or age.

* **Public Awareness and Education**: Governments and institutions should leverage social media and educational programs to highlight the issue of gender inequality.

* **Regulatory Measures**: Governments need to enforce regulations ensuring equal treatment and opportunities in workplaces, with stringent penalties for discrimination.

* **Support for Working Mothers**: Companies should offer flexible work arrangements and additional training for women returning from maternity leave, facilitating their reintegration and career progression.

<br />

**You can also download the full report** <a href="/assets/pdf/pay.pdf" target="_blank">here</a>.
