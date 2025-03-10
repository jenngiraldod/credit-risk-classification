# credit-risk-classification
The purpose of this analysis is to develop a machine learning model to assess credit risk by predicting whether a loan is healthy (0) or high-risk (1). The goal is to assist financial institutions in making informed lending decisions based on borrower risk.

Financial Information and Prediction Objective:

The dataset contains financial attributes of borrowers, including:

loan_size

interest_rate

borrower_income

debt_to_income

num_of_accounts

derogatory_marks

total_debt

loan_status (target variable: 0 = healthy loan, 1 = high-risk loan)

The objective is to predict loan_status, identifying loans that are more likely to default.

An initial analysis of the target variable distribution (value_counts) revealed a class imbalance:

Healthy loans (0): 56,271

High-risk loans (1): 1,881

Stages of the Machine Learning Process:

Data Preprocessing:

Extracted features (X) and target variable (y).

Split the dataset into training (75%) and testing (25%) sets using train_test_split.

Model Selection:

Chose Logistic Regression as the primary classification model.

Addressed class imbalance using Random Over-Sampling (ROS) with RandomOverSampler.

Model Training:

Trained the logistic regression model on the resampled training dataset.

Model Evaluation:

Generated predictions using predict().

Evaluated performance using accuracy, precision, recall, and F1-score.e
