# Chaotic Time Series Forecasting

This repository contains an implementation of a multi-step forecasting algorithm for chaotic time series, focusing on identifying non-predictable points to minimize error propagation. The project is based on research conducted at the National Research University Higher School of Economics (HSE).

## 📌 Project Overview

The algorithm predicts chaotic time series (e.g., Lorenz system) by:
1. Using **z-vectors** for irregular embeddings of time series data.
2. Introducing **non-predictable points** to skip high-uncertainty predictions.
3. Combining clustering and regression (e.g., gradient boosting) to optimize multi-step forecasts.

**Key Features:**
- Multi-step prediction with error control.
- Adaptive skipping of non-predictable points.
- Comparison of three approaches: single-step, multi-step, and step-isolated prediction.

## 📊 Results

| Metric           | Baseline (All Points Predicted) | Ideal Model | Our Model (Approach 2) |
|------------------|--------------------------------|-------------|------------------------|
| MSE (avg)        | 0.0580                         | 0.0007      | 0.0250                 |
| Skipped Points   | 0                              | 28          | 34                     |

![Example Prediction](https://via.placeholder.com/600x400?text=Prediction+Plot)  
*Figure: Example of multi-step forecasting on Lorenz system (t=5000, h=75).*

## 🛠 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/chaotic-time-series-forecasting.git
   cd chaotic-time-series-forecasting
