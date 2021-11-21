# Yelp Sentiment Analysis


## Abstract:
Building unsupervised Natural Language Processing (NLP) machine learning models to predict whether a business review text is positive or negative. Also, assigns topics(clustering) based on the raw text data to find out the business domains and implement a recommendation system.
## Data:
Two separate datasets were imported from [Yelp](https://www.yelp.com/dataset) in json format. The first data contains the user's review text the other one contains the business names. The two datasets were merged and a sample of 10000 observations was selected.
## Design:
Starting with performing EDA such as removing duplicates, null values, and unnecessary columns. Also, converting user stars rating column to a sentiment column with only two values (positive and negative). For data visualization, we used Scattertext, seaborn, and matplot.
Next, preprocessing the user's review text by applying the below methods:
- Removing digits, punctuation, special characters, stop words and non-English words, 
- Adding a spell checker
- converting words to lower case
- Lemmatization
- Vectorization

After applying vectorization, a logistic regression model was selected as a baseline. From there we tried different models as well such as MultinomialNB, BernoulliNB, Logistic Regression Weighted, ada Boost, Random Forest, and Extra Tree. After comparing the accuracy and F1 scores for all the mentioned models the bassline Logistic Regression provided the best result.  
Topic Modeling was the most time-consuming since we had to revest the text preprocess stage to add more stop words and do research about the Yelp app categories and sub-categories while waiting for the device to finish with computing. (LSA, NMF, Corex)(CV & TF-IDF) were used for topic clustering with NMF giving the clearest six topics.
Note: K-means clustering count vectorizer and TF-IDF were attempted but showed poor results.
We designed two recommendation systems showing what business you should try and what not. This was successfully done by separating our clean data frame into two datasets one with only the positive sentiment and the other with only the negative. Then creating dummy variables for all businesses and summing up all the user's ratings with taking into consideration the unique users-ID.

## Algorithms:


| Model | Count Vectorizer Train | Count Vectorizer Validation | Count Vectorizer F1-Score | 
| :---: | :---: | :---: | :---: | 
| Logistic Regression | 0.944 | 0.936  | 0.544 | 
| MultinomialNB| 0.891 | 0.891 | 0 | 
| BernoulliNB | 0.870 | 0.871 | 0 | 
| Logistic Regression Weighted | 0.938| 0.927  | 0 |
| Ada Boost | 0.868 | 0.869  | 0| 
| Random Forest | 0.8580 | 0.8616  | 0 | 
| Extra Tree| 0.8916 | 0.8856  | 0 | 

| Model | TF-IDF-Train | TF-IDF-Validation | TF-IDF-F1-Score | 
| :---: | :---: | :---: | :---: | 
| Logistic Regression | 0.940 | 0.937  | 0 | 
| MultinomialNB| 0.898 | 0.898 | 0 | 
| BernoulliNB | 0.870 | 0.871 | 0 | 
| Logistic Regression Weighted | 0.934| 0.927  | 0 |
| Ada Boost | 0.868 | 0.868  | 0| 
| Random Forest | 0.9035 | 0.9067  | 0 | 
| Extra Tree| 0.9266 | 0.9179  | 0 | 

#### Count Vectorizer NMF

- Topic: 0(Food menu) sauce, menu, cheese, fresh, dish, sweet, pork, flavor, salad, meat, taste, beef, meal, rice, fish, spicy, lunch, soup, cream, hot 
- Topic: 1(bars) bar, staff, night, drinks, table, drink, beer, area, coffee, hour, friends, happy, work, location, free, line, bartender, server, parking, friend 
- Topic: 2(Automotive)car, customer, work, manager, rental, honda, phone, cars, company, dealership, hours, vehicle, business, days, drive, oil, sales, guy, change, appointment
- Topic: 3(Italian food) pizza, cheese, crust, sauce, topping, slice, sausage, salad, pepperoni, garlic, pie, slices, fresh, italian, delivery, bread, oven, half, dough, pasta 
- Topic: 4(restaurant)restaurant, table, menu, meal, server, dinner, waitress, restaurants, waiter, seated, dining, dishes, wine, manager, tables, dish, reservation, dessert, party, family
- Topic: 5(food) chicken, fried, rice, sandwich, salad, spicy, sauce, crisp, lunch, fries, hot, wings, sides, curry, thai, soup, juicy, beans, cheese, dry


#### Negative recommendation System output example:

User-ID ‘t5SRIRU6INiAyVkiMJhRPA’
Don’t go to these businesses :[('Prides Osteria'), ('Bonchon Salem'),("Santarpio's Pizza")]

#### Positive recommendation system output example:
There are 1 businesses that user ID# 2 did not visit 1 businesses for User ID# 2 to check out: ['Yamato Sushi Restaurant'] 

#### User similarity output example:
User ID# 2 is most similar to User ID# #1335 

#### Business similarity output example:
business  ‘Finz Seafood & Grill ‘Similar businesses :
[('Scratch Kitchen', 2), ('Howling Wolf Taqueria', 2), ('Engine House Pizza', 2)]
 
## Tools:
•Jupyter Notebook •Seaborn •Matplotlib •Numpy •Pandas •Sklearn •Pickle •Nltk •String •Regular Expression •Scattertext•Spacy

## Communication:
Pdf and PowerPoint slides used to communicate our findings and results.










