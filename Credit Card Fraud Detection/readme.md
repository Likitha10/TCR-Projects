# Credit Card Fraud Detection

This project aims to detect fraudulent credit card transactions using machine learning algorithms. By leveraging a dataset of anonymized transaction records, the goal is to create a robust model that can identify fraudulent transactions with high accuracy.

---

## 🚀 **Project Overview**

Credit card fraud is a growing concern worldwide, and early detection is critical to preventing financial losses. This project explores various machine learning techniques to classify transactions as fraudulent or legitimate, based on anonymized transaction data. 

The dataset used in this project is sourced from Kaggle and consists of numerical features derived from PCA transformation, ensuring user privacy while enabling effective fraud detection.

---

## 📊 **Dataset Information**

- **Source:** [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- **Size:** 284,807 transactions
- **Imbalance:** Only **0.172%** of the transactions are fraudulent, making this a highly imbalanced dataset.
- **Features:**
  - **V1, V2, ..., V28:** Numerical features obtained from a PCA transformation to protect sensitive information.
  - **Time:** Seconds elapsed between the first transaction and the current transaction.
  - **Amount:** Transaction amount.
  - **Class:** Target variable:
    - `0` for legitimate transactions.
    - `1` for fraudulent transactions.

---

## 🛠️ **Technologies Used**

- **Python Libraries:**
  - `pandas` for data manipulation.
  - `numpy` for numerical computation.
  - `matplotlib` and `seaborn` for data visualization.
  - `scikit-learn` for machine learning models and evaluation.
  - `imbalanced-learn` for handling class imbalance.
- **Machine Learning Algorithms:**
  - Logistic Regression.
  - SMOTE (Synthetic Minority Oversampling Technique) for handling class imbalance.
- **Evaluation Metrics:**
  - Confusion Matrix.
  - Precision, Recall, F1-Score.
  - Precision-Recall Curve.

---

## 📜 **Project Workflow**

1. **Data Exploration:**
   - Investigated the distribution of features and identified class imbalance.
   - Visualized class distribution using a count plot.

2. **Data Preprocessing:**
   - Scaled the `Time` and `Amount` features using `RobustScaler` to handle outliers.
   - Replaced original features with their scaled versions.

3. **Handling Class Imbalance:**
   - Applied **SMOTE** to oversample the minority class in the training data.
   - Ensured no data leakage by applying SMOTE only after splitting the dataset.

4. **Model Development:**
   - Built a Logistic Regression model as a baseline.
   - Evaluated performance using a confusion matrix and classification report.

5. **Evaluation:**
   - Observed high recall but low precision, highlighting a need to reduce false positives.
   - Analyzed the Precision-Recall Curve to understand the trade-off between precision and recall.

6. **Prediction:**
   - Tested the model on arbitrary input data to demonstrate its prediction capability.

---

## 🔍 **Key Observations**

- The Logistic Regression model achieved high recall, effectively detecting most fraudulent transactions.
- Low precision indicated a significant number of false positives, requiring improvement to avoid customer dissatisfaction.
- Suggested next steps include exploring other algorithms like Random Forest and hyperparameter tuning to balance precision and recall.

---

## 🤝 **Contributing**

Contributions are welcome! Feel free to submit a pull request or open an issue for suggestions or improvements.

---

## 📝 **Acknowledgments**

- Thanks to [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud) for providing the dataset.




