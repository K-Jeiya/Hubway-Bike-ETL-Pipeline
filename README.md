# 🚴‍♀️ Hubway Bike Data ETL Pipeline (PySpark + MongoDB)

An end-to-end **data engineering pipeline** built using **PySpark** to analyze and transform the **Hubway Bike Sharing Dataset**.  
The project performs data extraction, transformation, aggregation, and storage in MongoDB for analytical use.

---

## 🧾 Project Overview

This project replicates a real-world data engineering workflow using PySpark and MongoDB.  
It was developed as part of a graded assignment to demonstrate ETL (Extract, Transform, Load) skills.

### 📊 Dataset Overview
- **Trips Table:** Contains trip duration, start/end station, subscriber type, and user ZIP code.  
- **Stations Table:** Includes station names, coordinates, and landmarks.  
- **Zip Code Mapping:** Used to extract and join customer state information.

---

## ⚙️ ETL Pipeline Steps

### Step 1: Data Preparation
- Load CSV data into Spark DataFrames for Trips and Stations.  

### Step 2: Data Transformation
- Join trips and stations twice — for start and end landmarks.  
- Extract **State** using Zip Code Mapping.  
- Derive **Month_Year** from trip start date.  
- Select only relevant columns.  

### Step 3: Data Aggregation
Grouped by:

Metrics calculated:
- `Number_of_Trips` → count of unique trip IDs  
- `Duration_Total_Minutes` → total duration (sum of seconds ÷ 60)

### Step 4: Data Storage
- Load final DataFrame into MongoDB.  
- **Database:** `Hubway`  
- **Collection:** `Trips_transformed`

---

## 🧠 Tech Stack

| Component | Description |
|------------|-------------|
| **Framework** | Apache Spark (PySpark) |
| **Database** | MongoDB |
| **Language** | Python |
| **Environment** | Jupyter / Colab Notebook |
| **Data Processing** | DataFrames, Joins, Aggregations |

---

## 🧾 Example Output

✅ Aggregated dataset saved successfully to MongoDB  
✅ Includes calculated trip counts and total duration per state/month  
✅ Verified via MongoDB Compass screenshot

---

## 👩‍💻 Developer
**Jeiya Kumari**  
📍 Karachi, Pakistan  
📧 [jeiyakumari@gmail.com](mailto:jeiyakumari@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/jeiyakumari/)  
🔗 [Portfolio](https://k-jeiya.github.io/Jeiya-Portfolio/)

---

## 🏷️ Tags
`#PySpark` `#MongoDB` `#ETL` `#DataEngineering` `#BigData` `#JeiyaKumari`
