# Fraud Detection
Predicting Fraudulent Transactions in Financial Data
Overview
This project focuses on developing a predictive model to detect fraudulent transactions for a financial company. The dataset, consisting of 6,362,620 rows and 10 columns, provides valuable information about various transaction types, transaction amounts, customer details, and labels indicating whether a transaction is fraudulent.

The primary objective of this project is to build a machine learning model capable of identifying potentially fraudulent transactions in real-time. By doing so, the financial company aims to mitigate the risks associated with fraudulent activities and protect its customers' accounts.

Data Description
The dataset used in this project contains the following columns:

step: A unit of time in hours, where 1 step represents 1 hour.
type: Transaction type, including CASH-IN, CASH-OUT, DEBIT, PAYMENT, and TRANSFER.
amount: The amount of the transaction in the local currency.
nameOrig: The customer who initiated the transaction.
oldbalanceOrg: The initial balance before the transaction.
newbalanceOrig: The new balance after the transaction.
nameDest: The customer who is the recipient of the transaction.
oldbalanceDest: The initial balance of the recipient before the transaction (excluding merchant accounts).
newbalanceDest: The new balance of the recipient after the transaction (excluding merchant accounts).
isFraud: A binary label indicating whether the transaction is fraudulent (1) or not (0).
isFlaggedFraud: A binary label that flags illegal attempts, such as transferring more than 200,000 in a single transaction (1 for flagged, 0 for not flagged).
Project Steps
The project can be divided into the following key steps:

Data Exploration and Preprocessing: Initial data exploration was performed to understand the dataset's characteristics, identify missing values, and preprocess the data. This included handling categorical variables, scaling numerical features, and addressing class imbalance.

Model Selection: Several machine learning models were considered for fraud detection, including Logistic Regression, XGBoost, Support Vector Machine (SVM), and Random Forest Classifier. Each model was trained and evaluated on relevant metrics.

Data Balancing: Due to class imbalance (only 361 fraudulent cases out of 600,250), the dataset was balanced using Synthetic Minority Over-sampling Technique (SMOTE) to improve the model's performance.

Model Training and Evaluation: All selected models were trained on the balanced dataset. Training and validation datasets were used to assess model performance. The primary evaluation metric used was ROC-AUC score, considering the trade-offs between true positive and true negative rates.

Best Model Selection: Based on ROC-AUC scores, the best-performing model was identified and selected as the final model for detecting fraudulent transactions.

Confusion Matrix Visualization: The confusion matrix for the best model, XGBoost, was plotted to provide a detailed breakdown of its performance in terms of true positives, true negatives, false positives, and false negatives.

Conclusion
This project successfully developed a predictive model, leveraging machine learning techniques, to detect fraudulent transactions in financial data. The selected XGBoost model demonstrated strong performance in terms of ROC-AUC score, making it a valuable tool for real-time fraud detection.

The project's findings and model outcomes provide the financial company with an effective means of identifying and preventing potentially fraudulent activities, enhancing the security of customer accounts, and safeguarding financial assets.

Future Work
For future work, the project could be extended in the following ways:

Continuous model monitoring and retraining to adapt to evolving fraud patterns.
Integration of real-time data streams for immediate fraud detection.
Incorporation of additional features or external data sources to improve model performance.
Implementation of advanced anomaly detection techniques for enhanced fraud detection capabilities.
Acknowledgments
The project makes use of a financial dataset, and we acknowledge the data provider for making it available for analysis.

References
No specific external references were used in this project.
