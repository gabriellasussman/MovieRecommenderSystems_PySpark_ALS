# MovieRecommenderSystems_PySpark_ALS
A Movie Recommender System using PySpark's ALS algorithm 

----------------------------------------------------------------------

The MovieLens is a dataset that is collected by the GroupLens Research Project at the University of
Minnesota and made available rating data sets from the MovieLens web site. You can download and
unzip the MovieLens 100K Dataset (ml-100k.zip) from this link: http://grouplens.org/datasets/movielens/

u.data is the dataset for this project

The full dataset contains 100,000 ratings by 943 users on 1682 items. Each user has rated at 
least 20 movies. Users and items are numbered consecutively from 1. The data is randomly
ordered.The format is:
user_id<tab>item_id<tab>rating<tab>timestamp.

The time stamps are unix seconds since 1/1/1970 UTC

In this project I have build a recommendation model using Alternating Least Squares (ALS).
The performance of the models are measured using Mean Squared Error (MSE), and I have used
10-fold cross validation and the Cold-start strategy to try to improve the model's
performance, including using ParamGridBuilder() to try different hyperparameters in order 
to find out the best parameters to use in the model.

The code will output the top 10 movies for all the users with the following format:
userID<\tab>itemID1,itemID2,itemID3 ...,itemID10
