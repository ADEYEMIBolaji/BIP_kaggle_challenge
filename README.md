# BIP_kaggle_challenge
## Predicting Patient Vital Status with Machine Learning

This repository contains the code and resources for building machine learning models to predict patient vital status based on various features. This project was a group effort, with data cleaning performed by a team of two, while the exploratory data analysis (EDA) and machine learning were conducted by me.

### Exploratory Data Analysis (EDA)

#### Data Cleaning

The initial phase of the project involved data cleaning, which was handled by a team of two individuals. This process included handling missing values, encoding categorical variables, scaling numerical features, and creating a feature transformer pipeline. The main data preprocessing steps are as follows:

##### Missing Value Imputation

We used the `SimpleImputer` from scikit-learn to impute missing values in numerical features with the median.

##### Encoding Categorical Variables

Categorical columns were one-hot encoded using the `OneHotEncoder`. We also addressed infrequently occurring categories by setting `handle_unknown='infrequent_if_exist'` and filtering categories with a minimum frequency of 0.01.

##### Scaling Numerical Features

Numerical features were standardized using the `StandardScaler` to achieve zero mean and unit variance.

##### Feature Transformation Pipeline

All preprocessing steps were combined into a `ColumnTransformer` to handle categorical and numerical features separately. This transformer was applied to both the training and test data.

#### Exploratory Data Analysis (EDA)

Following data cleaning, I conducted an extensive EDA to gain insights into the dataset. The EDA included the following analyses:

1. **Top 5 Death Locations**: We identified and described the top 5 death locations (excluding specified codes) and their respective death counts.

2. **Diagnosis Year Trend**: A line chart was used to visualize the trend in diagnosis years, providing an understanding of how the data was distributed over time.

3. **Stage and Vital Status Distribution**: We analyzed the distribution of vital status across different cancer stages, providing valuable insights into the data.

4. **Behaviour Distribution**: The distribution of cancer behavior codes was explored, and the occurrences of each behavior code were detailed.

### Machine Learning Models

With the data cleaned and insights gained from the EDA, I proceeded to build machine learning models for predicting patient vital status. The following models were considered:

- Support Vector Classifier (SVC)
- K-Nearest Neighbors Classifier (KNN)
- Random Forest Classifier (RF)

For each model, I created a pipeline that included the preprocessing steps and the model estimator. Grid search was used to find the best hyperparameters for the models.

### Feature Selection

Feature selection was performed using Recursive Feature Elimination (RFE) with linear regression as the estimator. This step helped identify the most important features for prediction.

### Model Evaluation and Prediction

I evaluated the models using various metrics such as accuracy, precision, recall, and F1-score. The final predictions were saved in CSV files (`svm_pred.csv` for SVC and `rf_pred.csv` for RF).

For a more detailed understanding of the code implementation and results, please refer to the Jupyter Notebook provided in this repository.
