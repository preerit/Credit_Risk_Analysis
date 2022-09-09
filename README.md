# Credit_Risk_Analysis
## Overview of the analysis: Explain the purpose of this analysis.
Fast lending, a peer to peer lending services, wants to use ML to predict credit risk. ML will provide a quicker and more reliable experience. It will provide a more accurate indication of good candidates for loans that will lead to lower default rates. 

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. We use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once done, we will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

----

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.
![RandomOversampling](https://github.com/preerit/Credit_Risk_Analysis/blob/main/RandomOversampling.png)
* Prediction for high risk is low and recall is high, while prediction for low risk is 100% and recall is less than that of high risk
* Balanced accuracy score of this model is about 65%. 

![SMOTEOversampling](https://github.com/preerit/Credit_Risk_Analysis/blob/main/SMOTEOversampling.png)
* Does not show improvements on prediction
* Recall/Sensitivity has slighly reduced for high risk and improved for low risk
* There is marginal improvement to balanced accuracy score which is now at 66%

![undersampling](https://github.com/preerit/Credit_Risk_Analysis/blob/main/undersampling.png)
* No improveemnts in prediction
* Sensitivity has improved for high risk and reduced for low risk
* Balanced accuracy score is at 66%

![combination_sampling](https://github.com/preerit/Credit_Risk_Analysis/blob/main/combination_sampling.png)
* High sensitivity for high risk and slighly lower recall for low risk
* Prediction for high risk is still low
* Balanced accuracy score is at 65%

![BalancedRandomForestClassifier](https://github.com/preerit/Credit_Risk_Analysis/blob/main/BalancedRandomForestClassifier.png)
* Slighly better at predicting high risk
* High sensitivities for both high risk and low risk candidates
* Balanced accuracy score of 79%

![AdaboostClassifier](https://github.com/preerit/Credit_Risk_Analysis/blob/main/AdaboostClassifier.png)
* Highest prediction thus far for high risk
* High sensitivities for low risk and high risk candidates
* Balanced accuracy score of 93%

----

## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
* Random Oversampling - This model cannot predict high risk candidates well. Hence not useful
* SMOTE Oversampling - This model still cannot predict high risk candidates well and it only has a marginal improvement in sensitivity over random oversampling
* Undersampling - Same limitations as above 2 models for predicting high risk candidates
* Combination sampling - Does not do a good job at predicting risky candidates
* Balanced Random forest classifier - Slighly better at predicting high risk candidates with high sensitivities 
* Adaboost classifier - Highest prediction out of all the models thus far and highest sensitivity too.

The last 2 models are highest at predicting high risk. However, they have high recall rates as well. Hence, the sensitivities might sway the model into rightly predicting low risk but falsely predicting high risk. Hence I will not recommend any of these models.
