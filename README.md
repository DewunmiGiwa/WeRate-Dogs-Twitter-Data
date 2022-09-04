# Data-Wrangling-Project (Udacity Data Analyst Nanodegree)
I wrangled and analyzed the WeRateDogs (@dog_rates) Twitter data

I have successfully gathered, assessed, cleaned and visualized the twitter_archive dataset, image_predictions dataset, and json data file obtained after querying twitter API.
My data wrangling process was in three stages (Data Gathering, Data Assessing, Data Cleaning).

## Data Gathering
I began with gathering all three datasets to be used in the project. 
I directly downloaded the WeRateDogs Twitter archive data from the classroom and read it into a Pandas DataFrame
I downloaded the image predictions dataset from the url provided using the request and the os libraries. 
I queried each tweet's retweet count and favourite count using the Tweepy library and stored the data in tweet_json.txt. Thereafter, I read the tweet_json.txt line by line into a pandas DataFrame with tweet_id, favourite count, and retweet count. 

## Data Assessing
I assessed my data both visually and progamatically, and observed the following issues relating to inappropriate dog names, dropping irrelevant columns, NaN rows, removing retweets, merging and spliting columns, and merging all three datasets.

All issues observed were addressed and cleaned. After cleaning, all three datasets were merged. I made the following insights:

## Insights:
1. The most common source of tweets was Twitter for iphone, and the least common source was TweetDeck
2. The most common dog name is Cooper
3. A dog named 'Stephan' from the Chihuahua breed had the highest number of likes and retweets

## The following visualizations were made:
1. Distribution of the top 20 dog breeds
2. Top 20 most common dog names
3. Distribution of the least 20 dog breeds
