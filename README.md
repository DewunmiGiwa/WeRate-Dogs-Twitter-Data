# WeRate-Dogs-Twitter-Data
I wrangled and analyzed the WeRateDogs (@dog_rates) Twitter data

I have successfully gathered, assessed, cleaned and visualized the twitter_archive dataset, image_predictions dataset, and json data file obtained after querying twitter API. My data wrangling process began with gathering all three datasets to be used in the project. 

I directly downloaded the WeRateDogs Twitter archive data from the classroom and read it into a Pandas DataFrame, I downloaded the image predictions dataset from the url provided using the request and the os libraries. 

I queried each tweet's retweet count and favourite count using the Tweepy library and stored the data in tweet_json.txt. Thereafter, I read the tweet_json.txt line by line into a pandas DataFrame with tweet_id, favourite count, and retweet count. 

For the data assessing, I assessed my data both visually and progamatically, and observed the following issues:

## Quality Issues in The Twitter Archive Dataset
1. Some dog names are not actual names
2. full html link should be replaced with the actual source in the source column
3. remove retweets by dropping rows with values in the retweeted_status_id column
4. drop the following columns: in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id column, retweeted_status_user_id, retweeted_status_timestamp, text.
5. after spliting timestamp column, drop the timestamp column
6. drop pupper, doggo, puppo and floofer columns after merging into one "dog_stage"
7. drop expanded_urls column

## Tidiness Issues in The Twitter Archive Dataset
1. The timestamp column should be split into date and time columns, and dtype of the date column should be changed to datetime
2. doggo, floofer, pupper, and puppo columns should be merged into one (dog_stage)

## Quality Issues in The Image Predictions Dataset
1. some dog breeds are not actual dog breeds. remove p1_dog, p2_dog, p3_dog values set as 'False: as they are not dogs of any breed

## Tidiness Issues in The Image Predictions Dataset
1. For each row, generate each maximum p_conf value and the corresponding p and p_dog values

## Additional Quality Issues
1. change data type of tweet_id column in all three datasets to string object before merging

## Additional Tidiness Issues
1. Merge all three datasets

All Issues Observed were Addressed and Cleaned. After cleaning, all three datasets were merged. I made the following insights:

## Insights:

The most common source of tweets was Twitter for iphone, and the least common source was TweetDeck
The most common dog name is Cooper
A dog named 'Stephan' from the Chihuahua breed had the highest number of likes and retweets

## The following visualizations were made
1. distribution of the top 20 dog breeds
2. top 20 most common dog names
3. distribution of the least 20 dog breeds

After assessing my data, i made a copy each of my three datasets before cleaning. I successfully cleaned all issues identified during assessing. After cleaning, I saved the gathered and combined dataset into master_twitter_archive.csv. 

Thereafter, I generated some insights and made some visualizations

 
