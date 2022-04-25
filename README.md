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
#### ClusterCentroids algorithms
#
ClusterCentroids
#
![cl](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/cluster.PNG)
#
accuracy score
#
![clacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/clusteracc.PNG)
#
confusion matrix
#
![clcm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/clustercm.PNG)
#
imbalanced classification report
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
#### Ensemble Classifiers to Predict Credit Risk
#### Balanced Random Forest Classifier
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
!eaacc](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/eaacc.PNG)
#
confusion matrix
#
![eacm](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/eacm.PNG)
#
imbalanced classification report
#
![eaclass](https://github.com/jcsargis00/Credit_Risk_Analysis/blob/main/images/eaclass.PNG)
#