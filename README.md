# KAGGLE Hotel booking data analysis

<a target="_blank" href="https://colab.research.google.com/github/Yagami11111/Hotel-booking-Analysis/blob/main/main.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

This repository contains an analysis of hotel booking data. The analysis includes data preprocessing, exploratory data analysis (EDA), and machine learning models to predict hotel cancellations and average daily rate (ADR).

## Files

- **hotel_bookings.csv**: The dataset used for the analysis.
- **main.ipynb**: The Jupyter Notebook containing the entire analysis process.
- **Technical Report.pdf**: A detailed technical report of the analysis.
- **README.md**: This file, providing an overview of the repository and its contents.

## Exploratory Data Analysis (EDA)

The dataset contains various features related to hotel bookings. Key steps in the EDA include:

1. **Data Cleaning**:
    - Handling missing values by dropping or imputing.
    - Removing duplicate entries.
    - Filtering outliers.

2. **Visualizations**:
    - Correlation heatmap.
    - Pie chart showing the proportion of each hotel type.
    - Bar charts for cancellation counts and lead time distribution.
    - Histograms for the number of stays in weekend and weekday nights.
    - Pie charts for the proportion of reserved vs. assigned rooms.
    - Choropleth map showing the number of guests from each country.
    - Line plot for average daily rate per person by month.

## Machine Learning

### Regression: Predicting Average Daily Rate (ADR)

1. **Feature Selection**:
    - Lasso regression was used to select the most important features.

2. **Models**:
    - **Linear Regression**: RMSE = 38.30, R2 = 0.414
    - **ElasticNet Regression**: RMSE = 40.12, R2 = 0.357
    - **Random Forest Regression**: RMSE = 16.67, R2 = 0.889

### Classification: Predicting Cancellations

1. **Feature Selection**:
    - SelectKBest with mutual information criteria.

2. **Models**:
    - **Logistic Regression with GridSearchCV**: Best F1 Score = 0.832
    - **K-Nearest Neighbors with GridSearchCV**: Best F1 Score = 0.660
    - **Random Forest Classifier with RandomizedSearchCV**: Best F1 Score = 0.832