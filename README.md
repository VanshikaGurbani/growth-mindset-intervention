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

- The intervention had a **positive causal effect** on achievement, with results robust across multiple estimators.
- Uncertainty quantified via confidence intervals and graphical diagnostics.

## 🛠️ Tools & Languages

- Python (Jupyter Notebooks)
- pandas, matplotlib, scikit-learn, econml
- Git & GitHub

## 🧾 References

- Yeager et al. (2019). *A national experiment reveals where a growth mindset improves achievement*. [Nature](https://doi.org/10.1038/s41586-019-1466-y)
