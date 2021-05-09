## Credit-card-fraud-detection: Project overview
The objective of this project was to build a machine learning model to detect fraudulent credit card transactions from given data. The Kaggle dataset used in this notebook can be found [here](https://www.kaggle.com/mlg-ulb/creditcardfraud). In this project we will also explore some of the techniques that are used to handle class imbalance in machine learning problems. We also use this problem to illustrate the concept of example dependent cost sensitive learning. (Every case in the dataset has different cost implications based on the transaction amount and the prediction made by the model)

## Approach
We approach the problem from two perspectives, first trying to use traditional ML models which minimize misclassification ignoring the financial costs and second by trying to minimize the cost while allowing higher missclassfication. We will choose the best model basis the cost savings instead of traditional measures like F1-score, given the financial and reputational implications of credit card frauds.
Following three methods have been illustrated to explore this:
1. Traditional ML models which try to which minimize misclassification (Using Logistic regression and Random forest algorithms)
2. Cost sensitive classification using Bayes minimum risk classifier
3. Threshold optimization to minimize costs
The approaches 2 and 3 are illustrate two ways of dealing with class imbalance in machine learning problems.

## Results & outcome
We see that the Random forest classifer with threshold optimization gives us the best result. We are able to achieve cost savings of 81% using a threshold of 0.0408. It is worth noting that the models which give the most cost savings are not necessarily the ones with best F1-score indicating that we have allowed for higher misclassification in order to achieve the best financial outcome.

|Model version|f1 score|Cost savings|
|-------------|--------|------------|
|Logistic regression|||
|Random forest classifier|||
|Logistic regression with Bayes minimum risk classifier|||
|Random forest with Bayes minimum risk classifier|||
|Logistic regression with threshold optimization|||
|Random forest with threshold optimization|||
