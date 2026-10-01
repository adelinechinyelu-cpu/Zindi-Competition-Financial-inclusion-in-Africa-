# Financial Inclusion in Africa

A machine learning project for the **Zindi Financial Inclusion in Africa** competition.

The goal was to predict whether a person has a bank account based on demographic and socioeconomic information from respondents in Kenya, Rwanda, Tanzania and Uganda.

**Zindi public leaderboard score: 0.1094 MAE**

## About the Dataset

The dataset contains information about respondents, including:

* Country and survey year
* Location type
* Cellphone access
* Household size
* Age and gender
* Education level
* Marital status
* Relationship with household head
* Job type

The target variable is `bank_account`, where `1` means the respondent has a bank account and `0` means they do not.

The data is not included in this repository because it was provided through the Zindi competition.

## What I Did

I started by exploring the data and checking for missing values, duplicates and class imbalance.

I then created additional features, including age groups, household size relative to age, and a country-year feature.

For modelling, I tested:

* Logistic Regression
* Random Forest
* Histogram Gradient Boosting

I used **stratified 5-fold cross-validation** to evaluate the models and used ROC-AUC and MAE to compare their performance.

I also combined the predictions from the three models into an ensemble and used a 0.5 threshold to generate the final predictions.

## Tools

Python, pandas, NumPy, scikit-learn, Jupyter Notebook, Git and GitHub.

## What I Learned

This project gave me more practice with binary classification, feature engineering, imbalanced data, cross-validation, model comparison and ensemble modelling.

It also gave me practical experience taking a machine learning project from exploration through to a competition submission.

## Next Steps

I'd like to experiment with more advanced boosting models, improve the feature engineering and spend more time understanding which factors have the strongest relationship with bank account ownership.

**Competition:** Zindi – Financial Inclusion in Africa
