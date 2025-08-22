# Movie Recommendation System (User-Based Collaborative Filtering)

In this project, we will explore the MovieLens 100K data set. We will build a recommendation system using user-based collaborative filtering, with the goal of predicting how a user might rate a movie based on ratings from similar users in order to recommend potential movies the user might enjoy.

We will explore some approaches to collaborative filtering on the MovieLens dataset, starting with an interpretable baseline like user mean, and progressing to more powerful latent factor models like SVD, with the help of the `Surprise` package.

## What is Collaborative Filtering?

The core idea is that:

- If User A and User B have similar tastes i.e. they rate the same items similarly,
- And user A liked Item X,
- Then maybe User B will also like Item X

There are two main types of Collaborative Filtering:

- **User-based**: Finds users similar to the target user i.e. "People like you liked..."
- **Item-based**: Finds items similar to those the user liked i.e. "You liked this, so you might like..."

Once you find similar users / items, you **filter** the data to

- Predict how much a user will like an item
- Recommend top-N items they haven't seen yet

## Uses of Movie Recommendation System

- **Personalized experience**: helps users discover movies they're likely to enjoy, cutting through the noise of endless options
- **User engagement**: recommendation systems help keep viewers hooked to platforms, increasing watch time and customer satisfaction
- **Content discovery**: surfaces hidden gems / niche films that users might never find on their own
- **Data utilization**: turn user behavior (ratings, watch history, search queries) into actionable insights
- **Business value**: recommender systems drive subscriptions, reduce churn, and improve retention by making the platform feel tailored

## Dataset

Information about the dataset:

- **Source**: https://grouplens.org/datasets/movielens/100k/
- **Structure**: 100,000 ratings from 943 users on 1,682 movies

## Structure of the Project

- Data Exploration (EDA)
- Model Building & Evaluation
  - Baseline Model using User Average
  - Manual Pearson Similarity Model
  - Surprise: KNNBasic Model
  - Surprise: KNNWithMeans Model
  - Surprise: SVD Model
- Prediction & Demo Movie Recommendation using Best Performing Model

## Findings

<table>
    <tr>
        <th>Model</th>
        <th>RMSE</th>
        <th>MAE</th>
        <th>Notes</th>
    </tr>
    <tr>
        <td>Baseline</td>
        <td>1.0437</td>
        <td>0.8362</td>
        <td>Uses user's average rating for seen movies as likely rating for an unseen movie</td>
    </tr>
    <tr>
        <td>Manual Pearson</td>
        <td>1.1177</td>
        <td>0.8703</td>
        <td>Potential overfitting</td>
    </tr>
    <tr>
        <td>KNNBasic</td>
        <td>1.0517</td>
        <td>0.8295</td>
        <td></td>
    </tr>
    <tr>
        <td>KNNWithMeans</td>
        <td>0.9847</td>
        <td>0.7644</td>
        <td></td>
    </tr>
    <tr>
        <td>SVD</td>
        <td>0.9378</td>
        <td>0.7395</td>
        <td>Best Performing</td>
    </tr>
</table>

The SVD model was the best performing one out of the 5 with the lowest RMSE at 0.9378 and MAE at 0.7395. By splitting the data into `user` and `movie` separately through matrix factorization, the model was able to learn about underlying characteristics of users and movies apart from just the ratings themselves, suggesting that these characteristics could have a deeper part to play in predicting whether a user will like a new movie or not.

## Future Enhancements / Other Model Approaches

- Streamlit app to let users select a user ID and see movie recommendations _(WIP)_
- Incorporating other features e.g. movie genres, user age, gender, occupation
- Deep learning approach using embeddings / neural networks
- Item-based collaborative filtering
