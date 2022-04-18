# Credit_Risk_Analysis

## Overview of the Analysis
Banks have traditionally relied on measures, such as income, credit score, and collateral assets to assess lending risks, but the rise of fintech (financial technology) and allowed lenders to use machine learning to analyze risk. We used 6 different machine learning models to predict credit risk. For oversampling the data, we used **RandomOverSampler** and **SMOTE** algorithms. For undersampling the data, we used the **ClusterCentroids** algorithm. We also tried an approch by combining the oversampling and undersampling using the **SMOTEENN** algorithm. Then we used the **BalancedRandomForestClassifier** and **EasyEnsembleClassifier** that reduces bias. We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results
- **Random Over Sampler**
  - 64.0% Accuracy
  - 1% Precision
  - 66% Recall 
  - 2% F1-Score
    - <img width="366" alt="image" src="https://user-images.githubusercontent.com/58046234/163725117-020c729f-df5b-4486-8c29-05cf3587384a.png">
    - <img width="545" alt="image" src="https://user-images.githubusercontent.com/58046234/163724997-2f5d6053-e286-4c42-ab12-e85f1233aa35.png">

- **SMOTE** 
  - 65.2% Accuracy
  - 1% Precision
  - 61% Aecall
  - 2% F1-Score
    - <img width="326" alt="image" src="https://user-images.githubusercontent.com/58046234/163725148-e3f06b2c-1474-446a-a79b-3ff4b31a1655.png">
    - <img width="552" alt="image" src="https://user-images.githubusercontent.com/58046234/163725165-119d8012-073b-4340-99ef-5e401d084005.png">

- **ClusterCentroids**
  - 54.5% Accuracy
  - 1% Precision
  - 69% Recall 
  - 1% F1-Score
    - <img width="305" alt="image" src="https://user-images.githubusercontent.com/58046234/163725196-04014c1e-6816-4299-a26e-ca2408c6df2f.png">
    - <img width="568" alt="image" src="https://user-images.githubusercontent.com/58046234/163725217-94ed61bc-36f0-4668-80cb-48975871a9a5.png">

- **SMOTEENN**
  - 64.5% Accuracy
  - 1% Precision
  - 72% Recall
  - 2% F1-Score
    - <img width="323" alt="image" src="https://user-images.githubusercontent.com/58046234/163725260-d26b3e92-9eaf-4a13-a143-eb39c0ed3672.png">
    - <img width="562" alt="image" src="https://user-images.githubusercontent.com/58046234/163725268-e44591c0-76f9-420e-8acd-28ddd728cea2.png"> 

- **Balanced Random Forest Classifer**
  - 78.9% Accuracy
  - 3% Precision
  - 70% Recall 
  - 6% F1-Score
    - <img width="311" alt="image" src="https://user-images.githubusercontent.com/58046234/163725298-6c6993fb-4280-43bd-a052-37b048d40727.png">
    - <img width="553" alt="image" src="https://user-images.githubusercontent.com/58046234/163725329-08680c69-8b2e-47c7-a0f6-d20f2f633c90.png">

- **Easy Ensemble Classifer**
  - 93.2% Accuracy
  - 9% Precision
  - 92% Recall
  - 16% F1-Score
    - <img width="336" alt="image" src="https://user-images.githubusercontent.com/58046234/163725356-9c4dd6cc-fd47-4678-88c8-fcfdf596055f.png">
    - <img width="556" alt="image" src="https://user-images.githubusercontent.com/58046234/163725368-6c79a091-c3c0-4814-96ca-6af8da620612.png">

## Summary
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high. The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits. The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities. For those reasons I would not recommend the bank to use any of these models to predict credit risk.
