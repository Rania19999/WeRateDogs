# WeRateDogs
>- Gathering Data:
For this project, we gather data from 3 different sources: <br>

**-The WeRateDogs Twitter archive**: It is a csv file provided by Udacity classroom.<br>
**-The tweet image predictions**: It is a tsv file hosted on Udacity's servers and downloaded programmatically using the Requests library.<br>
**-Additional data from the Twitter API**: To Gather each tweet's retweet count and favorite ("like") count. <br>
In this case, we should create a twitter acount and set up a developer account, after that we use the tweepy library in order to create 
an API object that we can use to gather Twitter data,
and store each tweet's entire set of JSON data in a file called tweet_json.txt file. <br>
>- Assessing the data:<br>
In this step, we assess the pieces of data collected visually and programmatically for quality and tidiness issues.<br>

**Quality issues** : Visually, by exploring the data, we notice that the source column contain more information than 
those wanted and that there is Errors in the name of dogs column. <br>
Tidiness issues: The various stages of dog (doggo, floofer, pupper and puppo) should be in one column and we should concatenate df and df2 dataset. <br>
Programmatically: <br>
In this step, we used the functions provided by pandas library: <br>

df.info(): to check the missing values and the shape of the dataset. <br>
df.describe(): to have a general information about the int column (percentile, min and max values...;) <br>
df.dtypes: types of the value for each column <br>
df_clean.columns: to explore the columns of the dataset. <br>
df['column_name'].unique(): to see the values that vary in this column <br>
df.sample(5): in order to take 5 randomly rows from the dataset to have a genrela idea about it. <br>
df.tweet_id.isin(df1.tweet_id): to check if the two dataset cover the same tweets. <br>
After that, we notice that: <br>

The duplicated values are the retweeted tweets.(same information reposted) <br>

The rating numerator contain values more and less than 10. <br>

There are some missing tweet_id that exist in the df Dataset but not in the df1 dataset. <br>

Convert timestamp datatype to datetime. <br>

Convert in_reply_to_status_id, in_reply_to_user_id from float to int. <br>


>- Cleaning the data: <br>
First step done was the creation of a copy of our dataset, in order to keep our original data in case we make errors. <br>

For each point mentionned in the assessing step, we define the issue, We proceed to the programmatical treatment (coding) 
whether we have to drop those rows or redefine the errors, and finally, the testing step, to check if the issue was solved/ cleaned.<br>

>- Visualization:
After exploring those points: <br>
- The most source used for the tweets.<br>
- The most attributed numerator rating. <br>
- The distribution of ineteraction with the twitter account post's over time.<br>
- The distribution of tweets over years. <br>
We come up with those insights:<br>
- They are 3 sources used: "Iphone, Twitter Web,and tweetdeck", the most source used is Iphone. <br>
- The most attributed rating is 12.<br>
- The visual presentation of the interaction over time, make an insight about the The WeRateDogs Twitter account interaction. 
From 2015 to 2017, the interaction (reposts and likes) are growing. The WeRateDogs Twitter account content has more of attention over time from other users. <br>
- The WeRateDogs twitter account made a lot of posts "tweets" in 2016.<br>
