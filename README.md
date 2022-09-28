# Credit Risk Analysis

## Overview of the analysis:
We will evaluate various machine learning models for their ability to predict credit risks on loans.  For this analysis, we will use credit card credit dataset from LendingClub, a peer-to-peer lending service company.  

## Results:
Credit risk is an inherently unbalanced risk, meaning in a typical pool of loan, there will only be a small numbers of the loan turns into "high risk" or "bad loans".  We evaluated six machine learning models for their ability to identify as many of these potential bad loans while minimized the false positive. (False Positive: predicting a loan that ultimately turn out to be a good loan as a bad loan) Below we listed their performance and analysis:

**Logistic Regression Based Models:**<br>
Using four different ways to sample our data in a Logistic Regression model, we find that the Combination (Overand Under) Sampling method gave us the best sensitivity in identifying potential bad loans. In the confusion matrix, we can see the Combination Sampling method identify the highest percentage of the bad loans among the four Logistic Regression based models (81 out of the total of 101 high risk loans).  

On the other hand, the SMOTE Oversampling method perform the best in identifying low risk loans.  In the confusion matrix, the SMOTE method has the highest percentage of True Negative (11,816 out of the total of 17,104 low risk loans)


<img src = 'images/NavieRandomOversampling.JPG' width = '400px'>


<img src = 'images/SMOTE.JPG' width = '400px'>

<img src = 'images/ClusterCentroidsUndersampling.JPG' width = '400px'>

<img src = 'images/Combination.JPG' width = '400px'>
<br>
<br>

**Random Forest and Ensemble Models:**
<br>


<img src = 'images/BalancedRandomForest.JPG' width = '400px'>

<img src = 'images/EasyEnsembleAdaBoost.JPG' width = '400px'>

## Summary:
Since none of the four logistic regression models can achieve high sensitivity to both the high and low risk loans, we concludes logistic regression models are not good choice for our task of identifying credit risk.  

We can see both the Random Forest and the Ensemble models perform much better than the above four Logistic Regression models.  Both models achieve high sensitivity (rec) scores for both high and low risk loans, especially the Easy Ensemble AdaBoosts model.  This is reflected in the desirable confusion matrix outcome where


