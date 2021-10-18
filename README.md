# Movie Recommendation - ML Model

## Abstract
Content recommendation based on user activities has been used for years. Along with collaborative-based recommendations, that find similar user profiles and recommends the same content to both. I will be working on a content-based model. Recommending a movie based on an input of the movie you wish to find similar movies to it. The data I am working with is [IMDb movies extensive dataset](https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset), it has been scraped from IMDb and provided by [Stefano Leone](https://www.kaggle.com/stefanoleone992). I will be exploring the features of the data to help understand the dataset. After that, I will visualize the interesting aspects of the data to find some insights. Lastly, preparing the dataset for modelling hopefully to get as close and similar results as the user inputs.


## Design
The project helps with deciding on the content to present to the user based on his/her activities. The idea is make use of the provided features to find the similarities in the habit of the user's preference when watching movies. It would help the user finds what suits his preference and also the provider to have longer time spent on the service and less bounce rate.

## Data
The dataset contains 85,855 movies with 22 features. The features contains the details of the movies from title, director, actors, language, year, descriptions of the movies' plot, and many more. Most of the data concerned and can be used for the project are text. Other data such as budget, year and such could be used to have an overview of the data and to find any correlations between the features.

## Algorithms
*Feature Engineering*
- Tinkering with datatypes to the correct type. (year, date published, budget)
- Dealing with outliers in the duration of the movies, as most of them were between 75-120 minutes mark.
- Filling in the NaN values so our algorithms so to avoid running into errors in modelling.
- Splitting the genres and having each keyword in a new row (explode) to visualize the most popular genres.
- Combining all the features we are concerned with to prepare it for modelling.

*Models*
Looking at the problem we would like to solve, which is looking for similarities between different movies. We want to find the similar movies to our target movie. Out options here are cosine-similarity, euclidean distance, manhattan distance to name a few.

*Model Evaluation*
Since we will be working with text, we could use dummy variables or vectorizations. Euclidean distance is that important in the project due to that I don't care much about the actual distance between each item. Cosine-similarity works by calculating the degree between each item, a lower degree would mean they are similar, 90 degree means they are not similar. Furthermore, Cosine-similarity used frequently to find similar documents which essentially what our project would be.

## Tools
- Pandas and Numpy for data manipulation.
- Matplotlib and Seaborn for visualization.
- Scikit-learn for modelling.
