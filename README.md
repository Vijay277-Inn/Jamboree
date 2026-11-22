# Jamboree Graduate Admission Prediction 🎓✈️

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg) 
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg) 
![Statsmodels](https://img.shields.io/badge/Library-Statsmodels-green.svg) 
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

An end-to-end predictive modeling and statistical analysis project to help **Jamboree** (a leading study-abroad prep platform) understand the academic and profile features that influence a student's probability of graduate admission.

## 📌 Project Overview
Jamboree wants to identify the key factors determining a student's graduate admission probability (from `0` to `1`). Using a dataset of 500 applicants, this project conducts rigorous Exploratory Data Analysis (EDA), validates regression assumptions, builds robust predictive models, and delivers data-backed recommendations.

## 📊 Key Findings & Insights
1. **CGPA is King:** Academic performance is the strongest single predictor. For every standard deviation increase in CGPA, the baseline chance of admission rises by **~6.9%**.
2. **Standardized Tests Matter:** GRE and TOEFL scores are statistically significant and powerful predictive drivers.
3. **Quality over Quantity (LOR vs. SOP):** Letter of Recommendation (LOR) strength is highly statistically significant, whereas Statement of Purpose (SOP) was statistically insignificant when other factors were accounted for.
4. **Research Value-Add:** Prior research experience adds an immediate, flat **2.46%** boost to an applicant's probability.

## 🛠️ Models Implemented & Performance
We trained and evaluated multiple linear algorithms. The **Lasso Regression** model (fully tuned) and **OLS (with robust standard errors)** yielded the best results:

| Model | MAE | RMSE | $R^2$ Score |
| :--- | :--- | :--- | :--- |
| **Tuned Lasso Regression** | **0.0425** | **0.0608** | **81.91%** |
| **Multiple Linear Regression (OLS)** | 0.0427 | 0.0608 | 0.8188% |
| **Tuned Ridge Regression** | 0.0428 | 0.0610 | 0.8183% |

### Statistical Validation (Diagnostics):
* **Multicollinearity:** Checked via Variance Inflation Factors (VIF). All final features scored below **4.65**, proving no severe multicollinearity was present.
* **Heteroscedasticity:** Handled using heteroscedasticity-robust standard errors (`HC3`) to ensure stable p-values.
* **Autocorrelation:** Verified with a Durbin-Watson statistic of **2.05**, indicating independent residuals.

## 🚀 Actionable Recommendations for Jamboree
* **Academic Coaching:** Prioritize counseling around undergraduate GPA (CGPA) maintenance, as it carries the heaviest weight.
* **Targeted Test Preparation:** Guide students to reach specific target score thresholds on the GRE and TOEFL to complement their CGPA.
* **Qualitative Strategy:** Advise students to spend more energy securing strong, personalized letters of recommendation (LORs) rather than over-polishing general SOPs.
* **Research Incubation:** Encourage underrepresented or borderline-score students to acquire research internships to gain an immediate boost.
