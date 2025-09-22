# CodeAlpha Credit Scoring Model

## 📌 Project Overview
This project was built as part of my **CodeAlpha Internship**.  
The goal is to predict an individual’s **creditworthiness** (loan approval vs. rejection) based on their personal and financial information.

This is a **binary classification problem**:
- `1` → Good credit / Loan Approved  
- `0` → Bad credit / Loan Rejected  

---

## 📊 Dataset
- **Size:** 45,000 rows × 14 columns  
- **Target:** `loan_status` (0 = rejected, 1 = approved)  
- **Features include:**
  - Personal info: `person_age`, `person_gender`, `person_education`  
  - Financial info: `person_income`, `person_emp_exp`, `credit_score`  
  - Loan details: `loan_amnt`, `loan_intent`, `loan_int_rate`, `loan_percent_income`  
  - Credit history: `cb_person_cred_hist_length`, `previous_loan_defaults_on_file`  
  - Home ownership: `person_home_ownership`

---

## ⚙️ Approach
1. **Exploratory Data Analysis (EDA)**
   - Class balance visualization  
   - Feature distributions  
   - Correlation with target  
   - Boxplots and countplots  

2. **Data Preprocessing**
   - Scaled numeric features with `StandardScaler`.  
   - Encoded categorical features with `OneHotEncoder`.  
   - Used **Pipeline** + **ColumnTransformer** to keep preprocessing consistent.  

3. **Models Tested**
   - Logistic Regression  
   - Decision Tree  
   - Random Forest  

4. **Evaluation Metrics**
   - Precision, Recall, F1-score  
   - ROC-AUC Score  
   - Confusion Matrix visualization  

---

## 🧠 Algorithms in Plain English
- **Logistic Regression** → Predicts probability of default, good baseline.  
- **Decision Tree** → Flowchart of if/else rules, interpretable but can overfit.  
- **Random Forest** → Ensemble of trees, more robust and accurate.  

---

## 📈 Results
- **Random Forest** achieved the best trade-off between Precision, Recall, and ROC-AUC.  
- `credit_score` and `loan_percent_income` were the most important predictors.  

---

## 🚀 Future Improvements
- Handle class imbalance with **SMOTE** or class weights.  
- Try boosting algorithms (XGBoost, LightGBM, CatBoost).  
- Build a simple **web app (Flask/Streamlit)** for interactive predictions.  

---

## 📜 License
This project is licensed under the MIT License – feel free to use and adapt.
