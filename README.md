Context
Thera Bankis a US bank that has a growing customer base. The majority of these customers are liability customers (depositors) with varying sizes of deposits. The number of customers who are also borrowers (asset customers) is quite small, and the bank is interested in expanding this base rapidly to bring in more loan business and in the process, earn more through the interest on loans. In particular, the management wants to explore ways of converting its liability customers to personal loan customers (while retaining them as depositors).
A campaign that the bank ran last year for liability customers showed a healthy conversion rate of over 9% success. This has encouraged the retail marketing department to devise campaigns with better target marketing to increase the success ratio.

As a Data scientist at Thera Bank have to build a model that will help the marketing department to identify the potential customers who have a higher probability of purchasing the loan.

Motivation : To understand Logistic regression and Decision tree and explore this algorthims using Sklearn, Statmodel, Roc-Auc Curve,Precision Curve,Sequential feature selection, hyperparamter tuning Decision tress and post pruning Decision trees

Data Set
ID: Customer ID
Age: Customer’s age in completed years
Experience: #years of professional experience
Income: Annual income of the customer (in thousand dollars)
ZIP Code: Home Address ZIP code.
Family: the Family size of the customer
CCAvg: Average spending on credit cards per month (in thousand dollars)
Education: Education Level. 1: Undergrad; 2: Graduate;3: Advanced/Professional
Mortgage: Value of house mortgage if any. (in thousand dollars)
Personal_Loan: Did this customer accept the personal loan offered in the last campaign?
Securities_Account: Does the customer have securities account with the bank?
CD_Account: Does the customer have a certificate of deposit (CD) account with the bank?
Online: Do customers use internet banking facilities?
CreditCard: Does the customer use a credit card issued by any other Bank (excluding All life Bank)?
Problem
To predict whether a liability customer will buy a personal loan or not.
Which variables are most significant.
Which segment of customers should be targeted more.
Does Age have any impact of customer buying loan?
Do people with less income borrow loans .?

Key Findings:
Using GridSearch for Hyperparameter tuning of our tree model
Grid search is a tuning technique that attempts to compute the optimum values of hyperparameters.
It is an exhaustive search that is performed on a the specific parameter values of a model.
The parameters of the estimator/model used to apply these methods are optimized by cross-validated grid-search over a parameter grid.
Let's see if we can improve our model performance even more.

Conclusion
We analyzed the Personal Loan campaign data using EDA and by using different models like Logistic Regression and Decision Tree Classifier to build a likelihood of Customer buying Loan.
First we built model using Logistic Regression and performance metric used was Recall. The most important features for classification were Income,Education, CD account ,Family and CCAvg .
Coefficient of Income, Graduate and Advanced Education, Family_3,Family 4,CCavg,CD account,Age, are positive , ie a one unit increase in these will lead to increase in chances of a person borrowing loan
Coefficient of Securities account,online ,Family_2 credit card are negative increase in these will lead to decrease in chances of a person borrowing a loan.
We also improved the performance using ROC-AUC curve and optimal threshold .This was best model with high recall and accuracy .
Decision tree can easily overfit. They require less datapreprocessing compared to logistic Regression and are easy to understand.
We used decision trees with prepruning and post pruning. The Post pruning model gave 96 % recall with 97% accuracy.
Income, Customers with graduate degree, customers having 3 family members are some of the most important variables in predicting if the customers will purchase a personal loan.

Recommendation
Decision trees doesn't require to much data preparation or handling of outliers like logistic regression. They are easy to understand. Decision tress can easily overfit , so we have to be careful using decision tree.
Based on EDA, logistic Regression , Decision tree , Income ,Educatoin,Family,CCavg are most important factor.
Customers who have income above 98k dollars , Advance/graduate level education, a family of more than 2, such customers have higher chances of taking personal loans.
So for this campaign we can have different profiles for customers.
High Profile Clients :-Higher income,Advanced/Graduate level education, 3 /4 Family members,high spending
Average Profile :- Medium income group,Graduate level education.3/4Family members,medium spending
Low Profile:-Lower income group,undergrads ,3/4Family Member,low spending
Customer Average Spending and Mortages can also be looked upon as based on EDA and logistic Regression this parameters also play some role in likelihood of buy loan.
We can 1st target high profile customers , by providing them with a personal relationship managers who can address there concerns and can pursue them to buy loan from the bank with completive interest rates.
Prequalifying for Loan can also attract more customers.
Our 2nd target would be Medium profile customers.
The model cannot identify well if there are some exceptional cases when low profile customer is ready to buy a personal loan.
