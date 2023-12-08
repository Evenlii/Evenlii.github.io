---
layout: page
title: Monty Hall Meets AI
description: AI transparency, Human-AI interaction, decision making, experimental study 
img: assets/img/monty1.jpeg
importance: 3
category: Data Science
---

**Supervisors and Collaborators**:
Prof. Boris Babic, Prof. Dabid Soberman, Prof. Pankaj Aggarwal


AI (Artificial Intelligence) has been playing an increasingly important role in everyday life. AI promises to transform human decision-making in almost all domains of life, including the most complex and seemingly ambiguous domains such as healthcare, law, and others. However, it is not clear the extent to which humans are comfortable with the recommendations given by AI and the extent to which decision makers are willing to accept such recommendations. One reason that has been proposed as being a key bottleneck in the acceptance of AI in all domains, especially in domains where the outcome is risky and uncertain, is the lack of clear understanding of how AI works. In other words, it is generally believed that people’s perception of the process by which AI comes up with its recommendation is not much more than seeing it as a black box. As such, the decision makers, who are often ‘experts’ in their domain tend to reject the recommendation of the AI over their own intuition or even ‘expert’ recommendation.

This current research studies the extent to which people are willing to accept the recommendation of AI in a risky decision context that involves a probabilistic outcome. We use experimental design to study the extent to which decision makers accept or reject the ‘advice’ given by AI. Specifically, we chose the Monty Hall problem,  a famous probability problem reasoning using Bayes’ theorem as our experimental framework and innovated the scenario by incorporating AI-generated suggestions to help participants make the right decision. 

## Monty Hall Problem: An Introduction

The Monty Hall Problem is a game show scenario where you choose from three doors, behind each of which lies either a car (a desirable prize) or a goat (less desirable). After selecting a door, the host, Monty Hall, who knows what's behind each door, opens one of the remaining doors, always revealing a goat. He then offers you a chance to switch your choice to the other unopened door. The critical decision is whether to stick with your original choice or switch, assuming you prefer a car over a goat.

Contrary to intuition, the optimal strategy, supported by Bayes Theorem, is to switch doors. In our research, we incorporated an additional element: participants received AI-generated hints before making their final decision.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/monty2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Monty Hall problem
</div>


## Study Design

Our research explored the impact of AI recommendations on decision-making across three dimensions:

(i) **AI transparency**: We had two different conditions of AI – in one condition AI was presented as a ‘black box’ – meaning no additional information was given to explain what AI is and how it works. In the other condition, the participants were given an explanation about what AI is and how it works. 

(ii) **Cost of AI advice**: We employed three different levels of ‘simulations’ to examine if people were willing to pay to see the recommendation of the AI at each of these three levels. The levels varied by the number of simulations done by the AI – 5, 30, 100. The study was designed such that AI’s recommendations with a greater number of simulations generated more accurate suggestions but cost more to the participants.

(iii) **AI involvement stage (anchoring effect)**: we presented the information about the AI either after the participants had made their choice with a chance to change their choice (late stage) or before they had a chance to make their choice (early stage). We wish to examine if participants who think of AI as a black box are less willing to change their decision compared to those who are given more information about AI and how it works. 

## Main Hypothesis:

(i) It is hypothesized that transparency about AI (explanation about AI condition) would make people more likely to endorse and accept its recommendation compared to the opaque (black box condition). \\
(ii) We think that people will show greater confidence in the condition that has a higher number of simulations, but that this effect will be observed only in the transparent condition. When the AI is presented as a black box, we hypothesize that there will be no preference shown for higher number of simulations. If these results are observed, they will support our contention that lack of understanding about AI is a key factor that limits its acceptance.  \\
(iii) It is further hypothesized that presenting the information after the decision has been made might be less effective due to anchoring, especially for people who are ‘skeptical’ about the value of AI. 


## Qualtric Survey and data collection

To realize our experimental design and effectively conduct hypothesis testing, we formulated an interactive Qualtric survey. There are two different sources that we used/will use to recruit the participants. Our key source would be M-Turk, where we would recruit US citizens with no particular exclusion criteria. Our second pool of participants would be the Management Subject Pool run by the Department of Management, UTSC. Again, all undergraduates who are eligible to be in the Subject Pool will be eligible to participate in the study with no exclusion criteria. In order to recruit, we will post the study on the M-Turk website for the 'workers' to sign up, and on SONA for the students to sign up.  A total of 1600 participants will be involved, with all studies conducted post-consent. Personal data will not be matched with individual responses nor made public.

Check a sample survey of one of the studies <a href="https://rotman.az1.qualtrics.com/jfe/form/SV_6mu2gpQNC1uT0y2" target="_blank">here</a>.

## Pilot study

We’ve conducted a pilot study to test our experimental framework. A total of 200 participants from the University of Hong Kong who enrolled in the course ‘’Fundamentals of AI, Data and Algorithms” were invited to participate in the pilot study. The key results are as follows: 

(i) Participants exhibit a preference for obtaining AI information when it’s available at no cost or a lower cost, regardless of the transparency of the AI information or the timing of its presentation.  \\
(ii) Participants tend to stick with their initial choice of doors before AI information is presented.  \\
(iii) The majority of participants who purchased either 5 or 30 trials of information demonstrated a reluctance to change their decision even after receiving AI information. Moreover, the transparency of AI information did not significantly impact their decision-making behavior.  \\
(iv) Approximately 30% of participants utilized AI information to make their decisions. Remarkably, these individuals had roughly four times the odds of winning compared to those who did not mention AI-related information. 

