# Uber-Data-Analysis-Python

A Data Science project performing Exploratory Data Analysis (EDA) and data cleaning on Uber trip data using Python, Pandas, and Matplotlib.

---

## 🚀 Project Overview (STAR Method)

### **Situation**
Uber generates massive amounts of data regarding trips, categories, and purposes. However, raw data is often "messy"—containing missing values, inconsistent date formats, and hidden patterns that are difficult to interpret without systematic analysis.

### **Task**
My objective was to perform a comprehensive Exploratory Data Analysis (EDA) to clean the dataset and extract actionable insights. Specifically, I aimed to identify peak travel times, the most common reasons for trips, and the distribution of "Business" vs. "Personal" categories to better understand user behavior.

### **Action**
* **Data Cleaning:** Handled missing values in the PURPOSE column and converted date-time objects into a standard format using Pandas.
* **Feature Engineering:** Extracted specific features like Hour, Day, Month, and Weekday to enable time-series analysis.
* **Data Visualization:** Leveraged Matplotlib and Seaborn to create:
    * Bar charts for trip purposes.
    * Count plots for the busiest days of the week.
    * Comparison plots between Business and Personal categories.
* **Statistical Analysis:** Calculated average trip distances and identified the most frequent start and stop locations.

### **Result**
* Successfully transformed a messy dataset into a clean, structured format ready for modeling.
* Discovered that the majority of trips occur during **afternoon hours** for "Business" purposes.
* Identified that **Friday** is the busiest day for Uber users in this dataset.
* Provided a clear roadmap for how data-driven decisions can optimize fleet management.
