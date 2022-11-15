# WeRateDogs - Twitter Archive - Data Wrangling and Analysis Project
## by (Shoh Chama Anderson Abi-Ache)


## Dataset

The dataset that I wrangled (and analyzed and visualized) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog.

Most of the focus of this project was on data wrangling. So what exactly is data wrangling? Data wrangling refers to the process of cleaning, restructuring and enriching the raw data available into a more usable format

The WeRateDogs Twitter project goals included:

- Wrangling the data
- Gathering data
- Assesing data
- Cleaning data
- Storing the wrangled data
- Analyzing and visualizing wrangled data
- Reporting on the wrangled effors and insights obtained from the data

The data that were gathered are:

1. The WeRateDogs Twitter archive: twitter-archive-enhanced.csv. This file was provided to Udacity students and contains basic tweet data for all 5000+ of their tweets till August 1, 2017
2. The tweet image predictions: image-predictions.tsv. This file contains the breed of dogs, images etc. that is present in each tweet according to a neural network.
3. Additional data from the Twitter API: tweet-json.txt. This file conatins each tweets retweet count and favourite count at minimum.

## Summary of Findings

Analysis
There are several analysis that can be done on the WeRateDogs data, I have done 3 analysis and provide 3 insights.

First i defined the questions i wanted answers to from my dataset and they are

Questions
What are the top 5 most popular dog names?
What day of the week do people tweet mostly about dogs?
What are the top 5 dog breeds in the p1 column?
Insights
The dataset has various names that were given to the dogs that were tweeted. Names are important because they give a personal conenction especially to dogs.

Ignoring the None labels, the top 5 most popular dog names are

 1. Charlie
 2. Oliver
 3. Lucy
 4. Cooper
 5. Penny
Timestamps are important in data and markerting to determine the days most people are on social media which could be used to target ads. The timestamps for the WeRateDogs data tells us that Mondays has the highest tweets.
Dog Breed popularity: The most popular dogs breeds are:
 1. Golden Retriever
 2. Labrador Retriever
 3. Pembroke
 4. Chihuahua
 5. pug


Visualizations
There is a positive correlation between the retweet counts (how much a post was retweeted) and favourite ("likes") counts. The correlation is important to understand when determining methods to incread users traffic.





## Key Insights for Presentation

Assessing Data
Once all required data was gathered, I began to assess the data based on quality and tidiness issues

**Quality Issues identified**
- Some tweets contains retweets and therefore duplicates
- Some tweets are replies and therefore duplicate
- Drop columns: ('in_reply_to_status_id', 'in_reply_to_user_id', 'retweeted_status_id', 'retweeted_status_user_id', 'retweeted_status_timestamp'), they are not needed
- Inaccurate data: Some dog names are 'None', 'a', 'an', 'the', 'quite', 'such' etc.
- 'timestamp' datatype is object instead of datetime
- Consistency issues in columns (p1, p2, and p3) Dog's breed has no standard. Capital letter or lowercase names
- Standardize dog ratings
- tweet_id should be a string not int datatype for the 3 datasets

**Tidiness Issues identified**
- doggo, floofer, pupper, and puppo are categorical variable, and can be combined into one column.
- the 'text' column has more than one information in a single column (tweet and URL)
- Merge the 3 tables together

**Cleaning Data**
After assessment and documenting the quality and tidiness issues, I cleaned the data by

- defining the issues to be cleaned
- coding to solve the issue
- testing to see if the code worked well

But before cleaning the data, I copied each dataset so as to keep the original dataset intact in case I need to refer back to it in future.

**Define, code and test steps:**

 - Delete rows that have retweets 'retweeted_status_id
 - Drop any tweet with 'in_reply_status_id'
 - drop columns in 'twitter_archive' that are not needed using .drop() method
 - Replace inaccurate dog names with an empty string
 - Change the datatype of 'timestamp' to datetime
 - Standardize the dog breeds (convert all names to lowercases, all spaces and hyphens to underscore)
 - Convert numerator and denominator datatypes to float, remove non expected value of denominator and numerator anything different of 10
 - Convert 'tweet_id' to string
 - Merge doggo, floofer, pupper and puppo columns into one column
 - Merge the clean versions of twitter_archive, image_prediction, and df_tweet_json dataframes to create a master dataset

**Storing Data**
The cleaned data was stored to a CSV file named "twitter_archive_master.csv"
