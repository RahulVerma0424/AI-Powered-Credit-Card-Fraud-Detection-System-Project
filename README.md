# 💳 Credit Card Fraud Detection

This project aims to build a **machine learning model** that detects fraudulent credit card transactions using the popular **Kaggle Credit Card Dataset**.  
Fraud detection is highly important in the financial sector, as fraudulent transactions are rare but can cause huge financial losses.  

---

## 📂 Dataset
- **Source:** [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- **Size:** 284,807 transactions
- **Features:**
  - 28 anonymized numerical features (V1–V28)
  - `Time` (seconds elapsed between transactions)
  - `Amount` (transaction amount)
  - `Class` (target → 0 = Non-fraud, 1 = Fraud)

---

## ⚙️ Steps Performed

### 1. Data Preprocessing
- Loaded dataset using `pandas`
- Standardized the `Amount` and `Time` columns using `StandardScaler`
- Handled class imbalance using **class weights** in Logistic Regression

### 2. Train-Test Split
- 80% Training, 20% Testing  
- Stratified split to maintain class distribution

### 3. Model Used
- **Logistic Regression** with `class_weight='balanced'`
- Optimized for rare class detection

### 4. Model Evaluation
- Evaluated using:
  - **Classification Report** (Precision, Recall, F1-score)
  - **Confusion Matrix**
  - **ROC-AUC Score**

---

## 📊 Results

- **Accuracy:** ~98%  
- **Recall (Fraud Class 1):** ~92%  
- **ROC-AUC Score:** **0.97**  

Although accuracy is very high, recall is more important here since we aim to **catch as many fraud cases as possible**.

---

## 🚀 Future Improvements
- Try **Random Forests / XGBoost** for better fraud detection  
- Use **SMOTE / Oversampling techniques** to balance the dataset  
- Deploy the model with a **Flask/Django API** for real-time fraud detection  

---

## 🛠️ Technologies Used
- Python 🐍  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  

---


