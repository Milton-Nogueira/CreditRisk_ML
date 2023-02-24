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


![dash1](https://user-images.githubusercontent.com/121902546/221280547-717a55c0-3578-47fd-ad91-6fb6a45db93d.png)


* It's important to note that the dataset doesn't specify if people classified as 'No' in the Historical Defaulters feature have paid all their debts or have never requested a loan before. Regardless, it is noticeable that a significant portion of those who have defaulted on loans have not repaid their debts. As for the other category, it's difficult to assume that every person registered has a record of more than one loan in the past. Without more information, we can't reliably draw insights from this feature.

* Checking the age profile, the range of 20-30 is where most people request loans from this institution, and it is also the range with the most defaulters. However, it's also the range that requests the lowest loan amount.

* As one could expect when analyzing the employment length feature, people with less job stability tend to default on their loans.

* DTI is a financial metric used to evaluate a person's ability to manage their debts payments. Generally, a DTI ratio of 36% or less is considered good, while a ratio above 43% may indicate that a borrower is at higher risk of defaulting on their debts. Looking at this dataset, non-defaulters have an average DTI ratio of 14.88%, while defaulters have a ratio of 24.69%, which falls under the good range. This could indicate that this institution should restrict the range considered good.


![dash2](https://user-images.githubusercontent.com/121902546/221194152-cdf6d951-ca54-4bd9-a21c-e06b3ed94f71.png)

* The majority of loans in this institution are intended for educational or medical purposes, with the latter having the most defaulters. However the venture category is the one with the highest average loan amount. Also important to note that the only category where we have most non-defaulters is home improvement, but we should be careful with this since it has the lowest number of borrowers as well.  

* We can see a strong relation between the type of home ownership and the amount of defaulters. People that own their homes, as one would expect, are the ones that have the lowest number of defaulters and also the lowest number of borrowers in general. We can also see this category presenting the lowest average annual income, although this may be attributed to the lack of statistics. Individuals who live in rented houses tend to default on their loans more frequently.

* The pie chart shows the percentage of defaulters and non-defaulters in the financial insitution. Filtering with the loan grades, as the classifications increase to D and beyond, the number of defaulters begins to dominate over non-defaulters. D-grade has the highest number of defaulters. 

* In the section 'How to Predict?' we can see pie charts showing two machine learning approaches to predict defaulters. One model presenting a higher recall rate, while the other, a higher precision rate. Further about those models in the following section.

# Machine Learning

In this analysis, we used stratified cross-validation, a technique for evaluating the performance of a machine learning model. It involves dividing a dataset into k folds or partitions of approximately equal size, where k is a specified number (in this case, 5), and ensuring that the same proportion of each class or target variable category is present in each fold.

Data cleaning, outlier removal, and standardization were performed after the data splitting step in the cross-validation process to avoid data leakage.

After preprocessing the data, we applied several machine learning models, ranging from a simple Logistic Regression model to ensemble models like XGBoost Classifier.

In the table below we can check the metrics obtained for each of the models: 

![table](https://user-images.githubusercontent.com/121902546/221022436-aac16929-b8da-4301-aa8f-654f5448f9e8.png)

About the metrics:

* Accuracy measures the overall performance of the model in correctly predicting the loan status (default or non-default). However, accuracy alone can be misleading.

* Precision measures the proportion of correctly identified defaulters out of all the predicted defaulters. A high precision indicates that the model correctly identifies most of the defaulters, but it may miss some non-defaulters.

* Recall measures the proportion of correctly identified defaulters out of all the actual defaulters. A high recall indicates that the model correctly identifies most of the defaulters, but it may mistakenly label some non-defaulters as defaulters.

* F1 Score is the harmonic mean of precision and recall, which balances both metrics. A high F1 score indicates a good balance between precision and recall.

In credit risk analysis, precision and recall are the most important metrics, as they reflect the cost and benefit of correctly identifying defaulters. However, it is also important to consider the accuracy. 

It is up to the financial institution to align their business strategies with the machine learning department to properly choose a model with the best precision, recall, or even F1-score.

In this analysis, evaluating the metrics:

* GradientBoostingClassifier is the model with the best recall.

* RandomForestClassifier is the model with the best precision.

* XGBoost has the best is the model with the best F1-Score.

All three models have a good accuracy rate above 92%.

![cm_combined](https://user-images.githubusercontent.com/121902546/221022437-906c7154-2c0c-4385-b59d-4c505c8e595a.png)




To check the dashboard click [here](https://app.powerbi.com/view?r=eyJrIjoiYzRlNzVkYzQtN2JlOC00MTJkLTk2YTYtNzUzNTY2NjJjN2E0IiwidCI6IjJjOTUwZWUxLWY4ZWYtNDY1MS05ZmRiLTIwZjRjNjk0ZTAzYyJ9).

To check the commented code click [here](ML_Credit_Risk.ipynb).
