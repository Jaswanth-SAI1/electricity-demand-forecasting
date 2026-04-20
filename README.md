Electricity Demand Forecasting using XGBoost

Project Overview :
This project predicts hourly electricity demand (in Megawatts) by combining power grid history with weather data and macroeconomic indicators. I used an XGBoost model to handle the complex relationships between these variables, achieving a final accuracy of 90.37% (9.63% MAPE).

How I Built It? :
Data Merging: Combined hourly grid data with weather patterns and World Bank economic statistics (GDP and Population).
Data Cleaning: Fixed "invisible" column naming errors and patched missing years in the economic data using forward and backward filling.
Feature Engineering: Since AI cannot read dates, I extracted the hour, day of the week, and month from the timestamps. I also created a "weekend" feature to help the model learn daily human routines.
Chronological Split: I used a strict 80/20 split (training on the past, testing on the future) to ensure the model wasn't "cheating" by peeking at future data.

Results :
Primary Score (MAPE): 9.63%
Key Insight: The model relied most heavily on Agriculture/GDP to set the baseline scale of the grid, while Temperature and the Hour of the day were the main reasons for hourly spikes in demand.
