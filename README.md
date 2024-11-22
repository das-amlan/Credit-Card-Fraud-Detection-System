# Credit-Card-Fraud-Detection-System

This repository contains the implementation of a Credit Card Fraud Detection System using machine learning techniques. The project focuses on detecting fraudulent transactions in highly imbalanced datasets.

## Features
- Built machine learning models: Random Forest, XGBoost, and SVM.
- Applied advanced data balancing techniques, including SMOTE, under-sampling (NearMiss), and in-algorithm class weighting.
- Explored anomaly detection methods: One-Class SVM and Isolation Forest.
- Evaluated model performance using metrics like precision, recall, F1-score, and ROC-AUC.

## Dataset
The dataset used is the [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). It contains anonymized credit card transactions with features scaled to preserve confidentiality.

## Installation
1. Clone the repository:
   git clone https://github.com/yourusername/credit-card-fraud-detection.git

2. Navigate to the project directory:
    `cd credit-card-fraud-detection`
   
3. Install the required libraries:
    `pip install -r requirements.txt`


## Usage
1. **Preprocess the data:**
- Split the dataset into training and test sets.
- Scale features using `StandardScaler`.
- Handle class imbalance using SMOTE, NearMiss, or algorithm-specific techniques.

2. **Train models:**
- Random Forest, XGBoost, and SVM can be trained using the provided scripts.
- Anomaly detection models like One-Class SVM and Isolation Forest are included for unsupervised fraud detection.

3. **Evaluate models:**
- Use evaluation metrics such as ROC-AUC, precision, recall, and F1-score to assess model performance.


## Results
- Achieved high detection accuracy and ROC-AUC scores using ensemble models like Random Forest and XGBoost.
- Anomaly detection models provided an alternative approach, suitable for unsupervised fraud detection.
- Imbalance handling techniques (SMOTE, class weighting, etc.) significantly improved model robustness.

## Future Work
- Experiment with deep learning models for fraud detection.
- Optimize hyperparameters using grid search or Bayesian optimization.
- Deploy the model as an API for real-time fraud detection.

## Acknowledgments
- [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- [Imbalanced-learn Library](https://imbalanced-learn.org/stable/)
