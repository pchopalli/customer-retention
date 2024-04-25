# Prediction Model for Customer Retention
___
Customer behavior prediction is used by many companies to understand the behavior of their customers. The dataset wcontains information about customers who stayed with the provider and those who switched providers, or 'churned'. The goal is to predict the if the customer will churn or not using the various features like services utilized by the customer, demographics etc.

Better understanding which customers are likely to switch to a different provider can help the company target their services and advertising to the most at-risk customers so as to improve their customer retention. If done successfully, this can help the company maximize their profits.

This program performs a number of functions. In the first few cells, we import the data set from a csv file, and then we run several commands to evaluate the structure of the dataset, such as printing the data types and number of missing values of each of the variables. In the next section, we create visualizations of the data in order to perform an exploratory data analysis.

Implemented below steps
Upsampling the minority feature in order to make the yes and no observations closer to equal. Drop missing values in the total charges variable, before creating a correlation matrix. Feature selection, and drop the target variable (churn) from the data frame, before using "kbest" to find the best independent variables for the models based on their chi-squared scores. This analysis tells us that the best features to use in are as follows: SeniorCitizen Dependents tenure OnlineSecurity OnlineBackup DeviceProtection TechSupport Contract MonthlyCharges TotalCharges.

Build a pipeline that uses standard scaler for numerical features and one-hot encoding for categorical features. Apply label encoding on the target variable (churn). Deploy seven models: logistic regression, decision tree, random forest, extra tree classifier, Gaussian Naive Bayes, logistic regression with PCA, and SVM. Also tune the hyperparameters for the first three models to see if that improves accuracy.

For this project,analyzed customer churn data to evaluate what model would best predict a customers likelihood of changing service providers based on a number of independent factos, such as whether they purchased device protection and whether they had dependents. Overall, the random forest model with default parameters is the most accurate for this data set, and would be the best choice for analyzing this data set and improving customer retention. This model predicts customer churn with over 90% accuracy.

<br></br>
<table >
<tr><th >Model <th><th> Accuracy <tr><tr>
<tr><td> Logistic Regression <td><td> 76.22 <td><tr>
    <tr><td> Stocashtic Gradient <td><td> 75.44 <td><tr>
        <tr><td> Decision Tree  <td><td> 88.88 <td><tr>
            <tr><td> Random Forest <td><td> 90.29 <td><tr>
                <tr><td> Extree Tree  <td><td> 89.86 <td><tr>
                    <tr><td> Gaussian Naive Bayes  <td><td> 75.25 <td><tr>
                         <tr><td> Logistic with PCA  <td><td> 74.86 <td><tr>
                        <tr><td> SVM  <td><td> 75.83 <td><tr>
<table>


