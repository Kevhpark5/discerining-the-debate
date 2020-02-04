# Discerning the Debate - By: Kevin Park

## Overview

## The Data
Using the full debate transcripts provided by Politico.com, each line was recorded into a dataset through webscraping and cleaning processes. Debates ranged around 20,000 words, translating to about 400 lines rows of data per debate. A total of _ debates were used for the analysis.
## EDA
TBD
## Analysis
Initial attempts at analysis involved creating a classification model to discern the speech between Trump and Clinton during the 2016 election. Two models were considered at first, both Multinomial Naive Bayes and Logistic Regression, to predict the speaker using the three Presidential Debates not including the primary. The ROC Curves and Precision-Recall Curves for these models are provided below.

![initial_roc](Data/Images/Initial_ROC.png)
![initial_poc](Data/Images/Initial_POC.png)