# Forest Fire Prediction Using Machine Learning

## Overview
This project focuses on predicting the risk of forest fires using machine learning techniques. By analyzing meteorological data, we aim to provide insights that can help in forest fire management and prevention.

## Table of Contents
- [Introduction](#introduction)
- [Dataset Overview](#dataset-overview)
- [Data Preprocessing](#data-preprocessing)
- [Model Selection](#model-selection)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results and Analysis](#results-and-analysis)
- [Model Visualization](#model-visualization)
- [Conclusion](#conclusion)
- [Recommendations for Future Work](#recommendations-for-future-work)

## Introduction
Human civilization has evolved significantly, but with this evolution comes the responsibility to protect our environment. Forest fires, often exacerbated by climate change and human activities, pose a significant threat to ecosystems and human life. This project aims to predict forest fire risks using machine learning, allowing for timely preventive measures.

## Dataset Overview
The dataset used in this project contains information about forest fires in the northeast region of Portugal. Key features include:
- **Temporal Columns**: Month and day of the fire occurrence.
- **Fire Weather Indices**: 
  - FFMC (Fine Fuel Moisture Code)
  - DMC (Duff Moisture Code)
  - DC (Drought Code)
  - ISI (Initial Spread Index)
- **Weather Factors**: 
  - Temperature
  - Humidity
  - Wind Speed
  - Rainfall

The target variable is the area affected by the fire, which we log-transform to improve model performance.

## Data Preprocessing
Data preprocessing is crucial for ensuring the dataset is clean and structured. The steps include:
- **Data Selection**: Selecting relevant columns.
- **Handling Missing Values**: Ensuring no missing values are present.
- **Log Transformation**: Applying log transformation to the target variable.
- **Feature Engineering**: Creating new features (Temp_Wind and Humidity_Rain) to enhance model learning.
- **Normalization**: Scaling features using StandardScaler.

## Model Selection
We selected two machine learning algorithms for this project:
- **Random Forest Regressor**: An ensemble learning method that builds multiple decision trees.
- **XGBoost Regressor**: A highly efficient implementation of gradient boosting known for its performance.

## Model Training and Evaluation
The dataset was split into training (80%) and testing (20%) sets. Both models were trained and evaluated using:
- **Mean Squared Error (MSE)**: Measures the average of the squares of the errors.
- **R-squared (R²)**: Indicates how much variance in the dependent variable is explained by the independent variables.

## Results and Analysis
The performance of the models was as follows:
- **Random Forest Regressor**: 
  - MSE: 12789.27
  - R²: 0.85
- **XGBoost Regressor**: 
  - MSE: 11568.23
  - R²: 0.87

Both models performed well, with XGBoost slightly outperforming Random Forest.

## Model Visualization
Visualizations were created to understand model performance:
1. **Actual vs Predicted Scatter Plot**: Shows the correlation between actual and predicted fire risk values.
2. **Residuals Histogram**: Displays the distribution of prediction errors for both models.
3. **Time-Series Plot**: Compares actual fire risk values with model predictions over time.

## Conclusion
This project demonstrated the effectiveness of machine learning in predicting forest fire risks based on meteorological data. Both models provided valuable insights, with XGBoost showing slightly better performance. Future work could focus on optimizing models further and integrating additional features for improved accuracy.

## Recommendations for Future Work
- **Hyperparameter Tuning**: Optimize model parameters for better performance.
- **Cross-Validation**: Implement cross-validation techniques to ensure model robustness.
- **Feature Expansion**: Include additional features such as terrain and vegetation data.
- **Real-Time Prediction Systems**: Develop systems that provide real-time fire risk assessments.

## Acknowledgments
- **Author**: Daswadayalan Myladumparai Deenadayalan
- **Student ID**: 23068427
- **Email**: dm24aak@herts.ac.uk

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

---
## Refrence
Reference
"Deep Learning Models for Enhanced Forest-Fire Prediction at Mount Etna"
This study develops ConvLSTM, LSTM, and CNN models to predict forest fires 
using satellite imagery, weather, and human activity data.
https://www.sciencedirect.com/science/article/pii/S2666592124000933
"A Forest Fire Prediction Model Based on Meteorological Factors and Machine 
Learning"
This research analyzes meteorological factors influencing forest fires and 
develops a machine learning-based prediction model, focusing on regions in 
SouthKorea.
https://www.mdpi.com/1999-4907/15/11/1981
"A Data Mining Approach to Predict Forest Fires using Meteorological Data"
The paper presents a novel data mining approach for forest fire prediction, 
achieving an 80% accuracy rate using bagging decision trees.
https://arxiv.org/abs/2502.01550
"FireCastNet: Earth-as-a-Graph for Seasonal Fire Prediction"
Introducing FireCastNet, this research employs a 3D convolutional encoder 
with GraphCast to capture wildfire spatio-temporal dynamics for seasonal 
forecasting.
https://arxiv.org/abs/2111.02736
