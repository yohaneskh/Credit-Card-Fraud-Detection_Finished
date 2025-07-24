# Credit-Card-Fraud-Detection_Finished

This repository contains a complete end-to-end machine learning project focused on detecting fraudulent credit card transactions. The project was originally developed and tested on Kaggle, and has been adapted for GitHub with dataset integration via Google Drive due to size limitations.

### A. Objective
The objective of this notebook is to build and evaluate a classification model to detect fraudulent credit card transactions from a highly imbalanced dataset. The final goal is to optimize the recall and precision metrics for fraud detection using various techniques like SMOTE for balancing the TRAIN SET and Optuna for hyperparameter tuning.

### B. Dataset Information
- The dataset contains credit card transactions from European cardholders in September 2013.
- Features are anonymized due to confidentiality (V1–V28), with only `Time`, `Amount`, and `Class` being interpretable.
- Class `1` represents fraud, Class `0` represents legitimate transactions.
- Due to GitHub's file size limit (> 100 MB), the dataset is imported from my personal Google Drive using `gdown`.
- The link to the original dataset on Kaggle is `https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud`.

### C. Dataset Access (Google Drive)
- To load the dataset, the following code is used:

i. **_Import gdown library_**

import gdown

ii. **_Download creditcard.csv from Google Drive_**

file_id = '1OoO2imBU1Tl8g76geHdk12B3tNqe5GYu'

download_url = f'https://drive.google.com/uc?id={file_id}'

output = 'creditcard.csv'

gdown.download(download_url, output, quiet=False)

### D. Project Workflow
1. Importing required libraries.
- Please make sure the following libraries are installed. If not, you may uncomment and run:

a. !pip install -U scikit-learn

b. !pip install optuna

c. !pip install xgboost

d. !pip install imbalanced-learn

2. Data loading & exploration.

- Load CSV, check for missing values, outliers, imbalance.

3. 
