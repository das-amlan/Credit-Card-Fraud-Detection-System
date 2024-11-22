# Credit Card Fraud Detection Using ML and Different Class Imbalance Handling Approaches

A machine learning-based system for detecting fraudulent credit card transactions, leveraging advanced techniques like SMOTE, under-sampling, and anomaly detection models. Built with Random Forest, XGBoost, and SVM for robust performance on imbalanced datasets.

## Features
- Built machine learning models: Random Forest, XGBoost, and SVM.
- Applied advanced data balancing techniques, including SMOTE, under-sampling (NearMiss), and in-algorithm class weighting.
- Explored anomaly detection methods: One-Class SVM and Isolation Forest.
- Evaluated model performance using metrics like precision, recall, F1-score, and ROC-AUC.

## Imbalance Handling Methods Explored

- **In-Algorithm Techniques**:  
  - **Random Forest and XGBoost**: These models can handle imbalanced datasets by adjusting the `class_weight` (for Random Forest) or `scale_pos_weight` (for XGBoost). This modification assigns higher weights to the minority class (fraudulent transactions), helping the model to focus more on detecting fraud.
  - **SVM**: The `class_weight` parameter in Support Vector Machine (SVM) adjusts the weight of the classes, making the model more sensitive to the minority class (fraud).

- **Under-Sampling**:  
  - **NearMiss and Random Under-Sampling**: These techniques involve reducing the majority class (non-fraudulent transactions) to balance the class distribution. NearMiss selects examples that are close to the decision boundary, while random under-sampling removes random examples from the majority class to make the dataset more balanced.

- **Anomaly Detection**:  
  - **One-Class SVM and Isolation Forest**: These methods treat fraudulent transactions as outliers or anomalies. Instead of classifying all data, these models try to identify data points that deviate from the norm (fraud). They are particularly useful in fraud detection when there is a significant imbalance, as they do not require balancing the classes in the dataset.


| Method                   | Description                                         | Pros                         | Cons                                     |
|--------------------------|-----------------------------------------------------|------------------------------|------------------------------------------|
| **In-Algorithm Techniques** | Adjusts the model itself using class weights.      | Simple to implement.         | May not work well on extreme imbalance.  |
| **Under-Sampling**       | Reduces the majority class to balance data.         | Works well for large datasets.| Risk of losing important information.   |
| **Anomaly Detection**    | Treats fraud as an anomaly (unsupervised).          | No need for balancing.        | Assumes fraud is rare and distinct.     |


## Dataset
The dataset used is the [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). It contains anonymized credit card transactions with features scaled to preserve confidentiality.

## Installation
1. Clone the repository:
   git clone https://github.com/das-amlan/credit-card-fraud-detection.git

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
