# -Customer-Churn-Prediction-System-Python-Project-
End-to-end Python project for customer churn prediction using data engineering, feature engineering, and machine learning (Random Forest). Includes full pipeline from raw data to model evaluation.

## 📌 Project Overview

This project builds a complete **Customer Intelligence System** using Python.  
It processes raw transaction data, creates meaningful customer features, and predicts whether a customer is likely to churn.

The goal is to help businesses **identify at-risk customers** and take actions to improve retention.

## 🎯 Business Problem

Companies often lose customers without knowing in advance.  
This project predicts:

> Which customers are likely to stop purchasing (churn)?

## 🧠 Objective

Build a machine learning model that:
- Uses past transaction data  
- Identifies customer behavior  
- Predicts churn (0 = active, 1 = churn)

---

## 🏗️ Project Architecture

Raw Data → Cleaning → Feature Engineering → Model Training → Prediction

## 📂 Project Structure
customer-intelligence-platform/

├── data/
│ ├── raw/ # Original dataset
│ └── processed/ # Cleaned + feature datasets
│
├── src/
│ ├── ingestion/ # Data loading
│ ├── processing/ # Cleaning + feature engineering
│ └── models/ # Model training
│
├── docs/
│ └── problem_definition.md
│
└── requirements.txt

## 🔄 Pipeline Steps

### 1. Data Ingestion
- Load raw CSV dataset
- Handle encoding issues

### 2. Data Cleaning
- Remove missing CustomerID
- Remove invalid transactions (negative values)
- Convert date format

### 3. Feature Engineering (Most Important)
Created customer-level features:

- **Recency** → Days since last purchase  
- **Frequency** → Number of purchases  
- **Monetary** → Total spending  

Advanced features:
- **AvgOrderValue** → Spending per order  
- **CustomerLifetime** → Activity duration  
- **PurchaseFrequency** → Engagement rate  

## 🎯 Target Variable (Churn)
Churn = 1 → No purchase in last 180 days
Churn = 0 → Active customer

## 🤖 Machine Learning Models

### 1. Random Forest (Final Model)
- Handles non-linear patterns  
- Works better with imbalance  

### 2. Logistic Regression (Baseline)
- Simpler model  
- Failed to detect churn properly  

## 📊 Model Results

### Random Forest
- Accuracy: ~77%  
- Churn Recall: ~36%  

### Logistic Regression
- Accuracy: ~79% (misleading)  
- Churn Recall: 0% ❌  

## ⚠️ Key Insight

Higher accuracy does NOT mean better model.

- Logistic Regression predicted all customers as "active"
- Random Forest successfully identified churn customers

👉 Therefore, Random Forest is selected

## 💡 Business Insights

- Customers with low frequency are more likely to churn  
- Customers with low spending are at higher risk  
- Engagement (purchase frequency) is a strong signal  

## 🚀 How to Run

### Step 1: Install dependencies
pip install -r requirements.txt

### Step 2: Run pipeline



[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/srishti-dev-sr1r1s/)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/srishti_devv/)
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/srishti.dev.1)


