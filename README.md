# Credit_Risk_Analysis

## Overview of Analysis

### Purpose:

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I employed different techniques to train and evaluate models with unbalanced classes. I used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.
#### Deliverable 1:
- Using imbalanced-learn and scikit-learn libraries, I evaluated three machine learning models by using resampling to determine which is better at predicting credit risk. First, I used the oversampling RandomOverSampler and SMOTE algorithms, and then the undersampling ClusterCentroids algorithm. Using these algorithms, I resampled the dataset, viewed the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated a classification report.
#### Deliverable 2:
- Using imbalanced-learn and scikit-learn libraries,I used a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, I resampled the dataset, viewed the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated a classification report.
#### Deliverable 3:
- Using imblearn.ensemble I trained and compared two different ensemble classifiers (BalancedRandomForestClassifier and EasyEnsembleClassifier). These algorithms helped me to resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.
## Results
RandomOverSampler model
![Screenshot](https://github.com/salvamike/Credit_Risk_Analysis/blob/main/1.png)
- The balanced accuracy score is 65%.
- The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.
SMOTE model
![Screenshot](https://github.com/salvamike/Credit_Risk_Analysis/blob/main/2.png)
- The balanced accuracy score is 64%.
- The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.
ClusterCentroids model
- The balanced accuracy score is 65%
![Screenshot](https://github.com/salvamike/Credit_Risk_Analysis/blob/main/balancedaccuscore.png)
- The high_risk precision is about 1% only with 61% sensitivity which makes a F1 of 1% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 45%.
![Screenshot](https://github.com/salvamike/Credit_Risk_Analysis/blob/main/1.png)
SMOTEENN model
- The balanced accuracy score is about 62%.
- The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.
- Due to the high number of false positives, the low_risk sensitivity is 57%.
![Screenshot](https://github.com/salvamike/Credit_Risk_Analysis/blob/main/3.png)

BalancedRandomForestClassifier model
- The balanced accuracy score improved to about 79%.
- The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
- Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.
![Screenshot](https://github.com/salvamike/Credit_Risk_Analysis/blob/main/4.png)

EasyEnsembleClassifier model
- The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
- Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.
![Screenshot](https://github.com/salvamike/Credit_Risk_Analysis/blob/main/5.png)

## Summary 
The models we used to discover the credit risk analysis have shown very weak precision when it comes to see if credit risk is high. However, the ensomble models brought some improvement in regards to the sensitivity of the high risk credits. For example, the easyensembleclassifier model shows 92% recall. This says that it can find almost all the high risk credit. Yet with low precisions, many of the low risk credis are wrongly detected as high risk. This would not be good for the bank's credit strategy and infringe on its revenue because it is missing business.
I would not recommend that the bank uses any of these models to predict credit risk.