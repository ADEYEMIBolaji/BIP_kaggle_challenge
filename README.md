# BIP_kaggle_challenge - Machine Learning Models for Predicting Patient Vital Status

This repository contains code for building machine learning models to predict patient vital status based on a dataset. The project involved exploratory data analysis (EDA) and model building. The data cleaning was a collaborative effort by a team of two, while the EDA and machine learning were performed by one individual.

## Exploratory Data Analysis (EDA)

The EDA was an essential step in understanding the dataset before building machine learning models. Here are some key insights and visualizations from the EDA:

### Death Locations Analysis

We began by analyzing the top 5 death locations (excluding specified codes) and their descriptions:

```
Interpretation: Top 5 Death Locations (Excluding Specified Codes) and Their Descriptions

Death Location Code: 1
Description: HOSPITAL
Number of Deaths: 9968

Death Location Code: 4
Description: NURSING HOME
Number of Deaths: 8392

Death Location Code: 2
Description: PRIVATE HOME
Number of Deaths: 3131

Death Location Code: X
Description: UNKNOWN
Number of Deaths: 2011

Death Location Code: 5
Description: OTHER
Number of Deaths: 1003
```

### Diagnosis Year Trend

We visualized the diagnosis year trend as a line chart to understand how the number of diagnoses evolved over the years.

![Diagnosis Year Trend](output_238_0.png)

### Stage and Vital Status Distribution

We analyzed the distribution of stage and vital status, providing insights into the number of patients in different stages and their vital status:

```
Interpretation: Stage and Vital Status Distribution

Stage: 0 - 0
Alive: 141
Dead: 5

Stage: 1 - 1
Alive: 21880
Dead: 2137

Stage: 2 - 2
Alive: 19813
Dead: 2114

Stage: 3 - 3
Alive: 9387
Dead: 5167

Stage: 4 - 4
Alive: 3333
Dead: 12846

Stage: I - Description not available
Alive: 3864
Dead: 2676

Stage: U - UNSTAGEABLE
Alive: 176
Dead: 43
```

### Behaviour Distribution

We also analyzed the distribution of behavior codes:

```
Interpretation: Behaviour Distribution

Behaviour: 3 - MALIGNANT
Count: 83397

Behaviour: 5 - MICRO-INVASIVE
Count: 141

Behaviour: X - UNKNOWN/INAPPLICABLE
Count: 13

Behaviour: 9 - MALIGNANT, UNCERTAIN WHETHER PRIMARY OR METASTATIC
Count: 8
```

## Data Cleaning and Feature Engineering

The data cleaning phase involved handling missing values using domain knowledge. Additionally, encoding categorical variables, scaling numerical features, and creating a feature transformer pipeline were performed.

## Model Building

### Dependencies

Make sure you have the necessary libraries installed:

```shell
pip install category_encoders
```

### Feature Preprocessing

We utilized various data preprocessing techniques, such as target encoding for categorical variables, standard scaling for numerical features, and imputing missing values.

### Model Selection

We experimented with several machine learning classifiers, including:
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Random Forest (RF)

### Hyperparameter Tuning

We conducted hyperparameter tuning using techniques like grid search and randomized search to optimize model performance.

### Model Evaluation

We evaluated model performance using metrics like accuracy, precision, recall, and F1-score. Additionally, we employed techniques like Recursive Feature Elimination (RFE) to select relevant features.

### SHAP (SHapley Additive exPlanations) Analysis

We performed SHAP analysis to interpret and visualize the impact of features on model predictions. This helped us gain insights into the model's decision-making process.

## Conclusion

This project provides a comprehensive overview of machine learning model development for predicting patient vital status. The EDA phase helped us understand the dataset, while the model building phase involved data preprocessing, model selection, hyperparameter tuning, and model evaluation. SHAP analysis enhanced our understanding of feature importance in the model. Feel free to explore the code and adapt it for your own healthcare-related predictive modeling tasks.
