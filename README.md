# Machine Learning Assignment 2

## a. Problem statement
Implement five classification algorithms, evaluate them with six metrics, and create an interactive Streamlit application.

## b. Dataset description
Wisconsin Diagnostic Breast Cancer dataset, loaded through scikit-learn.
- 569 instances
- 30 numeric input features
- Binary target: 0 = malignant, 1 = benign
- Dataset information: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic

## c. GitHub Repository Link
Add your own GitHub repository URL after uploading the project.

## d. Models and evaluation
Actual results are in metrics.csv and metrics.json. Write your own observations based on the results.

| Model | Accuracy | AUC | Precision | Recall | F1 | MCC |
|---|---:|---:|---:|---:|---:|---:|
| Logistic Regression | 0.9860 | 0.9977 | 0.9889 | 0.9889 | 0.9889 | 0.9700 |\n| K-Nearest Neighbors | 0.9790 | 0.9845 | 0.9677 | 1.0000 | 0.9836 | 0.9555 |\n| Support Vector Machine | 0.9790 | 0.9969 | 0.9888 | 0.9778 | 0.9832 | 0.9553 |\n| Gaussian Naive Bayes | 0.9371 | 0.9878 | 0.9355 | 0.9667 | 0.9508 | 0.8644 |\n| Decision Tree | 0.9371 | 0.9186 | 0.9551 | 0.9444 | 0.9497 | 0.8657 |\n
## Files
dataset.csv, test_data.csv, metrics.csv, metrics.json, models/, app.py, requirements.txt.

## Run Streamlit
Install requirements and run: streamlit run app.py. The app loads saved models and does not retrain them.
