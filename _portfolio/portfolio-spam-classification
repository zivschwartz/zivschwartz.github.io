---
title: "Spam Classification on SMS Messages"
date: 2018-12-08
excerpt: "Performing 'spam' or 'ham text classification on SMS messages.<br/><img src='/images/sempre_feature_performance.png' style='width:295px;height:254px;'>"
collection: portfolio
---

## Summary

For our assignment, we analyzed SMS text messages to classify them as ‘spam’ or ‘ham’. As online communication has adapted and shifted from email to various forms of direct messaging, phishers have adjusted where and how they target individuals with spam. Users want to know that their accounts and data are secure, and they do not have time to be bothered by receiving spam messages.

Our report can be found [here](https://github.com/zivschwartz/SpamClassification/blob/master/WhosInMyDMs-Final_Report.pdf), and relevant code can be found [in this GitHub repo](https://github.com/zivschwartz/SpamClassification).

**Methods**: Logistic Regression, Random Forest, and an LSTM Neural Network. For each of these models, we performed feature extraction using sparse vectoratization techniques, CountVectorizer and TfidfVectorizer, as well as utilizing bigrams, n-grams and word embeddings to test against a dense vector representation.

<p align="center">
  <img width="442.5" height="381" src="/images/sempre_feature_performance.png">
</p>

Logistic Regression seemed to perform the best, when used with the n-gram TF-IDF vectorization. It seems that the custom embeddings were not trained on enough data and possibly overfit, so that set of feature engineering did not seem so useful. The random forests models also seemed to overfit slightly, but the performance was comparable to the logistic regression. The LSTM classifier overfit completely.

