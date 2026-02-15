# 🏃‍♀️ Personal Activity Analysis Dashboard (Power BI)
## 📊 Project Overview

This Power BI project analyzes personal activity data extracted from Apple Health. 

The dashboard explores:
- Daily activity trends
- Behavioral patterns (weekdays vs weekends)
- Correlation between step count and health metrics

The goal of this project was to practice data modeling, DAX measures, and analytical storytelling.
## 🗂 Dataset

Source Data – Apple Health Export (export.xml)

The raw XML file is highly nested and not analysis-ready. Therefore, it required parsing, cleaning, and transformation before it could be used in Power BI.

The data preparation process included:

1. XML parsing
- Extracting relevant <Record> elements
- Filtering only selected health metrics (e.g., steps, calories, distance)

2. Data cleaning

- Converting date-time fields to proper datetime format
- Removing duplicates
- Handling missing values
- Standardizing units

3. Aggregation

- Aggregating granular records (minute/hour level) into daily summaries
- Creating calculated metrics where necessary

The final result is a structured analytical model with one row per day granularity optimized for reporting.

## 🧱 Data Model

The dashboard follows a star schema structure:

- Fact_Activity (daily metrics)
- Dim_Date (date dimension)

A one-to-many relationship ensures correct filtering and aggregation.

![Model](https://github.com/user-attachments/assets/f551fc92-ae85-488c-8efd-86238085dede)

## 📈 Page 1: Activity Overview

This page provides a high-level summary of overall activity levels and trends over time.

![Screenshot_1](https://github.com/user-attachments/assets/f3faa22f-afca-477a-959a-aa61ee23c514)


## 🔎 Page 2: Patterns & Relationships

This page investigates behavioral patterns and metric relationships.

Key insights:

- Step count shows a strong positive correlation with active calories (0.89).
- Step count shows weak correlation with resting heart rate (0.15).
- Activity levels differ between weekdays and weekends.

These findings highlight the difference between short-term activity effects and longer-term physiological indicators.


![Screenshot_1839](https://github.com/user-attachments/assets/7f7921ac-6d43-43a1-8afb-ed31092e9b6b)

To enhance report interactivity and improve user experience, I implemented a dynamic metric selection mechanism that allows switching between key indicators. This eliminates the need for multiple duplicated visuals and enables a flexible analytical view using a single chart.

A parameter table was created using DATATABLE (not related to fact tables, used exclusively to drive a slicer):

![Screenshot_3](https://github.com/user-attachments/assets/f5898812-3d60-4de9-bed7-aae9d5ae3a30)


Dynamic Measure Using SWITCH (dynamically adjusts calculation logic based on slicer selection):


![Screenshot_2](https://github.com/user-attachments/assets/4558a314-ab74-4293-8587-f49babb2599b)




![apple_health_analysis](https://github.com/user-attachments/assets/6ebad1c3-38ea-42f5-acc8-b370086ec10e)


This project demonstrates how structured data modeling and DAX calculations can transform simple personal activity data into meaningful analytical insights.

Through the proper use of a star schema, calculated measures, and correlation analysis, I was able to validate expected relationships (a strong link between steps and calories) and identify weaker associations (a limited short-term impact of steps on resting heart rate).


