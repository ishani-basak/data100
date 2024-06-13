
## Spam/Ham 

### Introduction

I create a binary classifier that can distinguish spam (junk or commercial or bulk) emails from ham (non-spam) emails. I evaluate work based on my model's accuracy and my written responses in this notebook.

This first part of the project focuses on initial analysis as well as Feature Engineering and Logistic Regression. In the second part of this project, I will build my own spam/ham classifier.

### Project B.1

In email classification, my goal is to classify emails as spam or not spam (referred to as "ham") using features generated from the text in the email. 

The dataset is from [SpamAssassin](https://spamassassin.apache.org/old/publiccorpus/). It consists of email messages and their labels (0 for ham, 1 for spam). My labeled training dataset contains 8,348 labeled examples, and the unlabeled test set contains 1,000 unlabeled examples.

**Part 1**

I note observations of the dataset to understand the background before diving into a full-scale analysis.

**Part 2**

I would like to take the text of an email and predict whether the email is ham or spam. This is a **binary classification** problem, so I can use logistic regression to train a classifier. Recall that to train a logistic regression model we need a numeric feature matrix $\mathbb{X}$ and a vector of corresponding binary labels $Y$. Unfortunately, my data are text, not numbers. To address this, I create numeric features derived from the email text and use those features for logistic regression.

Each row of $\mathbb{X}$ is an email. Each column of $\mathbb{X}$ contains one feature for all the emails. I create a simple feature and more interesting ones as I try to increase the accuracy of my model.

**Part 3**

I need to identify some features that allow us to distinguish spam emails from ham emails. One idea is to compare the distribution of a single feature in spam emails to the distribution of the same feature in ham emails. If the feature is itself a binary indicator, such as whether a certain word occurs in the text, this amounts to comparing the proportion of spam emails with the word to the proportion of ham emails with the word.

**Part 4**

Notice that the output of `words_in_texts(words, train['email'])` is a numeric matrix containing features for each email. This means we can use it directly to train a classifier!

**Part 5**

Presumably, our classifier will be used for **filtering**, i.e. preventing messages labeled `spam` from reaching someone's inbox. There are two kinds of errors we can make:
- **False positive (FP)**: a ham email gets flagged as spam and filtered out of the inbox.
- **False negative (FN)**: a spam email gets mislabeled as ham and ends up in the inbox.

To be clear, I label spam emails as 1 and ham emails as 0. These definitions depend both on the true labels and the predicted labels. False positives and false negatives may be of differing importance, leading me to consider more ways of evaluating a classifier, in addition to overall accuracy:

**Precision**: Measures the proportion $\frac{\text{TP}}{\text{TP} + \text{FP}}$ of emails flagged as spam that are actually spam.

**Recall**: Measures the proportion $\frac{\text{TP}}{\text{TP} + \text{FN}}$ of spam emails that were correctly flagged as spam. 

**False positive rate**: Measures the proportion $\frac{\text{FP}}{\text{FP} + \text{TN}}$ of ham emails that were incorrectly flagged as spam. 

Note that a True Positive (TP) is a spam email that is classified as spam, and a True Negative (TN) is a ham email that is classified as ham.

### Project B.2

I build and improve on the concepts and functions implemented in Project B.1 to create my own classifier to distinguish spam emails from ham (non-spam) emails. I evaluate my work based on your model's accuracy and my written responses in this notebook.
