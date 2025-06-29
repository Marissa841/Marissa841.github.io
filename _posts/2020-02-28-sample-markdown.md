---
title: NLP Project
date: 2022-11-29
layout: post
category: General
---

NLP Project 

For the following, I will detail the steps I took to complete an NLP project. The business case, to start, was to find a model that would be able to assess whether a tweet could be marked as either positive or negative. I looked at the different machine learning models by the f1 score and chose the one that was closest to 1. After several run-throughs of models, I found the first iteration of a random forest model from sci-kit learn had the highest f1 score at 0.93. The following paragraphs will detail the steps I took to arrive at that score. 

To begin, I first applied the OSEMN data analysis method where I would follow the order of obtaining the data, scrub, explore, model, and then interpret the findings. I obtained the data from Crowd Flower on the data.world website. The data contained a single CSV file with three rows and a little over 9,000 columns. Once the data was loaded into a data frame, I began the second portion of the OSEMN method, scrub. To do this, I took a look at the data frame and used .describe() and .shape. With .describe(), I was able to see that the most commonly marked tweet was neither “Positive emotion” nor “Negative emotion”, but marked as  “No emotion toward brand or product”. I then dropped the “No emotion toward brand or product” value as well as the “I can’t tell” value. The reason for dropping these two values is that I wanted the machine learning models to find out which tweets were positive or negative. I decided it’d be a lot easier for the models to train on tweets that were marked decisively, rather than neutral. 

For the next portion of the scrubbing and exploring stage, I began to apply the well-known packages and data-cleaning methods that are associated with a typical NLP project. I changed the text of the tweets to lowercase, removed punctuation, and removed stop words. For the stopwords, I loaded them into my notebook and applied the English setting to NLTK(Natural language tool kit). Stopwords are removed because they are the most common words in the data and language, but provide little elaboration or specificity towards an NLP problem in general, and my project problem in particular. Stopwords are useful in every other context in spoken and written language, I would say, but for machine learning, they are too widespread to provide anything gainful in a machine learning context. 

After I removed the stopwords, I added a couple of graphs (+) that would show what were the top 10 most common words in positive tweets versus negative tweets. For positive tweets, interestingly, there were no specifically associated “positive” words present. The top ten words can be seen below:

![words in positive tweets](https://raw.githubusercontent.com/Marissa841/Marissa841.github.io/master/images/nlp_project_post/words_in_positive_tweets.PNG)

 For the top 10 negative tweets, there were also somewhat bland words that wouldn’t be associated with being “negative”:

![words in negative tweets](https://raw.githubusercontent.com/Marissa841/Marissa841.github.io/master/images/nlp_project_post/words_in_neg_tweets.PNG)

After obtaining, scrubbing, and exploring the data, I then applied a function that would input the train test split “x” and “y” values, input a model, and apply bag-of-words, TF-IDF, or neither. Bag-of-words is a commonly used model that counts the number of times a word occurs in a document and I wanted to include that to allow the model to have an easier time with computation. TF-IDF stands for term frequency-inverse document frequency. Using the Tfidf vectorizer would help associate how relevant a word is to a given document. It can determine which words are most important to a given document. Once I had applied my function, I think iteratively ran through models to find which one would output the best f1-score. I first ran through basic logistic regression, a decision tree classifier, and a random forest classifier, all with a bag of words. I then ran through the same three models, with bag-of-words, and also added the argument “class-weight=” balanced”, to help with the imbalance of positive and negative tweets. After that iteration, I did the same three classification models, but instead, applied tfidf. And for my final run-through of models, I used tfidf, and “class_weight = “balanced”. From these four iterations of modeling, I found that the basic bag-of-words random forest classifier achieved the highest f1_score close to one, at 0.93. 

Once I had the best model, I moved on to the OSEMN method of interpretation and looked at the feature importance (word importance) of the random forest model. Here I found that in the top 10 most important words, there were slightly more words associated with negative tweets that carried more weight. To further look at the information, I applied another function “word_count_by_class” to gain a sense of the target count when adding a keyword from a tweet. 

Finally, my conclusions from this project are that with machine learning, we can predict whether a tweet is positive or negative. Also, negative tweets have strongly negative words while positive tweets have less obvious words that indicate positive sentiment. For future work with this dataset, I’d be interested to look at the labels of the tweets more closely. Some tweets appear to be incorrectly marked within the dataset. 

