# da_module_20
Supervised Machine Learning
The purpose of this model is to assesss the factors related to an individual's credit to predict whether or not they default on a loan. The source data includes the following features: loan size, interest rate, borrower income, debt to income ratio, number of accounts, deragatory marks, and total debt of the borrower. Using this data, the goal is to create a model to answer the binary, yes or no question: Will the borrower default on this loan? The data includes a column for the labled data for loan status. Imbalance in the lables exists, so in splitting the data into a training and test set, stratificiation was used. No encoding or imputation was needed for the dataset. A standard scalar was used for the features in the dataset. 

Multiple machine learning models were tested: a logistic regression,  single decision tree, random forest, support vector classifier, K Nearest Neighbors, Extra trees, AdaBoost algorithm, gradient boost algorithm, and x gradient boost. The performance of the logistic regression and the AdaBoost algorithm will be compared here.

For the logistic regression, the following performance metrics were calculated (weighted average):
* Accuracy: 0.99
* Precision: 1.00
* Recall: 0.99
* F1: 0.99

For the AdaBoost algorithm, the following performance metrics were calcultated (weighted average):
* Accuracy: 0.99
* Precision: 0.99
* Recall: 0.99
* F1: 0.99

While on it's surface, it looks like the logistic regression is the better model with a higher accuracy, there are two additional metrics that should be considered:
* The AUC Score (area under curve of the ROC chart) which is 0.9958 for the logistic regression and 0.9964 for the AdaBoost. It should be noted that because of the imbalance of the dataset, AUC should not be used in isolation as the metric of best performance.
* The count of type II errors, which is 12 for the logistic regression and 5 for the AdaBoost. Given the nature of the problem, type II error should be treated as more sever than type I error and specific intereste should be taken in minimizing it.

For these reasons, the Adaboost model is recommended. It has high accuracy, precision, recall, and F1 scores and performs marginally better than a logistic regression in it's AUC score and minimization of type II error. 