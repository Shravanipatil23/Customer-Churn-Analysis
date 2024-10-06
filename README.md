# Customer Churn Analysis using 'Random Forest Classifier' Machine learning Algorithm.


## Problem Statement: Online Retail Customer Churn Prediction.


## Overview:
Customer churn is a significant issue for businesses, especially in highly competitive markets like online retail. Understanding why customers leave and predicting which customers are at risk of churning is crucial for implementing retention strategies. This project focuses on developing a predictive model to identify potential customer churn in an online retail business, allowing the company to take proactive measures to retain valuable customers.

### Objective:
The goal of this project is to build a machine learning model that predicts whether a customer will churn (i.e., stop purchasing) based on historical retail data. The model will help the business understand churn patterns and take data-driven actions to reduce customer attrition.

### Dataset:
The dataset contains information about online retail customers, including their purchase history, demographics, and engagement metrics. Each record represents a customer, and the target variable is whether the customer has churned.

### Key Features:
- Customer ID: Unique identifier for each customer.
- Age: The age of the customer.
- Annual Income: The customer’s yearly income.
- Total Spend: The total amount the customer has spent at the online store.
- Number of Purchases: Number of purchases made by the customer.
- Years as Customer: Duration (in years) that the customer has been with the company.
- Promotion Response: Whether the customer responded to promotional offers.
- Satisfaction Score: Customer satisfaction score based on surveys.
- Churn: The target variable indicating whether the customer has churned (1) or not (0).

### Approach:
#### Data Preprocessing:

- Handled missing values and clean the dataset.
- Feature engineering, including encoding categorical variables and scaling numerical data.
- Model Building:

Developed a Random Forest Classifier to predict customer churn.
Split the data into training and testing sets.
Evaluated the model using appropriate metrics like accuracy, precision, recall, and F1-score.
- Model Evaluation:

Analyzed feature importance to understand key drivers of churn.
- Visualization in Power BI:

Exported the model’s predictions and import them into Power BI for creating interactive visualizations.
Visualized churn rates, customer behavior trends, and important features contributing to churn.
- Outcome:
 
A machine learning model that predicts customer churn with high accuracy. The business can use the predictions and insights from the analysis to identify at-risk customers and implement targeted retention strategies, reducing customer attrition and improving overall profitability.

#### Steps followed
Step 1 : Imported pandas, matplotlib and seaborn. Used pandas to load the dataset into a DataFrame. Data was a csv file. Inspected the data using functions head(), info(), and describe() to understand its structure and get an overview of the features available for analysis.

Step 2 : Checked for missing values by using function isnull().sum(). There were no missing values, the sum returned was 0 for all the columns of the table.

Step 3 : Imported required Libraries for ML Model. Libraries: train_test_split, LabelEncoder, StandardScaler. Copied the original data to avoid altering of values of the original dataset.

Step 4 :Encoded Categorical Columns using LabelEncoder. Stored the relevent columns in X and y for further training and testing purpose. Droped the unnecessary columns while storing in X and y.

Step 5 : Scaled th columns to a standard scale using StandardScaler to avoid False prediction caused by different scales of the columns.

Step 6 : Splitted the data into training and testing using train_test_split.

Step 7 : Imported RandomForestClassifier for classification and prediction. Imported classification_report and accuracy_score to view score metrics.

Step 8 : Trained the training data with RandomForestClassifier and checked accuracy score and classification report. predicted the churn and stored it into a column named "Predicted_churn".

Step 9 : With checking of the accuracy Score and classification report, following is the analyis of the classification report:

Precision:

For False (class 0): 0.51 For True (class 1): 0.55 Overall, this means that out of all the instances predicted as False or True, 51% and 55% were correct, respectively.

Recall:

For False (class 0): 0.37 For True (class 1): 0.69 Recall measures the ability of the model to find all the positive samples. It shows that 37% of actual False instances were correctly classified, while 69% of actual True instances were correctly classified.

F1-Score:

For False (class 0): 0.43 For True (class 1): 0.61 F1-score is the harmonic mean of precision and recall, which balances the two. A higher F1-score indicates a better balance between precision and recall.

Support:

Number of instances in each class (94 False, 106 True).

Accuracy:

The overall accuracy is 54%, meaning the model correctly classified 54% of the instances out of 200.

Macro Average:

Macro average calculates the unweighted mean of the precision, recall, and F1 scores for both classes. Precision: 0.53, Recall: 0.53, F1-score: 0.52.

Weighted Average:

Weighted average takes into account the support (the number of instances) for each class when averaging precision, recall, and F1-score. Precision: 0.54, Recall: 0.54, F1-score: 0.53.

The report suggests that the model has moderate performance, with better performance for the True class than the False class.

Step 10 : Prepared the predictions for export to CSV. Saved the dataset with predictions (churn_predictions.csv) for further analysis and visualization.

Step 11 : Loaded the churn_predictions.csv file into Power BI for creating interactive visualizations.

### Insights:
Two page report was created on Power BI Desktop.

#### Page 1
Snapshot: 

<img width="431" alt="Churn_analysis" src="https://github.com/user-attachments/assets/0567e64f-c745-4e2b-a0dc-90b9684ce387">

- Total Number of Customers - 200 Satisfaction Score - 3000
- Predicted Churn By Years joined:
  - 28.00% customers churned of 6-10 years of joining.
  - 27.00% customers churned of 1-5 years of joining.
  - 23.00% customers churned of 11-15 years of joining.
  - 22.00% customers churned of 16-20 years of joining.
- Promotion Response:
  - 361 (36.1%) of customers Unsubscribed.
  - 338 (33.8%) of customers Responded.
  - 301 (30.1%) of customers Ignored.
- Predicted Churn by Income Group:
  - 55 (27.5%) of Predicted Chruned customers belonged to 1.5L to 2L.
  - 55 (27.5%) of Predicted Chruned customers belonged to 1L to 1.5L.
  - 50 (25%) of Predicted Chruned customers belonged to 50K to 1L.
  - 40 (20%) of Predicted Chruned customers belonged to 0 to 50K.
Customer Id by Gender and Predicted Churn:
  - 61.76% of females will be churned.
  - 77.94% of other gender will be churned.
  - 57.81% of males will be churned.
- Customer Id by Satisfaction Score and Predicted Churn:
  - As the satisfaction score decreases the customer churn increases signinficantly.
- Customer ID by Age Group and Predicted Churn:
  - Age group of '0-20', 11 customers may churn.
  - Age group of '21-40', 52 customers may churn.
  - Age group of '41-60', 51 customers may churn.
  - Age group of '60 and above', 18 customers may churn.
The table gives a brief idea and showcases deep insights of the customers and their information which contributes to stastical prediction of the churned customers in the near future.

#### Page 2
Snapshot: 

<img width="410" alt="Customer analysis" src="https://github.com/user-attachments/assets/9800dc1f-c3b3-44bd-a7c5-f9944a4b4d03">

This Power BI report provides a comprehensive overview of customer information for an online retail store. Through interactive visualizations, key customer demographics such as age, income, and years as a customer are highlighted. The report also explores customer behavior, including total spend, number of purchases, and promotional responses. This data-driven report allows the business to better understand its customer base and identify at-risk customers for targeted retention strategies.
