# Wrangle and Analyze Data
In this project, I gathered, assessed, and cleaned data then analyzed, visualized. 
The entirety of this project was implemented using Python language, Pandas, Matplotlib,  Seaborn, Requests, Tweepy, Json, and NumPy under Data Analyst Nanodegree Program from Udacity!

# Dataset
The dataset that you will be wrangling (and analyzing and visualizing) is the tweet archive of 
Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that 
rates people's dogs with a humorous comment about the dog. These ratings almost always 
have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 
12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million 
followers and has received international media coverage.

# Data Wrangling
Data wrangling, which consists of: 
- Gathering data 
The data used was gathered from three different sources:
1. Enhanced Twitter Archive dataset was a file on hand. The file was stored in the CSV file.
2. Image Predictions File dataset was retrieved from Udacity’s servers through the Requests library. The file was stored in the TSV file.
3. Data via the Twitter API dataset was retrieved from Tweeter’s API call, using the Tweepy library. Retrieved data was stored in JSON format.

- Assessing data 
After gathering each of the above pieces of data, I assessed them visually and 
programmatically for quality and tidiness issues.
1. Tidiness Issues
• doggo, floofer, pepper, and puppo columns should be one column 
(merge columns).<br/>
• twitter_archive, image_predictions, and tweet_data Dataframes 
should be part of one Dataframe (merge dataframes).<br/>
2. Quality Issues 
• Delete retweets by filtering the NaN of retweeted_status_user_id.<br/>
• Delete in_reply_to_status_id, retweeted_status_id, in_reply_to_user_id 
retweeted_status_user_id, retweeted_status_timestamp columns.<br/>
• Correcting data type in tweet_id (from int into string).<br/>
• Correcting data type in timestamp (from string into datetime).<br/>
• Delete rows with jpg_url have missing.<br/>
• Create 1 column for dog image prediction and 1 column for dog 
image prediction confidence.<br/>
• Delete p1, p1_conf, p1_dog, p2, p2_conf, p2_dog, p3, p3_conf, p3_dog, 
img_num columns.<br/>
• Convert underscore to space and convert lowercase to uppercase in 
prediction_dog.<br/>

- Cleaning data 
The previous issues I cleaned as appropriate resulting in high quality and tidy 
master pandas DataFrame.
