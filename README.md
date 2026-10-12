# Growth Mindset Causal Inference Project

This project estimates the causal effect of a growth mindset intervention on student academic achievement using synthetic data inspired by the National Study of Learning Mindsets (NSLM).

## 🧠 Project Overview

- **Goal:** Estimate the Average Treatment Effect (ATE) of a growth mindset "nudge-like" intervention.
- **Approach:** Apply causal inference techniques (e.g., T-learner, S-learner, IPW regression, Causal Forests).
- **Data Type:** Observational (synthetically generated but based on NSLM design).
- **Outcome Variable (Y):** Continuous measure of student achievement.
- **Treatment Variable (Z):** Binary indicator for intervention.

## 📂 Contents

| Folder/File       | Description                                      |
|-------------------|--------------------------------------------------|
| `analysis/`       | Jupyter notebooks for different causal methods  |
| `visuals/`        | Final plots and visualizations                  |
| `poster/`         | Project research poster (PDF)                   |
| `data.csv`        | Synthetic dataset used for analysis             |

## 🧪 Methods Used

- **Propensity Score Modeling**
- **T-Learner and S-Learner**
- **Inverse Probability Weighting (IPW)**
- **Causal Forests**
- **Covariate Adjustment & Assumption Checks**

## 📊 Key Findings

Dataset: 10,391 synthetic student records from 76 schools (32.6% treated); continuous achievement outcome `y` (standard deviation about 0.72).

| Method | ATE | 95% CI |
|:---|:---:|:---:|
| Linear regression (covariate adjusted) | 0.413 | [0.388, 0.438] |
| Inverse propensity weighting (IPW) | 0.415 | [0.387, 0.442] |
| T-Learner (Random Forest) | 0.422 | [0.409, 0.434] |
| T-Learner (XGBoost) | 0.422 | [0.410, 0.434] |
| S-Learner (Random Forest) | 0.421 | [0.409, 0.434] |
| S-Learner (XGBoost) | 0.421 | [0.411, 0.431] |
| Causal Forest (EconML) | 0.415 | [0.208, 0.623] |

(Values printed by notebooks `01` to `04` in `analysis/`; the regression and IPW point estimates are the midpoints of their reported intervals.)

- The intervention had a **positive causal effect of about 0.41 to 0.42 outcome units** in every specification, so the result is robust to the choice of estimator.
- The naive treated-vs-control difference is 0.457; covariate adjustment moves it to about 0.41.
- The Causal Forest interval is much wider than the parametric and learner-based intervals.
- The data is synthetic (modeled on the National Study of Learning Mindsets), so these numbers illustrate the method rather than describe real students.

## 🛠️ Tools & Languages

- Python (Jupyter Notebooks)
- pandas, matplotlib, scikit-learn, econml, xgboost
- Git & GitHub

## 🧾 References

- Yeager et al. (2019). *A national experiment reveals where a growth mindset improves achievement*. [Nature](https://doi.org/10.1038/s41586-019-1466-y)
