# Customer Service Text Generation using NLP Algorithms and Models

## Summary

The purpose of this project is to show how to build a customer service text generator using Natural Language Processing algorithms using the Keras API and TensorFlow. The generator is intended to possibly replace the first interaction many consumers have with a company. And will either offere information to help the customer or if the issue is escalated it will send the consumer to a human representative. This would allow a company to have a smaller customer service team dealing with more important issues. I made a dataset of customer service tweets pulled from Twitter using Twitter's API and the tweepy library in Python. A jupyter notebook showing how to do this is in the repo. The purpose of the models are to learn from the tweets and be able to respond to a seed tweet either asking for help or some other customer service option. The models build in complexity and are explained in detail about how to build the models, why layers are chosen, and how certain model options affect the text generator. 

## Tweet Generator

This notebook is dedicated to working with the Twitter API by using the Tweepy library. The Tweepy library allows you to use Python to interact with the Twitter API. With the Tweepy API you are able to pull tweets, analyze them, send tweets, look at users, etc. For this project the main focus of this notebook is to access as many tweets as possible from ten well reviewed customer service accounts on Twitter. These accounts are known for responding to customers tweets as well as offering solutions or where to find more information. While there are some limits to the amount of tweets you can pull from individual accounts. I was able to get a little more than 7,000 tweets. While more tweets would have been better, I tried to make sure that the tweets had meaningful content and weren't just words spewed by bots that are incoherent. The original data set for this project consisted of tweets containing the words "big data" or "data science." While this sounds like an ideal way of training a data science bot to tweet in these terms, there were several issues. Many tweets had nothing to do with data science, perhaps they were themselves produced by bots and then you have a loop of one bad bot creating another bad one and so on with no useful output. Another issue that was encountered was the models would predict the words "big data" and "data science" over and over again in a loop. They seemed to have found the search criteria for the tweets and would get stuck in a loop. In the end I stuck with the customer service tweets and tried to make thoses work. The results can be found in the model notebooks. 

[Tweet Generator](text_generator.ipynb)

## Character Level RNN Model using LSTM layers


The first model is a simple character tokenized RNN with a few LSTM layers.

The second model is word tokenized and uses a similar RNN archeticture
