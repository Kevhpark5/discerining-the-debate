# Discerning the Debate

## Overview

### The Data
Using the full debate transcripts provided by Politico.com and The American Presidency Project hosted at the University of California, Santa Barbara, each line was recorded into a dataset through webscraping and cleaning processes. Debates contained up to 20,000 words, equating to about 11000 sentences as rows of data in total. 11 debates were used for the analysis.
### EDA
Inital exploration was centered around Hillary Clinton's data throughout the primary debates as well as her debates against Donald Trump. The total number of sentences said per candidate for the primaries are shown below:

![primarycount](Data/Images/primarylines.png)

Clearly there are two main candidates considering the primaries, with Hillary Clinton and Bernie Sanders speaking the most lines compared to Martin O'Malley. Considering the debates are meant to give the most prominent candidates equal time to speak, this data is appropriate.

Below is the count between Hillary Clinton and Donald Trump during the main presidential debates:

![prescount](Data/Images/preslines.png)

Interestingly, the divide is much larger when there are only two candidates supposed to give equal time. This could be due to numerous factors, such as sentence length, and rebuttals spoken outside of the candidate's allocated time to speak.

In terms of word counts, the following were the most common words for the primaries:

![wordcount1](Data/Images/wordcountsprim.png)

Similar words can be found in the presidential debate count:

![wordcount2](Data/Images/wordcountpres.png)

Noting some words that are the most frequent seem that they should be associated with other words, such as "street". This will be accounted for later in the analysis.

## Analysis
### Speaker Classification
Initial attempts at analysis involved creating a classification model to discern the speech between Trump and Clinton during the 2016 election. Several models were used to predict the speaker using the three Presidential Debates. Multinomial Naive Bayes and Logistic Regression had the best results. The Precision-Recall Curves for these models are provided below.

![initial_roc](Data/Images/presspeakerroc.png)

![initial_poc](Data/Images/prespoc.png)


The following table shows the results for Multinomial Naive Bayes:

| Multinomial NB|               |
| ------------- | ------------- |
| Accuracy      | .727          |
| Precision     | .746          |
| Recall        | .573          |

According to these findings, predicting speakers

### Audience Reaction Prediction
Further analysis involved predicting which terms and lines spoken lead to audience reaction and applause. In total, the audience applause indicators, in which the transcripts explicitly noted "[applause]" and in other similar ways. Lines that contained these indicators or led to sole moments of applause were considered to be the lines leading to the applause. However, in total, the total instances of applause equated to less than 10% of the rows in the data, therefore, undersampling, oversampling, and other methods were used for analysis.

Despite these adjustments and compensations, the final results were very poor. Two model scores are shown:

| MultinomialNB         |        |
| ------------- | ------------- |
| Accuracy | .721 |
| Precision| .132 |
|Recall| .424|


|Random Forest| |
|-|-|
|Accuracy|.865|
|Precision|.107|
|Recall|.088|

Unfortunately, these results reveal very little in terms of predictions. So some adjustment must be made. Possible reasons as to why the prediction models struggled could be the instances of rebuttals/short remarks that produced audience cheers. These one or two word responses would carry more weight in the prediction model, and would thus influence the results heavily.


## Conclusion and Future Steps
### Conclusion
Classifying which speaker spoke according to the debate transcripts can be done to some degree. Identifying distinct speaker tones/dialogue can help specific topic modeling in the future to determine which policies have the most focus.

Very little can be said in terms of what lines spoken contribute to audience reaction and applause with the current models. Further analysis and model creation should be done.