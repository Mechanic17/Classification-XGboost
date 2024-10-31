Time Series Classification Project
Project Description
In this project, you are required to solve a time series classification problem with two classes. The solution encompasses the full process from data analysis (EDA) to model training and prediction on the test dataset. The target metric for this task is ROC AUC.

The data includes:

train.parquet: Training dataset containing a unique object identifier (id), an array of observation dates (dates), an array of observations (values), and the class label (label).
test.parquet: Test dataset containing id, dates, values.
sample_submission.csv: Sample solution containing id and prediction (score).
Solution Requirements
The solution must include a single submission.csv file with predictions on the test dataset. The format of submission.csv must strictly follow the format of sample_submission.csv.
The solution should contain a script for generating the submission.csv file, which reads features, the trained model, and makes predictions.
The code for model training and feature engineering must be reproducible and well-organized.
A README file describing the files in the solution and instructions for running the code.
Installation and Preparation
Before running the script, ensure you have all the necessary libraries installed:

sh
Копировать код
pip install pyarrow
pip install xgboost
Script Content
Data Loading
Downloading data from GitHub and loading it into variables train_data, test_data, and sample_submission.
Exploratory Data Analysis (EDA)
Analyzing the data structure and main characteristics.
Checking feature correlations to identify potential multicollinearity issues.
Data Preprocessing
Extracting statistical features from the dates and values columns.
Scaling numerical features using StandardScaler.
Model Training and Cross-Validation
Utilizing two models: XGBoost and Logistic Regression.
Performing 5-fold cross-validation and evaluating performance using the ROC AUC metric.
Prediction and Submission File Generation
Generating predictions for the test dataset and saving them to the submission.csv file.
Execution
To run the project, follow these steps:

Clone the repository from GitHub:
sh
Копировать код
git clone https://github.com/Mechanic17/time_series_classification.git
Launch Jupyter Notebook and open the file time_series_classification.ipynb.
Execute all the cells to train the model and generate the submission.csv file.
After the script runs successfully, the submission.csv file will be created and available for download.
Hypotheses and Testing
Hypothesis 1: The feature values_mean has a strong correlation with the target variable.
Hypothesis 2: The dispersion of values values_std affects the probability of belonging to class 1.
Correlations have been calculated and are displayed in the script for further analysis.

Data Usage
The datasets with open data used in the solution are available in the GitHub repository for download.
