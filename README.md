# CreditCardFraudDetection
## Our dataset

 
Due to confidentiality issues, we cannot provide the original credit card numbers, so they have been transformed with PCA transformation into numerical values. 
PCA (Principal Component Analysis ) is a dimensionality reduction technique that transforms a set of features in a dataset into a smaller number of features called principal components while at the same time trying to retain as much information in the original dataset as possible.
Other advantages:
Improves machine learning algorithm performance.
With the number of features reduced with PCA, the time taken to train your model is now significantly reduced.

## What models will we use?
Our data depends on , the target value (in ‘Class’ column) is having categorical values:
1 for fraud
0 for non-fraud
So this is a binary classification problem, that’s why we are going to use different classification algorithms:
Logistic Regression
Decision Tree Classifier
Random Forest Classifier

## Why do we use logistic regression?
Logistic regression is commonly used for prediction and classification problems. Some of these use cases include Fraud detection.

## Why do we use  Decision Tree classifier?
Decision Tree is one of the easiest and popular classification algorithms to understand and interpret.
It belongs to the family of supervised learning algorithms. Unlike other supervised learning algorithms, the decision tree algorithm can be used for solving regression and classification problems too.
The goal of using a Decision Tree is to create a training model that can use to predict the class or value of the target variable by learning simple decision rules inferred from prior data(training data).

It can be of two types:
Categorical Variable Decision Tree: Decision Tree which has a categorical target variable then it called a Categorical variable decision tree.
Continuous Variable Decision Tree: Decision Tree has a continuous target variable then it is called Continuous Variable Decision Tree.

In our case we are going to use Categorical Variable Decision Tree. 

## Why do we use  Random forest classifier?
Random Forest Algorithm is a supervised machine learning algorithm which is extremely popular and is used for Classification and Regression problems in Machine Learning.

Random Forest is a classifier that contains several decision trees on various subsets of the given dataset and takes the average to improve the predictive accuracy of that dataset.
 Instead of relying on one decision tree, the random forest takes the prediction from each tree and based on the majority votes of predictions, and it predicts the final output.
 
## Unbalanced data
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the frauds represent 0.172% of all transactions.

## What happens if we don’t handle unbalanced data?
Compared to accuracy, precision, recall and f1 scores are too low.
This is because of the highly unbalanced data.
We will have the same problem in every other model.

Note: it’s very dangerous to use ONLY the accuracy score as a metric!
 We have to check precision, recall and f1 scores if our data is unbalanced.
![image](https://github.com/RawanGamil/CreditCardFraudDetection/assets/131316628/f2f98ba6-6508-4065-9d29-7c84e85465f7)

## Handle unbalanced data
To handle unbalanced data, we can choose to methods: 
### Oversampling: 
getting all the classes to the same amount as the minority class by removing data from the majority class
### Undersampling: 
duplicating or creating new synthetic data values in the minority class until it reaches the same amount of majority class.
![image](https://github.com/RawanGamil/CreditCardFraudDetection/assets/131316628/7fb1a3f4-3cbc-4be8-ad52-d236d93d9a06)

## After underbalancing 
After performing undersampling, we can see that Logistic Regression is the best model for this dataset. 
But the problem with undersampling is that we lose a lot of valuable data, so we are going to perform oversampling and see if we still get the same results.

![image](https://github.com/RawanGamil/CreditCardFraudDetection/assets/131316628/bf5ae36e-ae99-4c89-a8f7-b23cf77782c3)
![image](https://github.com/RawanGamil/CreditCardFraudDetection/assets/131316628/551cbfa8-f106-4fa7-91ac-dd45e302a868)

## After Oversampling
We are going to use SMOTE to perform oversampling. It stands for Synthetic Minority Oversampling Technique.
Unlike random oversampling, SMOTE doesn't duplicate data, but rather, it creates  synthetic data points that are  slightly different versions from the original data. It create new data based on the old data we have, NOT randomly.

After performing undersampling, we can see that Random Forest is the best model for this dataset. 
![image](https://github.com/RawanGamil/CreditCardFraudDetection/assets/131316628/6942932e-fbf2-444b-9129-d827037c1035)
![image](https://github.com/RawanGamil/CreditCardFraudDetection/assets/131316628/24447cdd-d490-4c8f-bda9-cf30f8a75d81)


















































