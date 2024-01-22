# credit-risk-classification
## Supervised Machine Learning

### Overview
This repository provides a comprehensive guide on training and evaluating a machine learning model designed to assess loan risk. The goal is to utilize various techniques to analyze a dataset of historical lending activities obtained from a peer-to-peer lending services company. By leveraging this dataset, we aim to build a robust model capable of accurately identifying the creditworthiness of borrowers.

### Split the Data into Training and Testing Sets

1. Read and Prepare Data:
- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
- Create the labels set (y) from the “loan_status” column, where 0 indicates a healthy loan and 1 indicates a high-risk loan.
- Create the features (X) DataFrame from the remaining columns.
2. Split Data:
- Use the train_test_split function to split the data into training and testing datasets. This ensures that the model is trained on a subset of the data and evaluated on unseen data.
- Check the balance of target value  (75036, 2500).

### Create a Logistic Regression Model with the Original Data

1. Logistic Regression:
- Fit a logistic regression model using the training data (X_train and y_train).
- Save predictions for the testing data labels using the testing feature data (X_test) and the fitted model.
2. Model Evaluation:
- Generate a confusion matrix to visualize true positives, true negatives, false positives, and false negatives.
- Print the classification report, including precision, recall, and F1-score.
3. Analysis:
Evaluate how well the logistic regression model predicts both healthy loans (0) and high-risk loans (1).

**Results**
Accuracy Score: 94%
Precision Score: 94%
Recall Score: 94%

### Create a Logistics Regression Model using Resampled Training Data

1. Random Over Sampler Module:
- Instantiate the random oversampler model.
- Fit a random oversampler model with training data (X_train and y_train).
- Count the distinct value of resampled label data (y_resampled).
- Check the balance of target value  (56277, 56277).

2. Logistic Regression:
- Fit a logistic regression model using the resampled training data (X_resampled and y_resampled).
- Save predictions for the testing data labels using the testing feature data (X_test) and the fitted model.
3. Model Evaluation:
- Generate a confusion matrix to visualize true positives, true negatives, false positives, and false negatives.
- Print the classification report, including precision, recall, and F1-score.
4. Analysis:
Evaluate how well the logistic regression model predicts both healthy loans (0) and high-risk loans (1).

**Results**
Accuracy Score: 99.59%
Precision Score: 94%
Recall Score: 100%

### Summary
The resampling instance help in recreating the imbalanced data further contributing to the accuracy of the model.
The machine learning model exhibits promising results in predicting credit risk. The accuracy, precision, and recall scores provide valuable insights into the model's performance. This information is crucial for decision-making in the lending process.



### Recommendation

Based on the analysis, we recommend the utilization of the logistic regression model for assessing loan risk. The model demonstrates a good balance between precision and recall, making it suitable for identifying both healthy and high-risk loans. However, continuous monitoring and periodic model updates are recommended to ensure its efficacy in dynamic lending environments.
