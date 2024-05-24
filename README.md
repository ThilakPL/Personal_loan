Predicting Personal Loan Acceptance
Overview

Welcome to the Predicting Personal Loan Acceptance project repository. This project aims to build a predictive model to identify potential customers who are likely to accept a personal loan offer. This model will help in targeted marketing strategies to enhance loan acceptance rates.

Context
Thera Bank, a US bank with a growing customer base, primarily serves liability customers (depositors) and has a smaller base of asset customers (borrowers). To expand its loan business and earn more through loan interest, the bank aims to convert more liability customers into personal loan customers while retaining them as depositors.

A previous campaign achieved over a 9% conversion rate, encouraging the retail marketing department to devise better-targeted marketing campaigns to improve this success ratio. As a data scientist, the goal is to build a model to help the marketing department identify customers with a higher probability of purchasing a loan.
Motivation

The primary goal of this project is to understand and implement logistic regression and decision tree algorithms. The project includes:

    Logistic Regression using Sklearn and Statsmodels
    Decision Tree Classifier
    ROC-AUC Curve Analysis
    Precision Curve Analysis
    Sequential Feature Selection
    Hyperparameter Tuning for Decision Trees
    Post-Pruning of Decision Trees

Data Set

The dataset includes various customer attributes:

    ID: Customer ID
    Age: Customer’s age in completed years
    Experience: Number of years of professional experience
    Income: Annual income (in thousand dollars)
    ZIP Code: Home address ZIP code
    Family: Family size
    CCAvg: Average monthly spending on credit cards (in thousand dollars)
    Education: Education level (1: Undergrad, 2: Graduate, 3: Advanced/Professional)
    Mortgage: Value of house mortgage (in thousand dollars)
    Personal_Loan: Target variable indicating whether the customer accepted a personal loan offer
    Securities_Account: Does the customer have a securities account with the bank?
    CD_Account: Does the customer have a certificate of deposit (CD) account with the bank?
    Online: Does the customer use internet banking facilities?
    CreditCard: Does the customer use a credit card issued by any other bank?

Problem Statement

    Predict whether a liability customer will accept a personal loan.
    Identify the most significant variables influencing loan acceptance.
    Determine which customer segments should be targeted more.
    Analyze the impact of age on loan acceptance.
    Investigate whether people with lower income are more likely to borrow loans.

Key Findings

    Logistic Regression: Important features for classification include Income, Education, CD Account, Family, and CCAvg. The model's performance was evaluated using recall, ROC-AUC curves, and optimal threshold.
    Decision Tree: This model requires less data preprocessing, is easy to understand, but can easily overfit. Post-pruning improved the model's performance, achieving 96% recall and 97% accuracy.
    Significant Variables: Income, education level, family size, and average credit card spending are critical factors in predicting loan acceptance.

Conclusion

We analyzed the personal loan campaign data using EDA and built models using logistic regression and decision tree classifiers. The logistic regression model identified key features that influence loan acceptance, while the decision tree model, with post-pruning, achieved high recall and accuracy.
Recommendations

    Decision Trees: Easy to understand and require less data preparation but can overfit; careful use is advised.

    Target Profiles:
        High Profile: High income, advanced/graduate education, 3-4 family members, high spending.
        Average Profile: Medium income, graduate education, 3-4 family members, medium spending.
        Low Profile: Lower income, undergrad education, 3-4 family members, low spending.

    Marketing Strategy: Focus on high-profile customers first, offering personalized relationship managers and competitive interest rates. Prequalifying for loans can attract more customers. Medium-profile customers can be targeted next, while the model may not effectively identify low-profile customers ready to buy a loan.

Thank you for visiting this repository!
