# Credit_Risk_Analysis

### Overview of the analysis: Explain the purpose of this analysis.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we need to employ different techniques to train and evaluate models with unbalanced classes. we use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. 

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk, evaluate the performance of these models.

### Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Using the imbalanced-learn and scikit-learn libraries to evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First the oversampling RandomOverSampler and SMOTE algorithms, and then the undersampling ClusterCentroids algorithm. Using these algorithms to resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

#### Naive Random Oversampling

![This is an image](naive.png)

- balanced accuracy: 0.6249984891886339
- precision: the precision is pretty low for high_risk loans and is high for low_risk loans.
- recall(high_risk/low_risk): 0.60/0.65

#### SMOTE Oversampling

![This is an image](smote-over.png)

- balanced accuracy: 0.6512584051472337
- precision: the precision is pretty low for high_risk loans and is high for low_risk loans.
- recall(high_risk/low_risk): 0.64/0.66

#### Undersampling

![This is an image](under.png)

- balanced accuracy: 0.6512584051472337
- precision: the precision is pretty low for high_risk loans and is high for low_risk loans.
- recall(high_risk/low_risk): 0.57/0.47

#### Combination (Over and Under) Sampling

![This is an image](combination.png)

- balanced accuracy: 0.5214958241173839
- precision: the precision is pretty low for high_risk loans and is high for low_risk loans.
- recall(high_risk/low_risk): 0.72/0.58

#### Balanced Random Forest Classifier

![This is an image](emb.png)

- balanced accuracy: 0.7877672625306695
- precision: the precision is pretty low for high_risk loans and is high for low_risk loans.
- recall(high_risk/low_risk): 0.67/ 0.91

#### Easy Ensemble AdaBoost Classifier

![This is an image](adaboost.png)

- balanced accuracy: 0.925427358175101
- precision: the precision is pretty low for high_risk loans and is high for low_risk loans.
- recall(high_risk/low_risk): 0.91/0.94

### Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

By comparing all the models, Easy Ensemble AdaBoost Classifier is the best machine learning model to choose because of the highest accuracy score which is 0.92, also the recall score is pretty close to 1 for this model which is good but the precision is pretty low for high_risk loans for all models. so by comparing the numbers Easy Ensemble AdaBoost Classifier has better results which makes it a better choice for credit card analysis.
