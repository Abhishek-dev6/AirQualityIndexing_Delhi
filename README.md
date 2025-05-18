# # 🌫️ Delhi AQI Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Model-orange?logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Project-Active-brightgreen)

> A Machine Learning project to predict **Air Quality Index (AQI)** in Delhi using environmental pollution data and a **Random Forest Regressor** model.

---

## 📌 Overview

Air pollution in Delhi is a major concern. This project leverages machine learning to **predict AQI levels** using key atmospheric pollutant indicators. With the help of Python, we clean data, compute synthetic AQI, train a model, and visualize predictions.

---

## 📁 Dataset Information

The dataset used: `delhi_aqi.csv`  
It contains pollutant measurements:

- 🌫 PM2.5
- 🌁 PM10
- 🧪 NO, NO₂, SO₂
- 🌬 CO, O₃
- 🧼 NH₃

---

## ⚙️ Workflow Summary

### 🔹 Step 1: Data Cleaning
- Missing values handled using forward-fill (`ffill`).

### 🔹 Step 2: AQI Construction
Weighted formula based on pollutant severity:
```python
AQI = (
    pm2_5 * 0.4 +
    pm10 * 0.3 +
    no2 * 0.1 +
    so2 * 0.05 +
    co * 0.1 +
    o3 * 0.05
)
