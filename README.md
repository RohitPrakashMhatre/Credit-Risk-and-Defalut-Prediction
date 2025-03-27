# Credit-Risk-and-Default-Prediction

# 📌 Overview
This project focuses on predicting loan defaults using Machine Learning. The dataset comes from Kaggle, and the goal is to identify key risk factors that contribute to loan defaults. By analyzing borrower characteristics, the aim is to help financial institutions assess credit risk and reduce defaults.
# 📊 Dataset
- SOURCE: https://www.kaggle.com/datasets/wordsforthewise/lending-club (accepted_2007_to_2018Q4)
- Size: 2200000 + rows, 151 features
- key features: (for Credit risk analysis and default prediction)
    - 'loan_amnt':      Loan amount applied for
    - 'int_rate':       Interest rate of the loan
    - 'installment':    Monthly repayment amount
    - 'grade' :         Credit grade (A to G)
    - 'emp_length':     Years of employment 
    - 'annual_inc':     Borrower's annual income
    - 'dti':            Debt-to-Income ratio (high = risk)
    - 'fico_range_low': Lower bound of FICO credit score
    - 'revol_util':     Credit utilization rate (indicator of credit behavior)
    - 'total_rec_prncp':Total principal paid (loan repayment indicator)
    - 'purpose':        Loan purpose (categorical - insights on default risk)
    - 'loan_status':    Target variable (Fully Paid, Charged Off, Default)
    - 'verification_status': Whether borrower's income is verified
    - 'last_pymnt_amnt': Last payment amount 
    - 'total_rec_int':   Total interest received 
# 📈 Data Preprocessing & Feature Engineering
- Outliers detection
- Handle missing values
- Feature selection
- Encoding categorical features

# 🛠️ Machine Learning Models Used
- Random Forest Classifier
- XGBoost
- VotingClassifier
  
# 🛠️ Hyperparameter Tuning: Performed using RandomizedSearchCV.
# 📌 Model Evaluation: Focused on Recall due to the high cost of false negatives in credit risk prediction.

# 🎯 Key Insights
- Loan amount distribution varies significantly across different credit grades.
- High-risk credit grades were identified, helping assess loan default probabilities.
- Credit grades impact interest rates: Borrowers with higher credit scores receive lower interest rates, while lower credit scores are associated with higher interest rates.
- Top predictive features: Annual income, interest rate, and debt-to-income ratio are the most influential factors in determining loan default risk.

# Evaluation result
- Random Forest Classifier: Recall = 0.73
- XGBoost: Recall = 0.91
- Voting Classifier: Recall = 0.83

# 📌 Tools & Libraries Used
- Python (pandas, numpy, scikit-learn, imbalanced-learn, matplotlib, seaborn, scipy)

# 📌 Future Work
- Planning to expand the more data and add more features.
- Fine-tune the model for a better F1-score, ensuring both defaults and fully-paid customers are accurately classified. 
- Conduct a more detailed risk assessment to identify and quantify key risk factors.
- Also planing for deployment
