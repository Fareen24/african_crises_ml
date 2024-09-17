

# Systemic Crisis Prediction in Africa

## Project Overview

This project aims to predict the likelihood of a systemic crisis emergence in 13 African countries using a dataset that includes information on various types of crises (Banking, Debt, Financial, Inflation, Systemic) from 1860 to 2014. The dataset includes indicators such as annual inflation rates and other financial metrics.

## Dataset

- **Description**: The dataset focuses on crises occurrences across different countries, including Algeria, Angola, Central African Republic, Ivory Coast, Egypt, Kenya, Mauritius, Morocco, Nigeria, South Africa, Tunisia, Zambia, and Zimbabwe.
- **Link**: https://www.kaggle.com/datasets/chirin/africa-economic-banking-and-systemic-crisis-data

## Instructions

### 1. Import Data and Basic Exploration

- **Data Import**: Load the dataset using pandas.
- **Basic Exploration**: Perform an initial exploration to understand the dataset structure and contents.

### 2. Display General Information

- **Dataset Information**: Use pandas functions to display general information about the dataset (e.g., column names, data types, missing values).

### 3. Create Pandas Profiling Report

- **Generate Report**: Use `pandas_profiling.ProfileReport` to create a comprehensive report that provides insights into the dataset, including statistics and data distributions.

```python
import pandas as pd
from pandas_profiling import ProfileReport

# Load dataset
df = pd.read_csv('path_to_dataset.csv')

# Generate and save profile report
profile = ProfileReport(df, title="Systemic Crisis Profiling Report", explorative=True)
profile.to_file("systemic_crisis_profiling_report.html")
```

### 4. Handle Missing and Corrupted Values

- **Missing Values**: Identify and handle missing values through imputation or removal. There were no missing values.


### 5. Encode Categorical Features

- **Encoding**: Convert categorical features into numerical values using label encoding.

### 6. Feature and Target Selection

- **Feature Selection**: Identify and select relevant features for the model from the correlation matrix in the ydata profile report.
- **Target Variable**: Define the target variable (`systemic_crisis`).

### 7. Split Dataset

- **Training and Testing Split**: Split the dataset into training and testing sets using `train_test_split`.

`
### 8. Model Training and Evaluation

- **Algorithm**: Used Logistic Regression to train the model on the training set.
- **SMOTE**: Applied  SMOTE to address class imbalance in the target variable.
- **Evaluation**: Assess the model performance using relevant metrics like accuracy, precision, recall, and F1-score, and confusion matrix.




