# 🌍 Air Quality Data Analysis & Preprocessing (India 2015–2020)

## 📌 Project Overview

This project focuses on **data preprocessing and analysis** of air quality data across Indian cities from **2015 to 2020**.
The goal is to transform raw, unclean data into a **machine learning-ready dataset** using a complete industry-level preprocessing pipeline.

---

## 🎯 Objectives

* Clean and preprocess raw air quality data
* Handle missing values, duplicates, and outliers
* Perform feature engineering for better insights
* Prepare data for machine learning models
* Generate meaningful visual insights

---

## 📂 Dataset Information

The dataset contains air quality measurements such as:

* PM2.5, PM10
* NO, NO2, NOx
* CO, SO2, O3
* Benzene, Toluene, Xylene
* AQI (Air Quality Index)
* City and Date information

---

## ⚙️ Project Workflow

### 🔰 Step 0: Extract ZIP Data

* Extracted compressed dataset using `zipfile`
* Organized files into a working directory

---

### 📥 Step 1: Load Data

* Loaded CSV into pandas DataFrame
* Verified shape, columns, and sample data

---

### 🔍 Step 2: Data Inspection

* Used:

  * `df.info()`
  * `df.describe()`
  * `df.isnull().sum()`
* Identified missing values and incorrect data types

---

### 🧹 Step 3: Handling Missing Values

* Numerical columns → filled using **median**
* Categorical columns → filled using **mode**
* Ensured minimal data loss

---

### 🔁 Step 4: Removing Duplicates

* Checked duplicate rows using `df.duplicated()`
* Removed duplicates to maintain data integrity

---

### 🔄 Step 5: Data Type Conversion

* Converted `Date` to datetime format
* Ensured numerical columns are correctly typed

---

### 📊 Step 6: Outlier Detection

* Used **IQR (Interquartile Range)** method
* Visualized using **boxplots**
* Retained outliers as they represent real-world pollution spikes

---

### 🧠 Step 7: Feature Engineering

Created new meaningful features:

* `Year`, `Month`, `Day` (time-based)
* `Avg_Pollution` (combined pollution metric)
* `Pollution_Level` (categorical bins)
* `High_Pollution` (binary flag)

---

### 🔢 Step 8: Encoding

* Label Encoding → ordered categories (`AQI_Bucket`)
* One Hot Encoding → unordered categories (`City`)
* Avoided dummy variable trap using `drop_first=True`

---

### 📏 Step 9: Feature Scaling

* Applied **StandardScaler**
* Ensured all features have equal importance
* Handled outliers effectively

---

### ✅ Step 10: Final Dataset

* Verified:

  * No missing values
  * No duplicates
  * Proper data types
* Exported clean dataset:

  ```
  clean_air_quality_data.csv
  ```

---

## 📊 Visualizations Used

* 📦 Boxplot → Outlier detection
* 📈 Line Plot → AQI trends over time
* 📊 Histogram → Data distribution
* 🔥 Heatmap → Feature correlation

---

## 🔍 Key Insights

* AQI shows **high variability** across time and cities
* PM2.5 and PM10 are **strongly correlated**
* Pollution levels show **seasonal trends**
* Outliers represent **real environmental conditions**, not errors

---

## 🛠️ Technologies Used

* Python 🐍
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 🚀 Future Work

* Build **AQI Prediction Model**
* Perform advanced EDA
* Deploy as a web application
* Integrate real-time air quality APIs

---

## 💡 Interview-Ready Summary

This project demonstrates a complete **data preprocessing pipeline**, including:

* Data cleaning
* Feature engineering
* Encoding & scaling
* Outlier handling
* Time series preparation

It reflects real-world data science workflow used in industry.

---

## 👨‍💻 Author

**Satish**
Data Science Enthusiast | DSCE Bangalore

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and share your feedback!
