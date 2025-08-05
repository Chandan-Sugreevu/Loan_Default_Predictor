Loan Default Predictor
This project aims to select the most suitable and optimal machine learning model that accurately predicts loan default based on loan and borrower information, financial indicators, collateral details, and more. Loan default prediction is treated as a binary classification problem where each loan is classified as either default (non-payment) or non-default (successful repayment).

Dataset Description
The dataset contains 67,463 entries with 35 columns, including features such as Loan Amount, Funded Amount, Interest Rate, Loan Title, Debit to Income, etc. The target column is ‘Loan Status’ with values 0 (non-default) and 1 (default).

Data Exploration and Preprocessing
Removed attributes with single unique values (e.g., Loan Title, Payment Plan, Accounts Delinquent).

Converted categorical variables to numerical using LabelEncoder and ordinal mappings to maintain inherent order.

Checked for missing values with none found.

Analyzed correlation matrix but did not drop features due to low correlation.

Detection of Outliers
Used box plots to visually detect outliers in several features (e.g., Funded Amount Investor, Interest Rate, Debit to Income).

Applied Interquartile Range (IQR) method to cap outliers at upper and lower limits, reducing skewness.

Handling Imbalance
The dataset is imbalanced with 61,222 non-default and 6,241 default entries.

Compared oversampling and undersampling; oversampling the minority class yielded better model performance.

After oversampling, dataset size increased to 122,444 entries.

Model Selection and Training
Split data into 70% training and 30% testing.

Considered various models: K-Nearest Neighbors, Gaussian Naive Bayes, Logistic Regression, XGBoost, Decision Tree, and Random Forest.

Performed hypertuning to improve performance.

Random Forest demonstrated the best performance with accuracy close to 1.0, outperforming Decision Tree and other models.

Conclusion
This project demonstrates the application of machine learning techniques for loan default prediction. The Random Forest model is highly effective due to its robustness against overfitting, ability to handle imbalanced data, and feature importance estimation. This solution aids in risk assessment and informs better financial decision-making.
