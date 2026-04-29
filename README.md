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
