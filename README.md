# Time Series Classification Project ## Project Description This project is to solve the problem of classifying time series into two classes. The solution involves the complete process from data analysis (EDA) to model training and prediction for a test sample. The target metric for the task is ROC AUC. Data include: - train.parquet: a training sample containing a unique object identifier (id), an array with observation dates (dates), an array with observations (values), and a classlabel (label). - test.parquet: test sample containing id, dates, values. - sample_submission.csv: sample solution containing id and prediction (score). ## Solution requirements Just translate into English and that's it - Solution must contain one submission.csv file with predictions on the test sample. The format of submission.csv should strictly repeat the format of the sample_submission.csv file . - The solution must contain a script to generate the submission.csv file that reads the features, trains the model and makes predictions. - The model training code and feature assembly code should be reproducible and accurate. - ReadMe file describing the files in the solution and instructions on how to run it. ## Installation and Preparation Before running the script, make sure you have all the necessary libraries installed: 
sh
pip install pyarrow
pip install xgboost

## Script contents

1. **Data Download**
   - Downloading data from GitHub and loading it into variables train_data, test_data and sample_submission. 2. **Enalyze Data (EDA)** - Analyze data structure

Translated with DeepL.com (free version)
Data Usage
The datasets with open data used in the solution are available in the GitHub repository for download.
