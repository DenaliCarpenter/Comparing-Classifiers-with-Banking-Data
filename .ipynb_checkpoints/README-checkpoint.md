# Comparing Classification Algorithms

This repository contains an analysis and predictive modeling project comparing classification algorithms on Portuguese banking data. The objective is to identify potential subscribers to term deposits during telemarketing campaigns using multiple machine learning models.

## Project Structure
- Jupyter Notebook: Comparing_Classifiers_on_Portuguese_Banking_Data.ipynb contains all the code, analysis, and results.
- Data: Includes preprocessed and cleaned data with detailed steps for imputation, outlier handling, and feature transformations. The raw data can be found in the data folder.
- README: Provides an overview of the project, methods, and key findings.

## Summary of Findings

### Business Context
- Objective: Develop a classification algorithm to predict whether a customer will subscribe to a term deposit during incoming or outgoing telemarketing calls.
- Use Case: This model enables efficient resource allocation by identifying likely subscribers, reducing costs, and enhancing the campaign’s success.

### Data Summary
- Dataset:
    - 41,188 rows and 21 columns (20 features and 1 target variable).
- Target Variable:
    - y, indicating subscription (1 for yes, 0 for no).
- Key Preprocessing Steps:
    - Removal of duplicates and outliers (final dataset: 37,924 rows, 19 columns).
    - Encoding of categorical variables and handling missing values.
    - Scaling numeric features.

### Modeling and Results
- Models Used:
    - Logistic Regression
    - K-Nearest Neighbors (KNN)
    - Decision Tree
    - Support Vector Machines (SVM)
- Evaluation Metrics:
    - Accuracy,
    - Precision,
    - Recall,
    - and F1 Score, with a focus on F1 to balance precision and recall due to class imbalance.
- Findings:
    - SVM achieved the highest F1 Score but required the longest training time.
    - The Decision Tree performed best after hyperparameter tuning, balancing training time, and predictive performance.
    - Dummy classifier established a baseline accuracy of 89% by predicting the majority class.
- Key Insights:
    - Feature importance analysis and Chi-Square tests highlighted key predictors, including job, marital, and education.
    - Imbalanced target variable (89% no, 11% yes) necessitated careful evaluation beyond accuracy.

### Recommendations
1.	Model Selection: Use the Decision Tree model for initial implementation. Explore Random Forest for further improvement.
2.	Feature Engineering: Refine the dataset by focusing on features showing strong correlations or statistical significance.
3.	Next Steps:
    - Experiment with SMOTE to address class imbalance.
	- Optimize hyperparameters for all models through GridSearchCV.
	- Validate results using additional performance metrics.
