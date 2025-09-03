# An Algorithm for Credit Card Fraud Detection  

This project implements an **unsupervised anomaly detection system** for detecting fraudulent credit card transactions using the **Credit Card Fraud Detection Dataset**. The focus is on applying **Isolation Forest** and **Local Outlier Factor (LOF)** to identify suspicious transactions.  

---

## 🎯 Project Goal  

- Detect fraudulent credit card transactions from highly imbalanced data.  
- Compare the performance of **Isolation Forest** and **Local Outlier Factor**.  
- Build an algorithm that generalizes well to unseen transactions.  

---

## 📂 Dataset  

- **Name**: [Credit Card Fraud Detection Dataset (Kaggle)](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- **Samples**: 284,807 transactions  
- **Fraudulent transactions**: 492 (~0.17% of total)  
- **Features**:  
  - 30 numerical input variables (V1–V28 are PCA-transformed features, `Time`, `Amount`)  
  - `Class`: Target variable (0 = normal, 1 = fraud)  

---

## 🧭 Workflow  

### 1. Data Preprocessing  
- Load dataset and normalize `Amount` feature  
- Handle class imbalance (fraudulent cases << non-fraudulent cases)  
- Train/test split  

### 2. Algorithms  
- **Isolation Forest**  
  - Tree-based anomaly detection  
  - Isolates rare fraud cases with fewer splits  

- **Local Outlier Factor (LOF)**  
  - Density-based anomaly detection  
  - Detects fraud by measuring local deviation from neighbors  

### 3. Evaluation  
- Metrics:  
  - Accuracy (not sufficient due to imbalance)  
  - Precision, Recall, F1-score  
  - ROC-AUC score  
- Confusion matrix to analyze False Positives/Negatives  

---

## 📂 Repository Structure  

- `data/` – Credit card fraud dataset (CSV)  
- `notebooks/` – Jupyter notebooks for EDA, modeling, and evaluation  
- `models/` – Scripts implementing Isolation Forest & LOF  
- `results/` – Performance metrics and plots  

---

## 🚀 How to Run  

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/Credit_card_fraud_detection.git
   cd Credit_card_fraud_detection
