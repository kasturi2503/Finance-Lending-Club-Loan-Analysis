# Lending Club Loan Dataset - Credit Risk Analysis

## **Project Description**

This project analyzes the Lending Club Loan Dataset to predict loan defaults and assess the factors contributing to credit risk. The dataset includes information about loans issued through Lending Club, covering borrower characteristics, loan details, and repayment statuses.

---

## **Objectives**

1. Perform **Exploratory Data Analysis (EDA)** to uncover trends and insights related to borrowers, loans, and default patterns.
2. Develop machine learning models to predict loan default status.
3. Identify key factors influencing loan defaults and provide actionable insights.

---

## **Dataset Overview**

The Lending Club Loan Dataset contains the following key features:

### Loan Information:

- **`loan_amnt`**: The loan amount requested by the borrower.
- **`funded_amnt`**: The amount funded by investors.
- **`term`**: Loan term in months (e.g., 36 or 60 months).
- **`int_rate`**: Interest rate charged on the loan.
- **`installment`**: Monthly installment amount.

### Borrower Information:

- **`grade`**** and ****`sub_grade`**: Credit grades assigned to borrowers.
- **`emp_length`**: Length of employment in years.
- **`home_ownership`**: Borrower's homeownership status (e.g., RENT, OWN).
- **`annual_inc`**: Annual income of the borrower.
- **`verification_status`**: Indicates if income was verified.

### Loan Status:

- **`loan_status`**: The status of the loan (e.g., Fully Paid, Charged Off, Default). This is the target variable for prediction.

### Credit History:

- **`dti`**: Debt-to-income ratio.
- **`earliest_cr_line`**: Date of the borrower’s earliest credit line.
- **`open_acc`**: Number of open credit accounts.
- **`revol_bal`**: Total credit revolving balance.
- **`revol_util`**: Revolving line utilization rate.

### Additional Features:

- **`purpose`**: Purpose of the loan (e.g., debt consolidation, home improvement).
- **`addr_state`**: Borrower's state of residence.
- **`issue_d`**: Loan issue date.
- **`total_acc`**: Total number of credit accounts.

---

## **Workflow**

1. **Data Preprocessing**:

   - Handle missing values for both numerical and categorical features.
   - Encode categorical variables (e.g., `grade`, `purpose`) using suitable encoding techniques.
   - Normalize numerical features like `int_rate`, `loan_amnt`, etc.

2. **Exploratory Data Analysis (EDA)**:

   - Visualize borrower demographics and loan characteristics.
   - Analyze correlations between variables such as `int_rate`, `grade`, and `loan_status`.
   - Identify patterns in defaults based on borrower attributes and loan terms.

3. **Model Development**:

   - Use binary classification models (e.g., Logistic Regression, Random Forest, XGBoost) to predict loan defaults.
   - Evaluate model performance using metrics such as precision, recall, F1-score, and accuracy.
   - Address data imbalance using techniques like SMOTE, undersampling, or oversampling.

4. **Insights and Recommendations**:

   - Identify factors most predictive of loan defaults.
   - Provide actionable recommendations to minimize credit risk.

---

## **Technologies Used**

- **Programming Language**: Python
- **Libraries**: pandas, numpy, matplotlib, seaborn, scikit-learn, imbalanced-learn, XGBoost
- **Tools**: Jupyter Notebook, Power BI (optional for visual dashboards)

---

## **Key Challenges**

1. **Imbalanced Dataset**: The dataset is skewed, with more "Fully Paid" loans than "Default" or "Charged Off".
2. **Missing Data**: Features like `emp_length` and `revol_util` may contain missing values that need imputation.
3. **Feature Engineering**: Handling time-based features (`earliest_cr_line`, `issue_d`) and deriving meaningful insights.
4. **Overfitting**: Ensuring the model generalizes well by validating performance on unseen test data.

---

## **Results**

- **Random Forest Performance**:
  - **Accuracy**: \~100%
  - **Precision**: Perfect for both classes.
  - **Recall**: High, but slightly lower for the minority class.
  - **F1-Score**: Balanced and robust performance.

These metrics indicate strong predictive capability, but validation on unseen data is essential to confirm generalizability.

---

## **Conclusion**

This project demonstrates the effective use of the Lending Club Loan Dataset for credit risk prediction. By leveraging EDA and machine learning models, we can:

- Identify high-risk loans.
- Understand the driving factors behind loan defaults.
- Provide insights to mitigate risks for lenders.

### **Next Steps**:

1. Validate the model with an independent test dataset.
2. Explore advanced techniques like feature selection and hyperparameter tuning.
3. Deploy the model for real-time predictions.

