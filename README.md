# Practical-Application-Assignment-17.1-Comparing-Classifiers
Practical Application Assignment 17.1: Comparing Classifiers



## The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit (variable y).


Here's the table converted to markdown format:

| Variable Name | Role    | Type       | Demographic     | Description |
|---------------|---------|------------|-----------------|-------------|
| age           | Feature | Integer    | Age             |             |
| job           | Feature | Categorical| Occupation      | type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown') |
| marital       | Feature | Categorical| Marital Status  | marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed) |
| education     | Feature | Categorical| Education Level | (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown') |
| default       | Feature | Binary     |                 | has credit in default? |
| balance       | Feature | Integer    |                 | average yearly balance |
| housing       | Feature | Binary     |                 | has housing loan? |
| loan          | Feature | Binary     |                 | has personal loan? |
| contact       | Feature | Categorical|                 | contact communication type (categorical: 'cellular','telephone') |
| day_of_week   | Feature | Date       |                 | last contact day of the week |
| month         | Feature | Date       |                 | last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec') |
| duration      | Feature | Integer    |                 | last contact duration, in seconds (numeric). Important note: this attribute highly affects the target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model. |
| campaign      | Feature | Integer    |                 | number of contacts performed during this campaign and for this client (numeric, includes last contact) |
| pdays         | Feature | Integer    |                 | number of days that passed by after the client was last contacted from a previous campaign (numeric; -1 means client was not previously contacted) |
| previous      | Feature | Integer    |                 | number of contacts performed before this campaign and for this client |
| poutcome      | Feature | Categorical|                 | outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success') |
| y             | Target  | Binary     |                 | has the client subscribed a term deposit? |


# Summary
# The Logistic Regression model is the best model for this dataset with the following metrics:
# - Accuracy: 0.91
# - Precision: 0.67
# - Recall: 0.33
# - F1-Score: 0.44
# - ROC-AUC: 0.93
# The most important features for the Logistic Regression model are:
# - euribor3m
# - pdays
# - emp.var.rate
# - cons.price.idx
# - cons.conf.idx
# - nr.employed
# - poutcome
# - previous
# - contact
# - month
# The Decision Tree model has the following metrics:
# - Accuracy: 0.89
# - Precision: 0.53
# - Recall: 0.50
# - F1-Score: 0.52
# - ROC-AUC: 0.73
# The most important features for the Decision Tree model are:
# - euribor3m
# - pdays
# - emp.var.rate
# - cons.conf.idx
# - cons.price.idx
# - nr.employed
# - poutcome
# - previous
# - month
# - contact
# The Support Vector Machine model has the following metrics:
# - Accuracy: 0.91
# - Precision: 0.67
# - Recall: 0.33
# - F1-Score: 0.44
# - ROC-AUC: 0.93
# The most important features for the Support Vector Machine model are:
# - euribor3m
# - pdays
# - emp.var.rate
# - cons.price.idx
# - cons.conf.idx
# - nr.employed
# - poutcome
# - previous
# - contact
# - month
# The K-Nearest Neighbors model was not able to run due to memory limitations.



### Summary Report: Feature Importance Analysis for Customer Response Prediction

#### Introduction
This analysis aims to identify the key features that influence whether a customer will say "Yes" to a bank's offer. By understanding these features, the bank can more effectively focus its marketing and operational strategies to improve customer engagement and conversion rates.

#### Key Features Identified

Based on the analysis from Logistic Regression, Decision Tree, SVM, and KNN models, the following features were identified as significant contributors to customer responses:

1. **Duration**:
    - **Importance**: The call duration is consistently the most influential feature across all models.
    - **Recommendation**: Ensure that customer service representatives engage customers effectively during calls, potentially increasing the length of meaningful conversations to improve conversion rates.

2. **Employment Variation Rate (emp.var.rate)**:
    - **Importance**: Highly significant in the Logistic Regression and SVM models.
    - **Recommendation**: Monitor economic indicators closely, as changes in employment rates can affect customer responses. Tailor marketing strategies during periods of economic variability.

3. **Euribor 3-Month Rate (euribor3m)**:
    - **Importance**: Notable in Logistic Regression and Decision Tree models.
    - **Recommendation**: Consider the Euribor rate when designing financial products and offers, as it influences customer decisions. Highlight benefits in the context of current rates.

4. **Number of Employees (nr. employed)**:
    - **Importance**: Significant across multiple models.
    - **Recommendation**: Align marketing efforts with periods when employment rates are high, as a larger workforce may indicate a more receptive customer base.

5. **Consumer Price Index (cons.price.idx)**:
    - **Importance**: Important in Logistic Regression and SVM models.
    - **Recommendation**: Adjust marketing messages based on inflation and consumer price trends. Emphasize the value and affordability of bank offers during high inflation periods.

6. **Contact Type (contact)**:
    - **Importance**: Influential in Logistic Regression and Decision Tree models.
    - **Recommendation**: Optimize the contact method (telephone vs. cellular). Invest in improving the customer experience through the most effective communication channels.

7. **Month**:
    - **Importance**: Significant in Logistic Regression.
    - **Recommendation**: Analyze seasonal trends and adjust marketing campaigns to align with months that show higher customer responsiveness.

8. **Pdays (number of days since the client was last contacted) and Previous**:
    - **Importance**: Influential in Decision Tree and Logistic Regression models.
    - **Recommendation**: Implement follow-up strategies based on the recency and frequency of past contacts. Prioritize customers with favorable contact histories.

#### Strategic Recommendations

1. **Enhanced Customer Engagement**:
    - Focus on the quality and length of customer interactions during calls.
    - Train representatives to engage customers effectively and provide comprehensive information about the bank's offers.

2. **Economic Condition Monitoring**:
    - Adapt marketing strategies based on economic indicators like employment variation and Euribor rates.
    - Develop flexible offers catering to the economic environment, appealing to customers' financial situations.

3. **Tailored Communication Channels**:
    - Identify the most effective communication channels for different customer segments.
    - Invest in improving the infrastructure and training for the most successful contact methods.

4. **Seasonal and Historical Trends**:
    - Leverage data on monthly trends and customer contact history to optimize time marketing campaigns.
    - Use predictive analytics to identify the best periods for customer outreach.

#### Conclusion

The bank can enhance its customer engagement and conversion rates by focusing on these critical features and implementing the recommended strategies. Tailoring marketing efforts to economic conditions, optimizing communication methods, and understanding customer interaction history are crucial steps in achieving better outcomes in customer response to bank offers.





