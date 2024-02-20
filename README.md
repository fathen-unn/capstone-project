# capstone-project
Portfolio project on optimizing a model for real-life data.

# SMS Spam Detection 
This model is trained on a collection of SMS messages from the UCI Machine Learning Repository, it accurately distinguishes between spam and legitimate text messages.

It analyzes message content using a technique called "bag-of-words" to identify patterns associated with spam. In tests, it correctly classified 97.67% of messages, and its consistent performance across different data splits suggests it can generalize well to new messages.

## DATA
The dataset used in training and testing the model is 'SMS Spam Collection' from UCI Machine Learning Repository. It contains a public set of SMS labeled messages that have been collected for mobile phones spam research. It is a multivariate, text, domain-theory dataset with 5574 instances and no features. The messages were collected from a variety of sources, including a UK forum, a dataset of legitimate messages collected for research at the National University of Singapore, and a collection of SMS ham messages collected from Caroline Tag’s PhD Thesis.

source: https://archive.ics.uci.edu/dataset/228/sms+spam+collection

## MODEL 
The model combines two key components: a Random Forest Classifier and a CountVectorizer. 

The Random Forest, built with multiple decision trees, excels in classification tasks, particularly ones sensitive to overfitting like handling text data. 

CountVectorizer prepares the text data by converting each message into a numerical representation, analyzing the "bag-of-words" (word presence/absence) rather than their order. This approach efficiently captures relevant features for the classifier.

## HYPERPARAMETER OPTIMSATION
No tuning is required since high accuracy is reached. However, these are the particular parameters applied:

1. Random Forest Classifier:
n_estimators (100): The number of decision trees used in the forest. Each tree contributes to the final classification outcome, and increasing the number can improve accuracy but also computational cost.

2. CountVectorizer:
None specified: By default, CountVectorizer uses standard settings, including considering all words (no minimum frequency or stop words removal) and converting them to binary features (presence/absence).

## RESULTS
Accuracy:
The model achieved an accuracy of 97.49% on the test set. This suggests it correctly classified almost all messages into "ham" or "spam" categories.

Cross-validation scores:
The cross-validation scores show performance on 5 different splits of the data.
They range from 96.79% to 97.82%, signifying consistent performance across different data subsets.
This helps avoid overfitting and suggests the model generalizes well to unseen data.
