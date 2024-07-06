# Description  
Machine Learning powered Movie Recommender System, created for the AI HUB competition of University of Patras.

For the competition, a Movie Recommendation System was implemented. This system displays movies to the user, which they are asked to rate on a scale from 0.5 to 5, in increments of 0.5. Based on the user's ratings, the algorithm then presents movie recommendations that match the user's profile.

Two neural networks are used to create the recommendations. With pairs of (user, movie), the first neural network takes the user's information (user features) as input, while the second takes the movie's information (item features) as input. Each neural network outputs a vector nx1. By calculating the dot product of the two vectors, we arrive at the system's numerical prediction for the user's rating of the movie.

We then train our network based on the predictions given by the neural network for each (user, item) pair. When the validation error of the training stops decreasing or decreases minimally, we consider that we have approached the global minimum and achieved convergence. We then save our model and certain necessary tables in CSV format. Using the CSV files, we created an API that takes movies selected by the user via the GUI and, based on the trained model, generates a list of recommendations, which it returns to the GUI.

To visualize our results, we implemented a GUI (graphic user interface) where the user can rate movies either from a selection of random movies displayed or by searching for specific movies of their choice (from those that participated in the training). Once the user rates the movies, the API presents movie recommendations on the screen.
