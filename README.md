This project presents a deep learning-based framework to detect and forecast extreme rainfall events across India using high-resolution gridded daily rainfall data from the Indian Meteorological Department (1951–2023). It employs Convolutional Neural Networks (CNN) for detection and Long Short-Term Memory (LSTM) networks for time series forecasting, incorporating both spatial and temporal patterns. Model performance is further validated using outputs from 12 CMIP6 global climate models to ensure generalization and robustness.

Key Metrics
CNN Detection: Precision 0.29 | F1 Score 0.35

LSTM Forecasting: Accuracy 89% | MAE 2.56 mm | RMSE 7.62 mm | Precision 0.75 | F1 Score 0.61

Methodology Overview
Data: IMD daily gridded rainfall (1951–2023), spatial resolution 0.5° × 0.5°

Models: CNN for spatial anomaly detection; LSTM for sequential rainfall forecasting

Preprocessing: Linear interpolation for missing values, normalization, 30-day temporal windowing

Training Setup: 50 epochs | Batch size 32 | 20% validation split | Adam optimizer | MSE loss

Cross-Validation: Forecast outputs evaluated against 12 CMIP6 models to assess model transferability and distributional alignment

Validation with CMIP6 Models:  Model generalization was assessed via cross-validation with 12 CMIP6 global climate models, comparing IMD-based predictions against synthetic outputs using KDE, CDF plots, precision-recall curves, and error metrics (MAE/RMSE). The BSS-ESM1 and ACCESS-CM2 models showed the closest alignment in terms of statistical distribution and extreme event representation.

Highlights:-

Dual-model framework integrating spatial and temporal deep learning

Robust evaluation across multiple climate models and geographic zones

Deployment-ready pipeline with TensorFlow/Keras and GPU acceleration

Visual diagnostics: heatmaps, KDE, CDFs, and regional rainfall variability plots

