---
title: Qianyu Dong
description: ""
statement: "Measuring health where data are sparse"

# Research cards. Optional per card: image (path under static/) and alt (a short description of the image).
research:
  - title: "Small area estimation"
    summary: "Model evaluation and prevalence mapping with complex household surveys."
    link: "research/#small-area-estimation-sae"
    image: "images/research/sae-kenya-map.webp"
    alt: "Map of Kenya shaded by estimated antenatal care (ANC4+) coverage in each Admin-2 area"
  - title: "Aging health"
    summary: "Machine learning for cognitive impairment and dementia in the All of Us Research Program."
    link: "research/#machine-learning-models-for-aging-health"
    image: "images/research/aging-shap.webp"
    alt: "SHAP beeswarm plot of social determinants predicting progression from mild cognitive impairment to dementia"
  - title: "Opioid epidemic"
    summary: "Bayesian spatio-temporal models to guide treatment resource allocation."
    link: "research/#bayesian-spatio-temporal-model-for-the-opioid-epidemic"
    image: "images/research/opioid-nc-2021.webp"
    alt: "Map of North Carolina counties shaded by illicit opioid overdose death rate in 2021"

software_more:
  label: "More on sae4health"
  url: "https://sae4health.stat.uw.edu/"
software:
  - name: "surveyPrev"
    summary: "R package for processing, modeling, and visualizing the prevalence of binary health indicators in Demographic and Health Surveys."
    links:
      - label: "CRAN"
        url: "https://cran.r-project.org/web/packages/surveyPrev/index.html"
      - label: "GitHub"
        url: "https://github.com/richardli/surveyPrev"
  - name: "sae4health"
    summary: "R Shiny application for subnational estimates and prevalence maps of 150+ binary indicators."
    links:
      - label: "Shiny app"
        url: "https://rsc.stat.washington.edu/sae4health/"
      - label: "CRAN"
        url: "https://cran.r-project.org/web/packages/sae4health/index.html"
  - name: "Multi-indicator SAE estimates"
    summary: "Website with pre-calculated estimates for selected countries and indicators."
    links:
      - label: "Website"
        url: "https://sae4lmic.stat.uw.edu/"

---

I'm a Ph.D. candidate in [Statistics](https://engineering.ucsc.edu/departments/statistics/) at UC Santa Cruz, advised by [Zehang Richard Li](https://zehangli.com/). I build statistical models for public health, drawing on Bayesian methods, survey statistics, and small area estimation. My current project uses cross-fitting to evaluate models that estimate prevalence from complex surveys.
