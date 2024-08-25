# BoomBikes Demand Prediction

This repository contains a project to build a multiple linear regression model for predicting the demand for shared bikes provided by BoomBikes. The analysis and modeling are based on a dataset that includes various factors influencing daily bike rentals in the American market.

## Project Overview

BoomBikes, a bike-sharing provider in the US, experienced a dip in revenues due to the COVID-19 pandemic. To better understand and predict future demand, this project aims to identify the key factors affecting bike rentals and build a model to predict demand based on these factors. The insights from this model will help BoomBikes optimize their operations and meet customer expectations more effectively as the market recovers.

## Dataset

The dataset used for this project contains daily records of bike rentals along with various features such as weather conditions, season, and day type. The key columns in the dataset include:

- **temp**: Normalized temperature in Celsius.
- **atemp**: Normalized feeling temperature in Celsius.
- **hum**: Normalized humidity.
- **windspeed**: Normalized wind speed.
- **season**: Season of the year (winter, spring, summer, fall).
- **weathersit**: Weather situation (clear, mist, light rain/snow, heavy rain/snow).
- **yr**: Year (0 = 2018, 1 = 2019).
- **holiday**: Whether the day is a holiday (0 = No, 1 = Yes).
- **workingday**: Whether the day is a working day (0 = No, 1 = Yes).
- **cnt**: Total number of bike rentals (target variable).

## Project Structure

The project is organized as follows:

- **data/**: Contains the dataset used for the analysis.
- **notebooks/**: Contains the Jupyter notebook used to explore the data, build the model, and evaluate its performance.
- **subjective_questions/**: Contains the PDF with answers to the subjective questions related to linear regression.
- **README.md**: This file, providing an overview of the project.

## Steps in the Analysis

1. **Data Preprocessing**: 
   - Categorical variables like `season`, `weathersit`, `weekday`, and `mnth` were converted into dummy variables.
   - The data was scaled to a range of 0 to 1 to ensure all features are on the same scale.

2. **Exploratory Data Analysis (EDA)**:
   - Correlation analysis and pair plots were used to understand relationships between variables.
   - The impact of different factors on bike rentals was explored.

3. **Model Building**:
   - The dataset was split into training and testing sets.
   - A multiple linear regression model was built and evaluated using R-squared to assess how well the model explains the variance in bike demand.

4. **Model Evaluation**:
   - The model's performance was evaluated using R-squared on the test data, with an R-squared value of approximately 0.809, indicating a strong fit.
