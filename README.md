# Discerning the Debate

## Overview

## The Data
Using the full debate transcripts provided by Politico.com and The American Presidency Project hosted at the University of California, Santa Barbara, each line was recorded into a dataset through webscraping and cleaning processes. Debates contained up to around 20,000 words, translating to about 7000 sentences as rows of data per debate. A total of _ debates were used for the analysis.
## EDA
Inital exploration was centered around Hillary Clinton's data throughout the primary debates as well as her debates against Donald Trump. The total number of sentences said per candidate for the primaries are shown below:

![primarycount](Data/Images/primarylines.png)

Clearly there are two main candidates considering the primaries, with Hillary Clinton and Bernie Sanders speaking the most lines compared to Martin O'Malley. Considering the debates are meant to give the most prominent candidates equal time to speak, this data is appropriate.

Below is the count between Hillary Clinton and Donald Trump during the main presidential debates:

![prescount](Data/Images/ClintonTrumpLines.png)

Interestingly, the divide is much larger when there are only two candidates supposed to give equal time. This could be due to numerous factors, such as sentence length, and rebuttals spoken outside of the candidate's allocated time to speak.

## Analysis
Initial attempts at analysis involved creating a classification model to discern the speech between Trump and Clinton during the 2016 election. Two models were considered at first, both Multinomial Naive Bayes and Logistic Regression, to predict the speaker using the three Presidential Debates not including the primary. The ROC Curves and Precision-Recall Curves for these models are provided below.

![initial_roc](Data/Images/Initial_ROC.png)
![initial_poc](Data/Images/Initial_POC.png)