# Hyperlocal Air Quality Prediction in Houston neighborhoods

## Motivation and Brief Summary
Between 2017 and 2018, The Environmental Defense Fund (EDF) partnered with Google Earth Outreach to map air pollution at the hyperlocal level. In various cities around the world, mobile air quality sensors were used to gather air pollution data at street level, showing how air pollution varies over very short distances. One of those cities was Houston, where low-cost sensors were outfitted on city fleet vehicles, Google Street View cars, and stationary locations. 

Given this unique data source, we were motivated to focus our project on air quality prediction in Houston. For simplicity, and on the basis of data availability, we decided to focus on data for just one pollutant: NO2. Unlike ozone and particle pollution, which can be of concern over large regions, NO2 levels are appreciably higher in close proximity to pollution sources (e.g., vehicles on major freeways, factories) – hence we felt it was an important pollutant to analyze.

In particular, we undertook to develop machine learning models that could learn to associate EDF’s air quality data with hyperlocal data on meteorological conditions, local emissions, and traffic. From there, our goal was to predict pollution levels in nearby Houston neighborhoods that have weather, emissions, and traffic data available but did not take part in EDF’s air quality monitoring.

## Data
Our target variable, hyperlocal NO2 pollution levels, comes from the EDF Houston air quality dataset available for download through the OpenAQ portal. NO2 levels were collected over nine months in certain designated areas in Houston. The result is a dataset with average NO2 readings in ppm, latitude, and longitude for 11,534 precise locations around the city. Traffic data was acquired from the Overpass API from Open Street Maps, emissions data using NEI's data for point sources and the Daymet API to collect meteorological data.

## Notebooks Structure
The 'cleaning' directory consists of the notebooks that carry out data manipulation on the individual data sources in order to prep them for combining into a single dataset at the modeling stage.

The 'models' directory consists of:
* baseline.ipynb - Consists of code for the simple OLS baseline model
* standard_models.ipynb - Consists of code for the Lasso, Ridge, Random Forest, XGBoost and PCA models.
* DL_model.ipynb - Consists of code for the Deep Learning model developed using PyTorch

## Final Report and Presentation
The overall analysis and results of this project are documented in the [final report](https://github.com/vjoseph21/air-quality-prediction/blob/main/Report.pdf "final_report"). The presentation used to communicate the same can be found [here](https://github.com/vjoseph21/air-quality-prediction/blob/main/Presentation.pdf "final_presentation").
