Sales Prediction for Stores
This project aims to help a store forecast its future sales using machine learning models. These predictions enable inventory optimization, prevent stockouts, and improve strategic planning.

Objectives
Perform a comprehensive analysis of historical sales data.
Develop and optimize sales prediction models.
Deploy a final model that can be easily used for real-time sales forecasting.
Project Contents
The repository includes three Jupyter notebooks, reflecting the main workflow stages:

SHOP-ANALYSIS.ipynb: Data exploration and initial experimentation.
MODELING-2.ipynb: Model optimization and evaluation.
Deploy_model.ipynb: Deployment of the final model.
Detailed Notebook Descriptions
SHOP-ANALYSIS.ipynb
This notebook serves as the starting point for the project. It includes:

Data loading and exploration:

Analysis of historical data, including daily sales by store, product, and category.
Visualization of trends, seasonality, and sales patterns using various plots.
Example visualizations:

Time series graphs showing daily sales trends.
Correlation analysis to identify factors influencing sales.
Data preprocessing:

Identification and handling of missing values.
Conversion of categorical variables into numerical ones (One-Hot Encoding).
Normalization to ensure models work efficiently.
Feature Engineering:

Creation of new relevant features:
Lags: Sales from previous days to capture temporal dependencies.
Moving averages: Short-term and long-term sales trends.
Day of the week: To account for seasonal effects.
Initial Model Testing:

Two main approaches are tested:

LSTM (Long Short-Term Memory): A recurrent neural network for time series data.
XGBoost: A decision tree-based model with optimizations.
Initial metrics such as RMSE (Root Mean Squared Error) and MAE (Mean Absolute Error) are compared.

Results:

LSTM: Better generalization but high computational cost.
XGBoost: Lower computational cost with promising performance.
Initial Conclusions:

XGBoost is selected for further optimization due to its efficiency and competitive performance.
MODELING-2.ipynb
This notebook focuses on:

Hyperparameter optimization for the XGBoost model using Optuna.
Cross-validation for time series data (TimeSeriesSplit).
Training the final model with all available data and generating definitive metrics.
Deploy_model.ipynb
The final model is deployed with:

Modelbit for deployment.
Creation of custom functions for easy predictions on new data.
Technologies Used
Language: Python
Libraries:
Data Analysis: pandas, numpy, matplotlib, seaborn
Modeling: xgboost, scikit-learn
Optimization: optuna
Deployment: Modelbit



Execute SHOP-ANALYSIS.ipynb for data exploration and preprocessing.
Continue with MODELING-2.ipynb to optimize and train the final model.
Use Deploy_model.ipynb to deploy the model in a production environment.
Make Predictions with the Model:

Once deployed, use the model to make predictions on new data.
Results
The final model, optimized using Optuna, achieved the following metrics in recursive validation:

RMSE: 0.9494
MAE: 0.2390
RMSSE: 0.1406
This model is designed to deliver precise and efficient short-term sales predictions.