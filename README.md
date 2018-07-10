## Project-3 - Credit Card Fraud Detection using Machine learning Algorithms/Models

This project contains the predictive analysis of the Credit Card Fraud Detection using Machine Learning.

#### Algorithms/models used:
 1. Local Outlier Factor
 2. Isolation Forest Algorithm

#### Data Source: Kaggle.com

#### Description of dataset:

* Place: This dataset contains the transactions made by the credit card by European cardholders
* Time Period: It presents the transactions occurred in two days in September, 2013.
* Number of transactions: 284,807
* Frauds: 492
* Percent of Fraud = 0.172%

Note: As the number of frauds are very less 0.172% of all transactions making the dataset highly unbalanced.

What is PAC (Principal Component Analysis) transformation?
Ref:https://www.lusispayments.com/uploads/4/4/8/2/44826195/a_comparison_of_machine_learning_techniques_for_credit_card_fraud_detection.pdf
https://en.wikipedia.org/wiki/Principal_component_analysis


#### The input variables that are used in this project:

###### 1.PCA (V1,V2...V28 ):
It contains only numerical variables like V1,V2...V28 as a result of PCA transformation in order to protect the sensitive information, like, identity of the individual who made those transactions or the location etc.
These are the principal components obtained with PCA.

###### 2. Inputs with No PCA Transformation:
 Time, Class and Amount

###### 3. Time:
Feature "Time" contains the seconds elapsed between each transaction and first transaction in the dataset

###### 4. Amount
It's the actual transaction amount. This feature can be used for example-dependant cost-sensitive learning.

###### 5. Class
It's a response variable. It takes two values-0 and 1
 1: for success, *Fraud*  in this project
 0:for Failure, *Valid transaction* in this project

#### Language used: Python 3.6.1

#### Libraries used:
 1. Scikit-Learn (for documentation:http://scikit-learn.org/stable/)
    * sklearn.metrics for classification_report, accuracy_score.
    * sklearn.ensemble for IsolationForest.
    * sklearn.neighbors for LocalOutlierFactor.
 2. NumPy (for documentation:http://www.numpy.org/)
 3. Pandas (for documentation:http://pandas.pydata.org/)   
 4. Matplotlib (for documentation:https://matplotlib.org/)
 5. Seaborn (for documentation https://seaborn.pydata.org/)

#### Code file: cc_fraud_detection.ipynb

#### Limitations:
1. Data size: The dataset that we used is 284,807 which is 143 MB. Github has the limit to upload the data, which is 100 MB. So, the last row of dataset is deleted to make smaller size.
There are 100,000 transactions downsizing it to 43 MB now

2. Confusion Matrix is meaningless: The dataset is highly unbalanced as there are very few Fraud transactions as compare to the Valid transactions. In reality it is the best scenario, but for this project it's not useful as Machine will not get enough cases of Frauds to train itself to predict Frauds. So, Confusion Matrix is not meaningful for unbalance classification.

The dataset has been collected and analyzed during a research collaboration of Worldline and the Machine Learning Group (http://mlg.ulb.ac.be) of ULB (Université Libre de Bruxelles) on big data mining and fraud detection.
