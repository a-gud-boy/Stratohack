# Dynamic Airline Ticket Price Forecasting

## Problem Statement

Predict airline ticket prices by considering not only routes but also fuel prices, holidays, and seasonality.

## Dataset

The baseline model is trained on the [Kaggle Flight Price dataset](httpss://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction). The dataset used in the notebook is `Clean_Dataset.csv`.

For the advanced model, the plan is to incorporate the IATA Fuel Index and a Holiday Calendar for more accurate predictions.

## Approach

This project currently implements the baseline approach, which consists of a regression model with tabular flight features.

### Data Preprocessing
The following feature engineering and preprocessing steps were performed:
- **Feature Engineering:** New features were created for routes, and categorical features were mapped to numerical values based on their mean price correlation.
- **Encoding:** Categorical features like `stops`, `airline`, and `class` were converted to numerical representations.
- **Scaling:** Time-based features like `departure_time` and `arrival_time` were scaled based on their average price.

### Models
The following regression models were trained and evaluated:
- **Random Forest Regressor**
- **XGBoost Regressor**
- **Ensemble Model:** An ensemble of the Random Forest and XGBoost models was created by averaging their predictions.

The ensemble model achieved an **R2 score of approximately 0.98**, indicating a high level of accuracy for the baseline model.

## Future Work

### Advanced Model
- Implement a time-series model using Prophet or Transformers.
- Incorporate external features like the IATA Fuel Index and a Holiday Calendar.

### Bonus Points
- Build a "Price Alert Bot" to notify users of the cheapest time to fly.
- Simulate the impact of changing fuel prices on ticket costs.
- Predict ticket price uncertainty with confidence intervals.

## How to Run

The code for this project is available in the `stratohack.ipynb` notebook. To run the project, open the notebook in a Jupyter environment and execute the cells.
