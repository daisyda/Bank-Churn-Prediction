# Bank-Churn-Prediction
Certainly! Let's create an updated description for your project based on the two code snippets you provided:

---

# Bank Customer Churn Prediction using Neural Networks and Feature Importance

## Introduction
Customer churn prediction is crucial for businesses, especially in the banking industry. Identifying customers who are likely to leave can help banks take proactive measures to retain them. In this project, we explore two approaches: using **Artificial Neural Networks (ANNs)** and analyzing **feature importance** with a Random Forest classifier.

## Dataset
We use a dataset containing customer information from a bank. The features include age, estimated salary, credit score, account balance, and the number of bank products used. The target variable is whether the customer has churned (1) or not (0). You can find a similar dataset on Kaggle: [Bank Customer Churn Dataset](https://www.kaggle.com/datasets/shubhammeshram579/bank-customer-churn-prediction).

## Approach 1: Neural Networks
### Data Preprocessing
- We load the dataset and drop unnecessary columns (`RowNumber`, `CustomerId`, and `Surname`).
- The selected features are `Age`, `EstimatedSalary`, `CreditScore`, `Balance`, and `NumOfProducts`.
- Data is split into training and testing sets, and features are standardized.

### Neural Network Architecture
- We create an ANN model using TensorFlow:
  - Input layer with 128 neurons and ReLU activation.
  - Dropout layer (30% dropout rate) to prevent overfitting.
  - Hidden layer with 64 neurons and ReLU activation.
  - Output layer with a sigmoid activation (for binary classification) and L2 regularization.

### Training and Evaluation
- The model is trained using the training data.
- Learning rate scheduling is applied to the Adam optimizer.
- Model performance is evaluated on the test set using accuracy, precision, and recall.

## Approach 2: Feature Importance
### Data Preprocessing
- We drop unnecessary columns (`RowNumber`, `CustomerId`, and `Surname`).
- Categorical variables (`Geography` and `Gender`) are mapped to numerical values.
- Rows with missing values are removed.

### Random Forest Classifier
- We train a Random Forest classifier on the preprocessed data.
- Feature importances are calculated.
- The top features are identified.

## Conclusion
By combining neural networks and feature importance analysis, we aim to build an effective churn prediction model for the banking industry. Feel free to explore further improvements, hyperparameter tuning, and additional feature engineering techniques.

---

