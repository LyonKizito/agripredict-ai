# Agripredict-AI
Streamlit dashboard + ML models for democratizing agricultural forecasting

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)](https://streamlit.io/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.5+-blue.svg)](https://pandas.pydata.org/)
[![Plotly](https://img.shields.io/badge/Plotly-5.0+-purple.svg)](https://plotly.com/python/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 🌍 The Problem

Over **33 million smallholder farmers** in East Africa lack access to data-driven yield predictions, contributing to:
- Food insecurity affecting 60% of the region’s population  
- Financial instability due to poor harvest planning  
- 20–30% crop losses from preventable causes  
- Limited access to credit without yield forecasts  

While large commercial farms use advanced AI forecasting, **80% of East African farmers rely solely on traditional methods**, widening the agricultural digital divide.

---

## 💡 The Solution

AgriPredict AI is an **ML-powered decision support tool** that predicts maize yields 3–6 months in advance using:
- ☁️ Weather patterns (rainfall, temperature, humidity)  
- 🌱 Historical yield data  
- 📊 Agricultural best practices  

**Designed for:**
- Individual smallholder farmers (mobile-friendly interface)  
- Agricultural cooperatives and NGOs (regional insights)  
- Government extension officers (planning support)  

---

## 🎯 Impact Potential

- 📈 Improve yield planning for 100,000+ farmers  
- 💰 Increase farmer income stability by 25%  
- 🌾 Reduce post-harvest losses by 15–20%  
- 🍽️ Support food security in climate-vulnerable regions  

---

## 🚀 Key Features

1. **Accurate Predictions**  
   - R²: 0.82 with Random Forest on test set  
   - MAE: 0.42 tons/ha  
   - Validated on synthetic + historical-style datasets  

2. **Explainable AI**  
   - Feature importance visualization  
   - Scenario testing (“what if rainfall increases by 20%?”)  
   - Farmer-friendly outputs  

3. **Accessibility First**  
   - Mobile-responsive Streamlit interface  
   - Low-bandwidth optimized  
   - Bilingual support (English/Swahili – planned)  
   - No login required  

4. **Actionable Insights**  
   - Personalized recommendations  
   - Seasonal comparisons  
   - Risk assessment for weather variability  

---

## 📊 Demo

🔗 **[Live Demo – Streamlit Cloud (Coming Soon)]()**  

For now, run locally with the instructions below.  

**Screenshots**  

**Prediction Dashboard**  
![Dashboard](plots/eda_overview.png)  

**Scenario Analysis**  
![Scenarios](plots/correlation_matrix.png)  

---

## 🛠️ Quick Example

```python
from models.predict import predict_yield

features = {
    "location": "Kakamega",
    "total_rainfall": 850,
    "avg_temp": 24,
    "min_temp": 18,
    "max_temp": 32,
    "avg_humidity": 70,
    "prev_year_yield": 2.8,
}

yield_pred, conf = predict_yield(features)
print(f"Predicted Yield: {yield_pred:.2f} tons/ha (± {conf:.2f})")
