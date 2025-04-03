# Astana_Bus_Arrival_Time_Prediction

This project investigates various machine learning models to predict **bus arrival times** in **Astana** using GPS data. The goal is to enhance public transportation reliability through accurate forecasting of bus arrivals.

---

## 📌 Project Overview

- **Objective**: Predict the arrival time of buses using real-time GPS and bus stop data.
- **Location**: Astana city, Kazakhstan
- **Data Sources**: 
  - GPS data of buses
  - Bus stop metadata
  - Passenger flow information

---

## 🧠 Models Implemented

1. **K-Nearest Neighbors (KNN)**
2. **Logistic Regression**
3. **Support Vector Machine (SVM)**
4. **Linear Regression**
5. **Convolutional LSTM (Conv_LSTM)**

---

## 🧪 Evaluation Metrics

The models were assessed using:

- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **RMSE (Root Mean Squared Error)**
- **R² Score (Coefficient of Determination)**

| Model              | MAE   | MSE   | RMSE  | R²   |
|--------------------|-------|-------|--------|------|
| KNN                | 5.47  | 47.74 | 6.91   | 0.88 |
| SVM                | 2.39  | 13.95 | 3.73   | 0.97 |
| **Linear Regression** | **0.00**  | **0.00**  | **0.00**   | **1.00** |
| Logistic Regression| 3.85  | 25.48 | 5.05   | 0.94 |
| Conv_LSTM          | 3.54  | 19.91 | 4.46   | 0.95 |

---

## 📊 Key Results

- **Linear Regression** showed perfect performance (R² = 1.00) — indicating a strong linear relationship in the dataset.
- **Conv_LSTM** and **SVM** performed well and captured complex patterns.
- **KNN** performed poorly, highlighting limitations of distance-based models in this task.

---

## ⚙️ Data Preprocessing

- Combined 4 raw `.csv` files (bus positions, stops, passenger flows)
- Merged using `bus_id`, or alternatively rounded coordinates
- Extracted time-based features: hour, minute, day of week
- Applied **mean imputation** for missing values

---

## 🧠 Conv_LSTM Architecture (Deep Learning)

- Input: sequences of previous timestamps
- Layers:
  - Convolutional 1D Layer (feature extraction)
  - LSTM Layer (temporal modeling)
  - Dense output layer (regression)

---

## 📦 Technologies Used

- **Python**
- `pandas`, `scikit-learn`, `TensorFlow/Keras`, `matplotlib`, `seaborn`, `NumPy`

---

## 🧭 Future Work

- Incorporate **weather and traffic data**
- Explore **ensemble methods** (e.g. VotingRegressor, Stacking)
- Use **attention-based models** or Transformers for sequential forecasting
- Build a live **web interface** for displaying arrival time predictions

---

## 📁 Files

- `Astana_Bus_Arrival_Time_Prediction.ipynb`: Full notebook with preprocessing, modeling, and evaluation
- `*.csv`: Raw GPS and stop datasets
- Supplementary: Conv_LSTM implementation and plots

---

## 👨‍💻 Author

- **Maxim Azarnov**  
  Bachelor Student, Big Data Analysis  
  Astana
