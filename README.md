# JusticeGuard: Bias Mitigation in Criminal Risk Assessment 

---

## Problem

Machine learning systems are increasingly used in criminal justice risk assessment to predict recidivism and support decisions related to bail, sentencing, and parole. However, many of these systems have been criticized for reinforcing historical and demographic bias present in the training data. Studies on the COMPAS dataset demonstrated significant disparities in prediction outcomes across racial groups, raising concerns around algorithmic fairness and accountability.

Traditional black-box classifiers often optimize predictive accuracy without considering fairness constraints. As a result, models may achieve strong performance metrics while still producing discriminatory outcomes for protected groups.

This project addresses the challenge of developing a criminal justice risk prediction pipeline that balances:

* Predictive performance
* Fairness-aware modeling
* Bias mitigation
* Ethical interpretability

---

## Solution

FairPredict implements a fairness-aware machine learning pipeline for recidivism prediction using the COMPAS dataset.

The project combines supervised learning techniques with fairness evaluation and bias mitigation strategies to reduce demographic disparities in prediction outcomes. Multiple classification models were trained and evaluated using fairness metrics to measure disparate impact across racial groups.

The pipeline focuses on identifying and mitigating algorithmic bias while preserving acceptable predictive performance. The system also includes post-training fairness analysis to quantify tradeoffs between accuracy and equity.

---

## Implementation

### Dataset

* **Dataset:** COMPAS Recidivism Dataset
* **Domain:** Criminal justice risk assessment
* **Prediction Task:** Binary recidivism classification
* **Protected Attribute:** Race

The dataset contains demographic, criminal history, and risk-related attributes commonly used in recidivism prediction systems.

### Data Preprocessing

A structured preprocessing pipeline was implemented to prepare the dataset for fairness-aware modeling.

#### Preprocessing Steps

* Missing value handling
* Categorical feature encoding
* Feature selection
* Train-test split
* Protected attribute isolation for fairness analysis

### Machine Learning Models

Multiple classification algorithms were evaluated to compare predictive behavior and fairness outcomes.

#### Models Used

* Logistic Regression
* Random Forest
* Decision Tree
* XGBoost

### Fairness Evaluation

The project incorporated fairness metrics to evaluate demographic bias in prediction outcomes.

#### Metrics Analyzed

* Demographic Parity
* Equal Opportunity
* Disparate Impact
* False Positive Rate disparity
* Accuracy by subgroup

The fairness analysis compared prediction distributions across racial groups to identify disproportionate outcomes.

### Bias Mitigation Techniques

Bias mitigation strategies were applied to reduce discriminatory behavior in the trained models.

#### Techniques Explored

* Feature sensitivity analysis
* Protected attribute exclusion
* Threshold adjustment
* Comparative fairness evaluation across models

The pipeline measured fairness-accuracy tradeoffs before and after mitigation to evaluate the effectiveness of debiasing strategies.

### Visualization & Analysis

The project included statistical visualization and fairness diagnostics using:

* Confusion matrices
* Distribution analysis
* Fairness metric comparison plots
* Feature importance analysis

### Tech Stack

* Python
* scikit-learn
* Pandas
* NumPy
* Matplotlib
* Seaborn
* XGBoost
* Jupyter Notebook

---

## Results and Output

* The baseline XGBoost model achieved approximately **69% accuracy** on the COMPAS recidivism dataset.
* Fairness evaluation revealed significant racial disparities in prediction outcomes, especially in **false positive rates** across demographic groups.
* After applying bias mitigation techniques, the **Demographic Parity Difference improved by ~18%** and subgroup prediction consistency increased.
* The debiased models maintained competitive predictive performance while reducing unfair classification behavior.
* Comparative evaluation showed that Logistic Regression produced better interpretability, while XGBoost delivered the highest predictive accuracy.

### Key Findings

* Fairness optimization reduced demographic imbalance without major accuracy degradation.
* Bias mitigation improved fairness metrics while preserving model stability.
* The project demonstrated the practical tradeoff between predictive accuracy and algorithmic fairness in criminal justice AI systems.

---

## Getting Started

### Clone Repository

```bash id="m1a2bc"
git clone https://github.com/rohantikotekar/FairPredict-An-Ethical-AI-Approach-to-Mitigating-Bias-in-Criminal-Justice-Risk-Assessment.git
cd FairPredict-An-Ethical-AI-Approach-to-Mitigating-Bias-in-Criminal-Justice-Risk-Assessment
```

### Install Dependencies

```bash id="x8y9za"
pip install -r requirements.txt
```

### Launch Notebook

```bash id="j7k8lm"
jupyter notebook
```

Run the notebook:

```bash id="u2v3wx"
CS108_212_STAT108_212_W25_Course_Project_Bias_Mitigation (2).ipynb
```

---

## Future Scope

### Advanced Fairness Algorithms

Integrate fairness-aware optimization frameworks such as:

* Adversarial debiasing
* Reweighing
* Fair representation learning

### Explainable Fairness

Combine fairness analysis with explainability frameworks such as SHAP and LIME to improve transparency in bias auditing.

### Intersectional Bias Analysis

Extend fairness evaluation across multiple protected attributes including:

* Race
* Gender
* Age
* Socioeconomic status

### Real-Time Fairness Monitoring

Develop a monitoring dashboard for continuous fairness evaluation in production environments.

### Policy-Aware AI Systems

Explore integration of legal and ethical constraints into model optimization pipelines for high-stakes AI systems.

---

