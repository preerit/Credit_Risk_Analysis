# Credit_Risk_Analysis
## Overview of the analysis: Explain the purpose of this analysis.
Fast lending, a peer to peer lending services, wants to use ML to predict credit risk. ML will provide a quicker and more reliable experience. It will provide a more accurate indication of good candidates for loans that will lead to lower default rates. 
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. We use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once done, we will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

----

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
