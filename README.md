# Credit_Risk_Analysis
The purpose of this project is to apply machine learning by training and evaluating models to assess credit card risk for LendingClub, a peer-to-peer lending services company.
#
### Resampling Models to Predict Credit Risk
Prepping the data
- Read in csv file, create DataFrame, drop null columns and rows, remove target column
- convert interest rate to numberical
- lable target columns low_risk and high_risk
- split data into training and testing sets
- create features and target, check balance of target values
### Start with Oversampling
#### RandomOverSampler
* The dataset was oversampled using the RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. 
#
RandomOverSampler (Naive Random Oversampling)
#
![ROS](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/random.PNG)
#
accuracy score
#
![ROSacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/randomacc.PNG)
#
confusion matrix
#
![ROScm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/randomcm.PNG)
#
imbalanced classification report
#
![ROSclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/randomclass.PNG)
#
* The dataset was then over and undersampled (combination of the techniques) using the SMOTEENN algorithm. 
#
#### SMOTE
#
![sm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smote.PNG)
#
accuracy score
#
![smacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smoteacc.PNG)
#
confusion matrix
#
![smcm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smotecm.PNG)
#
imbalanced classification report
#
![smclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/smoteclass.PNG)
#
* BalancedRandomForestClassifier and EasyEnsembleClassifier, the machine learning models that reduce bias,  were used to predict credit risk. 
#
and ClusterCentroids algorithms
#
![]()
#
accuracy score
#
![]()
#
confusion matrix
#
![]()
#
imbalanced classification report
#
![]()
#
#### SMOTEENN Algorithm to Predict Credit Risk
#### Ensemble Classifiers to Predict Credit Risk