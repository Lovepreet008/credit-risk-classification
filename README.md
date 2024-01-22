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

### Create a Logistic Regression Model with the Original Data

1. Logistic Regression:
- Fit a logistic regression model using the training data (X_train and y_train).
- Save predictions for the testing data labels using the testing feature data (X_test) and the fitted model.
2. Model Evaluation:
- Generate a confusion matrix to visualize true positives, true negatives, false positives, and false negatives.
- Print the classification report, including precision, recall, and F1-score.
3. Analysis:
Evaluate how well the logistic regression model predicts both healthy loans (0) and high-risk loans (1).


