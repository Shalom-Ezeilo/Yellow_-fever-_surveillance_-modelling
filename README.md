Yellow Fever Surveillance Predictive Modelling

A Machine Learning Project Using Python

1. Project Overview

This project demonstrates the application of Python and machine learning techniques to a simulated yellow fever surveillance dataset. It focuses on data cleaning, exploratory data analysis, feature engineering, classification modelling, and model evaluation.

The project aims to explore whether selected demographic characteristics, clinical symptoms, vaccination information, and other surveillance variables can be used to classify simulated cases according to their recorded laboratory outcome.

Important: This project uses simulated data for educational and portfolio purposes. It does not contain verified real-world yellow fever surveillance records.

2. Objectives

The main objectives are to:

Clean and prepare a large, deliberately messy surveillance dataset.

Identify missing values, duplicate records, inconsistent categories, invalid ages, and date-related errors.

Perform exploratory data analysis to understand the dataset.

Engineer relevant features, including symptom-onset month and quarter.

Train and compare multiple machine learning classification algorithms.

Evaluate model performance using cross-validation and a held-out test set.

Identify influential features and save the selected model for future experimentation.

3. Dataset Description

The project uses a simulated dataset containing approximately 5,000 records and 179 columns.

The dataset was designed to resemble a surveillance line list, with variables covering:

Demographics: age, sex, age group, and location.

Clinical information: fever, jaundice, headache, vomiting, fatigue, muscle pain, and other symptoms.

Vaccination: vaccination status and available vaccination dates.

Surveillance dates: symptom onset, reporting, investigation, admission, outcome, and sample collection.

Laboratory information: latest sample final laboratory result.

Record management: case identifiers, event information, and other surveillance fields.

The exact variables available for analysis depend on the cleaning and feature-selection steps.

4. Data Cleaning and Preparation

Data preparation includes:

Inspecting dataset dimensions, column names, data types, and summary statistics.

Converting date columns to appropriate datetime formats.

Treating invalid date placeholders and inconsistent date values as missing where appropriate.

Identifying implausible ages, including negative ages and extreme values.

Standardising categorical values and checking inconsistent labels.

Examining missing values and duplicate records.

Creating relevant date-based features.

Preparing the target variable and selecting suitable predictor variables.

Missing values are handled within machine learning pipelines to reduce the risk of information leakage during cross-validation.

5. Target Variable and Prediction Task

The proposed target variable is:

Latest sample final laboratory result

For the binary classification analysis:

Positive = 1

Negative = 0

Records with inconclusive or unrecognised laboratory results are excluded from this binary modelling task.

The model therefore attempts to classify positive versus negative laboratory outcomes in the simulated dataset. It does not predict future outbreaks or establish a clinical diagnosis.

6. Machine Learning Models

The project compares several classification algorithms:

Dummy Classifier — baseline performance.

Logistic Regression.

Decision Tree Classifier.

Random Forest Classifier.

Extra Trees Classifier.

Gradient Boosting Classifier.

Support Vector Classifier (SVC).

K-Nearest Neighbours (KNN).

The models use preprocessing pipelines that handle missing numeric and categorical values, scale numerical variables where appropriate, and encode categorical predictors.

7. Model Validation and Evaluation

The modelling workflow uses a stratified training-test split and five-fold stratified cross-validation.

Performance is assessed using:

ROC-AUC: ability to distinguish between the two outcome classes.

Precision: proportion of predicted positive cases that are positive in the reference labels.

Recall (sensitivity): proportion of positive cases correctly identified.

F1-score: balance between precision and recall.

Balanced accuracy: average recall across the two classes.

Confusion matrix: counts of correct and incorrect predictions.

The models are compared using their cross-validation results, followed by evaluation of the selected model on the held-out test set. Feature importance or permutation importance may be used to investigate which predictors contribute most to model performance.

8. Tools and Technologies

Python

Pandas

NumPy

Matplotlib

Scikit-learn

Joblib

Jupyter Notebook

9. Expected Outputs

Depending on the execution of the notebook, the project may produce:

A cleaned dataset.

Exploratory data analysis tables and visualisations.

A comparison table of cross-validation scores.

A confusion matrix and ROC curve.

Feature-importance results.

A saved trained model and associated metadata.

Actual model scores and findings should be reported only after the analysis has been run successfully.

10. Public Health Relevance

Yellow fever surveillance involves integrating demographic, clinical, laboratory, vaccination, and reporting information. This project provides an opportunity to practise data science methods relevant to epidemiological surveillance and to develop skills in preparing structured health data for predictive analysis.

With appropriately collected, validated, and ethically governed real-world data, similar methods could be investigated for supporting surveillance analysis and identifying patterns that warrant further epidemiological review.

11. Limitations and Disclaimer

The dataset is simulated and does not represent actual yellow fever cases.

Performance metrics reflect the simulated data-generating process and cannot establish real-world predictive accuracy.

Simulated relationships between symptoms, vaccination, demographics, and laboratory results may not reflect real epidemiological relationships.

The binary target excludes inconclusive laboratory outcomes.

Potential data leakage must be considered, particularly if predictors contain information recorded after the laboratory result or depend indirectly on the outcome.

The project is for educational and portfolio purposes only. It is not intended for clinical diagnosis, public health decision-making, outbreak forecasting, or operational surveillance.

12. Future Improvements

Potential extensions include:

Testing the workflow on a suitable, ethically accessible real-world dataset.

Investigating class imbalance and decision thresholds.

Performing hyperparameter tuning.

Assessing temporal and geographic generalisability.

Comparing model calibration and interpretability.

Developing a reproducible surveillance modelling pipeline.

Author

Shalom Amara Ezeilo

Veterinary Medicine | Epidemiology | Python and Data Science

GitHub: Shalom-Ezeilo

This project is an educational demonstration of machine learning applied to simulated epidemiological surveillance data.
