# 🌍 Earthquake Data Analysis

## 📌 Project Overview

This project analyzes historical earthquake data to identify patterns, trends, and insights related to seismic activities across the globe. The dataset spans from **2150 BC to 2019 AD**, offering a long-term perspective on earthquake occurrences.

The project demonstrates how raw geological data can be transformed into meaningful insights using **data cleaning, exploratory data analysis (EDA), visualization, and optional database integration**.

---

## 🎯 Objectives

* Analyze earthquake **frequency over time**
* Identify **high-risk seismic regions**
* Study **magnitude and depth relationships**
* Understand patterns in **earthquake occurrence**
* Support **disaster preparedness and risk assessment**

---

## 📂 Dataset Information

The dataset includes:

* Date and Time
* Latitude & Longitude
* Magnitude & Magnitude Type
* Depth (km)
* Location / Place
* Impact-related attributes (if available)

---

## ⚙️ Project Workflow

### 🔹 Data Preprocessing

* Handle missing values
* Remove duplicate records
* Convert date/time into proper format
* Clean and standardize data
* Handle outliers in magnitude and depth

---

### 🔹 Exploratory Data Analysis (EDA)

* Year-wise earthquake trend analysis
* Region-wise earthquake frequency
* Magnitude distribution
* Depth vs magnitude relationship

---

### 🔹 Data Visualization

* Line charts → Earthquake trends over time
* Bar charts → Top affected regions
* Scatter plots → Depth vs magnitude
* Heatmaps → Correlation between variables

---

## 🛠️ Technologies Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Jupyter Notebook
* MySQL (optional)
* SQLAlchemy (database integration)
* Streamlit (optional dashboard)

---

## 📂 Project Structure

```
earthquake_project/
│
├── data/
│   └── earthquake.csv
│
├── notebooks/
│   └── earthquake_analysis.ipynb
│
├── database/
│   └── earthquakes.sql
│
├── app.py
└── README.md
```

---

## 📊 Key Insights

* Earthquakes are concentrated in **tectonically active zones**
* High-magnitude earthquakes are **rare but impactful**
* Increase in recorded earthquakes due to **improved technology**
* Depth influences the **severity of impact**

---

## 💾 Database Integration (Optional)

```python
from sqlalchemy import create_engine

engine = create_engine("mysql+pymysql://root:password@localhost/earthquake_project")
df.to_sql("earthquakes", con=engine, if_exists="replace", index=False)
```

---

## 🚀 How to Run

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn sqlalchemy pymysql

# Run Jupyter Notebook
jupyter notebook

# (Optional) Run Streamlit app
streamlit run app.py
```

---

## 🔮 Future Enhancements

* Real-time earthquake data integration
* Machine learning prediction models
* Interactive dashboards (Power BI / Streamlit)
* Alert systems for high-risk zones

---

## 🤝 Contribution

Contributions are welcome! Feel free to fork and improve this project.

---

## 📜 License

This project is created for **educational purposes only**.

---



# 🌍 Earthquake Data Analysis (Program-Based)

## 📌 Overview

This project focuses on **Earthquake Data Analysis using Python**, aiming to clean, analyze, and visualize historical seismic data. It helps uncover meaningful patterns in earthquake **magnitude, depth, location, and occurrence over time**.

The project demonstrates a complete **data analytics workflow**, from preprocessing to visualization, with optional database integration for scalability.

---

## 🎯 Objectives

* Load and preprocess earthquake dataset
* Perform exploratory data analysis (EDA)
* Visualize trends and patterns using graphs
* Analyze relationships between key variables
* (Optional) Store processed data in MySQL

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SQLAlchemy (MySQL integration)

---

## ⚙️ Program Workflow

### 🔹 Step 1: Import Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

### 🔹 Step 2: Load Dataset

```python
df = pd.read_csv("earthquake.csv")
df.head()
```

Loads the dataset into a Pandas DataFrame for analysis.

---

### 🔹 Step 3: Data Preprocessing

```python
df.dropna(inplace=True)
df['date'] = pd.to_datetime(df['date'])
df = df[df['mag'] > 0]
```

* Removes missing values
* Converts date column to datetime format
* Filters invalid magnitude values

---

### 🔹 Step 4: Feature Engineering

```python
df['year'] = df['date'].dt.year
```

Extracts year for time-based trend analysis.

---

### 🔹 Step 5: Year-wise Analysis

```python
yearly = df['year'].value_counts().sort_index()
yearly.plot()
plt.title("Earthquake Trend")
plt.show()
```

Displays how earthquake frequency changes over time.

---

### 🔹 Step 6: Magnitude Distribution

```python
sns.histplot(df['mag'], bins=30)
plt.title("Magnitude Distribution")
plt.show()
```

Shows the distribution of earthquake magnitudes.

---

### 🔹 Step 7: Depth vs Magnitude

```python
plt.scatter(df['depth_km'], df['mag'])
plt.xlabel("Depth")
plt.ylabel("Magnitude")
plt.show()
```

Visualizes the relationship between depth and earthquake intensity.

---

### 🔹 Step 8: Database Storage (Optional)

```python
from sqlalchemy import create_engine

engine = create_engine("mysql+pymysql://root:password@localhost/earthquake_project")
df.to_sql("earthquakes", con=engine, if_exists="replace", index=False)
```

Stores cleaned data into a MySQL database for further use.

---

## 📊 Output

* 📈 Line Graph → Earthquake trends over time
* 📊 Histogram → Magnitude distribution
* 🔵 Scatter Plot → Depth vs Magnitude

---

## 🔍 Key Insights

* Earthquakes are concentrated in specific geographic zones
* High-magnitude earthquakes are rare but highly impactful
* Increase in recorded events is influenced by improved detection technology
* Depth plays a critical role in determining earthquake impact

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy pymysql
jupyter notebook
```

---

## 🔮 Future Scope

* Machine learning-based earthquake prediction
* Real-time data integration using APIs
* Interactive dashboards (Streamlit / Power BI)
* Early warning and alert systems

---

## 📜 License

This project is intended for **educational purposes only**.

---


earthquake_data_presentation
🎯 Slide 1: Title

🌍 Earthquake Data Analysis

Data Science Project
Your Name
Date
📌 Slide 2: Project Overview
Analysis of historical earthquake data (2150 BC – 2019 AD)
Understand seismic activity patterns
Convert raw data into meaningful insights
🎯 Slide 3: Objectives
Analyze earthquake frequency over time
Identify high-risk regions
Study magnitude & depth relationships
Support disaster preparedness
📂 Slide 4: Dataset
Source: NOAA
Features:
Date & Time
Latitude & Longitude
Magnitude
Depth
Location
⚙️ Slide 5: Tools Used
Python
Pandas, NumPy
Matplotlib, Seaborn
Jupyter Notebook
MySQL (optional)
🔹 Slide 6: Data Preprocessing
Removed missing values
Converted date format
Filtered invalid data
Handled outliers
🔍 Slide 7: Exploratory Data Analysis
Year-wise earthquake trends
Region-wise frequency
Magnitude distribution
Depth vs magnitude
📊 Slide 8: Visualization
Line chart → Trend over time
Histogram → Magnitude distribution
Scatter plot → Depth vs Magnitude
Heatmap → Correlation
📈 Slide 9: Key Insights
Earthquakes occur in tectonic zones
High magnitude = rare but impactful
Increase due to better detection
Depth affects damage
💾 Slide 10: Database (Optional)
Stored data in MySQL
Used SQLAlchemy
Enables scalable analysis
🚀 Slide 11: Real-World Impact
Identifies high-risk zones
Supports disaster management
Helps governments & researchers
🔮 Slide 12: Future Scope
Machine learning prediction
Real-time data
Dashboards
Alert systems
📜 Slide 13: Conclusion
Data analytics helps understand earthquakes
Improves preparedness and decision-making
🙏 Slide 14: Thank You
Questions?
