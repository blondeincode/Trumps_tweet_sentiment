# Sentiment analysis and search for the most frequently used words in Donald Trump's tweets in 2017-2020
## Project Overview

* the data has been downloaded from the website [www.thetrumparchive.com](https://www.thetrumparchive.com);
* the analysis was conducted on tweets published from January 20, 2017 to December 31, 2020;
* only tweets in English were analyzed;
* sentiment analysis was carried out using the TextBlob library;
* the thematic modeling was performed with the Latent Dirichlet Allocation (LDA).

After retrieving the data, I had to clean it to make it usable for analysis. I made the following changes and created the following variables:

* Created columns containing hashatgs, mentions, retweets;
* To clear the text removed links, punctuation marks, numbers, emoji icons, multiple spaces and the characters '@', '#', 'RT';
* Removed tweets with no text;
* The languages in which the tweets were written were identified;
* Tweets have been tokenized, lemmatized and stopwords removed.

As a result of the above operations, I received the following columns:
'text', 'clean_tweet', 'date', 'retweeted', 'mentioned', 'hashtags', 'language'.

To perform the analysis, it was necessary to define for each tweet:
* Subjectivity
* Polarity
* Sentiment

Then I checked how the number of tweets changed, taking into account the division into negative / neutral / positive tweets in individual years.

Finally, I conducted thematic modeling using Latent Dirichet Allocation and designated 10 topics that the analyzed tweets cover. For each topic, the 10 most frequently used words in tweets are highlighted.
