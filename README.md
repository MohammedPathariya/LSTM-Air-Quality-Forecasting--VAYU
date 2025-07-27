# 🧠 VAYU - Air Quality Prediction using LSTM and Stacked LSTM

Air pollution is a pressing environmental challenge, especially in urban areas where millions of people are exposed to hazardous air quality. This project leverages machine learning techniques, particularly **LSTM (Long Short-Term Memory)** and **Stacked LSTM**, to **predict the Air Quality Index (AQI)** using real-time sensor data from the [OpenAQ API](https://openaq.org/).

---

## 🌍 Problem Statement

Air pollution causes significant health risks such as asthma, lung disease, and cancer. Accurate AQI prediction can help authorities and individuals take preventive measures in time.

---

## ✅ Project Objectives

- Collect real-time air quality data from OpenAQ API
- Clean and preprocess the data (PM1, PM2.5, PM10, UM010, UM025, UM100)
- Visualize pollution trends and parameter correlations
- Calculate AQI based on Indian and WHO guidelines
- Train predictive models using:
  - Simple LSTM
  - 3-layer Stacked LSTM
  - 4-layer Stacked LSTM
- Compare RMSE performance metrics
- Generate actionable insights for public health

---

## 📦 Tech Stack

- **Python**
- **Pandas, NumPy**
- **Matplotlib, Seaborn, Folium**
- **Keras / TensorFlow**
- **Sklearn**
- **OpenAQ API**
- **Mlxtend** (for Association Rule Mining)

---

## 📊 Data Source

- API: [OpenAQ Measurements API](https://docs.openaq.org/reference/averages_v2_get_v2_averages_get)
- Location Used: **Pride Orchid, Whitefield, Bangalore**
- Data Extracted: PM1, PM2.5, PM10, UM010, UM025, UM100

---

## 📌 Workflow Overview

1. **Fetch & Store Data**:
   - Pull measurements from OpenAQ API
   - Store raw data to CSV

2. **Preprocessing**:
   - Drop unnecessary columns
   - Parse timestamp into date & time
   - Pivot data for time-series modeling
   - Normalize values for association mining

3. **Visualization**:
   - Plot PM and UM concentration trends
   - Display WHO vs India AQI standards
   - Map sensor locations using Folium
   - Correlation matrix heatmaps

4. **AQI Calculation**:
   - Based on Indian AQI standards (PM2.5 & PM10)
   - Custom function to assign AQI category

5. **Association Rule Mining**:
   - Apriori algorithm with min support 0.1 and confidence 0.7
   - Identify co-occurrence of pollutant levels

6. **Modeling**:
   - Split data into train/test
   - Apply MinMax scaling
   - Train three models:
     - Simple LSTM
     - 3-layer Stacked LSTM
     - 4-layer Stacked LSTM
   - Evaluate with RMSE

---

## 🧪 Model Results

| Model Type           | Train RMSE | Test RMSE |
|----------------------|------------|-----------|
| Simple LSTM          | 32.38      | 29.93     |
| 3-layer Stacked LSTM | 8.03       | 3.16      |
| 4-layer Stacked LSTM | 7.48       | 3.13      |

✅ **Stacked LSTM outperforms Simple LSTM** by capturing temporal dependencies more effectively.

---

## 🔬 Sample Visualizations

- **PM Concentrations Over Time**
- **AQI Trends**
- **Correlation Matrix**
- **Geolocation Map of Indian Sensors**

*(Use `plt.show()` or export to display in notebooks)*

---

## 📍 How to Use

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/air-quality-prediction.git
   cd air-quality-prediction
   ```

2. Install requirements:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the main notebook/script:

   ```bash
   python main.py
   ```

---

## 🌱 Tips to Reduce Air Pollution

* Use public transport or carpool
* Turn off appliances when not in use
* Plant trees and reduce plastic use
* Avoid burning waste
* Switch to energy-efficient products
* Raise awareness in your community

---

## 📌 Future Improvements

* Incorporate meteorological data (humidity, temperature)
* Use other time series models like GRU, ARIMA
* Add regional emission data
* Deploy as a real-time web dashboard

---

## 📜 License

MIT License © 2025

---

## 🙌 Acknowledgments

* [OpenAQ](https://openaq.org/)
* WHO & CPCB for AQI standards
* TensorFlow/Keras for model training

---
