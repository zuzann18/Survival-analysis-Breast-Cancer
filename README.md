# Survival Analysis in R using GBSG2 Dataset

This repository contains an in-depth exploration of survival analysis techniques using the **GBSG2** dataset. The analysis is implemented in R and includes statistical modeling, data visualization, and interpretation of survival patterns.

## Features of this Repository

### 1. Dataset Overview
The **GBSG2** dataset is a well-known dataset used in survival analysis studies. It includes data from a clinical trial involving patients with **breast cancer**, providing information on:
- `time`: Survival time (in days).
- `cens`: Censoring status:
  - `0`: Censored (patients alive at the end of the study or lost to follow-up).
  - `1`: Event occurred (e.g., death due to cancer or other complications).
- `horTh`: Hormonal therapy status.
- `tsize`: Tumor size.
- Additional variables include patient age, menopausal status, and other clinical factors.

### 2. Methods and Techniques
The analysis was conducted using the following survival analysis methods:
1. **Kaplan-Meier Estimator**:
   - Provides non-parametric survival curves to visualize survival probabilities over time.
   - Marks censored observations on the curve and includes confidence intervals.
2. **Weibull and Log-Normal Parametric Models**:
   - Enables estimation of survival probabilities and comparison of different patient subgroups.
3. **Cox Proportional Hazards Model**:
   - Evaluates the impact of covariates (e.g., hormonal therapy, tumor size) on survival.
4. **Exploratory Data Analysis (EDA)**:
   - Visualizations such as histograms, bar plots, and heatmaps to explore data distributions and correlations.

### 3. Key Visualizations and Insights

#### 1. **Kaplan-Meier Survival Curve**
The Kaplan-Meier estimator shows survival probabilities over time, accounting for censored data. It highlights how many patients remain alive at various time points.

**Key Insights**:
- The probability of survival decreases over time.
- Censored data is marked with red `+` symbols.

**Visualization**:
![Kaplan-Meier Survival Curve](#)

#### 2. **Weibull Survival Curve**
The Weibull model is a parametric survival model that estimates survival probabilities based on a mathematical distribution.

**Key Insights**:
- Survival probabilities decrease over time following a Weibull distribution.
- The curve aligns closely with the Kaplan-Meier estimate for most time points.

**Visualization**:
![Weibull Survival Curve](#)

#### 3. **Comparison of Weibull and Log-Normal Models**
This visualization compares the Weibull and Log-Normal survival curves. It highlights differences in model predictions for long-term survival.

**Key Insights**:
- The Weibull model predicts shorter survival times compared to the Log-Normal model for longer periods.
- Both models align well with early survival trends.

**Visualization**:
![Comparison of Weibull and Log-Normal Models](#)

#### 4. **Cox Model Survival Curves**
The Cox proportional hazards model was used to estimate survival probabilities for two patient groups:
- Group 1: Smaller tumors with hormonal therapy.
- Group 2: Larger tumors without therapy.

**Key Insights**:
- Patients with smaller tumors and hormonal therapy have significantly higher survival probabilities over time.
- The difference between groups widens as time progresses.

**Visualization**:
![Cox Model Survival Curves](#)

### 4. Conclusions
1. **Censoring is common**:
   - Out of 686 observations, 387 (56%) were censored.
   - Proper handling of censored data is crucial for accurate analysis.
2. **Survival patterns**:
   - Hormonal therapy improves survival significantly.
   - Smaller tumors predict better survival outcomes.
3. **Model comparisons**:
   - The Weibull model aligns closely with Kaplan-Meier estimates, while the Log-Normal model predicts slightly longer survival times.

### 5. Repository Contents
- **Notebooks and R Scripts**: Include all code for the analysis and visualizations.
- **Visualizations**: Kaplan-Meier, Weibull, Log-Normal, and Cox model curves.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/survival-analysis-r.git
   ```
2. Install necessary R libraries:
   ```R
   install.packages(c("survival", "survminer", "TH.data", "reshape2", "ggplot2"))
   ```
3. Open the Jupyter Notebook or run the R scripts to explore the analysis.

## Dependencies
- R (version >= 4.4.0)
- Libraries: `tidyverse`, `survival`, `survminer`, `TH.data`, `reshape2`, `ggplot2`.



-
