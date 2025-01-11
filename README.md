Bike Sharing Prediction Assignment
Overview
This programming assignment focuses on building a Multiple Linear Regression (MLR) model to predict the demand for shared bikes. Using the provided dataset, you will analyze and model the factors influencing bike demand, helping BoomBikes prepare a business strategy to recover revenue losses and cater effectively to the post-pandemic market demands.

Problem Statement
BoomBikes, a bike-sharing provider in the US, is experiencing a decline in revenue due to the ongoing pandemic. To address this issue, they aim to forecast bike demand based on various influencing factors.

The specific goals are:

Identify significant variables affecting bike demand.
Understand how well these variables predict demand.
Use the model to guide strategic business decisions to maximize revenue and improve service.
Business Goals
The MLR model you develop will serve two key purposes:

Predictive Analysis: Estimate bike demand using independent variables.
Strategic Insights: Provide actionable insights to the management about the demand dynamics, enabling BoomBikes to optimize operations and expand into new markets.
Dataset Description
The dataset contains daily bike demand data along with independent variables related to weather, time, and user types.

Target Variable:
cnt: Total number of bike rentals (sum of casual and registered users).
Key Variables:
casual: Number of rentals by casual users.
registered: Number of rentals by registered users.
season: Season (1: Winter, 2: Spring, 3: Summer, 4: Fall).
weathersit: Weather condition (1: Clear, 2: Mist, 3: Light Snow, 4: Heavy Rain).
yr: Year (0: 2018, 1: 2019).
Important Notes:

Variables like season and weathersit should be converted to categorical strings to better represent their meaning.
The yr column should be carefully evaluated for inclusion, as it might influence demand due to increasing popularity of bike-sharing systems.
Assignment Tasks
1. Data Preparation
Perform data cleaning and preprocessing:
Handle missing or inconsistent values.
Convert ordered numeric variables (e.g., season, weathersit) into categorical variables.
Conduct exploratory data analysis (EDA) to understand the relationships and trends in the dataset.
2. Model Building
Use the cnt column as the target variable for the regression model.
Exclude casual and registered columns during model building to avoid data leakage, as their sum equals cnt.
Perform feature selection to identify the most significant variables.
3. Model Evaluation
Evaluate the model’s performance using the R-squared score on the test dataset:
python
Copy code
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
4. Residual Analysis
Analyze residuals to ensure that the assumptions of linear regression (normality, homoscedasticity, etc.) are satisfied.
