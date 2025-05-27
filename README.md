# Heart Disease Risk Prediction using Interpretable Machine Learning
This project uses Electronic Health Records (EHR) data to build machine learning models that predict the risk of heart disease and provide interpretable explanations of the predictions.

## Objective

To compare two powerful models:

Random Forest Classifier
XGBoost Classifier

...and evaluate them using:
Accuracy
Precision, Recall, F1-Score
ROC AUC Score (macro-average)
Confusion Matrix
Feature Importance

## Dataset

The dataset is based on the UCI Heart Disease dataset, with the following features:
age, sex, cp, trestbps, chol, fbs, restecg, thalach, exang, oldpeak, slope, ca, thal, num.

This is the description of the data.


|index|age|sex|cp|trestbps|chol|fbs|restecg|thalach|exang|oldpeak|slope|ca|thal|num|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|count|303\.0|303\.0|303\.0|303\.0|303\.0|303\.0|303\.0|303\.0|303\.0|303\.0|303\.0|299\.0|301\.0|303\.0|
|mean|54\.43894389438944|0\.6798679867986799|3\.1584158415841586|131\.68976897689768|246\.69306930693068|0\.1485148514851485|0\.9900990099009901|149\.6072607260726|0\.32673267326732675|1\.0396039603960396|1\.6006600660066006|0\.6722408026755853|4\.73421926910299|0\.9372937293729373|
|std|9\.038662442446743|0\.4672988277701313|0\.9601256119600123|17\.599747729587687|51\.776917542637015|0\.35619787492797594|0\.9949712915251797|22\.875003276980376|0\.46979446452231716|1\.161075022068634|0\.6162261453459627|0\.9374383177242157|1\.9397057693786417|1\.2285356879701044|
|min|29\.0|0\.0|1\.0|94\.0|126\.0|0\.0|0\.0|71\.0|0\.0|0\.0|1\.0|0\.0|3\.0|0\.0|
|25%|48\.0|0\.0|3\.0|120\.0|211\.0|0\.0|0\.0|133\.5|0\.0|0\.0|1\.0|0\.0|3\.0|0\.0|
|50%|56\.0|1\.0|3\.0|130\.0|241\.0|0\.0|1\.0|153\.0|0\.0|0\.8|2\.0|0\.0|3\.0|0\.0|
|75%|61\.0|1\.0|4\.0|140\.0|275\.0|0\.0|2\.0|166\.0|1\.0|1\.6|2\.0|1\.0|7\.0|2\.0|
|max|77\.0|1\.0|4\.0|200\.0|564\.0|1\.0|2\.0|202\.0|1\.0|6\.2|3\.0|3\.0|7\.0|4\.0|

num is the target: 0 = no disease, y>=1 = presence of heart disease.


## Tools Used

Python

Scikit-learn

XGBoost

SHAP (for model interpretability)

Matplotlib & Seaborn

 ## Models Compared

Random Forest Classifier

Strong performance

Easy to interpret

XGBoost Classifier

Excellent accuracy and efficiency

Often used in real-world Kaggle competitions

## 📈 Evaluation Results

| Metric              | Random Forest | XGBoost  |
|---------------------|---------------|----------|
| Accuracy            | 0.902         | 0.869    |
| ROC AUC (macro)     | 0.94          | 0.92     |
| Class 0 F1-Score    | 0.90          | 0.87     |
| Class 1 F1-Score    | 0.90          | 0.87     |

> Both models perform well, but **Random Forest** had slightly better overall accuracy and AUC on this dataset.



## Interpretability
I used **SHAP (SHapley Additive exPlanations)** to interpret both models.

- SHAP summary plots were used to visualize global feature importance.  
- Waterfall plots explained individual patient predictions.

## Insights
- Features like **chest pain type (cp)**, **max heart rate (thalach)**, **oldpeak**, and **ca** were most influential.  
- Both models showed similar patterns in feature importance.


