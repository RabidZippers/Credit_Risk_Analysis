# Credit Risk Analysis

## Overview
Machine learning can be used to predict credit risk. By using this, it will not only provide a quicker but more reliable loan experience. It will also provide more identifications of people who would be good for loans. Credit risk is an unbalanced classification problem, as good loans outnumber risky loans. Therefore, different styles need to be employed to train and evaluate models with unbalanced classes. Numerous supervised machine learning models/algorithms have been built and evaluated to predict credit risk. 

### Supervised Machine Learning Models Utilized:
* Naïve Random Oversampling
* SMOTE Oversampling
* Cluster Centroids Undersampling 
* SMOTEENN Combination (Over and Under) Sampling
* Balanced Random Forest Classifier
* Easy Ensemble ADABoost Classifier  

### Resources Utilized to Complete Analysis
* **Data Sources:** 
[LoanStats_2019Q1.CSV](https://github.com/RabidZippers/Credit_Risk_Analysis/blob/main/Challenge/Resources/LoanStats_2019Q1.1.zip) 

* **Languages:** Python
* **Python Dependencies:** numpy, pandas, pathlib, collections, scikit-learn, imbalanced-learn
* **Tools:** MS Excel, Jupyter Notebook


## Results

### Naïve Random Oversampling

![Classification_Report_Naive_Random_Oversampling]()

* Balanced Accuracy Score: 65.03%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 69% 
* Recall Low Risk: 61%

**Confusion Matrix**
|             | Predicted True  | Predicted False | 
|-------------|------|------|
| Actually True | 70 | 31 |
| Actually False | 6711 | 10393 |



### SMOTE Oversampling

![Classification_Report_SMOTE_Oversampling](https://github.com/cmmgw/Credit_Risk_Analysis/blob/main/Resources/Classification_Report_SMOTE_Oversampling.JPG)

* Balanced Accuracy Score: 66.21%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 63% 
* Recall Low Risk: 69%

**Confusion Matrix**
|             | Predicted True  | Predicted False | 
|-------------|------|------|
| Actually True | 64 | 37 |
| Actually False | 5291 | 11813 |



### Cluster Centroids Undersampling 

![Classification_Report_Cluster_Centroids_Undersampling](https://github.com/cmmgw/Credit_Risk_Analysis/blob/main/Resources/Classification_Report_Cluster_Centroids_Undersampling.JPG)

* Balanced Accuracy Score: 54.42%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 69% 
* Recall Low Risk: 40%

**Confusion Matrix**
|             | Predicted True  | Predicted False | 
|-------------|------|------|
| Actually True | 70 | 31 |
| Actually False | 10340 | 6764 |



### SMOTEENN Combination (Over and Under) Sampling

![Classification_Report_SMOTEENN_Combination_Sampling](https://github.com/cmmgw/Credit_Risk_Analysis/blob/main/Resources/Classification_Report_SMOTEENN_Combination_Sampling.JPG)

* Balanced Accuracy Score: 64.61%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 71% 
* Recall Low Risk: 58%

**Confusion Matrix**
|             | Predicted True  | Predicted False | 
|-------------|------|------|
| Actually True | 72 | 29 |
| Actually False | 7195 | 9909 |



### Balanced Random Forest Classifier

![Classification_Report_Balanced_Random_Forest_Classifier](https://github.com/cmmgw/Credit_Risk_Analysis/blob/main/Resources/Classification_Report_Balanced_Random_Forest_Classifier.JPG)

* Balanced Accuracy Score: 78.85%
* Precision High Risk: 3%
* Precision Low Risk: 100%
* Recall High Risk: 70% 
* Recall Low Risk: 87%

**Confusion Matrix**
|             | Predicted True  | Predicted False | 
|-------------|------|------|
| Actually True | 71 | 30 |
| Actually False | 2153 | 14951 |



### Easy Ensemble ADABoost Classifier  

![Classification_Report_Easy_Ensemble_ADABoost_Classifier](https://github.com/cmmgw/Credit_Risk_Analysis/blob/main/Resources/Classification_Report_Easy_Ensemble_ADABoost_Classifier.JPG)

* Balanced Accuracy Score: 93.16%
* Precision High Risk: 9%
* Precision Low Risk: 100%
* Recall High Risk: 92% 
* Recall Low Risk: 94%

**Confusion Matrix**
|             | Predicted True  | Predicted False | 
|-------------|------|------|
| Actually True | 93 | 8 |
| Actually False | 983 | 16121 |



## Summary
Numerous machine learning models were utilized to determine which model is the most effective at predicting credit risk. Accuracy, precision and sensitivity can be assessed by reviewing the results of each model. The confusion matrix, collates the results of accuracy,precision and sensitivity and can be calculated as follows: 

**Confusion Matrix**
|             | Predicted True  | Predicted False | 
|-------------|------|------|
| Actually True | TP | FN |
| Actually False | FP | TN |

* Accuracy = (True Positives (TP) + True Negatives (TN)) / Total
* Precision = True Positives (TP) / (True Positives (TP) + False Positives (FP))
* Sensitivity = True Positives (TP) / (True Positives (TP) + False Negatives (FN)) 


The analysis highlighted above, indicates that the precision scores for all the models are overfit. A good balance of recall and precision is necessary to have an effective model and most of the models lack this. However, the Easy Ensemble ADABoost Classifier model is recommended for use, due to its high balanced accuracy score, along with its balance of precision and recall scores.
