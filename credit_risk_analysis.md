# Credit_Risk_Analysis

# Overview

This analysis considered loan risk as high or low, and applied machine learning algorithns to assist in making a predicted determination.  The data set consisted of many features which included categorical and numerical data.  The features are used to predict the outcomes (also referred to as labels in this analysis).  After identifying the label outcome as "loan_status" the remaining columns of data needed to be preprocessed for the analysis.  The details of this preprocessing are given in the Jupyter Notebooks.

Imbalance sampling methods were applied because the outcomes were imbalanced:  low risk loans only existed in the data set.  Since data is paired by feature data and outcome data for predictions , imbalanced sampling techniques were used to balance data between features and labels.  These techniques are referred to as Naive Random Oversampling, SMOTE Oversampling, Cluster Centroids, and SMOTEENN.  In addition to these methods, predictions of loan risk were attempted using an ensemble of decsion trees.  These methods are the Balanced Forest Random Classifier, and the Easy Ensemble Ada Boost Classifier.  Unlike the sampling techniques, only original data (feaures and labels) are used.  The data are distributed over a number of estimators and decision tree algoritms are used to predict an outcome.  Another noteworthy difference between these methods is that sampling methods apply logistic regression.  In contrast, logistic regression is not performed for the decision tree methods.  The results of these six methods are presented below.



# Results

  Method                           |     Accuracy     |   Precision     |   Recall       |
:----------------------------------|:----------------:|:---------------|:--------------|
|Naive Random Oversampling         |  0.587           |  0 -> 0.01      |  0 ->  0.70    |
|                                  |                  | 1 -> 1.0       |  1 ->  0.47    |
|SMOTE Oversampling                |  0.587           |  0 -> 0.01      |  0 ->  0.70    |
|                                  |                  | 1 -> 1.0       |  1 ->  0.47    |
|Cluster Centroids                 |  0.517           |  0 -> 0.01      |  0 ->  0.72    |
|                                  |                  | 1 -> 1.0       |  1 ->  0.31    |
|SMOTEENN                          |  0.517           |  0 -> 0.01      |  0 ->  0.72    |
|                                  |                  | 1 -> 1.0       |  1 ->  0.31    |
|Balanced Forest Random Classifier |  0.782           |  0 -> 0.04      |  0 ->  0.66    |
|                                  |                  |  1 -> 1.0       |  1 ->  0.91    |
|Easy Ensemble Ada Boost Classifier|  0.910           |  0 -> 0.08      |  0 ->  0.87    |
|                                  |                  |  1 -> 1.0       |  1 ->  0.95    |<br>

#### Table Descriptions

Note:  The outcome label **'1'** is for **low-risk**, and the outcome label **'0'** is for **high risk**.

**Accuracy**:  Related to the number of outcomes from the method prediction that are the same as in the test vector.<br><br>
**Precision**:  Related to the confusion matrix in that it represents the number of true positives out of all positives.<br><br>
**Recall**:  Also known as "senitivity" and related to the confusion matrix in that it represents true positives out of all outcomes that 
          should be positive.<br><br>



# Summary

The results definitively show that the ensemble decision tree methods outperform the sampling techniques.  This is based on:  1) higher accuracy, 2) correct prediction that low risk loans are predominant, and 3) a much higher sensitivity (recall) meaning that when an outcome is known that the predicted outcome has a high likelyhood of being correct.  The Easy Ensemble Ada Boost Classifier is the best choice for the given data set.  The Balanced Forest Random Classifier is worth further investigation.  This method has many more parameters to choose and to vary for the analysis than the boost method.  In fact, a quick check varied the parameter "max_depth" from 2 to 20 and found a remarkable improvement in performance.  The ability to adjust many parameters combined with a better performance than the sampling techniques makes this algorithm potentially useful for most data sets.




