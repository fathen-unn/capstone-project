# Model Card

## Model Description

**Input:** Raw text of an SMS message in English/Singaporean English. 

**Output:** A predicted label of "ham" (legitimate) or "spam".

**Model Architecture:** 
A pipeline consisting of:
- CountVectorizer for text vectorization (converting text into numerical features).
- Random Forest Classifier with 100 decision trees for classification.

## Performance

- Accuracy on test set: 97.67%
- Cross-validation scores (5-fold): [0.9769, 0.9782, 0.9679, 0.9705, 0.9692]
- Evaluation metric: Accuracy
- Data analyzed on: SMS Spam Collection dataset (https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection)

## Limitations

- Language: Limited to English/Singaporean English SMS messages.
- Data bias: Performance may be affected by biases in the training dataset, such as over- or underrepresentation of certain types of spam or legitimate messages.
- Static nature: Model does not adapt to evolving spam patterns.

## Trade-offs

- Accuracy vs. interpretability: Random Forest provides high accuracy but is less interpretable than simpler models like decision trees.
- Accuracy vs. speed: Training and prediction might be slower for larger datasets or resource-constrained devices compared to simpler models.
- False positives vs. false negatives: Adjusting classification thresholds can prioritize reducing false positives (spam incorrectly marked as ham) or false negatives (ham incorrectly marked as spam) based on specific use cases.
