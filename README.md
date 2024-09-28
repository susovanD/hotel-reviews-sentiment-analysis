# Sentiment Analysis on Trip Advisor Hotel Reviews

## Data Overview
This repository contains a comprehensive analysis of hotel reviews from Trip Advisor. The dataset includes textual reviews along with ratings ranging from 1 to 5. The goal is to analyze sentiments expressed in the reviews and predict the overall sentiment based on both text and numerical ratings.

## Folder Structure
/trip-advisor-sentiment-analysis │ ├── data/ │ ├── raw/ # Original dataset containing hotel reviews │ ├── processed/ # Processed data ready for analysis and modeling │ ├── notebooks/ # Jupyter notebooks documenting the analysis process │ ├── models/ # Saved models and results from model predictions │ ├── src/ # Source code for data processing and model training │ ├── data_preprocessing.py # Script for data cleaning and preprocessing │ ├── model_training.py # Script for training and evaluating models │ ├── requirements.txt # List of packages and dependencies └── README.md # Project documentation


## Packages Used
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical operations.
- **vaderSentiment**: For sentiment analysis of textual data.
- **textblob**: For processing textual data and performing sentiment analysis.
- **pycaret**: For simplifying the process of model training and evaluation.
- **matplotlib**: For data visualization.

## Data Preparation
In this phase, we generated sentiment scores from the textual reviews using two libraries:

- **VADER**: A rule-based sentiment analysis tool specifically designed for social media text, which works well on short texts like reviews.
- **TextBlob**: A library for processing textual data that provides a simple API for diving into common natural language processing (NLP) tasks.

From the rating column, we categorized sentiments as follows:
- **Negative**: Ratings of 1 and 2
- **Neutral**: Rating of 3
- **Positive**: Ratings of 4 and 5

We then created a final sentiment column based on the mode of the sentiments derived from VADER, TextBlob, and the rating column sentiment.

## Model Prediction
In this section, we employed **PyCaret** to streamline the modeling process. PyCaret is a low-code machine learning library that automates the training and evaluation of multiple models. We utilized it to identify the best model for predicting sentiment based on the generated features.

## Summary and Conclusion
This repository provides a complete framework for performing sentiment analysis on hotel reviews from Trip Advisor. Through data preprocessing, sentiment generation using VADER and TextBlob, and modeling with PyCaret, we have developed a robust approach to understanding sentiments expressed in customer reviews. The insights gained can help in enhancing customer satisfaction and improving hotel services.

For further exploration, feel free to clone the repository and experiment with the data and models!
