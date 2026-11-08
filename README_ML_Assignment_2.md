# Machine Learning Assignment 2

## a. Problem statement

Implement five classification algorithms on one public classification dataset, evaluate each model using six standard classification metrics, and create an interactive Streamlit application that loads saved models and evaluates an uploaded labelled test CSV without retraining.

## b. Dataset description

**Dataset:** Wisconsin Diagnostic Breast Cancer dataset, loaded through scikit-learn.

- 569 instances
- 30 numeric input features
- Binary target: `0 = malignant`, `1 = benign`
- Public dataset reference: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic

This dataset satisfies the assignment minimum of 12 features and 500 instances.

## c. GitHub Repository Link

https://github.com/sneha-1201/ML--Assignment---2-

## d. Models used and evaluation

### Comparison table

| ML Model Name | Accuracy | AUC | Precision | Recall | F1 | MCC |
|---|---:|---:|---:|---:|---:|---:|
| Logistic Regression | 0.9860 | 0.9977 | 0.9889 | 0.9889 | 0.9889 | 0.9700 |
| Decision Tree | 0.9371 | 0.9186 | 0.9551 | 0.9444 | 0.9497 | 0.8657 |
| K-Nearest Neighbors | 0.9790 | 0.9845 | 0.9677 | 1.0000 | 0.9836 | 0.9555 |
| Gaussian Naive Bayes | 0.9371 | 0.9878 | 0.9355 | 0.9667 | 0.9508 | 0.8644 |
| Support Vector Machine | 0.9790 | 0.9969 | 0.9888 | 0.9778 | 0.9832 | 0.9553 |

### Observations on model performance

- **Logistic Regression:** Best overall performance. It achieved the highest accuracy (0.9860), precision (0.9889), F1 score (0.9889), and MCC (0.9700), along with the highest AUC (0.9977).
- **Decision Tree:** Achieved 0.9371 accuracy and 0.9186 AUC. It had lower overall performance than the other models on this test split, although its precision was 0.9551.
- **K-Nearest Neighbors:** Achieved 0.9790 accuracy and a recall of 1.0000, meaning it identified all positive-class instances in this test split. Its precision was 0.9677.
- **Gaussian Naive Bayes:** Achieved 0.9371 accuracy and a relatively high AUC of 0.9878. Its precision (0.9355) and MCC (0.8644) were lower than those of the leading models.
- **Support Vector Machine:** Achieved 0.9790 accuracy and 0.9969 AUC, with strong precision (0.9888) and F1 (0.9832). Its results were close to Logistic Regression.

**Overall winner:** Logistic Regression, based on its strongest overall balance across accuracy, AUC, precision, recall, F1, and MCC on the held-out test set.

## Project files

- `app.py`
- `requirements.txt`
- `README.md`
- `dataset.csv`
- `test_data.csv`
- `metrics.csv`
- `metrics.json`
- Five saved `.joblib` classifier files

## Run the Streamlit application

Install the packages listed in `requirements.txt`, then run:

```bash
streamlit run app.py
```

The application loads the saved classifiers and evaluates uploaded labelled test data without retraining the models.
