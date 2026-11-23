# Loan Approval Prediction | Machine Learning

An academic machine learning project exploring loan approval prediction using a Florida 2013 mortgage application dataset provided as part of a course at Tel Aviv University.

## Project Overview

This project covers exploratory data analysis, data cleaning, feature engineering, model training, and performance evaluation to predict mortgage loan application outcomes.

## Methods

- Exploratory data analysis and missing-value handling
- Feature engineering and categorical encoding
- Numerical preprocessing and feature selection
- Model training and comparison
- Cross-validation and evaluation using classification metrics and ROC-AUC

## Machine Learning Models

- Logistic Regression
- Decision Tree
- Random Forest
- Multi-Layer Perceptron (MLP)

## Results

The notebook's concluding summary reports the following approximate ROC-AUC scores:

| Model | Reported ROC-AUC |
|---|---:|
| Logistic Regression | 0.867 |
| Decision Tree | 0.860 |
| Random Forest | 0.873 |
| MLP Neural Network | 0.875 |

These figures are taken from the notebook's concluding summary and have not been independently reproduced. Other sections may describe different evaluation settings.

## Repository Contents

- `loan_approval_analysis.ipynb` - analysis, modeling, visualizations, and results
- `requirements.txt` - main Python dependencies

## Dataset

The dataset is derived from Florida's 2013 Home Mortgage Disclosure Act (HMDA) data and was provided by the course instructor. The exact download source and redistribution terms have not been verified, so the original data files are not included.

To run the notebook, obtain authorized copies of `train.csv` and `test.csv` and place them in a local `data/` directory.

## Running the Project

1. Clone or download this repository.
2. Install the dependencies using `pip install -r requirements.txt`.
3. Place `train.csv` and `test.csv` in the `data/` folder.
4. Open `loan_approval_analysis.ipynb` in Jupyter Notebook.

**Note:** The notebook retains historical outputs and some Google Colab-oriented code. It has not been fully validated in a fresh environment.

## Academic Context

Developed as part of an Introduction to Machine Learning course at Tel Aviv University.
