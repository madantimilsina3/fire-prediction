# 🔥 Wildfire Prediction using Satellite Data (1-Week NASA Data)

This project predicts wildfire occurrence in the next hour and visualizes fire risk across the world for the upcoming week using machine learning. It uses NASA's FIRMS wildfire dataset for one week, processes the data in Google Colab, and builds a Random Forest classification model. 

NOTE: Because of having data of only one week, this model was not completely accurate as it locates some areas where there is very less chance of occurance of forest fire 



## 📊 Features Engineered
- Day of week, Hour of day
- Location-based clustering using grid IDs
- History-based features:
  - Fire count in the last 1 hour
  - Average brightness (T4) in the last 1 hour
  - Average FRP in the last 1 hour

---

## 🤖 Model
- **Type**: Random Forest Classifier
- **Target**: Predict if fire will occur in the next hour (`fire_next`)
- **Accuracy**: ~64% overall
- **Feature Importance**:
  - Brightness and FRP had stronger predictive power than fire count

---

## 🌍 Global Heatmap (Predicted Fire Risk)
- A global fire-risk heatmap was generated for the next week based on current week's data
- Data aggregated using grid-based latitude/longitude
- Final coordinates exported as CSV

---

## 🧰 Tools Used
- Google BigQuery (for NASA FIRMS data)
- Google Colab (Python coding & visualization)
- Pandas, GeoPandas, Matplotlib, Scikit-learn

---

## 📁 Files Included
- `fire_prediction.ipynb`: Full working notebook
- `filtered_fire_risk.csv`: Coordinates and predicted fire counts
- `heatmap.png`: Visual result (optional)
- `requirements.txt`: All packages used

---

## 📌 Future possibilities
- Use larger time windows (e.g., daily or weekly fire aggregation)
- Integrate real-time data stream for live monitoring
- Improve predictions using weather, wind, humidity, etc.
