# Loan Approval Prediction using Logistic Regression

This project focuses on predicting loan approval status based on customer data using logistic regression. The dataset contains various features like income, loan amount, CIBIL score, and asset values to determine whether a loan will be approved or rejected.



## Dataset

The dataset consists of 13 columns:

- **loan_id**: Unique identifier for each loan application
- **no_of_dependents**: Number of dependents the applicant has
- **education**: Applicant's education status (Graduate or Not Graduate)
- **self_employed**: Whether the applicant is self-employed (Yes or No)
- **income_annum**: Applicant's annual income
- **loan_amount**: The loan amount requested
- **loan_term**: The term for which the loan is taken (in months)
- **cibil_score**: The applicant's CIBIL score
- **residential_assets_value**: Value of residential assets owned by the applicant
- **commercial_assets_value**: Value of commercial assets owned by the applicant
- **luxury_assets_value**: Value of luxury assets owned by the applicant
- **bank_asset_value**: Bank assets value of the applicant
- **loan_status**: The target variable, whether the loan is **Approved** or **Rejected**

Sample dataset:

| loan_id | no_of_dependents | education  | self_employed | income_annum | loan_amount | loan_term | cibil_score | residential_assets_value | commercial_assets_value | luxury_assets_value | bank_asset_value | loan_status |
|---------|------------------|------------|---------------|--------------|-------------|-----------|-------------|--------------------------|-------------------------|--------------------|-----------------|-------------|
| 1       | 2                | Graduate   | No            | 9600000      | 29900000    | 12        | 778         | 2400000                  | 17600000                | 22700000           | 8000000         | Approved    |
| 2       | 0                | Not Graduate | Yes          | 4100000      | 12200000    | 8         | 417         | 2700000                  | 2200000                 | 8800000            | 3300000         | Rejected    |

## Steps Followed

### 1. **Data Cleaning**
   - Removed any unnecessary columns like `loan_id`.
   - Removed extra spaces from column names and specific columns (`education`, `self_employed`, `loan_status`).
   - Label encoding for categorical variables:
     - `loan_status`: 1 for Approved, 0 for Rejected
     - `education`: 1 for Graduate, 0 for Not Graduate
     - `self_employed`: 1 for Yes, 0 for No
     
### 2. **Exploratory Data Analysis (EDA)**
   - Performed basic data exploration using functions like `head()`, `info()`, `describe()`, and `isnull().sum()` to understand the dataset.
   - Visualized the distribution of the `loan_status` target variable using a bar chart.

### 3. **Correlation Analysis**
   - Generated a correlation matrix to understand relationships between numerical features.

### 4. **Feature Selection**
   - Selected relevant features for the model by dropping columns like `loan_status`, `no_of_dependents`, and `education`.
   
### 5. **Data Normalization**
   - Applied StandardScaler to normalize the numerical features to improve model performance.

### 6. **Model Training**
   - Used a **Logistic Regression** model for binary classification.
   - Split the data into training and testing sets using `train_test_split`.

### 7. **Model Evaluation**
   - Evaluated the model performance using the **accuracy score**.

## Model Performance

- Accuracy achieved: **0.90**

## How to Run the Project

### Prerequisites
- Python 3.x
- Jupyter Notebook
- Libraries:
  - pandas
  - scikit-learn
  - matplotlib (for visualizations)

### Steps to Run:
1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/Loan-Approval-Prediction.git
   cd Loan-Approval-Prediction


