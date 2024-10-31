# Time Series Classification Project

## Project Description
In this project, you are required to solve a time series classification problem into two classes. The solution includes the full process from data analysis (EDA) to model training and making predictions on the test set. The target metric for the task is ROC AUC.

### The data includes:

train.parquet: Training set containing a unique object identifier (id), an array with observation dates (dates), an array with observations (values), and the class label (label).
test.parquet: Test set containing id, dates, values.
sample_submission.csv: Sample solution containing id and the prediction (score).
Solution Requirements
The solution must include a single submission.csv file with predictions on the test set. The format of submission.csv must strictly follow the format of the sample_submission.csv file.
The solution must include a script to generate the submission.csv file, which reads the features, the trained model, and makes predictions.
The code for model training and feature extraction must be reproducible and well-organized.
A ReadMe file describing the files in the solution and instructions on how to run it.
Installation and Preparation
Before running the script, ensure that all necessary libraries are installed:

pip install pyarrow
pip install xgboost
Script Contents
Data Loading
Downloading data from GitHub and loading it into variables train_data, test_data, and sample_submission.
Exploratory Data Analysis (EDA)
Analyzing the data structure and its main characteristics.
Checking feature correlations to identify potential multicollinearity issues.
Data Preprocessing
Extracting statistical features from the dates and values columns.
Scaling numerical features using StandardScaler.
Model Training and Cross-Validation
Utilizing two models: XGBoost and Logistic Regression.
Performing 5-fold cross-validation and evaluating performance using the ROC AUC metric.
Prediction and Generating submission.csv
Generating predictions for the test set and saving them to the submission.csv file.
Execution
To run the project, follow these steps:

## Clone the repository from GitHub:
git clone https://github.com/Mechanic17/time_series_classification.git
Launch Jupyter Notebook and open the file time_series_classification.ipynb.
Execute all cells to train the model and generate the submission.csv file.
After successful execution of the script, the submission.csv file will be created and available for download.
Hypotheses and Their Testing
Hypothesis 1: The feature values_mean strongly correlates with the target variable.
Hypothesis 2: The variance of values_std affects the probability of belonging to class 1.
Correlations have been calculated and are displayed in the script for further analysis.

## Data Usage
The open datasets used in the solution are located in the GitHub repository and are available for download.
