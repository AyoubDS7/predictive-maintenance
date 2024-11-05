Predictive Maintenance for Industrial Machines
This project aims to predict potential machine failures using historical telemetry, maintenance, and error data. The model identifies patterns and conditions that often lead to failures, enabling timely maintenance and reducing machine downtime.

Project Overview
Predictive maintenance is a proactive maintenance strategy that uses data to predict when a machine is likely to fail, allowing for preemptive repairs. This project leverages machine learning techniques to analyze machine sensor data, maintenance logs, and error reports. Our target variable is the time to failure (time_to_failure), helping to predict the time remaining before a machine fails based on input data.

Dataset
The data consists of several CSV files, including:

Telemetry Data: Contains time-series data for machine parameters (voltage, rotation speed, pressure, and vibration).
Maintenance Logs: Records details of historical maintenance events.
Error Logs: Tracks error events detected on machines.
Machine Information: Provides unique identifiers and attributes for each machine.
These files were merged based on timestamps and machine IDs to create a cohesive dataset for analysis.

Key Features Used
Time-Based Features: Year, month, day, hour, day of the week.
Sensor Readings: Voltage, rotation speed, pressure, and vibration.
Machine Attributes: Machine age, machine ID.
Lagged Features: Previous values of sensor readings (e.g., lag_1, lag_2, lag_3) to capture recent trends.
Project Workflow
Data Preprocessing:

Combined telemetry, error, and maintenance datasets.
Created time-based features and lagged sensor readings to capture machine performance trends.
Labeled failure cases based on historical records to train the model.
Resampled data where necessary to manage irregular timestamps.
Exploratory Data Analysis (EDA):

Analyzed feature distributions, correlations, and trends in sensor data.
Investigated patterns associated with machine failures.
Modeling:

Classification and Regression Models: Experimented with various algorithms, including Random Forest, Gradient Boosting, and LSTM (for time series).
Evaluation Metrics: Evaluated models using accuracy, precision, recall, and F1 score. Set threshold probabilities to optimize precision and recall for failure detection.
Deployment:

The final model was deployed to predict time to failure on new data, giving maintenance teams an advanced warning of potential failures.
Threshold Tuning: Adjusted thresholds to maximize accuracy and ensure the timely detection of impending failures.
