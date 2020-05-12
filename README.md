# Recommendation-System

[![Google Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/singhsidhukuldeep/Recommendation-System/blob/master/Building_Recommender_System_with_Surprise.ipynb)

Building recommendation system to scale using scikit-surprise (surprise library)

[Recommender systems](https://en.wikipedia.org/wiki/Recommender_system) are one of the most common used and easily understandable applications of data science. Lots of work has been done on this topic, the interest and demand in this area remains very high because of the rapid growth of the internet and the information overload problem. It has become necessary for online businesses to help users to deal with information overload and provide personalized recommendations, content and services to them.

Two of the most popular ways to approach recommender systems are [collaborative filtering](https://en.wikipedia.org/wiki/Collaborative_filtering) and [content-based recommendations](https://www.analyticsvidhya.com/blog/2015/08/beginners-guide-learn-content-based-recommender-systems/). In this post, we will focus on the **collaborative filtering** approach, that is: the user is recommended items that people with similar tastes and preferences liked in the past. In another word, this method predicts unknown ratings by using the similarities between users.

## Dataset

GroupLens Research has collected and made available rating data sets from the MovieLens web site ([http://movielens.org](http://movielens.org/)). The data sets were collected over various periods of time, depending on the size of the set.

We are using *Small*: 100,000 ratings and 3,600 tag applications applied to 9,000 movies by 600 users. Last updated 9/2018.

Download: [ml-latest-small.zip](http://files.grouplens.org/datasets/movielens/ml-latest-small.zip) (size: 1 MB)

## Algorithm Comparisons

| Algorithm | test_rmse | fit_time | test_time |
| --- | --- | --- | --- |
| SVDpp | 0.849133 | 224.427830 | 10.164514 |
| KNNBaseline | 0.855728 | 0.198152 | 2.959032 |
| BaselineOnly | 0.861078 | 0.141793 | 0.198635 |
| SVD | 0.863973 | 3.470947 | 0.207932 |
| KNNWithZScore | 0.866793 | 0.142699 | 2.660879 |
| KNNWithMeans | 0.870065 | 0.101380 | 2.389334 |
| SlopeOne | 0.872713 | 1.340127 | 7.466537 |
| NMF | 0.901370 | 3.766373 | 0.215193 |
| CoClustering | 0.920521 | 1.404656 | 0.216376 |
| KNNBasic | 0.923332 | 0.088885 | 2.163818 |
| NormalPredictor | 1.401411 | 0.086856 | 0.249340 |

## Algorithms Used


#### NormalPredictor

* NormalPredictor algorithm predicts a random rating based on the distribution of the training set, which is assumed to be normal. This is one of the most basic algorithms that do not do much work.

#### BaselineOnly

* BasiclineOnly algorithm predicts the baseline estimate for given user and item.

### k-NN algorithms

#### KNNBasic

* KNNBasic is a basic collaborative filtering algorithm.

#### KNNWithMeans

* KNNWithMeans is basic collaborative filtering algorithm, taking into account the mean ratings of each user.

#### KNNWithZScore

* KNNWithZScore is a basic collaborative filtering algorithm, taking into account the z-score normalization of each user.

#### KNNBaseline

* KNNBaseline is a basic collaborative filtering algorithm taking into account a baseline rating.

### Matrix Factorization-based algorithms

#### SVD

* SVD algorithm is equivalent to Probabilistic Matrix Factorization (http://papers.nips.cc/paper/3208-probabilistic-matrix-factorization.pdf)

#### SVDpp

* The SVDpp algorithm is an extension of SVD that takes into account implicit ratings.

#### NMF

* NMF is a collaborative filtering algorithm based on Non-negative Matrix Factorization. It is very similar with SVD.

### Slope One

* Slope One is a straightforward implementation of the SlopeOne algorithm. (https://arxiv.org/abs/cs/0702144)

### Co-clustering

* Co-clustering is a collaborative filtering algorithm based on co-clustering (http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.113.6458&rep=rep1&type=pdf)


We use `rmse` as our accuracy metric for the predictions.

## CREDITS

>Kuldeep Singh Sidhu

Github: [github/singhsidhukuldeep](https://github.com/singhsidhukuldeep)
`https://github.com/singhsidhukuldeep`

Website: [Kuldeep Singh Sidhu (Website)](http://kuldeepsinghsidhu.com)
`http://kuldeepsinghsidhu.com`

LinkedIn: [Kuldeep Singh Sidhu (LinkedIn)](https://www.linkedin.com/in/singhsidhukuldeep/)
`https://www.linkedin.com/in/singhsidhukuldeep/`
