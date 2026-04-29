🌍 Earthquake Project
📌 Project Overview
The Earthquake Project focuses on analyzing historical earthquake data to identify patterns, trends, and key insights related to seismic activities across the globe. The dataset includes earthquake records spanning several centuries.

🎯 Objectives
Analyze earthquake occurrences over time
Identify high-risk regions prone to earthquakes
Study magnitude and depth relationships
Visualize seismic patterns using graphs
Perform data cleaning and transformation
🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook
MySQL (for data storage)
Streamlit (for dashboard, optional)
📂 Project Structure
earthquake_project/ │ ├── data/ │ └── earthquake.csv │ ├── notebooks/ │ └── earthquake_analysis.ipynb │ ├── database/ │ └── earthquakes.sql │ ├── app.py │ └── README.md

🔄 Data Preprocessing
Removed missing/null values
Converted date columns to proper datetime format
Cleaned invalid magnitude values
Standardized location names
📊 Analysis Performed
Year-wise earthquake trend analysis
Country/region-wise earthquake frequency
Magnitude distribution study
Depth vs Magnitude relationship
📈 Visualizations
Line charts → Earthquake trends over time
Bar charts → Top affected regions
Scatter plots → Depth vs magnitude
Heatmaps → Correlation between variables
🔍 Key Insights
Most earthquakes occur in tectonically active zones
High magnitude earthquakes are rare but impactful
Increase in recorded earthquakes due to better technology
Depth influences damage severity
🚀 How to Run the Project
Clone the repository: git clone https://github.com/your-username/earthquake_project.git

Install dependencies: pip install pandas numpy matplotlib seaborn

Run Jupyter Notebook: jupyter notebook

(Optional) Run Streamlit app: streamlit run app.py

🔮 Future Enhancements
Real-time earthquake data integration
Machine learning prediction models
Interactive dashboards with filters
Alert system for high-risk zones
🤝 Contribution
Contributions are welcome! Feel free to fork and improve the project.

📜 License
This project is created for educational purposes.

🌍 Earthquake Project (Program-Based)
📌 Overview
This project performs Earthquake Data Analysis using Python. It focuses on cleaning, analyzing, and visualizing earthquake data to identify patterns in magnitude, depth, and occurrence over time.

🎯 Objectives
Load and preprocess earthquake dataset
Perform exploratory data analysis (EDA)
Visualize trends using graphs
Understand relationships between variables
(Optional) Store data in MySQL
🛠️ Technologies
Python
Pandas
NumPy
Matplotlib
Seaborn
SQLAlchemy (MySQL integration)
⚙️ Program Explanation
🔹 Step 1: Import Libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
🔹 Step 2: Load Dataset
df = pd.read_csv("earthquake.csv")
df.head()
👉 Loads the dataset into a DataFrame

🔹 Step 3: Data Preprocessing
df.dropna(inplace=True)
df['date'] = pd.to_datetime(df['date'])
df = df[df['mag'] > 0]
👉 Removes null values and cleans invalid data

🔹 Step 4: Feature Engineering
df['year'] = df['date'].dt.year
👉 Extracts year for trend analysis

🔹 Step 5: Year-wise Analysis
yearly = df['year'].value_counts().sort_index()
yearly.plot()
plt.title("Earthquake Trend")
plt.show()
👉 Shows how earthquakes change over time

🔹 Step 6: Magnitude Distribution
sns.histplot(df['mag'], bins=30)
plt.title("Magnitude Distribution")
plt.show()
👉 Displays frequency of earthquake magnitudes

🔹 Step 7: Depth vs Magnitude
plt.scatter(df['depth_km'], df['mag'])
plt.xlabel("Depth")
plt.ylabel("Magnitude")
plt.show()
👉 Shows relationship between depth and intensity

🔹 Step 8: Database Storage (Optional)
from sqlalchemy import create_engine
engine = create_engine("mysql+pymysql://root:password@localhost/earthquake_project")
df.to_sql("earthquakes", con=engine, if_exists="replace", index=False)
📊 Output
Line Graph → Earthquake trend
Histogram → Magnitude distribution
Scatter Plot → Depth vs Magnitude
🔍 Key Insights
Earthquakes occur frequently in specific regions
Large earthquakes are rare
Increase in data over time due to better technology
Depth affects earthquake impact
🚀 How to Run
pip install pandas numpy matplotlib seaborn sqlalchemy pymysql
jupyter notebook
🔮 Future Scope
Machine learning prediction
Real-time dashboard
Alert systems
📜 License
Educational use only
