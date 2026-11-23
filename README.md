# Loan Approval Prediction | Machine Learning

**End-to-End Machine Learning Project | Tel Aviv University | 2025**

## Project Overview

Developed an end-to-end machine learning pipeline to predict mortgage loan approval outcomes using a dataset based on Florida's 2013 Home Mortgage Disclosure Act (HMDA) records.

The project covers the full data science workflow, from exploratory data analysis and preprocessing to feature engineering, model optimization, evaluation, and selection.

**Objective:** Predict whether a mortgage application will be approved (1) or denied (0), while comparing different machine learning approaches and evaluating their practical trade-offs.

## Technologies & Methods

**Languages & Libraries:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

**Machine Learning:** Logistic Regression, Decision Tree, Random Forest, Multi-Layer Perceptron (MLP)

**Techniques:** Exploratory Data Analysis, Feature Engineering, One-Hot Encoding, Cross-Validation, Hyperparameter Tuning, Feature Importance, ROC-AUC Analysis

## Methodology

### 1. Exploratory Data Analysis & Preprocessing

- Analyzed numerical and categorical features, missing values, class distributions, and correlations.
- Identified and removed redundant geographic features with strong correlations.
- Addressed missing and inconsistent values, including consolidating information across multiple race-related fields.
- Investigated outliers and evaluated their implications before deciding how to handle them.
- Applied numerical scaling and categorical encoding, restricting high-cardinality features to control dimensionality.

### 2. Feature Engineering

- Created additional predictors, including a loan-to-income ratio and a squared income feature.
- Evaluated relationships between application characteristics and approval outcomes.
- Examined potential redundancy and predictive value across features.

### 3. Model Development & Optimization

Trained and compared four classification models:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Multi-Layer Perceptron (MLP)

Used cross-validation and hyperparameter optimization with GridSearchCV and RandomizedSearchCV.

Evaluated model performance using ROC-AUC, Accuracy, F1-score, and confusion matrices.

## Model Performance

The following ROC-AUC scores were reported in the final project analysis:

| Model | ROC-AUC |
|---|---:|
| Logistic Regression | 0.867 |
| Decision Tree | 0.860 |
| Random Forest | 0.873 |
| Neural Network (MLP) | **0.875** |

Although the neural network achieved the highest reported ROC-AUC, **Random Forest was selected as the final model** based on its competitive predictive performance, highest reported cross-validation F1-score (0.797), faster training, and greater interpretability.

### Generalization & Overfitting

Random Forest achieved:

- **Training Accuracy:** 88.5%
- **Cross-Validation Accuracy:** 79.5%
- **Cross-Validation F1:** 0.797

The approximately 9-percentage-point difference between training and cross-validation accuracy suggests some overfitting.

This was identified as an important limitation and a potential area for further optimization.

## Key Findings

**1. Model selection requires more than maximizing a single metric.**

The neural network achieved a slightly higher ROC-AUC, but Random Forest offered a favorable combination of F1-score, computational efficiency, and interpretability.

**2. Feature engineering and preprocessing were central to the workflow.**

Handling incomplete records, reducing redundant variables, and constructing additional predictors helped establish a structured modeling pipeline.

**3. Feature importance requires careful interpretation.**

Loan amount, applicant income, loan-to-income ratio, and geographic variables were examined as potentially influential predictors.

An anonymized feature (`A`) also showed particularly high importance in the Random Forest analysis. Because its underlying meaning was not documented, this result requires additional investigation before drawing conclusions about its predictive significance.

**4. Demographic patterns raise fairness considerations.**

Exploratory analysis identified differences in approval outcomes across demographic groups. These observations do not establish causality and highlight the need for additional fairness and bias assessments before any real-world application.

## Limitations & Future Improvements

- **Overfitting:** Further regularization and model complexity adjustments could improve Random Forest generalization.
- **Feature transparency:** Investigate anonymized variables and assess potential data leakage.
- **Fairness:** Evaluate performance across demographic subgroups using appropriate fairness metrics.
- **Explainability:** Explore SHAP or other explanation techniques for more detailed model interpretation.
- **Reproducibility:** Validate the full pipeline in a fresh execution environment.

## Repository Contents

- `loan_approval_analysis.ipynb` - Complete analysis, preprocessing, model development, evaluation, and visualizations.
- `requirements.txt` - Python dependencies.
- `README.md` - Project documentation.

## Dataset

The project uses a Florida 2013 mortgage application dataset derived from HMDA data and provided as part of the Introduction to Machine Learning course at Tel Aviv University.

The original data files are not included in this repository. Their exact distribution source and redistribution terms have not been independently verified.

To reproduce the analysis, authorized copies of the training and test datasets are required.

## Running the Project

1. Clone or download this repository.
2. Install dependencies:

   `pip install -r requirements.txt`

3. Place `train.csv` and `test.csv` inside a local `data/` directory.
4. Open `loan_approval_analysis.ipynb` using Jupyter Notebook or JupyterLab.

**Note:** The notebook contains saved outputs from the original academic project. A complete clean-environment rerun has not yet been verified.

## Academic Context

**Course:** Introduction to Machine Learning  
**Institution:** Tel Aviv University  
**Year:** 2025

This project was independently developed as part of the course, applying machine learning techniques to a real-world classification problem.
