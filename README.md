# Reddit Post Binary Classifier

<i>Pulling information and classifying posts via Reddit's API</i>

**Author: Brendan McDonnell**
**Date: July 2019**

## Problem Statement:

I used the pushshift API to collect posts from two subreddits, `r/The_Donald` and `r/Republican`. Using natural language processing (NLP), I trained a binary classification model to predict which subreddit a given post came from.

**Reddit pages chosen**
- https://www.reddit.com/r/Republican/
- https://www.reddit.com/r/The_Donald/

**From r/Republican Community Details**

>/r/Republican is a partisan subreddit. This is a place for Republicans to discuss issues with other Republicans.<

**From r/The_Donald Community Details**

>The_Donald is a never-ending rally dedicated to the 45th President of the United States, Donald J. Trump.<

These two subreddits bear some similarities and should have some overlap. However, it's important to note that r/The_Donald has been quarantined recently for attempting to incite violence against police and other public officials, a violation of the reddit's content policy. It is a well known and used alt-right subreddit. By contrast, r/Republican is a subreddit that should reflect contemporary Republican views. There will likely be some NSFW material on r/The_Donald, but I believe a model like this could be very useful for understanding the difference in viewpoint between traditional republicans and the recent alt-right movement.

## Results:

Both a Gaussian Naive Bayes model and a Logistic Regression model were fit. The Logistic Regression model ended up being the best of the two, and it used Ridge Regression on term frequency–inverse document frequency (TFIDF) vectorized titles from the reddit data. The Logistic Regression was able to classify titles accurately ~75% of the time.

## Recommendations for Future Changes:

1. I would really like to fit a Random Forest model to this data and see if the weaker classification accuracy was a modeling error.
2. If other models don't seem to classify significantly better than a logistic regression, it would be smart to look at two subreddits that are a bit more dissimilar as there is a lot of overlap in material between these two.

[Link to Presentation](https://docs.google.com/presentation/d/1Fc48ODwGePA2ZDicAVo9BDJJtvvHrbufWn4YbHYvPF0/edit?usp=sharing)
