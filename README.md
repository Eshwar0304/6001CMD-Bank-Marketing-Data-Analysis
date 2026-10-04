# 6001CMD-Bank-Marketing-Data-Analysis
# Bank Marketing Dataset: Data Quality Analysis and Preprocessing

## 1. Project Overview

This repository contains the Python implementation for the 6001CMD Machine Learning Individual Assignment. The project focuses on investigating data quality, performing exploratory data analysis (EDA), and evaluating suitable data preprocessing techniques using the Bank Marketing dataset.

The primary objective is to prepare the dataset for a potential supervised machine learning classification task that predicts whether a customer subscribes to a term deposit following a bank marketing campaign.

The project explores data cleaning, feature transformation, feature selection, dimensionality reduction, categorical encoding, and class imbalance handling.

## 2. Dataset

**Dataset:** Bank Marketing Dataset (bank-full.csv)  
**Source:** UCI Machine Learning Repository  
**Dataset URL:** https://archive.ics.uci.edu/dataset/222/bank+marketing  
**DOI:** https://doi.org/10.24432/C5K306

### Dataset Information

- Total records: 45,211
- Original features: 16 predictors and 1 target variable
- Target variable: `y`
- Problem type: Binary classification

The target variable `y` indicates whether a customer subscribed to a term deposit (`yes` or `no`).

## 3. Project Objectives

- Investigate missing values, duplicate records, unusual observations, and data distributions.
- Identify skewness and potential outliers in numerical features.
- Examine relationships between predictors and the target variable.
- Apply suitable data cleaning and preprocessing techniques.
- Compare standardisation, normalisation, and power transformations.
- Investigate feature selection using Mutual Information.
- Explore dimensionality reduction using Principal Component Analysis (PCA).
- Examine class imbalance handling techniques.
- Develop a reproducible preprocessing workflow for subsequent machine learning development.

## 4. Data Analysis and Preprocessing

The project covers the following stages:

### Exploratory Data Analysis
- Dataset structure and data types
- Missing-value investigation
- Duplicate-record detection
- Descriptive statistics
- Numerical feature distributions and skewness
- Outlier investigation using the Interquartile Range (IQR)
- Correlation analysis
- Target class distribution

### Data Cleaning and Transformation
- Investigation of unknown categorical values
- Evaluation of outlier treatment
- Standardisation of numerical features
- Power transformations for skewed numerical variables
- One-hot encoding of categorical variables

### Feature Engineering and Selection
- Creation of the `previously_contacted` indicator
- Mutual Information-based feature ranking
- Feature selection
- PCA-based dimensionality reduction

### Class Imbalance Investigation
The following approaches were explored:

- Class weighting
- Random oversampling
- Random undersampling
- SMOTENC (Synthetic Minority Over-sampling Technique for Nominal and Continuous features)

### Final Preprocessing Workflow
The proposed workflow includes a stratified training and testing split, fitting preprocessing operations using training data, applying class-balancing techniques only to training data, and reserving the test set for final model evaluation.

The `duration` feature is excluded from the proposed pre-call prediction workflow because it represents the duration of the current call and would not be available before the call takes place.

## 5. Key Findings

- The dataset contains 45,211 records and 17 original columns.
- No missing values or exact duplicate records were identified.
- Several categorical features contain `unknown` values.
- Numerical features such as `balance`, `campaign`, and `previous` exhibit substantial positive skewness.
- The target variable is imbalanced, with approximately 88.3% negative cases and 11.7% positive cases.
- Mutual Information was used to investigate feature relevance.
- PCA indicated that 17 components retained approximately 90.35% of the variance, while 23 components retained approximately 95.11%.

These findings informed the selection of preprocessing techniques and the proposed machine learning workflow.

## 6. Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn

## 7. Repository Contents

The repository contains the Python notebooks, supporting files, and documentation associated with the assignment.

Please refer to the files and folders in this repository for the implementation of the data analysis and preprocessing stages.

## 8. How to Run

1. Clone or download this repository.
2. Install Python and Jupyter Notebook.
3. Install the required Python libraries.
4. Ensure the Bank Marketing dataset (`bank-full.csv`) is available in the location specified in the notebook.
5. Open the Jupyter Notebook.
6. Run the notebook cells sequentially to reproduce the analysis and preprocessing experiments.

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

## 9. Project Status

**Status:** Data analysis and preprocessing investigation completed.

The project focuses on data preparation and evaluation of preprocessing approaches. Comparative model training and predictive performance evaluation are identified as subsequent steps in the proposed workflow and are not presented as completed experiments.

## 10. Academic Use

This repository was developed for academic purposes as part of the 6001CMD Machine Learning Individual Assignment.

The dataset is obtained from the UCI Machine Learning Repository. Please refer to the original dataset source for its documentation and citation.
