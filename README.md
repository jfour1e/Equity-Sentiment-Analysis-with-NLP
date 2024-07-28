# Equity-Sentiment-Analysis with NLP
 
This project involves building and training a Bidirectional Encoder Representations from Transformers (BERT) language model to perform web scraping of news from Twitter, CapitalIQ, and Reddit. The goal is to aid in short-term sentiment analysis and earnings trading.

## Project Overview

#### Features

Sentiment Analysis:

Plan to implement an automated web scraping functionality that scrapes news from Twitter, CapitalIQ, and Reddit.
Uses BERT to analyze the sentiment of the scraped news.
Provides sentiment scores for individual stocks and the overall market.

Earnings Trading:
Analyzes sentiment changes to inform trading decisions.
Suggests long positions in stocks with positive sentiment changes.
Suggests short positions in stocks with negative sentiment changes.

#### Beta Features (Currently Implementing)
Dynamic Portfolio:

Crafts a dynamic portfolio of stocks.
Enters long positions in a basket of stocks with positive sentiment changes.
Enters short positions in a basket of stocks with negative sentiment changes.

Consistent Portfolio Updates:
Updates the portfolio based on adapting market conditions.
Adjusts positions according to reversing sentiment in stocks or the overall market.


## Specifics about the BERT Model 

BERT: Bidirectional Encoder Representations from Transformers
BERT is a language model based on the transformer architecture, notable for its dramatic improvement over previous state-of-the-art models. It was introduced in October 2018 by researchers at Google. A 2020 literature survey concluded that "in a little over a year, BERT has become a ubiquitous baseline in Natural Language Processing (NLP) experiments, counting over 150 research publications analyzing and improving the model."

Key Features of BERT
Model Sizes:

BERTBASE: 12 encoders with 12 bidirectional self-attention heads totaling 110 million parameters.
BERTLARGE: 24 encoders with 16 bidirectional self-attention heads totaling 340 million parameters.
Training Data:

Pre-trained on the Toronto BookCorpus (800M words) and English Wikipedia (2,500M words).
Design:

Embedding Module: Converts an array of one-hot encoded tokens into real-valued vectors.
Encoder Stack: A sequence of Transformer encoder blocks performing bi-directional self-attention transformations.
Un-embedding/Decoder Module: Converts final representation vectors into one-hot encoded tokens by producing a predicted probability distribution over token types.
Tokenization:

Uses WordPiece tokenization, a sub-word strategy like byte pair encoding.
Utilizes a vocabulary size of 30,000 with any token not appearing in its vocabulary replaced by [UNK] for "unknown."
