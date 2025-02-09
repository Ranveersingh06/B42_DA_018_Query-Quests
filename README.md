# B42_DA_018_Query-Quests

Mobile User Data Analysis Dashboard
Overview
This project analyzes user behavior and mobile data usage patterns to uncover trends, insights, and actionable recommendations. The analysis utilizes a combination of Power BI dashboards and exploratory data analysis in Python to present data-driven insights effectively.
________________________________________
Components
1. Power BI Dashboard
•	File: Mobile_User_Data_Analysis.pbix
•	Provides an interactive dashboard with key visualizations on user behavior and mobile usage.
•	Highlights: 
o	Key metrics such as average app usage time, data consumption, and battery efficiency.
o	Comparative analysis by device type, operating system, and user demographics.
o	Interactive filters for deeper exploration of specific user segments.
2. Exploratory Data Analysis (EDA)
•	File: User_data_EDA.ipynb
•	Python-based notebook for detailed analysis of the dataset.
•	Includes: 
o	Data cleaning and preprocessing steps.
o	Visualization of key patterns and distributions.
o	Statistical summaries of user behavior metrics.
3. User Behavior Dataset
•	File: User_behaviour.csv
•	Contains the raw data used for analysis.
•	Key Columns: 
o	User ID: Unique identifier for users.
o	Device Model, Operating System: User device information.
o	App Usage Time (min/day), Data Usage (MB/day): Behavioral metrics.
o	Battery Drain (mAh/day), Screen On Time (hours/day): Device performance metrics.
o	Age, Gender, User Behavior Class: Demographics and classifications.
________________________________________
Features
Power BI Dashboard
•	KPI Highlights: 
o	Average app usage time per user.
o	Daily data usage trends.
o	Device efficiency metrics.
•	Visualizations: 
o	Bar charts for user demographics.
o	Line charts for time series trends.
o	Pie charts for device distribution.
•	Interactive Slicers: 
o	Filter by operating system, device model, and user demographics.
EDA Insights
•	Correlations: 
o	Relationships between app usage, data consumption, and device performance.
•	Clustering: 
o	Identification of user segments based on behavior metrics.
•	Anomalies: 
o	Detection of outliers in battery usage and data consumption.
________________________________________
Python to MySQL Connection
This project also includes a Python script to connect to a MySQL database using Pandas. This allows for seamless data transfer and storage.

Code Snippet:


import pandas as pd
import mysql.connector

# Establish connection
connection = mysql.connector.connect(
    host='your_host',
    user='your_username',
    password='your_password',
    database='your_database'
)

# Load data into Pandas DataFrame
data = pd.read_csv('User_behaviour.csv')

# Insert data into MySQL table
data.to_sql('user_behavior', con=connection, if_exists='replace', index=False)

# Close connection
connection.close()

 

Benefits:
•	Enables centralized data storage.
•	Facilitates further analysis and integration with other tools.
________________________________________
How to Use
1.	Power BI Dashboard: 
o	Open the Mobile_User_Data_Analysis.pbix file in Power BI Desktop.
o	Interact with filters to customize the view.
2.	EDA Notebook: 
o	Open User_data_EDA.ipynb in Jupyter Notebook or a compatible IDE.
o	Run the notebook cells to replicate the analysis.
3.	Dataset: 
o	Review User_behaviour.csv for raw data.
o	Use it as input for custom analyses or extensions.
4.	MySQL Integration: 
o	Use the provided Python script to transfer data to a MySQL database.
________________________________________
Benefits
•	Understand user behavior patterns and optimize app performance.
•	Identify high and low-efficiency devices.
•	Discover trends in data usage for better infrastructure planning.
________________________________________
Technical Requirements
•	Power BI Desktop
•	Python 3.x (with libraries: Pandas, Matplotlib, Seaborn, mysql-connector-python)
•	A text editor or IDE for CSV and JSON files.
________________________________________
Future Enhancements
•	Real-time dashboard integration.
•	Advanced predictive models for user behavior forecasting.
•	Comprehensive device performance benchmarking.
________________________________________
Support
For queries or issues, please contact:
•	Email: support@mobileanalytics.com
•	Phone: +1-800-555-0199

