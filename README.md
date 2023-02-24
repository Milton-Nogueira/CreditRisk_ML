# Classification models for credit risk analysis

## About the Dataset

This dataset provides information about borrowers of a financial institution.

Features:

* person_age: Age.

* person_income: Annual income.

* person_home_ownership: Type of home ownership (Rent/Mortgage/Own/Other).

* person_emp_length: Employment lenght in years.

* loan_intent: Intent of the loan (Medical porpuses, Education, Ventures and others.)

* loan_grade: Loan classification with regards of the risk, ranging from A to G, where G is the category presenting the most risk.

* loan_amnt: Loan amount.

* loan_int_rate: Interest rate.

* loan_percent_income: DTI (Debt to Income) ratio - measure that compares an individual's total debt payments to their gross monthly income.

* cb_person_default_on_file: If the borrower already default before.

* cb_preson_cred_hist_length: Credit history length.

* loan_status: Target variable - If the person defaulted or not.

The features presented can help in analysis of credit risk, i.e, a potential loss that a financial institution may incur if a borrower fails to repay a loan or credit product. Using machine learning to analyse patterns and predict the likelihood of a borrower defaulting on a loan, lenders can minimize losses and help ensure long-term stability on their operations.


The dataset can be found on [Kaggle](https://www.kaggle.com/datasets/laotse/credit-risk-dataset).

# EDA

![dash1](https://user-images.githubusercontent.com/121902546/221193878-c184be1f-d13e-4db8-834f-2e7d2b477ca9.png)


![dash2](https://user-images.githubusercontent.com/121902546/221194152-cdf6d951-ca54-4bd9-a21c-e06b3ed94f71.png)

# Machine Learning

![table](https://user-images.githubusercontent.com/121902546/221022436-aac16929-b8da-4301-aa8f-654f5448f9e8.png)

![cm_combined](https://user-images.githubusercontent.com/121902546/221022437-906c7154-2c0c-4385-b59d-4c505c8e595a.png)




To check the dashboard click [here](https://app.powerbi.com/view?r=eyJrIjoiYmZkODAzNzYtOTEzZi00OTI1LWIyYWItN2ZlZDljNWQ4YWRkIiwidCI6IjJjOTUwZWUxLWY4ZWYtNDY1MS05ZmRiLTIwZjRjNjk0ZTAzYyJ9).

To check the commented code click [here](ML_Credit_Risk.ipynb).
