# 📊 End-to-End Telco Customer Churn Prediction  

This project is a **complete, end-to-end machine learning solution** designed to predict customer churn for a fictional telecommunications company.  
The primary goal is to identify customers who are likely to cancel their subscriptions, enabling the business to take **proactive retention measures**. 

---

## 🚨 Why Customer Churn Matters  
Customer churn is a **critical problem** for subscription-based businesses:  
- Acquiring new customers is far more expensive than retaining existing ones.  
- Accurately predicting churn allows businesses to:  
  ✅ Identify high-risk customer segments  
  ✅ Implement targeted retention campaigns  
  ✅ Quantify the financial impact of churn and interventions  

---

## 🛠 Tech Stack  
- **Data Analysis & Manipulation:** Pandas, NumPy  
- **Data Visualization:** Seaborn, Matplotlib  
- **Machine Learning:** Scikit-learn, Imbalanced-learn (SMOTE)  
- **Model Deployment:** Streamlit  
- **Version Control:** Git & GitHub  

---

## 🔄 Project Workflow  

### 1. Exploratory Data Analysis (EDA)  
- Analyzed dataset to uncover patterns and correlations with churn.  

### 2. Feature Engineering  
- Created predictive features such as `Is_Independent` and `TenureGroup`.  

### 3. Preprocessing & Modeling  
- Scaling numerical features  
- One-hot encoding categorical features  
- Balancing data with **SMOTE**  
- Built a **scikit-learn pipeline**  

### 4. Hyperparameter Tuning  
- Used **GridSearchCV** with stratified 5-fold cross-validation.  
- Optimized a **RandomForestClassifier**.  

### 5. Model Evaluation  
- Focused on metrics relevant for imbalanced data:  
  - Recall  
  - F1-Score  
  - ROC AUC    

---

## 📌 Key Findings  
- Customers with **Month-to-Month contracts** are the most likely to churn.  
- **Low tenure** is the strongest churn predictor.  
- Customers using **Fiber optic internet** and **Electronic Check payments** have higher churn risk.  

---

## 📈 Model Performance (Test Set)  

| Metric          | Score |
|-----------------|-------|
| ROC AUC Score   | 0.84  |
| Accuracy        | 80%   |

✅ The model improved **recall for churners (77%)**, meaning it correctly identified most customers who were about to leave.  

---

## 💰 Business Impact  
By targeting at-risk customers identified by the model, the company could save an estimated **$64,000+ in annual recurring revenue**.  

---

## 📂 Project Structure
├── data/               # Dataset
├── notebooks/          # EDA & experiments
├── app.py              # Streamlit application
├── models/             # Saved models/pipelines
├── requirements.txt    # Dependencies
└── README.md           # Project documentation

