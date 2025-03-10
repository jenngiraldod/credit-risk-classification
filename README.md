# credit-risk-classification

## Overview of the Analysis
The purpose of this analysis is to develop a machine learning model to assess credit risk by predicting whether a loan is healthy (0) or high-risk (1). The goal is to assist financial institutions in making informed lending decisions based on borrower risk.

**Financial Information and Prediction Objective:**
The dataset contains financial attributes of borrowers, including:
    - loan_size

    - interest_rate

    - borrower_income

    - debt_to_income

    - num_of_accounts

    - derogatory_marks

    - total_debt

    - loan_status (target variable: 0 = healthy loan, 1 = high-risk loan)

- he objective is to predict loan_status, identifying loans that are more likely to default.

- An initial analysis of the target variable distribution (value_counts) revealed a class imbalance:

    - **Healthy loans (0):** 56,271

    - **High-risk loans (1):** 1,881
 
### Stages of the Machine Learning Process:
**1. Data Preprocessing:**

    - Extracted features (X) and target variable (y).

    - Split the dataset into training (75%) and testing (25%) sets using train_test_split.

**2. Model Selection:**

    - Chose Logistic Regression as the primary classification model.

    - Addressed class imbalance using Random Over-Sampling (ROS) with RandomOverSampler.

**3. Model Training:**

    - Trained the logistic regression model on the resampled training dataset.

**4. Model Evaluation:**

    - Generated predictions using predict().

    - Evaluated performance using accuracy, precision, recall, and F1-score.

### Results
**Machine Learning Model 1: Logistic Regression**

**- Accuracy: 99%**

**- Precision:**

    - Healthy Loan (0): 1.00

    - High-Risk Loan (1): 0.84

**- Recall:**

    - Healthy Loan (0): 0.99

    - High-Risk Loan (1): 0.99

**- F1-score:**

    - Healthy Loan (0): 1.00

    - High-Risk Loan (1): 0.91

**Key Observations:**

- The model achieves high accuracy (99%), meaning it correctly classifies most loans.

- Healthy loans (0) are predicted with near-perfect precision and recall (1.00 and 0.99, respectively).

- High-risk loans (1) have lower precision (0.84), meaning some healthy loans are misclassified as high-risk.

- The high recall (0.99) for high-risk loans ensures that nearly all risky loans are identified.

### Summary & Recommendation

The logistic regression model demonstrates strong predictive performance, particularly in identifying high-risk loans with high recall (0.99). This ensures that most high-risk loans are correctly classified. However, the lower precision for high-risk loans (0.84) means that some healthy loans may be misclassified as risky, which could lead to unnecessary caution in lending decisions.

**Which Model Performs Best?**

- Since only one model (Logistic Regression) was used, its performance is evaluated based on the balance between precision and recall.

- The model is effective at minimizing false negatives (high-risk loans classified as healthy), which is crucial in credit risk assessment.

**Does Performance Depend on the Problem We Are Solving?**

- Yes, in credit risk analysis, it is more important to correctly identify high-risk loans (1) rather than healthy loans (0) to prevent financial losses.

- A high recall for high-risk loans (0.99) ensures minimal false negatives, which is desirable for risk-averse financial institutions.

- However, if reducing false positives (incorrectly identifying a healthy loan as high-risk) is critical, alternative models such as Random Forest or XGBoost could be explored.

**Recommendation:**

- This model is suitable for an initial credit risk assessment due to its high recall and accuracy.

- If reducing false positives is essential, fine-tuning the model, adjusting the decision threshold, or using ensemble methods may provide better results.

- A comparative analysis with additional models could further enhance decision-making in credit risk evaluation.

**Overall, this model serves as a strong foundation for credit risk assessment but may require refinements based on business objectives and risk tolerance.**







    