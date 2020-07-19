# SentimentAnalysis

                                       Project 1: Twitter Sentiment Analysis
                                       
__Problem Statement__: The objective of this project is to detect hate speech in tweets. For the sake of simplicity, we say a tweet contains hate speech if it has a racist or sexist sentiment associated with it. So, the task is to classify racist or sexist tweets from other tweets.

Formally, given a training sample of tweets and labels, where label '1' denotes the tweet is racist/sexist and label '0' denotes the tweet is not racist/sexist, your objective is to predict the labels on the test dataset.

__Dataset has been downloaded from:__ *__https://www.kaggle.com/c/twitter-sentiment-analysis2/data__*

__Steps Involved:__
1.	Importing libraries needed and Loading Data

2.	Reviewing dataset

3.	Pre-processing and Cleaning text which includes:

       •	Data Inspection: Searching for raciest/sexiest tweets or non-raciest/sexiest tweets.

       •	Data Cleaning: To remove unwanted text patterns from the tweets like, twitter handles, punctuations , numbers ,special characters and small words.

       •	Tokenization: It is the process of splitting the strings into tokens.

       •	Normalization: normalizing the tokenized tweets.

       •	Extracting feature from cleaned tweets using following features:
   
            a.	Bag-of-Words
            b.	TF-IDF
            c.	Word2vec
            d.	Doc2Vec
            
4.	Classification and Evaluation : Building models on the datasets with different feature sets prepared in the earlier sections — Bag-of-Words, TF-IDF, word2vec vectors, and doc2vec vectors. We will use the following algorithms to build models:

            	Logistic Regression
            	Support Vector Machine
            	RandomForest
            	XGBoost
            
5.	Model Finetuning using DMatrix .

General Approach for Parameter Tuning

We will follow the steps below to tune the parameters.

    1. Choose a relatively high learning rate. Usually a learning rate of 0.3 is used at this stage.
    2. Tune tree-specific parameters such as max_depth, min_child_weight, subsample, colsample_bytree keeping the learning rate fixed.
    3. Tune the learning rate.
    4. Finally tune gamma to avoid overfitting.
    
            	preparing a custom evaluation metric to calculate F1 score.
            
__Results:__ Considering the evaluation metric of the F1 score, our best performing model is XGBoost with tuned params applied on the Word2Vec features with an F1 score of 0.66. XGBoost model on word2vec features has outperformed all the other models.
