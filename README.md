# 20-credit-risk-classification
<br>
The purpose of this exercise is to train and evaluate a model based on loan risk. The dataset evaluates lending activity to build a model that can identify borrower creditworthiness where the focus is to minimize incorrect predictions of risky loans as healthy loans.<br><br>

### Model 01 - Logistic Regression Model
**Balanced Accuracy Score:**  95%<br><br>
- **<ins>Healthy Loans</ins>**<br>
    - **Precision:** Out of all the healthy loans that were predicted, 100% were truly healthy loans.<br>
    - **Recall:** Out of the total healthy loans, 99% were predicted as healthy<br><br>

- **<ins>Risky Loans</ins>**<br>
     - **Precision:** Out of all the risky loans that were predicted, 85% were truly risky loans<br>
     - **Recall:** Out of the total risky loans, 91% were predicted as risky<br><br>


While we see a high Accuracy score for the entire model as well as for Healthy Loan predictions, we are getting a lower Recall accuracy for Risky Loans. Specifically, the model predicted that 56 of the Risky Loans were Healthy Loans. The difference in accuracy could come from an imbalanced dataset that has a disparity between the two categories where Healthy Loan data outnumbers Risky Loan data at roughly 30:1.<br><br>



### Model 02 - Logistic Regression Model with Resampled Training data
**Balanced Accuracy Score:** 99%<br><br>
- **<ins>Healthy Loans</ins>**<br>
    - **Precision:** Out of all the healthy loans that were predicted, 100% were truly healthy loans.<br>
    - **Recall:** Out of total healthy loans, 99% were predicted as healthy<br><br>

- **<ins>Risky Loans</ins>**<br>
    - **Precision:** Out of all the risky loans that were predicted, 84% were truly risky loans<br>
    - **Recall:** Out the total risky loans, 99% were predicted as risky.<br><br>

In order to get a better accuracy on risky loans, the dataset was synthetically balanced using the RandomOverSampler module to resample the data and retrain the model with a 1:1 ratio of Healthy Loan data to Risky Loan data. While the overall accuracy increased from 95% to 99%, the important change occurred with the recall accuracy of risky loan predictions which increased from 91% to 99%. This means that Risky Loans that were predicted as Healthy Loans went down from 56 to 4 which is a significant improvement. The accuracy of Healthy Loan Precision and Recall as well as Risky Loan Precision stayed nearly the same with the resampled model.<br><br>

## Summary
The resampled model seems to perform better as it was able to better predict Risky Loans while still maintaining Healthy Loan prediction accuracy. This will be beneficial in ensuring better success in preventing Risky Loans being predicted as Healthy Loans.

#

Credits
#### Jose A Rodriguez<br>Tutor: Saad Khan<br>
<br>

**Imbalance Dataset(Over Sampling Under Sampling) by Data Science ML Professional**<br>
https://www.youtube.com/watch?v=HtBDg619ozg


### Language(s)/Libraries/Dependencies
Python<br>
numpy <br>
pandas <br>
pathlib<br>

sklearn.metrics
  - balanced_accuracy_score
  - confusion_matrix
  - classification_report

sklearn.model_selection
  - train_test_split

sklearn.linear_model
  - LogisticRegression

imblearn.over_sampling
  - RandomOverSampler


