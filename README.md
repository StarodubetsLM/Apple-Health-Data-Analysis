# 🏃‍♀️ Personal Activity Analysis Dashboard (Power BI)
## 📊 Project Overview

This Power BI project analyzes personal physical activity data extracted from Apple Health. 

The dashboard explores:
- Daily activity trends
- Behavioral patterns (weekdays vs weekends)
- Correlation between step count and health metrics

The goal of this project was to practice data modeling, DAX measures, and analytical storytelling.
## 🗂 Dataset

The dataset contains daily aggregated values from 2021–2025:

- Step Count
- Active Energy Burned
- Distance
- Resting Heart Rate
- Walking Heart Rate

All metrics were pre-aggregated at daily level.
## 🧱 Data Model

The dashboard follows a star schema structure:

- Fact_Activity (daily metrics)
- Dim_Date (date dimension)

A one-to-many relationship ensures correct filtering and aggregation.
![Model](https://github.com/user-attachments/assets/de78778f-cac0-4a81-8a8d-d6d61e1ac5fc)

