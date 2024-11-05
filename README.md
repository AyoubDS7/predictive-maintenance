# Predictive Maintenance for Industrial Machines

This project focuses on predictive maintenance, utilizing machine learning to forecast potential failures in industrial machines. By analyzing historical telemetry, maintenance, and error data, the model predicts the likelihood of future machine failures, enabling timely maintenance actions.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Modeling Approach](#modeling-approach)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Predictive maintenance is a data-driven approach aimed at predicting machine failures before they occur. This allows for proactive maintenance, reducing downtime and extending equipment lifespan. The target variable in this project is **time to failure** (`time_to_failure`), helping predict how much time is left before a machine needs maintenance.

## Dataset

The dataset includes multiple CSV files with detailed information on each machine:
- **Telemetry Data**: Time-series data capturing machine parameters (e.g., voltage, rotation speed, pressure, and vibration).
- **Maintenance Logs**: Record of historical maintenance activities.
- **Error Logs**: Logs of error events that occurred in each machine.
- **Machine Information**: Static information about each machine (e.g., machine ID, age).

## Features

The primary features used for model training include:
- **Temporal Features**: Extracted from date and time (year, month, day, hour, etc.).
- **Lagged Features**: Historical sensor readings (`lag_1`, `lag_2`, `lag_3`) to capture recent trends.
- **Machine Parameters**: Voltage, rotation speed, pressure, vibration, and age of the machine.
- **Error Indicators**: Captures instances of specific error events.

## Modeling Approach

1. **Data Preprocessing**: Cleaning and merging multiple data sources, creating lagged features, and engineering additional time-based features.
2. **Feature Engineering**: Added lagged features to capture time-based patterns.
3. **Model Training**: Used **XGBoost** for training on engineered features. Target variable was **time to failure** (`time_to_failure`).
4. **Evaluation**: Evaluated the model using metrics such as Mean Squared Error (MSE) and Mean Absolute Error (MAE) for regression tasks.

## Installation

Clone the repository and install the required packages:
```bash
git clone https://github.com/yourusername/predictive-maintenance.git
cd predictive-maintenance
pip install -r requirements.txt

