# LoanTap-Logistic_Regression
- LoanTap is an innovative online platform dedicated to providing customized loan solutions tailored to the needs of millennials. By reimagining the traditional loan landscape, LoanTap offers instant, flexible loans with consumer-friendly terms, catering specifically to salaried professionals and businessmen.

- In a bid to enhance their services, the data science team at LoanTap is developing an advanced underwriting layer aimed at accurately determining the creditworthiness of both MSMEs and individual borrowers. This underwriting process is crucial for deploying formal credit through LoanTap’s four primary financial instruments: Personal Loan, EMI Free Loan, Personal Overdraft, and Advance Salary Loan.

- This case study will delve into the intricacies of the underwriting process specifically for Personal Loans, highlighting the methodologies and data-driven approaches employed to assess and manage credit risk effectively.

## Objective:
The objective of this project is to develop a robust, data-driven underwriting model that accurately assesses the creditworthiness of individuals based on a set of attributes.
The model will determine whether a credit line should be extended and, if approved, provide business recommendations for the optimal repayment terms.
This will ensure that LoanTap offers personalized, fair, and risk-adjusted loan solutions to its customers.


## Dataset Information:
### Source: Please check the dataset at: "Dataset Link"

### Feature Information:
- loan_amnt : The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.
- term : The number of payments on the loan. Values are in months and can be either 36 or 60.
- int_rate : Interest Rate on the loan
- installment : The monthly payment owed by the borrower if the loan originates.
- grade : LoanTap assigned loan grade.
- sub_grade : LoanTap assigned loan subgrade.
- emp_title : The job title supplied by the Borrower when applying for the loan.
- emp_length : Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years.
- home_ownership : The home ownership status provided by the borrower during registration or obtained from the credit report.
- annual_inc : The self-reported annual income provided by the borrower during registration.
- verification_status : Indicates if income was verified by LoanTap, not verified, or if the income source was verified.
- issue_d : The month which the loan was funded.
- loan_status : Current status of the loan - Target Variable.
- purpose : A category provided by the borrower for the loan request.
- title : The loan title provided by the borrower.
- dti : A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LoanTap loan, divided by the borrower’s self-reported monthly income.
- earliest_cr_line : The month the borrower's earliest reported credit line was opened.
- open_acc : The number of open credit lines in the borrower's credit file.
- pub_rec : Number of derogatory public records.
- revol_bal : Total credit revolving balance.
- revol_util : Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.
- total_acc : The total number of credit lines currently in the borrower's credit file.
initial_list_status : The initial listing status of the loan. Possible values are – W(whole loans), F(fractional loans).
- application_type : Indicates whether the loan is an individual application or a joint application with two co-borrowers.
- mort_acc : Number of mortgage accounts.
- pub_rec_bankruptcies : Number of public record bankruptcies.
- Address: Address of the individual.
## Key Steps:

  ## 1. Exploratory Data Analysis (EDA):
    - Inspect dataset structure and characteristics
    - Visualize the relationship between Loan_Status and predictor variables (count plots, box plots, heat maps, etc.)
    - Analyze correlations among independent variables to understand their interactions

## 2. Feature Engineering:
    - Creating Flags for specific features:
    - Pub_rec: Flag set to 1 if value > 1, else 0
    - Mort_acc: Flag set to 1 if value > 1, else 0
    - Pub_rec_bankruptcies: Flag set to 1 if value > 1, else 0
    - Handling missing values and outliers
    - Scaling numerical features using MinMaxScaler or StandardScaler

## 3. Model Building:
    - Logistic Regression using sklearn or statsmodels
    - Explanation of model coefficients and their impact on loan approval

## 4. Model Evaluation:
    - Classification Report (Precision, Recall, F1-Score, Accuracy)
    - ROC-AUC Curve

## 5.Precision-Recall Curve:
    - Precision vs. Recall Tradeoff
    - Discussion on the importance of optimizing precision and recall:
    - Ensuring detection of real defaulters (Reducing false negatives)
    - Minimizing false positives to avoid unnecessary loan rejections
    - Addressing the industry challenge of Non-Performing Assets (NPA) while ensuring a profitable lending strategy

## Insights & Recommendations:
