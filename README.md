# Hired or not

I use the Gradient boosting classifier [1] to determine if a candidate is hired in this classification task. The features include a set of multiple-choice questions, job category, gender, and text response. 

## Classification
The notebook of the classification can be found in
https://github.com/juweiyu/hired_or_not/blob/main/Classification.ipynb


## Performance
The Gradient boosting classifier can achieve an average F1 score of 0.580. This can be improved by using parameter tunning or using other models such as XGBOOST (it will take longer time, so I choose the Gradient boosting classifier).

## Fairness
The prediction result shows that it is treating male and female candidates relatively fair. This can be shown in two aspects:

* The feature importance diagram shows that "gender" has lower importance compared to other features
* In the partial dependency plot of "gender", we can see that the difference between male and female is negligible

## Explainability
* The feature importance diagram shows that text_response and job_family are the two most important features to predict "selected"
* From the partial dependency plots, we can clearly see which value contributes more to the decision for each feature
* Our model is slightly more sensitive to negative texts compared to positive texts

## REFERENCE

[1] Friedman, Jerome H. "Greedy function approximation: a gradient boosting machine." Annals of statistics (2001): 1189-1232.  
