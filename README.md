# FreshGuard AI

### Machine Learning-Based Food Spoilage Prediction

## 1. Project Overview

FreshGuard AI is a machine learning-based project designed to investigate and predict food spoilage using environmental storage conditions and food characteristics.

The system aims to classify food items into three categories: Fresh, Nearing Spoilage, and Spoiled. The prediction process considers storage temperature, relative humidity, storage duration, and food type.

The project combines exploratory data analysis, supervised machine learning, model evaluation, and an interactive web application to examine the relationship between storage conditions and food freshness.

## 2. Problem Statement

Food spoilage contributes to household food waste, economic losses, and potential food-safety concerns. Storage conditions, particularly temperature, humidity, and duration, can influence the rate at which food deteriorates.

This project explores the application of machine learning to identify patterns in food-storage data and develop a classification model capable of estimating spoilage status.

## 3. Project Objectives

- Investigate the influence of storage conditions on food spoilage.
- Identify suitable datasets containing food-storage and spoilage observations.
- Develop a multiclass classification model.
- Compare different machine learning algorithms.
- Evaluate model performance using appropriate classification metrics.
- Investigate the contribution of individual input features.
- Develop an interactive application for spoilage prediction and data exploration.

## 4. Input Features and Target Variable

| Feature | Description |
|---|---|
| Food Type | Category of food being monitored |
| Storage Temperature | Temperature during storage (°C) |
| Relative Humidity | Relative humidity during storage (%) |
| Storage Duration | Duration of storage |

**Target variable:** Food spoilage status.

**Classification categories:**
- Fresh
- Nearing Spoilage
- Spoiled

## 5. Proposed Methodology

The project will follow a structured machine learning workflow:

1. Dataset identification and provenance assessment.
2. Data cleaning and quality assessment.
3. Exploratory Data Analysis (EDA).
4. Data preprocessing and feature engineering.
5. Training and testing dataset preparation.
6. Machine learning model development.
7. Hyperparameter optimisation and model evaluation.
8. Feature importance and model interpretability analysis.
9. Integration of the selected model into a Streamlit application.

## 6. Technology Stack

| Component | Technologies |
|---|---|
| Programming Language | Python |
| Data Processing | Pandas, NumPy |
| Data Visualisation | Matplotlib, Seaborn, Plotly |
| Machine Learning | Scikit-learn, XGBoost |
| Explainable AI | SHAP, Permutation Importance |
| Web Application | Streamlit |
| Model Persistence | Joblib |
| Version Control | Git, GitHub |

## 7. Planned Application Features

The Streamlit application is intended to provide:

- Interactive food spoilage prediction.
- Food-storage condition analysis.
- Model performance visualisation.
- Explainable prediction insights.
- Batch prediction through CSV uploads.
- Food inventory monitoring.
- Storage-condition scenario analysis.

## 8. Repository Structure

```text
freshguard-ai/
│
├── app/
├── data/
│   ├── raw/
│   └── processed/
│
├── models/
├── notebooks/
├── reports/
│   └── figures/
│
├── src/
├── tests/
│
├── README.md
└── .gitignore
```

## 9. Project Status

**Development phase:** Initial setup and dataset investigation.

Model training, performance evaluation, and application development are planned stages. Results will be documented after implementation and validation.

## 10. Limitations

Predictions will depend on the quality, representativeness, and reliability of the underlying dataset.

The proposed system is an educational and research prototype. It is not intended to replace established food-safety guidelines, laboratory testing, or professional food-safety assessments.

## 11. Author

Undergraduate project developed as part of a B.Tech programme in Bioinformatics with a specialisation in Artificial Intelligence and Machine Learning.
