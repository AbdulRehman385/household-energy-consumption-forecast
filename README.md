# Household Electric Power Consumption Forecasting Using LSTM  

## Overview  
This project focuses on forecasting **Global Active Power** consumption using time-series data from the [Household Electric Power Consumption Dataset](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set/data). By employing a **Long Short-Term Memory (LSTM)** neural network, we aim to predict future energy consumption patterns, providing insights that can aid in energy optimization and management.  

## Dataset  
The dataset contains measurements of electric power consumption for a single household over nearly four years. Key attributes include:  
- `Global Active Power` (kW) - the target variable.  
- `Global Reactive Power` (kW).  
- `Voltage` (V).  
- `Global Intensity` (Ampere).  
- Sub-metering variables measuring energy consumption across specific areas.  

The data is available on [Kaggle](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set/data).  

## Project Workflow  
### 1. **Data Preprocessing**  
- Handled missing values.  
- Scaled features using **StandardScaler** for faster convergence.  
- Created lagged input sequences using a sliding window approach.  

### 2. **Model Architecture**  
- Utilized an LSTM model, which is well-suited for sequential data.  
- Input shape: `(samples, time steps, features)`.  
- Hyperparameters:  
  - Number of LSTM units.  
  - Learning rate.  
  - Batch size and epochs.  

### 3. **Evaluation Metrics**  
The model was evaluated using the following metrics:  
- **Mean Absolute Error (MAE)**: 0.0887  
- **Root Mean Squared Error (RMSE)**: 0.2419  
- **Mean Absolute Percentage Error (MAPE)**: 193.06%  

### 4. **Results**  
The model performed moderately well on absolute metrics (MAE and RMSE) but struggled with relative accuracy (MAPE), suggesting room for improvement.
