## Usage Example

- **Predicting a user’s rating for a movie:**

    Inside the notebook:

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
