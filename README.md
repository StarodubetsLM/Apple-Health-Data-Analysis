# 🏃‍♀️ Personal Activity Analysis Dashboard (Power BI)
## 📊 Project Overview

This Power BI project analyzes personal activity data extracted from Apple Health. 

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

![Model](https://github.com/user-attachments/assets/88f37d74-5fa7-4e36-8fab-1aeb24f3f4b1)

## 📈 Page 1: Activity Overview

This page provides a high-level summary of overall activity levels and trends over time.

It includes:
- Main KPI metrics
- Average daily steps
- Distance trends
- Walking and resting heart trends
- Time-based analysis

![Screenshot_1829](https://github.com/user-attachments/assets/461fa855-7a68-4121-8432-9245b465d2cf)

## 🔎 Page 2: Patterns & Relationships

This page investigates behavioral patterns and metric relationships.

Key insights:

- Step count shows strong positive correlation with active calories (0.89).
- Step count shows weak correlation with resting heart rate (0.15).
- Activity levels differ between weekdays and weekends.

These findings highlight the difference between short-term activity effects and longer-term physiological indicators.

![Screenshot_1830](https://github.com/user-attachments/assets/942de64c-6cea-44be-8e70-8014e64259fb)

![Animation](https://github.com/user-attachments/assets/7b1d0e84-f6c6-4b75-b5c1-a9a148e9fbb5)



This project demonstrates how structured data modeling and DAX calculations can transform simple personal activity data into meaningful analytical insights.

Through the proper use of a star schema, calculated measures, and correlation analysis, I was able to validate expected relationships (a strong link between steps and calories) and identify weaker associations (a limited short-term impact of steps on resting heart rate).


