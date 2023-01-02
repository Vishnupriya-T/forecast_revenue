# forecast_revenue
Revenue forecast as the foundation for dynamic pricing

Business Problem:
Real-time automated price generation moves into focus for online retailers. Every day, category
management faces the challenge of adapting thousands of products to changing market factors.
We can easily predict the revenue when the prices are static but it is challenging to predict the
revenue when the prices are generated dynamically. This happens completely automatically
when using an intelligent pricing tool. Prices reflect customer appreciation and lead to increased
sales.
To help better understand the influence of Dynamic pricing on revenue and make more accurate
revenue predictions, we will develop a statistical model for predicting future revenue using
historical anonymised transaction data of a real mail-order pharmacy found online. The special
feature of this dataset is the product prices were dynamically generated automatically.

Dataset:
This dataset has around 660K rows with 21 Attributes. It contains the details of a 30 day
transaction of a pharmacy. It has information about products being sold and their information
like competitor price, revenue, manufacturer etc.
Approach:
1. Data Preprocessing
All features were analyzed to identify potential outliers and relationships among them. Further,
to hold significant information, missing values have been handled using KNN Imputer and other
strategies.
2. Data Transformation
Following is the pipeline we have created to apply encoding and scaling to the attributes based
on its characteristics and values. We did frequency encoding (which has more than 50 categories
in order to get rid of the curse of dimensionality) and one hot encoding for the categorical
columns.

Fig (a): Pipeline Transformer 
For features having outliers, robust scaling was applied and for other features, standard scaler has been used after studying them. 
3. Data Modeling 
There are many different statistical models that we can use to predict revenue when prices are dynamic. Ultimately, the best model for predicting revenue when prices are dynamic will depend on the characteristics of the data and the specific goals of the prediction. It is necessary to try out various models and compare their performance in order to find the one that works best. Hence, we have applied the following regression models which we felt suitable for this. 
- Linear Regression (Linear, Lasso and Ridge) 
- Decision tree models (Decision Tree, Random Forest and XGBoost regressors) - SVM Regression 
- KNN Regression 
We have obtained above results in which tree models such as Random Forest and XGBoost regressors worked better among all. 
