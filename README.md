# (Wrangle and Analyze Data)
## by (Oluyimika Sosanya)


## Dataset
> This data provided by Udacity in order to complete a Data Wrangling student project contains archived tweets 
of Twitter user [@dog_rates](https://twitter.com/dog_rates), also known as WeRateDogs.
WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. There are 2,356 tweets
with 17 features _(tweet_id, in_reply_to_status_id, in_reply_to_user_id, timestamp, source,
text, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp, expanded_urls, 
rating_numerator, rating_denominator, name, doggo, floofer, pupper, puppo)_.

## Goal of the project

> The goal of this project is to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses 
and visualizations. To achieve the goal of this project I gathered additional data from Udacity's server and 
Twitter's APIin different formats, and assessed the data gathered for dirtiness and messiness. Then, I proceeded to clean,
and then conduct an analysis of the cleaned data.

## Data Wrangling Process

> To obtain a dataset that is clean and fit for trustworthy analysis, I performed my data wrangling task using the following steps:

>1. **Gather**: The first step of my data wrangling process was to get the data that I needed for this analysis. 
For this project, the data were located in 3 different locations and formats, hence, required different data gathering methods. 
The methods used to gather all three pieces of data are:

>-   A manual download of the @WeRateDogs Twitter archive. It is a CSV file containing WeRateDogs tweet data.
>-	A programmatic download of an image predictions file using Python’s request library. It is a TSV file that contains predictions about the dog breed in the image accompanying each WeRateGogs tweet.
>-	A programmatic download of additional data directly from Twitter API using Python’s tweepy library. I used the tweet IDs in the archive file downloaded manually to query the API for retweet count and favorite count data for each tweet and stored it as a TXT file. Then, I read it line by line into a DataFrame.

>After successfully gathering the data, I loaded them into a DataFrame in readiness for the next step.

>2. **Assess**: I executed two types of assessments on the datasets.

>-	Visual assessment: I displayed each piece of gathered data in the Jupyter Notebook and assessed them visually. I also used 
a spreadsheet application to aid my visual evaluation of rows and columns not displayed in the DataFrame.
>-	Programmatic assessment: I used pandas’ functions and/or methods to assess the data.

>Based on the specifications given for the project, I spotted and documented eight (8) quality issues, including incomplete,
invalid, inaccurate, and inconsistent data, and two (2) tidiness issues.

>3. **Clean**: Before commencing cleaning operations, I made a copy of the original data for each piece of data. 
To organize my data cleaning task, I grouped detected issues into three priority levels:

>-   Completeness issue 
>-   Tidiness issue
>-	Quality issue

>Then, I used the **Define-Code-Test** framework to successfully clean all issues identified in the assessing phase 
using pandas’ functions and/or methods, and documented them.

>The conclusion of this process resulted in the creation of a master dataset, with all 
pieces of gathered and cleaned data, which I used for analysis.

## Key Insights

>1. Dog ratings do not determine likes and retweets. Dog breeds with a higher rating don't necessarily get the most likes.  

>2. Dog breeds drive likes and retweets with only 3 (out of 111) breeds accounting for the largest share (28%) of all likes. 

>3. The best time to post for more likes and retweets is between 2pm and 12am. However, engagement peaks at 12am and 4pm, respectively.
