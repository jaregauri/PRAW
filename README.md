# Overview

![](https://i.imgur.com/LYcDAGm.png)

The project is about extracting data from a sub reddit where the opinions shared by this subreddit users will be unbiased as the users are assumed to be anonymous.

Data extracted: date when post was created, score, title and the top three comments

In this project I'm using PRAW which is an acronym for Python Reddit API Wrapper. This is a python package that allows users to access reddit’s API.

# What is an API Wrapper?

API Wrapper can be used to add functions that the API might not have itself
Create a wrapper with all the calls to the normal API, plus add code that will add additional functionality
A wrapper could be made to make it a lot easier to use the API, as it takes care of the background stuff that you don’t really need to worry about

PRAW has two types of instances: read-only and authorized.

• Read-only instance: With this instance we can only retrieve public information

• Authorized instance: With this instance we can comment, post, repost, upvote etc

For this case study I have used the Read-only instance as we are only extracting data and not posting anything so we dont need extra permissions apart from read

# Methodology 

First step is to extract data from ‘datascience’ sub-reddit by initializing the reddit read only instance.

To initialize this instance, we need to pass the client ID, client Secret and user agent information.

For getting the posts according to the date we need to capture
the created_utc value -> convert the integer to time.

To do this conversion I have imported time package and extracted the day, month and year values.

# Insights

• The posts collected are not only about DS research or tools. Majority of them talk about the real problems faced by data scientists, no matter how trivial the problem is.

• Most of the posts with high scores are memes which a lot of redditors find relatable. This also might be because memes don’t have a huge reading content.

• Unlike LinkedIn where every user is trying to contribute something and show how useful their posts are, reddit users discuss their issues openly. This might be because of the anonymous profiles.

• Even the comments are filled with unbiased opinions unlike LinkedIn.

• When redditors don’t agree with a point, no one is afraid of criticizing an author or a commentor in the comment section




