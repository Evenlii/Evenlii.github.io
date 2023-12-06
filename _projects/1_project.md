---
layout: page
title: Surrogate Assisted Positive Unlabeled Learning on EHR data
description: semi-supervised, machine learning, EHR, clinical risk prediction
img: assets/img/poster.png
importance: 1
category: Data Science Research
related_publications: 
---

Clinical risk prediction models developed with electronic health record (EHR) data are critical for improving patient care and optimizing healthcare resource allocation. However, traditional supervised learning methods for risk prediction require extensive labeled data, which is costly and time-consuming to obtain due to the expertise required to label clinical data.  Fortunately, there are inherent structures in EHR data that can be leveraged by machine learning methods to overcome the labeling burden.  

For many diseases, subsets of patients have confirmatory evidence of the condition readily available in their EHR.  For example, many cancer patients have a pathological diagnosis code in their records.  Similarly, patients diagnosed with chronic conditions such as heart failure receive codes to monitor ongoing care.  EHR data therefore contains readily available positive examples (i.e., patients known to have the disease through confirmatory evidence) together with a large volume of unlabeled examples (i.e., patients with unknown disease status without confirmatory evidence).   While positive unlabeled learning (PUL) methods accommodate this data structure and do not require manual labeling, there are substantial limitations of existing methods.

Most PUL approaches require that the positive examples are a random subset of all positive examples.  This is unlikely in the EHR setting due to the complexities of clinical documentation and healthcare access.   Additionally, most approaches are restricted to the low-dimensional setting where the number of features is less than the number of positive examples, another assumption that is violated due to the volume of information in EHRs.   

To address these limitations, this project develops a novel PUL method derived under realistic assumptions for EHR-based research.  Specifically, we introduce a PUL method for high-dimensional single-index models to expedite the development of clinical risk prediction models.  We also demonstrate the practical utility of our methodology with a large-scale analysis of the MIMIC-III phenotyping dataset. 

## Key Results

(i) SAPUL performed as well as supervised learning with 500 labels on both real and simulated data \\
(ii) Utilizing NLP analysis to extract disease-indicative terms from patients' discharge summaries can improve SAPUL's predictive accuracy \\
(iii) SAPUL shows reliable performance for high-dimensional data \\
(iv) SAPUL has the potential to streamline the laborious chart review process and substantially minimize the effort required for data labeling

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/auc 2.PNG" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    SAPUL shows an AUC score that outperformed other baseline models
</div>

## Publication

We are now preparing a manuscript for submission to *Biometrics*, and an open-source R package 'SAPUL' will be published soon. \\
I also presented the poster at the 2023 Summer Research Showcase organized by the Data Science Institute at the University of Toronto. You can download the poster <a href="/assets/pdf/poster.pdf" target="_blank">here</a>.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/poster.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    SAPUL Poster
</div>










