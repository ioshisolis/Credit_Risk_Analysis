# Credit_Risk_Analysis with Supervised Machine Learning

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, is evident credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. This data analysis is conducted by using the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling with different techniques to train and evaluate models with unbalanced classes.

## Overview 

- Oversample the data using the **RandomOverSampler** and **SMOTE** algorithms
- Undersample the data using the **ClusterCentroids** algorithm. 
- Use a combinatorial approach of over- and undersampling using the **SMOTEENN** algorithm. 
- Compare two new machine learning models that reduce bias, **BalancedRandomForestClassifier** and **EasyEnsembleClassifier**, to predict credit risk.
- Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

<details><summary>Confussion Matrix and Formulas</summary>
 
|                         | Predicted True  | Predicted False|    |
| :---                    | :---:           | :---:          | :---: |
|Actually True            | TRUE POSITIVE   | FALSE NEGATIVE | Sensitivity|
| Actually False          | FALSE POSITIVE  | TRUE NEGATIVE  |   |
|                         |Precision        |                |   | 

- Precision = TP/(TP + FP)

- Sensitivity(Recall) = TP/(TP + FN)

- F1 = 2(Precision * Sensitivity)/(Precision + Sensitivity)
  
  
  
</details>





## Results

|Moodels|Accuracy Score|PreAvg|Pre_high_risk|Pre_low_risk|RecAvg|Rec_high_risk|Rec_low_risk|F1Avg|F1_high_risk|F1_low_risk|
| :---                    | :---: | :---: | :---:| :---: |:---:| :---: | :---: | :---: | :---: | :---: |
| Naive Random Sampling   | .64   | .99   |.01   |1.00   |.61. |.66.   |.61    |   .76 |.02.   |.76.   | 
| SMOTE Oversampling      | .66   | .99   |.01   |1.00   |.69  |   .62 | .69   |    .81|    .02|.82    |
| Undersampling           | .54   | .99   |.01   |  1.00 |.40  |   .69 | .40   |    .56|    .01|.57    |
| SMOTEENN                | .65   | .99   |.01   |  1.00 |.57  |   .72 | .57   |    .72|    .02|.73    |
| Balanced Random Forest  | .79   | .99   |.03   |  1.00 |.87  |   .70 | .87   |    .93|    .06|.93    |
| Easy Ensemble AdaBoost Classifier|.93 |.99|.09 |  1.00 | .94 |.92    |.94.   |.97    |.16    | .97.  |




### Naive Random Sampling
<details><summary>View Code</summary>
  
![NaiveRandomOversampling](https://user-images.githubusercontent.com/37987602/152732680-b63788c1-e9fe-48dd-867f-322c76368d41.png)
  
</details>

### SMOTE Oversampling
<details><summary>View Code</summary>
  
![SMOTE Oversampling](https://user-images.githubusercontent.com/37987602/152733253-7a819013-70f4-4913-889a-f75febeeb207.png)

</details>

### Undersampling
<details><summary>View Code</summary>
  
![Undersampling](https://user-images.githubusercontent.com/37987602/152733795-b319fb55-204a-4ee9-97f1-8f17b2274307.png)

</details>

### SMOTEEN
<details><summary>View Code</summary>
  
![SMOTEEN](https://user-images.githubusercontent.com/37987602/152733859-fc9e9bab-8d93-428f-8173-b3cb22cdf93d.png)

</details>


### Balanced Random Forest
<details><summary>View Code</summary>
  
![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/37987602/152739048-ed76d4df-c49d-4075-9eea-bc9cf2548a8f.png)

</details>

### Easy Ensemble AdaBoost Classifier
<details><summary>View Code</summary>
 
![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/37987602/152739132-99810b13-13f7-433d-9b2b-153bfdfc1dee.png)

</details>

## Summary


According to our table the Easy Ensemble AdaBoost Classifier with a 93% accuracy score seem to be the best model for this case. 

In all our model precision of high risk candidates is very low.

According to our table the Sensitivity or Recall percentages points to the Easy Ensemble AdaBoost Classifier with a 94% Recall Avg. 

High sensitivity means that among the people who actually are high risk candidates, most of the are high risk candidates. 

High sensitivity is more important than precision for analyzing risk on loan candidates because is better to detect everyone who might have a high risk of not paying, even if it means certain number of false positives, than to loan money to candidates who won’t pay. 

The Easy Ensemble AdaBoost Classifier is our Best Model for this Case Study


