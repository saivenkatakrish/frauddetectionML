# Fraud Detection on Bank Payments

## Project Overview
This project focuses on developing a reliable fraud detection model to identify potentially fraudulent transactions in a financial dataset. Using machine learning techniques, the model analyzes transaction patterns and flags suspicious activities, demonstrating essential data preprocessing and classification methods for effective fraud detection.

---

## Objective
The objective of this project is to build a high-performing machine learning model capable of accurately detecting fraudulent transactions while minimizing false positives and negatives.

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

### 2.
