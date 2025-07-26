# Credit-Card-Fraud-Detection_Finished

This repository contains a complete end-to-end machine learning project focused on detecting fraudulent credit card transactions. The project was originally developed and tested on Kaggle, and has been adapted for GitHub with dataset integration via Google Drive due to size limitations.

---

### A. Objective
The objective of this notebook is to build and evaluate a classification model to detect fraudulent credit card transactions from a highly imbalanced dataset. The final goal is to optimize the recall and precision metrics for fraud detection using various techniques like SMOTE for balancing the TRAIN SET and Optuna for hyperparameter tuning.

---

### B. Dataset Information
- The dataset contains credit card transactions from European cardholders in September 2013.
- Features are anonymized due to confidentiality (V1–V28), with only `Time`, `Amount`, and `Class` being interpretable.
- Class `1` represents fraud, Class `0` represents legitimate transactions.
- Due to GitHub's file size limit (> 100 MB), the dataset is imported from my personal Google Drive using `gdown`.
- The link to the original dataset on Kaggle is `https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud`.

---

### C. Dataset Access (Google Drive)
- To load the dataset, the following code is used:

i. **_Import gdown library_**

import gdown

ii. **_Download creditcard.csv from Google Drive_**

file_id = '1OoO2imBU1Tl8g76geHdk12B3tNqe5GYu'

download_url = f'https://drive.google.com/uc?id={file_id}'

output = 'creditcard.csv'

gdown.download(download_url, output, quiet=False)

---

### D. Project Workflow
1. Importing required libraries.
- Please make sure the following libraries are installed. If not, you may uncomment and run:

a. !pip install -U scikit-learn

b. !pip install optuna

c. !pip install xgboost

d. !pip install imbalanced-learn

2. Data loading & exploration.

- Load CSV, check for missing values, outliers, imbalance.

3. Data cleaning & preprocessing.

- Handle duplicated rows selectively from legitimate transactions only.

- Standardize `Amount` and `Time` variables.

- Apply `SMOTE` to address imbalance on TRAIN SET.

4. Model training.

- Train models using:

- RandomForest + SMOTE (baseline model).

- RandomForest + SMOTE + Optuna.

- XGBoost + SMOTE.

- XGBoost + SMOTE + Optuna.

5. Model evaluation.

Evaluate each model using:

a. Confusion Matrix.

b. Precision, Recall, and F1.

c. ROC-AUC and PR-AUC.

6. Model comparison & selection.

- Use grouped bar charts and summary metrics to compare.

- Final model: `XGB + SMOTE + Optuna`.

7. Model saving and inference.

- Save model with joblib.

- Run predictions on a synthetic random dataset.

8. Conclusion.

The final model achieved strong performance and balanced metrics, especially in identifying fraudulent transactions from a heavily imbalanced dataset. Optuna improved the model's ability to detect fraud while minimizing false positives.

---

### E. Environment

This notebook was developed and tested on **Kaggle Notebook**, for environments where dependencies are not pre-installed, use the optional `!pip install` commands mentioned on point D.

---

## AUTHOR

**Yohanes Kurniawan Hertanto**

An aspiring Data Analyst with interest in Machine Learning

https://www.kaggle.com/yohaneskhyekaha
