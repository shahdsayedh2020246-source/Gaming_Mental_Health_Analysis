# 🎮 Gaming & Mental Health: End-to-End Data Analysis

An end-to-end data analysis project exploring the impact of gaming habits on players' mental and physical health. This project features comprehensive exploratory data analysis (EDA), predictive modeling, a structured relational Star Schema database architecture, and a dynamic interactive Excel Dashboard.

---

## 👥 The Team: The Outliers
* **Members:** Mohamed Bedier, Belal Elkhamisy, Shahd Mohamed, Youssef Talaat, Ebrahim Elnemr
* **Supervised by:** Dr. Amal Mahmoud

---

## 📌 Project Overview
The gaming industry has grown exponentially, making it crucial to understand how gaming behaviors correlate with lifestyle, productivity, academic performance, and psychological well-being. This project analyzes player data to uncover key insights regarding gaming addiction risks, physical strain, social life impacts, and financial habits across different demographics.

### 🛠️ Tech Stack & Tools Used
* **Data Cleaning & ETL:** Power Query / Python (Pandas)
* **Database Design & Modeling:** SQL / Star Schema Relational Data Model
* **Data Visualization & Analytics:** Microsoft Excel (Advanced Dynamic Dashboards)

---

## 📐 Database Architecture & Data Modeling
To optimize analytical performance and maintain data integrity, a clean **Star Schema** was built. The architecture isolates descriptive attributes into structured Dimension tables linked directly to a central Fact table using validated foreign keys.

### 🗺️ Data Model Schema
![Star Schema Design](excel/Excel_Schema.png)

---

## 📊 Interactive Analytics Dashboards
The final analytical insights are presented through a fully interactive, multi-view dynamic Excel Dashboard designed with a modern futuristic dark/neon UI. 

### 1️⃣ Player Profile Dashboard
Focuses on general demographics, total player distribution, playtime across different platforms, financial spending by game genres, and productivity scores.
![Player Dashboard](excel/Excel_Dashboard_1.jpg)

### 2️⃣ Addiction Risk & Mental Health Dashboard
Analyzes the deep correlations between gaming addiction levels (Severe, High, Moderate, Low), social isolation scores, face-to-face social hours, and how different emotional/mood states affect overall gaming time.
![Addiction Dashboard](excel/Excel_Dashboard_2.jpg)

### 3️⃣ Healthcare & Physical Well-being Dashboard
Tracks physical health indicators including sleep quality against sleep hours, physical pain metrics (such as back and neck strain across platforms), and the relationship between physical exercise and mood stability.
![Healthcare Dashboard](excel/Excel_Dashboard_3.jpg)

---

## 🔑 Key Insights & Findings
* **Addiction & Social Life:** Higher gaming addiction risks strongly correlate with increased social isolation scores and a significant drop in face-to-face social hours weekly.
* **Physical Health Impact:** Mobile and PC players report varying degrees of physical discomfort, with higher daily gaming hours showing direct links to increased physical pain risks and sleep disruptions.
* **Productivity:** A distinct pattern emerges when comparing daily gaming hours against work/academic productivity scores, highlighting the sweet spot for balanced gaming versus over-indulgence.

---

## 📂 Project Structure
```text
├── excel/
│   ├── Excel Final.xlsx             # Main Excel Workbook with Data Model & Dashboards
│   ├── Excel_Schema.png             # Star Schema Diagram
│   ├── Excel_Dashboard_1.jpg        # Player Dashboard Screenshot
│   ├── Excel_Dashboard_2.jpg        # Addiction Dashboard Screenshot
│   └── Excel_Dashboard_3.jpg        # Healthcare Dashboard Screenshot
├── notebooks/
│   └── Gaming_Mental_Health_Analysis_python.ipynb   # Python Notebook for EDA & Modeling
└── README.md                        # Project Documentation
