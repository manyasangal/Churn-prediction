# Churn-prediction

1.INTRODUCTION

For any service company that bills on a recurring basis, a key variable is the Churn rate. Customer churn occurs when customers or subscribers stop doing business with a company or service, also known as customer attrition. It is also referred as loss of clients or customers. I have used Machine Learning to predict Churn Rate using various algorithm for telecom industry. It can help the company develop Business Strategies to avoid/reduce the loss of business.

2. MOTIVATION

Having worked with several telecom clients in the past, I noticed that Customer Churn is the greatest threat to a  telecom’s business. If a telecom provider is able to predict the possibility of a customer churning from their subscription, it is possible to retain the customer through certain offers. This can save telecom company a lot of business.

3. DATA

The data contains following 21 fields:
1. CustomerID
2. Gender : female, male
3. SeniorCitizen  : Whether the customer is a senior citizen or not (1, 0)
4. Partner : Whether the customer has a partner or not (Yes, No)
5. Dependents : Whether the customer has dependents or not (Yes, No)
6. Tenure : Number of months the customer has stayed with the company
7. PhoneService  : Whether the customer has a phone service or not (Yes, No)
8. MultipleLines  : Whether the customer has multiple lines r not (Yes, No, No phone service)
9. InternetService : Customer’s internet service provider (DSL, Fiber optic, No)
10. OnlineSecurity  : Whether the customer has online security or not (Yes, No, No internet service)
11. OnlineBackup : Whether the customer has online backup or not (Yes, No, No internet service)
12. DeviceProtection : Whether the customer has device protection or not (Yes, No, No internet service)
13. TechSupport  : Whether the customer has tech support or not (Yes, No, No internet service)
14. StreamingTV  : Whether the customer has streaming TV or not (Yes, No, No internet service)
15. StreamingMovies : Whether the customer has streaming movies or not (Yes, No, No internet service)
16. Contract : The contract term of the customer (Month-to-month, One year, Two year)
17. PaperlessBilling : Whether the customer has paperless billing or not (Yes, No)
18. PaymentMethod : The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
19. MonthlyCharges : The amount charged to the customer monthly — numeric 
20. TotalCharges : The total amount charged to the customer — numeric
21. Churn : Whether the customer churned or not (Yes or No). It is our target variable.

STEPS:

1)	Data Cleaning  :
•	For example “No internet Service” was replaced by “No” to make the data uniform.
•	All the missing values were removed. 
•	Minimum tenure is 0 months and maximum is 82 months. So, I created 5 tenure groups:
0-12 months, 12-24 months, 24-48 months, 48-60 months and >60 months

2)	Data Analysis and Visualisation :
•	For analyzing the data, I create visuals like Bar plots and various other graphs using ggplot in R for various categorical variables. 
•	This helps me visualize the distribution of Churn and Non Churn for each category. 
•	It can let me decide various insignificant variables and I can eliminate those fields from data before moving ahead with Machine Learning algorithms (Variable Reduction)

3)	After Data Preprocessing, I split the data into Taining Data(70%) and Test Data(30%) to apply various Machine Learning Algorithms.
4)	I move ahead and go on applying various algorithms like Logistic Regression, Decision Trees and Random Forest.
5)	The purpose of applying all these algorithms is to test and determine that which algorithm is giving us the best results on Historic Data. 
6)	The best result can be based on various statistical factors like  High Accuracy or Low Misclassification Cost depending on the Business Needs.
7)	Whichever algorithm gives the best result should be used by the business to predict Churn and accordingly develop Business Strategies. 
8)For this data set, I got best results with Logistic Regression(Accuracy of slightly more than 80.5%)

Note: More detailed explanation for each step has been provided along with the code in ChurnPredict.rmd




