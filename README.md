# Financial Inclusion in Africa: Bank Account Ownership Prediction

A machine learning project built for the **Zindi Financial Inclusion in Africa** challenge.

The goal was to predict whether individuals in **Kenya, Rwanda, Tanzania and Uganda** have or use a bank account using demographic and socioeconomic survey data.

**Zindi Public Leaderboard MAE: 0.1094**

## Problem

This is a binary classification problem where the target variable is:

`bank_account`

* `1` = Has a bank account
* `0` = Does not have a bank account

The dataset contains information about country, year, location, cellphone access, household size, age, gender, education, marital status, relationship to household head and job type.

The target was imbalanced, with approximately **14% positive cases**.

## Approach

The project followed these steps:

1. Explored the dataset and checked for missing values, duplicates and class imbalance.
2. Created additional features including age groups, household-size-to-age ratio and country-year combinations.
3. One-hot encoded categorical variables and standardised numerical features where required.
4. Trained three classification models:

   * Logistic Regression
   * Random Forest
   * Histogram Gradient Boosting
5. Used **stratified 5-fold cross-validation** for model evaluation.
6. Generated out-of-fold predictions and compared models using ROC-AUC and MAE.
7. Averaged model probabilities to create an ensemble.
8. Converted probabilities to 0/1 predictions using a 0.5 threshold for the final submission.

## Results

| Model                       |   ROC-AUC |        MAE |
| --------------------------- | --------: | ---------: |
| Logistic Regression         |     0.852 |     0.1155 |
| Random Forest               |     0.862 |     0.1121 |
| Histogram Gradient Boosting |     0.864 |     0.1115 |
| **Ensemble**                | **0.865** | **~0.112** |
| Baseline                    |         — |      0.141 |

**Final Zindi leaderboard score: 0.1094 MAE**

## Project Files

```text
Financial-inclusion-in-Africa/
├── Financial_inclusion_in_Africa.ipynb
├── submission (3).csv
└── README.md
```

The notebook contains the complete data exploration, preprocessing, feature engineering, modelling, validation and prediction workflow.

The original competition dataset is not included in this repository.

## Tools

* Python
* pandas
* NumPy
* scikit-learn
* Jupyter Notebook
* Git & GitHub
* Zindi

## Key Learning Outcomes

This project strengthened my practical experience with:

* Binary classification
* Imbalanced datasets
* Feature engineering
* Machine learning pipelines
* Stratified cross-validation
* Out-of-fold predictions
* Model evaluation
* Ensemble modelling
* Machine learning competition workflows

## Future Improvements

* Hyperparameter optimisation
* Additional gradient boosting models
* More feature engineering
* Model explainability and feature importance
* Country-specific analysis

## Acknowledgements

Dataset and competition provided by **Zindi**.
