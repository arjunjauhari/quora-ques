# quora-ques

## Summary of Finding similarity in Quora Questions set.

As a first Kaggle assignment, we started with reading up a top-rated Notebook [https://www.kaggle.com/anokas/data-analysis-xgboost-starter-0-35460-lb] by anokas.
The Notebook analyzed some basic properties of given data such as 
data size; max true positives etc
max sentence size.
word frequency
tfidf 
words shared between the questions. etc.

Before applying a neural network to this problem, we thought of applying more basic techniques like
Step 1: Machine Learning algorithms like Decision Trees, Random Forest, boosting algorithms.
Step 2: Logistic Regression 
Step 3: RNN

However, step 1 and step 2 required extracting features. Two features we ended up using are word_share_match and tfidf_word_share_match. 
Using these two features, Logistic regression and Decision Trees, Random Forest, boosting algorithms were implemented. 

**Gradient Boosting leaderboard score was 0.35535.**

Later RNN was applied using Dual encoder LSTM. Interestingly, the when model was being fitted on training data, accuracy was increasing while even logloss was increasing.
Why accuracy can increase when logloss is also increasing.?
**(arjun please comment)**

## *Current state:*
We could not calculate/submit accuracy of NN on the test set because we are facing technical issues for the submission.

## *Understing ROC_AUC (just for information)*
Learnt metric such as ROC_AUC accuracy
What is ROC: It is plot of the True Positive Rate (on Y-axis) and False Positive Rate (on X-axis) for every positive classification threshold.
True Positive Rate = # of true positive / all positives.
False Positive Rate = # of false positive / all negatives.
http://www.dataschool.io/roc-curves-and-auc-explained/ - very good explaination. 

AUC score tells us how good is the classifier. 
AUC score of 0.5 means very poor classifier (equivalent to random guessing). 
AUC score of 1 means best classifier. 
