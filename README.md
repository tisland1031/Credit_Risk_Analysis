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
- High Risk F1:1%

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
- Balanced Accuracy:54%

![under_BA](https://user-images.githubusercontent.com/96746207/174448132-4e240a25-abf7-4750-814f-ec13afe5e357.png)
- High Risk Precision:1%
- High Risk Recall:69%
- High Risk F1:2%

Imbalanced Classification Report below:

![under_ICR](https://user-images.githubusercontent.com/96746207/174448135-c2ae4c25-7402-4a8a-aa09-8d33907ffe2f.png)

### Combination (Over and Under) Sampling
- Balanced Accuracy:62%

![SMTEENN_BA](https://user-images.githubusercontent.com/96746207/174448138-0b483935-b31a-4e98-9562-a07da4062d51.png)
- High Risk Precision:1%
- High Risk Recall:68%
- High Risk F1:2%

Imbalanced Classification Report below:

![COMB_ICR](https://user-images.githubusercontent.com/96746207/174448139-e77c6bd2-db19-471f-a9a7-8740196207a0.png)

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
| Undersampling Cluster Centroids | 54%| 1%| 69% | 56% | 
| SMOTEENN Combination Sampling |  62%| 1%| 68% | 70% |
| Balanced Random Forest Classifier |  79%| 3%| 70% | 93% |
| Easy Ensemble AdaBoost Classifier |  93%| 9%| 92% | 97% |
   
The oversampling, undersampling, and combination sampling models all displayed a low balanced accuracy score in the range between 54-66 percent. Balance random forest classifier model has a higher balanced accuracy score of 79%, however, the best overall model is the easy ensemble AdaBoost classifier. 

Based on the given results above, easy ensemble AdaBoost classifier model is the preferred choice. The model has the highest balanced accuracy score at 93%, with a precision rank of 99% for predicting high-risk customers and the recall rate was the highest,92%. F1 score is 97% and the closer to one, the better the model.  








