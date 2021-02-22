# Natural Language Processing with Disaster tweets

This repo contains an approach I implemented for the Disaster Tweets competition on Kaggle. This particular challenge is perfect for data scientists looking to get started with Natural Language Processing, and Kaggle in general. You can access the Kaggle competition [here](https://www.kaggle.com/c/nlp-getting-started)

## About the Competition

In this competition, you’re challenged to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t. You’ll have access to a dataset of 10,000 tweets that were hand classified.

## Data

Each sample in the train and test set has the following information:

- The `text` of a tweet
- A `keyword` from that tweet (although this may be blank!)
- The `location` the tweet was sent from (may also be blank)

### Files
- **train.csv** - the training set
- **test.csv** - the test set
- **sample_submission.csv** - a sample submission file in the correct format

### Columns
- `id` - a unique identifier for each tweet
- `text` - the text of the tweet
- `location` - the location the tweet was sent from (may be blank)
- `keyword` - a particular keyword from the tweet (may be blank)
- `target` - in train.csv only, this denotes whether a tweet is about a real disaster (1) or not (0)

## My approach
Ful Kaggle notebook with explanations available [here](https://www.kaggle.com/nikhiljohnk/powerful-glove-embeddings-bilstm-network)

As in one of my [previous repositories](https://github.com/nikjohn7/News-Sentiment-Prediction), I used GloVe Embeddings + a BiLSTM Network. 

### Why GloVe with BiLSTM?
GloVe word embeddings are generated from a huge text corpus like Wikipedia and are able to find a meaningful vector representation for each word in the news data.
This allows us to use Transfer learning and train further over our data.
In this project I have used the 50-dimensional data.
When used with a BiLSTM, the results seem to be better than Bag-of-Words and Tf-Idf vectorization methods.
