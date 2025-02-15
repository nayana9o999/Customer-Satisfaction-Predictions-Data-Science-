# 1.Customer-Satisfaction-Predictions-Data-Science 😊

## Overview
This project is focused on predicting customer satisfaction ratings using historical support ticket data. The goal is to gain insights into what drives customer satisfaction, helping businesses understand and improve their customer support strategies. By analyzing trends and customer segments, the project builds and evaluates several machine learning models, including Random Forest, Logistic Regression, SVM, and XGBoost. To make the model's decisions more transparent and trustworthy, SHAP is used for explainability, shedding light on how different features influence the predictions.

## Objective
The main goal is to predict customer satisfaction ratings using historical support ticket data while gaining insights into the factors influencing customer satisfaction.

---

## Project Workflow
The project begins with data preprocessing, where irrelevant columns such as customer names and emails are dropped to maintain privacy and improve model efficiency. Missing values are handled by dropping rows with nulls, ensuring a clean dataset. Categorical features, like ticket priority, are encoded using Label Encoding, and numerical features are scaled for better model performance.

In the Exploratory Data Analysis (EDA) phase, the project dives into understanding customer behavior by analyzing age distribution and ticket priorities. Correlation heatmaps are used to identify relationships between features, while word clouds reveal the most frequent words in ticket descriptions, providing a deeper understanding of customer issues.

For the modeling stage, multiple machine learning models are implemented, including Random Forest, Logistic Regression, Support Vector Machine (SVM), and XGBoost Regressor. These models are evaluated using a variety of metrics, such as accuracy, precision, recall, and F1-Score for classification tasks, and Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R² Score for regression tasks.

The project goes a step further by incorporating explainability with SHAP. This allows for a deeper understanding of model predictions by showing global feature importance and providing local explanations for individual predictions. This transparency makes it easier to trust and interpret the model's decisions.

---

## Key Insights
The analysis revealed that certain features play a crucial role in predicting customer satisfaction. Specifically, Ticket Priority, Resolution Time, and Customer Age were identified as significant predictors. This suggests that how quickly a ticket is resolved and the priority assigned to it greatly influence customer satisfaction levels.

Using SHAP for explainability provided valuable insights into how these features interact with each other. For example, customers in certain age groups were more sensitive to resolution times, while high-priority tickets consistently impacted satisfaction ratings. These insights not only improved model accuracy but also offered actionable information for enhancing customer service strategies.

## Conclusion and Limitations
This project effectively predicted customer satisfaction ratings and uncovered valuable insights into the factors influencing customer experiences. By leveraging historical support ticket data, the models were able to identify key drivers of satisfaction, enabling more targeted improvements in customer service. The use of SHAP for explainability ensured that the models were not only accurate but also interpretable, making the insights more actionable.

However, there are some limitations to consider. The dataset showed an imbalance in ticket priorities, which could affect model performance. Additionally, while the current features provided meaningful predictions, exploring more advanced feature engineering techniques or incorporating text-based sentiment analysis could further enhance accuracy. Despite these challenges, the project demonstrates a robust approach to understanding and predicting customer satisfaction.
# 2. Movie Recommender System Project
Movie Recommender System Project

Overview

This project is all about building a Movie Recommender System that can suggest movies you’re likely to enjoy. I’ve used two main techniques: Content-Based Filtering and Collaborative Filtering. The idea is to analyze movie metadata (like genres, cast, and keywords) as well as user interactions to understand preferences and make personalized movie recommendations. Whether you’re looking for movies similar to your favorites or discovering new ones based on what others with similar tastes liked, this system has got you covered.

Objectives

The main goal of this project is to create a Movie Recommender System that feels intuitive and relevant to each user. We wanted to build a system that doesn’t just suggest the obvious choices but provides thoughtful and personalized movie recommendations. To achieve this, we decided to use two different approaches.

First,used Content-Based Filtering, which looks at the details of each movie—like genres, cast members, keywords, and even the director—to find movies that are similar to the ones you already like. For example, if you love action-packed superhero films, this method finds other movies with similar themes, characters, or storylines.

I also implemented K-Nearest Neighbors (KNN) Collaborative Filtering, which goes beyond the movie details and focuses on user behavior. This approach looks at the ratings given by users with similar tastes to find movies you might enjoy, even if they’re in genres you don’t typically watch. It’s like getting movie recommendations from a group of friends who share your tastes.

Finally, I wanted to see how well each system performed, so did a Comparative Analysis to understand the strengths and limitations of both approaches. By evaluating them side by side,I could determine which method worked better for different types of users and movie preferences.

## Datasets Used

The project uses the following datasets from the MovieLens and TMDB collections:

movies_metadata.csv: Contains movie information such as title, genres, overview, and release date.

credits.csv: Provides cast and crew details.

keywords.csv: Lists keywords associated with each movie.

ratings.csv: User ratings for movies, used for Collaborative Filtering.

Project Workflow

Data Preprocessing:

Cleaned and merged multiple datasets on the id column.

Extracted relevant features like genres, cast, director, and keywords.

Combined these features into a single combined_features column for Content-Based Filtering.

Content-Based Filtering:

Utilized TF-IDF Vectorization to convert text data into numerical vectors.

Calculated Cosine Similarity between movie vectors to find similar movies.

Recommended top N movies similar to a given movie.

Collaborative Filtering (KNN):

Implemented K-Nearest Neighbors using Cosine Similarity.

Recommended movies based on user behavior and preferences.

Evaluated model performance using RMSE and MAE.

Recommendation Generation:

Recommended movies for popular titles like 'Toy Story', 'The Lion King', and 'The Matrix'.

Saved recommendations to movie_recommendations.txt for reporting.

Model Comparison and Insights:

Content-Based: Recommended movies similar in content (genres, keywords, cast).

Collaborative Filtering: Provided personalized recommendations using user behavior.

## Key Insights

During this project, I uncovered some interesting insights about how recommendation systems work:

Content-Based Filtering was quite effective at recommending movies that share similar themes and genres. If you liked one sci-fi thriller, it suggested other sci-fi thrillers with a similar vibe. However, this approach felt a bit limited since it didn’t offer much variety beyond the obvious connections.

KNN Collaborative Filtering was fantastic at personalizing recommendations. It leveraged user behavior to suggest movies that people with similar tastes enjoyed. This led to more diverse recommendations but demanded more computational resources, especially with a large dataset.
