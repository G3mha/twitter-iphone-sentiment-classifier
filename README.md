# iPhone tweet relevance classifier

A coursework project that implements Naive Bayes in Python to classify how
relevant a tweet is to iPhones. The labels measure relevance, rather than
positive or negative sentiment.

| Label | Meaning |
| --- | --- |
| 0 — Very irrelevant | Off-topic or minimal content |
| 1 — Irrelevant | Sales advertisements |
| 2 — Neutral | Jokes or casual mentions |
| 3 — Relevant | Indirect iPhone-related comments |
| 4 — Very relevant | Direct opinions, questions, or purchase intent |

“Neutral” is the dataset’s name for the middle relevance category; it does not
mean neutral sentiment.

## Files and evaluation

- [Classifier notebook](src/tweet_sentiment_classifier.ipynb): preprocessing,
  classification, and evaluation.
- [Collector notebook](src/tweet_data_collector.ipynb): historical Twitter data collection.
- [Labeled dataset](db/iphone_tweets_dataset.xlsx): training and test sheets.

The first evaluation uses five classes. The later experiment merges the two
irrelevant classes and the two relevant classes, then runs 100 random splits
with three classes. These are different classification tasks. Results depend
on the split; the notebook does not set a random seed.

The classifier notebook’s `filename` must point to the dataset above. Its legacy
`Series.append` calls require pandas 1.x or a code update for newer versions.
Dependencies are listed in [requirements.txt](requirements.txt).

Authors: Enricco Gemha, Rafael Coca Leventhal, and Marcelo Rabello Barranco.
