# Recommendation-System

Building recommendation system to scale using scikit-surprise (surprise library)

[Recommender systems](https://en.wikipedia.org/wiki/Recommender_system) are one of the most common used and easily understandable applications of data science. Lots of work has been done on this topic, the interest and demand in this area remains very high because of the rapid growth of the internet and the information overload problem. It has become necessary for online businesses to help users to deal with information overload and provide personalized recommendations, content and services to them.

Two of the most popular ways to approach recommender systems are [collaborative filtering](https://en.wikipedia.org/wiki/Collaborative_filtering) and [content-based recommendations](https://www.analyticsvidhya.com/blog/2015/08/beginners-guide-learn-content-based-recommender-systems/). In this post, we will focus on the **collaborative filtering** approach, that is: the user is recommended items that people with similar tastes and preferences liked in the past. In another word, this method predicts unknown ratings by using the similarities between users.

## Dataset

GroupLens Research has collected and made available rating data sets from the MovieLens web site ([http://movielens.org](http://movielens.org/)). The data sets were collected over various periods of time, depending on the size of the set.

We are using *Small*: 100,000 ratings and 3,600 tag applications applied to 9,000 movies by 600 users. Last updated 9/2018.

Download: [ml-latest-small.zip](http://files.grouplens.org/datasets/movielens/ml-latest-small.zip) (size: 1 MB)