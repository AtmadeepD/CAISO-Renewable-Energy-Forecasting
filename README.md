# CAISO-Renewable-Energy-Forecasting

This project presents an end-to-end time series analysis and forecasting pipeline for predicting **renewable energy generation** in California, using CAISO (California Independent System Operator) data. We aim to build a highly accurate forecasting model and assess the contribution of renewables to overall grid demand.

## 🎯 Project Objectives

- 📊 Analyze seasonal and monthly trends in renewable production.
- 🔍 Perform correlation analysis between different renewable sources.
- 📈 Develop forecasting models with state-of-the-art accuracy.
- ⚖️ Compare renewable generation against total energy demand.
- ✅ Achieve over 99% forecast accuracy using advanced ML.

## 📁 Dataset Overview

- **Source**: [CAISO Renewable Energy Data (Kaggle)](https://www.kaggle.com/datasets/karatechop/caiso-renewable-energy-data-20212022)
- **Duration**: Jan 2021 to Sep 2022
- **Frequency**: 5-minute intervals
- **Features**:
  - Generation from solar, wind, geothermal, biogas, biomass, small/large hydro
  - Fossil and nuclear generation
  - Total demand and imports

 ## 🧠 Model Summary

| Model         | MAE     | RMSE     |
|---------------|---------|----------|
| Naive         | 5195.42 | 7622.27  |
| Prophet       | 1305.26 | 1599.31  |
| XGBoost       | **31.51** | **43.74** ✅

## 📊 Techniques Used

### 📌 EDA
- Time-based trends: monthly, hourly, daily
- Renewable vs fossil-based generation trends
- Peak generation periods for solar, wind, hydro

### 🏗️ Feature Engineering
- Lag features: t-1, t-24, t-48, t-72
- Rolling windows: mean and std for 3, 6, 12, 24 steps
- Time components: hour, day of week, month, is_weekend, season

### 🤖 Modeling
- **Naive Baseline**: yesterday's value = today’s forecast
- **Prophet**: time-series model from Meta (trend + seasonality)
- **XGBoost**: gradient boosting with lag/rolling/time features

### ✅ Evaluation Metrics
- **MAE**: Mean Absolute Error
- **RMSE**: Root Mean Squared Error
- Visual comparison of predicted vs actual



Clone the repository and install dependencies:


🙋‍♂️ Author
Atmadeep Dey
💼 Business Analyst → Aspiring Data Scientist
GitHub: github.com/AtmadeepD

### ✅ Installation

```bash
git clone https://github.com/yourusername/CAISO-Renewable-Energy-Forecasting.git
cd CAISO-Renewable-Energy-Forecasting
pip install -r requirements.txt
