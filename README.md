# Customer-Satisfaction-Predictions-Data-Science 😊

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

