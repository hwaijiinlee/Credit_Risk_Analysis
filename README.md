# Credit_Risk_Analysis

## Overview
The purpose of this analysis is to determine which machine learning model is best suited to predict credit risk. The models used were Random Oversampling, SMOTE Oversampling, ClusterCentroids Undersampling, SMOTEENN Sampling, BalancedRandomForestClassifier, and EasyEnsembleClassifier.

## Results
### Balanced Accuracy Scores:
![Random](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/Random_Oversampling_Acc_Score.png)

![SMOTE](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/SMOTE_Acc_Score.png)

![ClusterCentroids](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/Cluster_Acc_Score.png)

![SMOTEENN](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN_Acc_Score.png)

![BRF](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/BRF_Acc_Score.png)

![EzE](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/Eze_Acc_Score.png)

### Precision and Recall (Sensitivity) Scores:
![Random_Rpt](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/Random_Oversampling_Class_Rpt.png)

![SMOTE_Rpt](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/SMOTE_Class_Rpt.png)

![ClusterCentroids_Rpt](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/Cluster_Class_Rpt.png)

![SMOTEENN_Rpt](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN_Class_Rpt.png)

![BRF_Rpt](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/BRF_Class_Rpt.png)

![EzE_Rpt](https://github.com/hwaijiinlee/Credit_Risk_Analysis/blob/main/Resources/Eze_Class_Rpt.png)

## Summary
Out of the six models used, EasyEnsembleClassifier has the highest Balanced Accuracy Score of 93.2%, followed by the BalancedRandomForestClassifier with a score of 78.9%. The other four sampling models produced relatively low accuracy scores of between 54% and 66%.

Based on the Imbalanced Classification Reports of each model, it appears that every model is able to predict with 100% accuracy loans with low credit risk as the Precision score for the low risk category are all at 100%. That is relatively unimportant though as what is more important during a loan approval process is the ability to identify high risk applications as accurately as possible to avoid collection issues once loan is granted.

With that in mind, our focus will switch to the high risk category. 
Precision Scores:
All models have less than 10% Precision scores which means that there are lots of false positives i.e. loans that are not high risk but identified as high risk. That is bad for business as that would result in many unnecessary rejections.

Recall Scores:
The EasyEnsembleClassifier has the highest Recall score for the high risk category of 92%. All other models have scores of around 70%. This means that the EasyEnsembleClassifier model does not produce as many false negative results for high risk applications as the other models. 

Overall, it would look like EasyEnsembleClassifier has an edge over other models. However, the F1 score for the high risk category is still too low for the model to be considered for recommendation. Although its sensitivity for high risk applications are high, its precision is much too low to be considered good for business.