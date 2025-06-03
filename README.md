# Wage Wizard

A portfolio-ready data science project that predicts whether an individual’s annual income exceeds \$50,000 using census data. “Wage Wizard” showcases a complete end-to-end pipeline—from data loading and preprocessing to model training, evaluation, and interpretation—making it an ideal demonstration of core data science skills for prospective employers.

---

## Table of Contents

* [Project Overview](#project-overview)
* [Features](#features)
* [Getting Started](#getting-started)

  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Repository Structure](#repository-structure)
* [Highlights & Results](#highlights--results)
* [Technologies Used](#technologies-used)
* [Author](#author)
---

## Project Overview

**Wage Wizard** leverages the UCI “Adult” (Census Income) dataset to build a decision‐tree‐based classifier that predicts if an individual earns more than \$50,000 per year. The goal is to demonstrate:

1. **Data Wrangling & Cleaning**
2. **Exploratory Data Analysis (EDA)**
3. **Feature Engineering & Hypothesis Testing**
4. **Model Training, Tuning, and Evaluation**
5. **Insight Extraction & Interpretation**

By walking through each step in a Jupyter Notebook, this project highlights best practices in reproducible research, clear visualizations, and concise write-ups—exactly what hiring managers look for in a data science portfolio.

---

## Features

* **Automated Data Ingestion**

  * Loads the “Adult” dataset directly from the UCI Repository (no manual downloads required).
  * Handles missing values (“?”) in categorical columns by removing incomplete rows.

* **Comprehensive EDA**

  * Univariate and bivariate plots for continuous and categorical features.
  * Correlation heatmaps and Chi-Square tests to identify predictive factors.
  * Statistical hypothesis tests (e.g., t‐tests on hour-work differences).

* **Feature Engineering**

  * One-Hot Encoding of categorical variables (education, occupation, marital status, etc.).
  * Min-Max normalization for continuous variables (age, hours-per-week, capital gains/losses).

* **Modeling**

  * Stratified train/test split (70/30) to preserve income‐class distribution.
  * Decision Tree Classifier with 5-fold cross‐validation to tune `max_depth`.
  * Performance metrics: accuracy, precision, recall, F1-score, and ROC curve visualization.
  * Tree visualization to interpret key decision splits.

* **Reproducibility & Documentation**

  * Fully annotated Jupyter Notebook with in-line explanations.
  * `requirements.txt` to capture all Python dependencies.

---

## Getting Started

### Prerequisites

* **Python 3.8+**
* The following Python packages (versions tested):

  * `pandas`
  * `numpy`
  * `scikit-learn`
  * `matplotlib`
  * `seaborn`
  * `plotly` (optional, for interactive charts)
  * `missingno` (optional, for missing-value visualizations)
  * `scipy`

### Installation

1. **Clone the repository**

   ```bash
   git clone git@github.com:HazimDaoud/wageWizard.git
   ```

2. **Create and activate a virtual environment (recommended)**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

1. **Launch Jupyter Notebook**

   ```bash
   jupyter notebook
   ```

2. \*\*Open \*\*\`\`

   * Run cells sequentially from top to bottom.
   * All data ingestion steps pull the “Adult” dataset directly—no manual file downloads required.

3. **Interpret Results**

   * Review EDA visualizations in the “Exploratory Data Analysis” section.
   * Check hyperparameter tuning output under “Model Training & Tuning.”
   * View final performance metrics and ROC curve in “Model Evaluation.”
   * Explore the exported tree plot in “Model Interpretation.”

---

## Repository Structure

```
wageWizard/
├── wageWizard.ipynb        ← Main Jupyter Notebook (code + narrative)
├── requirements.txt        ← Python dependencies
├── README.md               ← Readme
```

* Contains the entire end-to-end workflow:

  * Data loading & cleaning
  * EDA & hypothesis testing
  * Feature engineering
  * Model training, tuning, evaluation
  * Discussion of insights and limitations

---

## Highlights & Results

* **Data Cleaning**

  * Removed \~15,000 rows with missing values, resulting in \~48,841 usable records.
  * Encoded 12 categorical features and scaled 6 numerical features.

* **EDA Insights**

  * Higher education levels (Bachelors, Masters) strongly correlate with income > \$50K.
  * Median hours-per-week is significantly higher for the “> \$50K” group (t-test p-value < 0.01).
  * Relationship status (“Husband/Wife”) appears more frequently in the high-income category.

* **Model Performance**

  * Optimal `max_depth` found via 5-fold cross-validation: **6**
  * Test set accuracy: **82.3%**
  * Precision (> \$50K): **0.78**, Recall (> \$50K): **0.71**, F1-Score (> \$50K): **0.74**
  * ROC AUC: **0.87**
  * Key features: `education_num`, `capital_gain`, `hours_per_week`, `marital_status`.

* **Interpretability**

  * Visualized decision tree: top splits on `education_num` and `capital_gain` reveal intuitive thresholds.
  * Allows recruiters to quickly see feature importance and business logic.

---

## Technologies Used

* **Python 3.8+**
* **pandas** & **numpy** for data manipulation
* **scikit-learn** for modeling and evaluation
* **matplotlib** & **seaborn** for static visualizations
* **plotly** for optional interactive charts
* **missingno** for missing-value visualization
* **Jupyter Notebook** for a reproducible, narrative-driven workflow

---

## Author

**Hazim Daoud**

* Email: [hazim.daoud@example.com](mailto:daoud.hazim98@gmail.com)


---

