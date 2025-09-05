# 🏦 Finance Loan Approval Prediction

## 📌 Project Overview
Finance company deals in all loans. The customer first applies for a home loan after that company validates the customer's eligibility for a loan.

The company wants to automate the loan eligibility process (real-time) based on customer detail provided while filling out the online application form. These details are Gender, Marital Status, Education, Number of Dependents, Income, Loan Amount, Credit History and others. To automate this process, they have given a problem identifying the customer segments eligible for loan amounts to target these customers specifically. Here they have provided a partial data set.

This project automates the **loan approval process** for a finance company using Machine Learning.  
The goal is to predict whether a customer is eligible for a home loan based on demographic and financial details provided in the loan application.

## 📊 Dataset
- **Train.csv** – contains customer details with `Loan_Status` (Y/N).
- **Test.csv** – contains customer details without labels (for predictions).
- Features include:
  - Gender
  - Married
  - Dependents
  - Education
  - Self_Employed
  - ApplicantIncome
  - CoapplicantIncome
  - LoanAmount
  - Loan_Amount_Term
  - Credit_History
  - Property_Area

## ⚙️ Workflow
1. **Data Preprocessing**
   - Handling missing values
   - Encoding categorical variables
   - Feature scaling and transformation

2. **Exploratory Data Analysis (EDA)**
   - Distribution of income, loan amounts
   - Loan status by categorical variables
   - Correlation analysis

3. **Model Building**
   - Algorithm: **Random Forest Classifier**
   - Hyperparameter tuning with **GridSearchCV**
   - Train/validation split for model evaluation

4. **Evaluation Metrics**
   - Accuracy: **0.75**
   - Precision: **0.80**
   - Recall: **0.92**
   - F1-score: **0.86**

5. **Feature Importance**
   - ApplicantIncome (0.305)
   - LoanAmount (0.254)
   - CoapplicantIncome (0.172)
   - Property_Area (0.086)
   - Dependents (0.058)
   - Others had lower contribution

6. **Final Prediction**
   - Generated loan approval predictions (`Y` / `N`) for test data
   - Saved as a submission file

## 📈 Results & Insights
- **High recall (92%)** ensures most eligible customers are correctly identified.
- **Decent precision (80%)** but some false approvals remain (potential risk for banks).
- **Applicant income, loan amount, and coapplicant income** are the strongest predictors.
- **Credit history importance was low** in this run, suggesting preprocessing could be improved.

## 🚀 Future Improvements
- Improve **feature engineering** (income-to-loan ratio, family income).
- Handle **credit history encoding** more effectively.
- Try advanced models like **XGBoost, LightGBM, CatBoost**.
- Apply **SMOTE or class weighting** if dataset is imbalanced.

## 🛠️ Tech Stack
- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- Jupyter Notebook

---
👤 **Author**: *Aldous Dsouza*  
---

## 🤝 Contribution
Contributions are welcome! Feel free to fork this repo and submit pull requests.  
