# Mental Health Care Data Analysis

##  Introduction
Mental health is a crucial aspect of overall well-being, yet it often goes unnoticed. This project aims to analyze mental health data using **SQL** and visualize insights using **Power BI**. The goal is to understand patterns related to mental health, including the impact of **physical activity, social support, stress levels, and self-esteem** across different age groups.

---

##  Dataset Overview
This project is based on a **Mental Health Care dataset** containing various attributes such as:
- **Age** (Demographic information)
- **Physical Activity Hours** (Impact on mental health)
- **Social Support Levels**
- **Anxiety, Depression, and Stress Scores**
- **Work & Financial Stress Levels**
- **Self-Esteem, Life Satisfaction, and Loneliness Scores**

The dataset has been cleaned and structured for analysis using **SQL**.

---

##  SQL Analysis
### **Key Steps Taken in SQL:**
    Dropped irrelevant columns (e.g., unnecessary links)
    Checked for **data types, null values, and duplicates**
    Cleaned missing values and handled inconsistencies
    Created **age categories** (e.g., Young Adults, Middle-aged, Seniors)
    Performed **KPI analysis** to derive insights

### **Key Queries Used:**
   Finding duplicate data:
```sql
SELECT name, city, cuisine, COUNT(*)
FROM restaurants
GROUP BY name, city, cuisine
HAVING COUNT(*) > 1;
```
   Checking null values:
```sql
SELECT column_name, COUNT(*) AS null_count
FROM table_name
WHERE column_name IS NULL
GROUP BY column_name;
```
   Categorizing Age Groups:
```sql
CASE
    WHEN age BETWEEN 18 AND 30 THEN 'Young Adults'
    WHEN age BETWEEN 31 AND 50 THEN 'Middle-aged'
    ELSE 'Seniors'
END AS Age_Group
```

---

##  Power BI Dashboard
### **Visualizations Created:**
  **Sleep Hours vs. Anxiety/Depression Levels** (Box Plot)  
  **Work Stress & Financial Stress across Age Groups** (Bar Chart)  
  **Self-Esteem & Life Satisfaction Score Trends** (Line Graph)  
  **Impact of Physical Activity on Mental Health** (Ribbon Chart)  
  **Overall Mental Health Score Dashboard** (Card Visualization)

### **Interactive Features:**
   **Slicers** for filtering by age groups, gender, and stress levels  
   **Drill-down insights** for deeper analysis  
   **KPI indicators** for key mental health metrics

---

##  Key Insights
  **Physical Activity** has a strong positive impact on mental health.  
  **Social Support** is crucial in reducing stress and improving well-being.  
  **Anxiety, Depression, and Stress Levels** vary significantly across age groups.  
  **Work & Financial Stress** peak in middle age (31-50 years).  
  **Self-Esteem and Life Satisfaction** decrease as loneliness increases.

---

## How to Use This Project
1. **SQL Analysis:** Open `Mental_health_care_Data.sql` and run queries to explore insights.
2. **Power BI Dashboard:** Open `Mental Health PBi.pbix` in Power BI and interact with visuals.
3. **GitHub Upload:** Upload this project on GitHub and share your insights!

---

## About the Author
This project was created to raise awareness about mental health using data-driven insights. If you have suggestions or would like to collaborate, feel free to connect! 

---

