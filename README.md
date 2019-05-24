# Motivation
The purpose of this project is to recommend restaurants to someone based on a similar restaurant that they have enjoyed in the past. It can serve as a recommendation for someone visiting a city and is searching for a restaurant that is similar to what they typically enjoy locally.

# Data source
- Yelp Open Dataset: https://www.yelp.com/dataset

# EDA
- The raw Yelp Open Dataset had many columns stored as columns that needed to be unpacked.
- It was also necessary to create dummy variables for all categorical variables as most filters on Yelp are descriptive.

## Identifying similar restaurants
### Clustering techniques
- In a first step, we considered clustering restaurants having similar descriptions (features) together using K-Means clustering or K-prototype which uses a combination of K-Mode & K-Means clustering, but our goal was to capture all restaurants that are similar to the one chosen and rank them in order of similarity. Therefore, in the next step, it made sense to calculate the Cosine Distance to obtain the most similar restaurants and let the user limit the number of recommendations.

### Cosine distance
- Cosine distance is defined as 1.0 minus the cosine similarity. Therefore, the smaller the value is in the Cosine distance matrix, the more the businesses are similar. We used pairwise cosine distance between restaurants to identify those that are the most similar to the chosen restaurant.

Next Steps

- Currently working on building a collaborative filtering recommendation system. Data was also gathered about reviewers to recommend restaurants based on other reviewers' ratings.
- Use the Surprise Library to build the collaborative filtering recommendation system
