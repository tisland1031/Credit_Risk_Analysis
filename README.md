# Credit Risk Analysis
## Overview of Project
The purpose of this analysis is to utilize machine learning algorithms to predict credit risk from LendingClub, a peer-to-peer lending company. This analysis will interpret results from six machine learning models and determine which supervised learning algorithms are best applied from the credit card credit dataset from LendingClub. 

## Results
Results are displayed for the following six machine learning models: 

### Oversampling 
#### Naive Random Oversampling Results:
- Balanced Accuracy:64%

![Naive Random ba](https://user-images.githubusercontent.com/96746207/173453920-a4279c88-b3eb-4075-81c2-3a74072eae94.png)

- High Risk Precision:1%
- High Risk Recall:72%
- High Risk F1:2%

Imbalanced Classification Report below:

![Naive Random](https://user-images.githubusercontent.com/96746207/173452786-342ba0bc-95fe-41c6-be8c-dfde170757f3.png)

#### SMOTE Oversampling
- Balanced Accuracy:66%
-
![SMOTE BA](https://user-images.githubusercontent.com/96746207/173453935-97e3cc4a-627f-46e1-b59e-aaed34764df4.png)

- High Risk Precision:1%
- High Risk Recall:62%
- High Risk F1:2%

Imbalanced Classification Report below:

![SMOTE](https://user-images.githubusercontent.com/96746207/173452791-4adc0a68-5d1e-46ce-af80-e9373891a69b.png)

### Undersampling
#### Cluster Centroids
- Balanced Accuracy:66%

![Undersampling BA](https://user-images.githubusercontent.com/96746207/173454132-960804a0-47d0-4a39-841a-0ca817233659.png)

- High Risk Precision:1%
- High Risk Recall:62%
- High Risk F1:2%

Imbalanced Classification Report below:

![Undersampling](https://user-images.githubusercontent.com/96746207/173452801-d5a0bb8d-c53d-451c-89b8-de82e4dc1abe.png)

### Combination (Over and Under) Sampling
- Balanced Accuracy:66%

![comb BA](https://user-images.githubusercontent.com/96746207/173454339-ab5f8bab-8dbc-44b5-a015-f0ac2ef44c0d.png)

- High Risk Precision:1%
- High Risk Recall:62%
- High Risk F1:2%

Imbalanced Classification Report below:

![Combination](https://user-images.githubusercontent.com/96746207/173452813-0af95abe-6b6e-4dff-86fd-db38d88d29cb.png)

### Ensemble Leaners
#### Balanced Random Forest Classifier
- Balanced Accuracy:79%

![BRFC BA](https://user-images.githubusercontent.com/96746207/173454357-d4a127be-6707-41a9-8c52-827a199d00e6.png)

- High Risk Precision:3%
- High Risk Recall:70%
- High Risk F1:6%

Imbalanced Classification Report below:

![BRFC](https://user-images.githubusercontent.com/96746207/173452822-44b9f192-1dc0-4e15-a92c-76292de3114c.png)


Balanced random forest algorithm ranked the features by their importance and what features are more relevant for the credit card application. 
The top five features of importance are displayed below:

![important_R](https://user-images.githubusercontent.com/96746207/173918328-e0638bc4-7608-4e1c-b365-74dc825e7e8f.png)


#### Easy Ensemble AdaBoost Classifier
- Balanced Accuracy:93%

![Easy Ensemble AdaBoost Classifier BA](https://user-images.githubusercontent.com/96746207/173454380-56db7ecb-f9a0-4ee1-a512-34de1824f726.png)

- High Risk Precision:9%
- High Risk Recall:92%
- High Risk F1:16%

Imbalanced Classification Report below:

![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/96746207/173452836-800a4c5b-f096-4837-8b3c-505628dbd63f.png)

	
## Summary 
#### Overall Performance of Supervised Machine Learning Algorithm based on "High Risk" Results:
|   Method     |  Balanced Accuracy  |  Precision  |  Recall | F1 (Avg/total | 
| -------------|:-------------------:|:-----------:|:-------:|:-------------:|
| Naive Random Oversampling    | 64%| 1%| 72% | 71% |
| SMOTE Oversampling     |  66%| 1%| 62% | 81% | 
| Undersampling Cluster Centroids | 66%| 1%| 62% | 81% | 
| SMOTEENN Combination Sampling |  66%| 1%| 62% | 81% |
| Balanced Random Forest Classifier |  79%| 3%| 70% | 93% |
| Easy Ensemble AdaBoost Classifier |  93%| 9%| 92% | 97% |
   
The oversampling, undersampling, and combination sampling models all displayed a low balanced accuracy score in the range of sixty percent. Balance random forest classifier model has a higher balanced accuracy score of 79%, however, the best overall model is the easy ensemble AdaBoost classifier. 

Based on the given results above, easy ensemble AdaBoost classifier model is the preferred choice. The model has the highest balanced accuracy score at 93%, with a precision rank of 99% for predicting high-risk customers and the recall rate was the highest,92%. F1 score is 97% and the closer to one, the better the model.  





