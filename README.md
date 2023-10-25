# Bone Marrow Disease Classification

This project is focused on building a classification model to predict the survival status of patients with bone marrow disease. The dataset used in this project is 'bone-marrow.arff,' and it includes various features related to patients' medical conditions and outcomes.

## Data Loading and Exploration

The initial step involves loading the dataset from an ARFF file and exploring its content. Data preprocessing is carried out to ensure that all columns are in numeric format, and binary columns are encoded as 0 and 1. A thorough examination of the dataset is performed, including checking for unique values in each column.

## Data Preparation

The target variable, 'survival_status,' is defined as 'y,' while the features, excluding 'survival_time' and 'survival_status,' are stored in 'X.' The features are categorized into numeric and categorical columns based on the number of unique values. Columns with missing values are identified.

A train-test split is executed to create two datasets for model training and evaluation.

## Creating Pipelines

To streamline the data preprocessing and model building process, pipelines are established. These pipelines include:

1. **Categorical Preprocessing Pipeline:** This pipeline fills in missing values using the mode and performs one-hot encoding on categorical features.

2. **Numerical Preprocessing Pipeline:** This pipeline fills in missing values using the mean and standardizes numeric features.

A column transformer is created to preprocess numerical and categorical features separately. The main pipeline encompasses the preprocessing, Principal Component Analysis (PCA), and a logistic regression model.

The pipeline is fitted to the training data and evaluated on the test data.

## Hyperparameter Tuning

Hyperparameter tuning aims to optimize the classification model. A search space of hyperparameters is defined, including different values for the regularization parameter 'C' and the number of principal components in PCA. A grid search is conducted to find the best hyperparameters and pipeline configuration.

The best model obtained from the grid search is stored, and its attributes, including the selected hyperparameters and the number of components chosen in the PCA step, are printed. The final accuracy score of the best model on the test set is also displayed.

This project serves as a comprehensive example of data preprocessing, pipeline creation, hyperparameter tuning, and model evaluation for a classification task. It showcases how to build and optimize a machine learning model to predict patient outcomes in the context of bone marrow diseases.