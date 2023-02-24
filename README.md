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

Miscrosoft Power BI was used to present the most important insights of the exploratory analysis.

The two page report shows a profile of defaulters and non-defaulters using the dataset features. To further analyze those profiles it is possible to filter not only for defaulters and non-defaulters, but also for their loan grades. 

Loan grades are a system to categorize and evaluate the risk associated with different loan applicants. They are based on an applicant's creditworthiness, income, employment status and other financial factors. In this dataset the grades vary from A to G, where A is the classification with lesser risk involved and G, the one with highest risk. 



![dash1](https://user-images.githubusercontent.com/121902546/221193878-c184be1f-d13e-4db8-834f-2e7d2b477ca9.png)


* It's important to note that the dataset doesn't specify if people classified as 'No' in the Historical Defaulters feature have paid all their debts or have never requested a loan before. Regardless, it is noticeable that a significant portion of those who have defaulted on loans have not repaid their debts. As for the other category, it's difficult to assume that every person registered has a record of more than one loan in the past. Without more information, we can't reliably draw insights from this feature.

* Checking the age profile, the range of 20-30 is where most people request loans from this institution, and it is also the range with the most defaulters. However, it's also the range that requests the lowest loan amount.

* As one could expect when analyzing the employment length feature, people with less job stability tend to default on their loans.

* DTI is a financial metric used to evaluate a person's ability to manage their debts payments. Generally, a DTI ratio of 36% or less is considered good, while a ratio above 43% may indicate that a borrower is at higher risk of defaulting on their debts. Looking at this dataset, non-defaulters have an average DTI ratio of 14.88%, while defaulters have a ratio of 24.69%, which falls under the good range. This could indicate that this institution should restrict the range considered good.


![dash2](https://user-images.githubusercontent.com/121902546/221194152-cdf6d951-ca54-4bd9-a21c-e06b3ed94f71.png)

# Machine Learning

![table](https://user-images.githubusercontent.com/121902546/221022436-aac16929-b8da-4301-aa8f-654f5448f9e8.png)

![cm_combined](https://user-images.githubusercontent.com/121902546/221022437-906c7154-2c0c-4385-b59d-4c505c8e595a.png)




To check the dashboard click [here](https://app.powerbi.com/view?r=eyJrIjoiYzRlNzVkYzQtN2JlOC00MTJkLTk2YTYtNzUzNTY2NjJjN2E0IiwidCI6IjJjOTUwZWUxLWY4ZWYtNDY1MS05ZmRiLTIwZjRjNjk0ZTAzYyJ9).

To check the commented code click [here](ML_Credit_Risk.ipynb).
