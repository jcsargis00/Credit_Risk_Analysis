# Credit_Risk_Analysis
### Purpose
The purpose of this project is to apply machine learning by training and evaluating models to assess credit card risk for LendingClub, a peer-to-peer lending services company.
#
### Overview of the loan prediction risk analysis
* Technique used - supervised machine learning
* Tools - python scikit-lean, imbalanced-learn
* Training set vs test set 75% to 25% split of dataset
#### Resampling Models to Predict Credit Risk
Prepping the data
- Read in csv file, create DataFrame, drop null columns and rows, remove target column
- convert interest rate to numerical
- lable target columns low_risk and high_risk
- split data into training and testing sets
- create features and target, check balance of target values
### Results - Oversampling, Undersampling, Combination, and Ensemble Classifiers
The dataset was oversampled using the RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. 
### Start with Oversampling
#### RandomOverSampler
#
RandomOverSampler (Naive Random Oversampling) - 51,366 low risk, 246 high risk in training set.  The algorithm randomly selects from the high risk class and adds to the training set until both classes have the same number of data.
#
![ROS](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/random.PNG)
#
accuracy score  was 66%
#
![ROSacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/randomacc.PNG)
#
confusion matrix 
#
![ROScm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/randomcm.PNG)
#
imbalanced classification
* high_risk 72% recall with 1% precision, giving an F1 of 1.972%
* low_risk  60% recall with 100% precision
#
![ROSclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/randomclass.PNG)
#
#### SMOTE
#
![sm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smote.PNG)
#
accuracy score was 65%
#
![smacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smoteacc.PNG)
#
confusion matrix
#
![smcm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smotecm.PNG)
#
imbalanced classification report
* high_risk 72% recall with 1% precision, giving an F1 of 1.972%
* low_risk  57% recall with 100% precision, slightly worse than RandomOverSampler
#
![smclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smoteclass.PNG)
#

#### ClusterCentroids algorithms - Undersampling
#
ClusterCentroids
#
![cl](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/cluster.PNG)
#
accuracy score was 65%
#
![clacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/clusteracc.PNG)
#
confusion matrix
#
![clcm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/clustercm.PNG)
#
imbalanced classification report
* high_risk 69% recall with 1% precision, giving an F1 of 1.972%
* low_risk  40% recall with 100% precision, a big degradation compared to random and SMOTE
#
![clclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/clusterclass.PNG)
#
#### SMOTEENN Algorithm to Predict Credit Risk (combination over- and under-sampling algorithm)
#
SMOTEENN
#
![cl](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/enn2.PNG)
#
accuracy score
#
![clacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/ennacc.PNG)
#
confusion matrix
#
![clcm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/enncm.PNG)
#
imbalanced classification report
#
![clclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/ennclass.PNG)
#
### Ensemble Classifiers to Predict Credit Risk
#### Balanced Random Forest Classifier
BalancedRandomForestClassifier and EasyEnsembleClassifier, the machine learning models that reduce bias,  were used to predict credit risk. 
#
Balanced Random Forest
#
![br](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/br.PNG)
#
accuracy score
#
![bracc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/bracc.PNG)
#
confusion matrix
#
![brcm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/brcm.PNG)
#
imbalanced classification report
#
![brclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/brclass.PNG)
#
Features sorted in descending order by feature importance
#
![brimp](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/brimp.PNG)
#
#### Easy Ensemble Classifier Algorithm
#
Easy Ensemble Classifier
#
![ea](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/ea.PNG)
#
accuracy score
#
![eaacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/eaacc.PNG)
#
confusion matrix
#
![eacm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/eacm.PNG)
#
imbalanced classification report
#
![eaclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/eaclass.PNG)
#
### Summary
#
When analyzing results of supervised machine learning models, it is important to consider the problem trying to be solved, in addition to the results of the models.  For example, when a model is used for medical testing, it is better to have too many false positives, than false negatives.  It is better to retest and find a person is not sick, than to send a sick person away with a false negative.  For our study, we are looking at loan risk.  It is better to have false negatives, than false positives, because too many false positives would make the majority of loans look at risk, when the reverse has been found to be true over years and years of looking at loan risk.  Below is a table of the results of each model on the data set.
![algscores](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/algscores.PNG)
We will look more carefully at high risk results.  For high risk prediction:
The most accurate model was the Easy Ensemble Cluster (93% accuracy, 9% precision, 92% recall, 16.72% F1.
)
Next is Balanced Random Forest, followed by SMOTE, SMOTEENN, RandomOverSampler and ClusterCentroids.
A summary of the results is shown in the table below ranking the most accurate models for high risk loan prediction.
![ranking](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/ranking.PNG)
