# Bank Customer Churn Prediction

A machine learning project that predicts whether a bank customer is likely to **churn** using **Logistic Regression** and hyperparameter tuning.

The project uses customer demographic, financial, and account-related information to build a binary classification model that predicts whether a customer will leave the bank.

## Project Overview

Customer churn is an important problem for banks because retaining existing customers can be more cost-effective than acquiring new ones.

This project explores customer data from ABC Multistate Bank and builds a machine learning pipeline to predict customer churn.

The dataset contains features including:

* Credit score
* Country
* Gender
* Age
* Tenure
* Account balance
* Number of bank products
* Credit card ownership
* Active membership status
* Estimated salary

The target variable is `churn`:

* `0` → Customer stayed with the bank
* `1` → Customer left the bank

The `customer_id` column was excluded from model training because it is an identifier rather than a predictive feature.

## Objective

The main objective of this project is to develop a classification model that can identify customers who are more likely to leave the bank.

The project focuses on:

1. Data preprocessing
2. Exploratory data analysis
3. Feature preparation
4. Categorical feature encoding
5. Logistic Regression
6. Feature scaling
7. Hyperparameter tuning
8. Model evaluation
9. Churn prediction

## Machine Learning Approach

### Logistic Regression

The primary model used in this project is **Logistic Regression**, a supervised learning algorithm commonly used for binary classification.

The model estimates the probability that a customer belongs to the churn class.

The workflow can be summarized as:

```text
Raw Customer Data
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Feature Selection
       ↓
Categorical Encoding
       ↓
Feature Scaling
       ↓
Train/Test Split
       ↓
Logistic Regression
       ↓
Hyperparameter Tuning
       ↓
Model Evaluation
       ↓
Customer Churn Prediction
```

## Hyperparameter Tuning

Instead of relying only on the default Logistic Regression configuration, hyperparameter tuning was performed to identify a better-performing configuration.

The tuning process can be used to optimize parameters such as:

* `C`
* `solver`
* `penalty`

The `C` parameter controls the strength of regularization. Testing different values allows the model to find a suitable balance between fitting the training data and generalizing to unseen customers.

## Dataset

The project uses the **Bank Customer Churn Dataset** available on Kaggle.

The dataset contains customer information from an ABC Multistate Bank and was specifically created for predicting customer churn.

### Features

| Feature            | Description                                          |
| ------------------ | ---------------------------------------------------- |
| `customer_id`      | Customer/account identifier                          |
| `credit_score`     | Customer's credit score                              |
| `country`          | Country of residence                                 |
| `gender`           | Customer gender                                      |
| `age`              | Customer age                                         |
| `tenure`           | Number of years with the bank                        |
| `balance`          | Account balance                                      |
| `products_number`  | Number of bank products                              |
| `credit_card`      | Whether the customer has a credit card               |
| `active_member`    | Whether the customer is an active bank member        |
| `estimated_salary` | Estimated customer salary                            |
| `churn`            | Target variable indicating whether the customer left |

The dataset documentation identifies `customer_id` as unused and `churn` as the prediction target.

## Evaluation

The model can be evaluated using classification metrics such as:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC-AUC

For a churn prediction problem, looking beyond accuracy is useful because the model should also identify customers who are actually at risk of leaving.

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* Logistic Regression
* Hyperparameter tuning

## Project Structure

```text
bank-customer-churn-prediction/
│
├── data/
│   └── Bank Customer Churn Prediction.csv
│
├── notebooks/
│   └── bank_churn_prediction.ipynb
│
├── src/
│   └── model.py
│
├── README.md
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/bank-customer-churn-prediction.git
cd bank-customer-churn-prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
notebooks/bank_churn_prediction.ipynb
```

Run the cells sequentially to reproduce the preprocessing, model training, hyperparameter tuning, and evaluation.

## Key Learning Outcomes

Through this project, I worked with:

* Binary classification
* Logistic Regression
* Categorical feature encoding
* Feature scaling
* Train/test splitting
* Hyperparameter tuning
* Model evaluation
* Classification metrics
* Interpreting customer churn predictions

## Future Improvements

Possible extensions to the project include:

* Comparing Logistic Regression with Random Forest, XGBoost, and other classifiers
* Handling class imbalance using techniques such as class weighting or resampling
* Optimizing the classification threshold based on business requirements
* Deploying the trained model as a web application
* Building an interactive customer churn prediction dashboard
* Adding model explainability using SHAP

## Dataset Source

Dataset: **Bank Customer Churn Dataset**

Source: Kaggle

The dataset is described as a classification dataset for predicting customer churn in an ABC Multistate Bank.

## Disclaimer

This project is intended for educational and machine learning practice purposes. Predictions should not be treated as definitive evidence that an individual customer will leave a bank.
