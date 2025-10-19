# Movie Recommendation System

A collaborative filtering-based movie recommendation system implemented in a Jupyter Notebook.

## Overview

This project builds a movie recommendation system using user-ratings data and predicts ratings for users on unseen movies. The approach uses user-based **Collaborative Filtering** with cosine similarity to suggest movies a user is likely to enjoy.

## Features

- Loads real-world movie and ratings datasets
- Analyzes rating trends and movie popularity
- Computes user-user similarity with cosine similarity
- Predicts ratings for any user-movie pair
- Recommends top N movies to each user based on predicted ratings

## Dataset

- Utilizes the [MovieLens 100k dataset](https://grouplens.org/datasets/movielens/100k/) (or compatible CSVs):
  - `u.data` — user ratings (`userid`, `movieid`, `rating`, `timestamp`)
  - `u.item` — movies metadata (`movieid`, `title`, `genre(s)`, etc.)

_You will need these CSVs in your project directory, or edit the notebook code to point to their location._

## Technologies & Libraries

- Python (Jupyter Notebook)
- **Pandas** — Data manipulation
- **NumPy** — Numerical operations
- **Matplotlib** — Visualizations
- **scikit-learn** — Cosine similarity calculation

## Installation

1. Clone the repository:
    ```
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```
2. Install dependencies:
    ```
    pip install pandas numpy matplotlib scikit-learn
    ```

## Usage

1. Open the notebook:
    ```
    jupyter notebook MovieRecommendation.ipynb
    ```

2. Run all cells after downloading the dataset.

## Usage Example

- **Predicting a user’s rating for a movie:**

    ```
    predicted = predict_rating(user_id=100, movie_id=25)
    print(predicted)  # e.g. Predicted rating for user 100 on 'The Birdcage': 3.44
    ```

- **Getting top N recommendations for a user:**

    ```
    recommendations = recommendmovies(user_id=5, movies_df=movies, ratings_df=ratings, num_recommendations=5)
    for title, score in recommendations:
        print(f"{title} | Predicted Rating: {score:.2f}")
    ```
