# Voyage-Analytics-Integrating-MLOps-in-Travel

# ✈️ Voyage Analytics: Integrating MLOps in Travel

## 📌 Project Overview

Voyage Analytics is an end-to-end Machine Learning and MLOps project designed to analyze travel data and build intelligent travel solutions using user, flight, and hotel datasets.

The project combines Machine Learning with modern MLOps practices to develop, track, deploy, automate, and scale travel-related models.

The system focuses on three major machine learning applications:

1. ✈️ Flight Price Prediction
2. 👤 User Gender Classification
3. 🏨 Personalized Hotel Recommendation

The project also demonstrates a complete MLOps workflow using MLflow, Flask, Docker, Kubernetes, Apache Airflow, Jenkins, and Streamlit.

---

## 🎯 Business Problem

The travel and tourism industry generates large amounts of data related to customers, flights, hotels, prices, destinations, and travel behavior.

Analyzing this information manually can make it difficult to:

- Predict flight ticket prices
- Understand customer characteristics
- Identify travel patterns
- Recommend relevant hotels
- Deploy machine learning models reliably
- Automate model workflows
- Scale prediction services according to demand

Voyage Analytics addresses these challenges by combining machine learning and MLOps technologies into a unified travel intelligence platform.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Build a regression model to predict flight prices.
- Develop a REST API for real-time flight price prediction.
- Containerize the ML application using Docker.
- Deploy and scale the API using Kubernetes.
- Automate ML workflows using Apache Airflow.
- Implement CI/CD using Jenkins.
- Track experiments and models using MLflow.
- Build a classification model for user gender prediction.
- Develop a hotel recommendation system based on historical booking behavior.
- Build an interactive Streamlit dashboard for travel insights and predictions.

---

# 📊 Datasets

The project uses three datasets:

## 1. Users Dataset

The users dataset contains demographic information about travelers.

| Column | Description |
|---|---|
| `code` | Unique user identifier |
| `company` | Associated company |
| `name` | User name |
| `gender` | User gender |
| `age` | User age |

---

## 2. Flights Dataset

The flights dataset contains information about flight journeys and prices.

| Column | Description |
|---|---|
| `travelCode` | Travel identifier |
| `userCode` | User identifier |
| `from` | Flight origin |
| `to` | Flight destination |
| `flightType` | Type of flight |
| `price` | Flight ticket price |
| `time` | Flight duration |
| `distance` | Flight distance |
| `agency` | Flight agency |
| `date` | Flight date |

---

## 3. Hotels Dataset

The hotels dataset contains hotel booking and stay information.

| Column | Description |
|---|---|
| `travelCode` | Travel identifier |
| `userCode` | User identifier |
| `name` | Hotel name |
| `place` | Hotel location |
| `days` | Number of days stayed |
| `price` | Price per day |
| `total` | Total booking price |
| `date` | Hotel booking date |

---

# 🤖 Machine Learning Components

## 1. ✈️ Flight Price Prediction

A regression model is developed to predict the price of a flight.

### Features Used

- Origin
- Destination
- Flight type
- Flight duration
- Distance
- Flight agency
- Flight month
- Day of week
- Passenger age

### Preprocessing

Categorical features are processed using:

- `OneHotEncoder`

Numerical features are normalized using:

- `StandardScaler`

A `ColumnTransformer` is used to apply the appropriate preprocessing to each feature type.

### Models

Two regression algorithms are evaluated:

- Gradient Boosting Regressor
- Random Forest Regressor

### Evaluation Metrics

The models are evaluated using:

- RMSE — Root Mean Squared Error
- MAE — Mean Absolute Error
- R² — R-squared

The model with the highest R² score is selected as the best regression pipeline.

The trained model is saved as:

```text
models/flight_price_model.pkl
