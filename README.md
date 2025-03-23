# AirPulseAI

A deep‑learning powered time‑series model that accurately forecasts hourly CO concentrations to help urban planners and communities monitor and mitigate air pollution in real time.

---

## 📊 Overview

AirPulseAI leverages a stacked recurrent neural network to learn temporal dependencies in urban air‑quality data and predict next‑hour carbon monoxide (CO) levels with high accuracy. This project demonstrates robust performance (R² = 0.9136, RMSE = 0.0381) on real‑world sensor readings, offering actionable insights for environmental monitoring and decision‑making.

---

## 📂 Dataset

- **Source:** Hourly air‑quality measurements from an urban monitoring station  
- **Features:** CO concentration (target), NO₂, temperature, humidity, and additional sensor readings  
- **Preprocessing:** Forward‑fill imputation, MinMax scaling, sliding window sequence generation (sequence length = 10)

---

## 🧠 Model Architecture

| Component        | Details                            |
|------------------|------------------------------------|
| Architecture     | 3‑layer stacked RNN                |
| Hidden Size      | 64                                 |
| Activation       | Tanh (RNN), ReLU (dense)           |
| Dropout          | 0.2                                |
| Output           | Single linear neuron               |
| Loss Function    | Mean Squared Error (MSE)           |
| Optimizer        | Adam (lr=0.001)                    |
| Batch Size       | 64                                 |
| Early Stopping   | Patience = 5 epochs                |

---

## 📈 Performance

| Metric        | Training | Validation | Test    |
|---------------|----------|------------|---------|
| Loss (MSE)    | 0.0016   | 0.0015     | 0.0014  |
| Accuracy      | 97.73%   | 99.57%     | 83.29%  |
| MAE           | —        | —          | 0.0292  |
| RMSE          | —        | —          | 0.0381  |
| R² Score      | —        | —          | 0.9136  |

---

## 📊 Visualizations

- **Loss Curves:** Converging training/validation loss with minimal overfitting  
- **Time‑Series Plot:** Actual vs. predicted CO concentrations  
- **Scatter Plot:** Strong linear correlation between predictions and ground truth

---

## 🚀 Usage

Load the trained AirPulseAI model to generate next‑hour CO forecasts from the latest sensor data. Ideal for integrating into dashboards, alerting systems, or decision‑support tools for air quality management.

---

## ⚙️ Future Work

- Experiment with LSTM/GRU and bidirectional architectures  
- Extend forecasting horizon beyond one step  
- Incorporate external features (weather, traffic, industrial activity)  
- Explore advanced imputation and feature engineering techniques  

---

## 📄 License

Distributed under the MIT License.
