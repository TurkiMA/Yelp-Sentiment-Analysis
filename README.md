# Yelp Sentiment Analysis

## Introduction:

Yelp is one of the most famous business review app in the Western Hemisphere countries, with more than 52 million unique visitors to its mobile sites as of December 2020. Yelp released some of their business reviews data online for educational purposes and we found it to be really interesting to work on for this project. 

## Project Objective:

building unsupervised Natural Language Processing (NLP) machine learning models to predict whether a business review text is positive or negative. Also, to build a recommendation system based on user id and review rating to predict the best business match for every user. Moreover, we will use NLP and unsupervised machine learning to find out what is the business domain based on users reviews text, and keywords.

## Data Description:

The datasets were imported from Kaggle in json format. Two datasets(reviews and business) contain over 8 million observations and 16 columns. some of them will be very useful for our goals such as text, user id, business id, stars for rating, and business name. stars (rating) between 1 to 5 were converted to the sentiment with 4 and 5 being positive and 1 and 2 negative. note 3-star rating where dropped.

## Stratgy:

-	Importing our data and selecting a sample of 100000 observation
-	Performing exploratory data analysis
-	Applying natural language processing techniques
-	Perform dimensionality reduction/topic modeling
-	Apply the results of dimensionality reduction/topic modeling

## Tools
•Jupyter Notebook •Seaborn •Matplotlib •Numpy •Pandas •Sklearn •Pickle •nltk •string •Regular expression
