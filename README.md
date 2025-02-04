# Fraud Detection on Bank Payments

## Project Overview
This project focuses on developing a reliable fraud detection model to identify potentially fraudulent transactions in a financial dataset. Using machine learning techniques, the model analyzes transaction patterns and flags suspicious activities. It demonstrates essential data preprocessing and classification methods for effective fraud detection.

---

## Objective
The objective of this project is to build a high-performing machine learning model capable of accurately detecting fraudulent transactions while minimizing false positives and false negatives.

---

## Dataset
The dataset consists of transaction records, including:
- **Customer demographics**
- **Merchant details**
- **Transaction specifics**

The target variable (`fraud`) indicates whether a transaction is:
- **Fraudulent (1)**
- **Non-fraudulent (0)**

---

## Steps Involved

### 1. Data Preprocessing
#### Step 1: Handling Categorical Variables
- **Variables Encoded**: `customer`, `age`, `gender`, `zipcodeOri`, `merchant`, `zipMerchant`, `category`
- **Method**: Label encoding using `LabelEncoder` from `sklearn.preprocessing`

#### Step 2: Class Distribution Analysis
- **Observation**: The dataset exhibits a significant imbalance (approx. 10:1), with a higher number of non-fraudulent cases.
- **Action**: Strategies to address this imbalance were considered during model evaluation.

#### Step 3: Feature Scaling
- **Scaler**: `MinMaxScaler` from `sklearn.preprocessing`
- **Feature Range**: 0 to 1

---

### 2. Model Development
#### Chosen Model: Support Vector Machine (SVM)
- **Kernel**: Linear
- **Parameters**: `C=1.0`, `gamma=scale`

#### Data Splitting
- **Train-Test Split Ratio**: 70% training, 30% testing
- **Random State**: 42 (for reproducibility)

---

### 3. Model Evaluation
The model’s performance was evaluated using the following metrics:

#### Key Metrics
- **Accuracy**: 95.4%
- **Precision**: 98.9%
- **Recall**: 58.3%
- **F1 Score**: 0.734
- **Specificity (True Negative Rate)**: 99.9%
- **Balanced Accuracy**: 79.1%
- **Matthews Correlation Coefficient (MCC)**: 0.74

#### ROC Curve and AUC
- **AUC Score**: 0.791
- The Receiver Operating Characteristic (ROC) curve illustrates the model's ability to distinguish between fraudulent and non-fraudulent transactions.

---

## Results and Insights
The Support Vector Machine (SVM) model achieved:
- **High accuracy (95.4%)** and **specificity (99.9%)**, effectively detecting non-fraudulent transactions.
- A **reasonable recall rate for fraud cases (58.3%)**, with opportunities for optimization to improve sensitivity.
- **Balanced Accuracy (79.1%)**, indicating a good trade-off between sensitivity and specificity.

While the model performs well overall, optimizing recall for fraudulent transactions could further enhance its robustness.

---

## Skills Acquired

### 1. Data Preprocessing and Analysis
- **Data Cleaning**: Handling duplicates, managing class imbalances, and preparing data for modeling.
- **Label Encoding**: Transforming categorical variables into numerical values for machine learning compatibility.
- **Class Distribution Analysis**: Evaluating class imbalances and dataset proportions.

### 2. Data Transformation and Scaling
- **Feature Scaling**: Normalizing data with `MinMaxScaler` to ensure uniform feature contribution.
- **Data Splitting**: Splitting datasets into training and testing sets using `train_test_split`.

### 3. Machine Learning Model Development
- **Support Vector Machines (SVM)**: Developing and tuning SVM classifiers for fraud detection.
- **Model Training and Prediction**: Training machine learning models and generating predictions.

### 4. Model Evaluation and Validation
- **Evaluation Metrics**: Interpreting metrics such as accuracy, precision, recall, F1-score, and specificity.
- **Confusion Matrix and Classification Report**: Assessing model performance using detailed reports.
- **Advanced Metrics**: Calculating metrics like Matthews Correlation Coefficient (MCC).

### 5. Performance Visualization and AUC Analysis
- **ROC Curve and AUC Score**: Evaluating model distinction between classes using the ROC curve.
- **Visualization**: Creating performance plots with `matplotlib`.

---

## Repository Structure
- **`/data`**: Contains the dataset used for the project.
- **`/notebooks`**: Jupyter notebooks for data preprocessing, modeling, and evaluation.
- **`/scripts`**: Python scripts for various steps of the pipeline.
- **`README.md`**: Project overview and documentation (this file).

---

## Tools and Libraries
- **Programming Language**: Python
- **Libraries**: `sklearn`, `numpy`, `pandas`, `matplotlib`

---

## Future Work
- Improve the recall rate for fraudulent transactions through advanced techniques such as:
  - Oversampling (SMOTE)
  - Undersampling
  - Cost-sensitive learning
- Experiment with additional models such as Random Forest or XGBoost.
- Incorporate ensemble methods to further enhance model performance.
