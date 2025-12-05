

### Small area estimation (SAE)

- **Comparing SAE using sample splitting.**  Our approach introduces cross validation schemes that preserve stratification and clustering from complex survey designs. We define error metrics that assess model accuracy in estimating finite population prevalence using direct estimates. We further develop a decomposition formula for the naive squared error estimates from the cross validation, which leads to finite sample adjustments to improve the scoring metrics. 
- **Prevalence mapping for categorical data**,  For area-level models, we apply continuation-ratio logit transformations to design-based direct estimates and model the transformed outcomes using a multivariate Fay–Herriot model. We also explore extending similar random effect construction to unit-level models, where we directly model cluster-level categorical response.
- **Softwear** I have been paticipted in developing: 

  - **`surveyPrev`**: R package for processing, modeling, and visualizing the prevalence of binary health indicators in Demographic and Health Surveys (DHS).
  [[cran]](https://cran.r-project.org/web/packages/surveyPrev/index.html) [[github]](https://github.com/richardli/surveyPrev)
  - **`sae4health`**: R 'shiny' application for generating subnational estimates and prevalence maps of 150+ binary indicators.
  [[shiny]](https://rsc.stat.washington.edu/sae4health/)[[cran]](https://cran.r-project.org/web/packages/sae4health/index.html) 
  - **`Multi-Indicator SAE Estimates`**: website providing pre-calculated estimates for selected countries and indicators.
  [[website]](https://sae4lmic.stat.uw.edu/)

  More software details can be find [here](https://sae4health.stat.uw.edu/).
---

### machine learning models for aging health  

- We applied machine learning methods, including XGBoost and feature-importance techniques, to study racial/ethnic differences in social determinants of mild cognitive impairment and its progression to dementia in the **All of Us** Research Program.

---

### Bayesian spatio-temporal model for Opioid epidemic

- We Developed a Bayesian spatio-temporal model for opioid-related outcomes (deaths and emergency-department visits) across 100 counties in North Carolina and predicted future outcomes under multiple resource-allocation scenarios and proposed an optimization criterion aimed at minimizing opioid-related harms.
