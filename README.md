# Credit_Risk_Analysis

## Overview of the analysis:
Credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

## Results:
Naive Random Oversampling results: Our balanced accuracy test it 67%, the precision for the high_risk has a very low positivity at 1% and the recall is 74%
naive
<img width="637" alt="Naive Oversampling" src="https://user-images.githubusercontent.com/74282781/118387679-92788c00-b5d4-11eb-8556-f07724b62397.png">

SMOTE oversampling results: the accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall
smote<img width="599" alt="SMOTE oversampling" src="https://user-images.githubusercontent.com/74282781/118387680-973d4000-b5d4-11eb-804a-d43772626645.png">



Undersampling results: balanced accuracy score is 66.2% overall, the precision is at 99% and the recall is 41%
undersampling
<img width="633" alt="Undersampling" src="https://user-images.githubusercontent.com/74282781/118387694-acb26a00-b5d4-11eb-993a-f1e8319c8088.png">


Combination(over and undersampling) results: balanced accuracy score is 54.7% the precision is 99% and the recall is 57% overall
combination
<img width="629" alt="Combination" src="https://user-images.githubusercontent.com/74282781/118387737-f69b5000-b5d4-11eb-876d-58c29e4a8065.png">


Balanced Random Forest Classifier results: the accuracy score is 78.9% the precision is 99% and the recall is 89%
random forest<img width="618" alt="Balance R F" src="https://user-images.githubusercontent.com/74282781/118387577-0b2b1880-b5d4-11eb-977e-53477b42d7f3.png">



Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94%
ensemble
<img width="610" alt="Easy Ensemble" src="https://user-images.githubusercontent.com/74282781/118387587-11b99000-b5d4-11eb-9645-ea85c9ae94f2.png">

## Summary:
In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
