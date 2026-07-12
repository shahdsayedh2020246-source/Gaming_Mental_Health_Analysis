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
<img src="excel/Excel Schema.png" alt="Star Schema Design" width="100%">

---

## 📊 Interactive Analytics Dashboards & Deep Insights

The analytical insights are presented through a fully interactive, multi-view dynamic Excel Dashboard designed with a modern futuristic dark/neon UI. Below is the detailed breakdown of each view:

### 1️⃣ Player Profile Dashboard
*Focuses on general demographics, total player distribution, playtime across different games, financial spending, and productivity scores.*

<img src="excel/Excel Dashboard 1.png" alt="Player Dashboard" width="100%">

#### 🔍 Deep Insights & Analytics:
* **Demographics & Volume:** The dataset tracks **1.0k total players** who collectively account for **6.2k daily gaming hours** and a massive total expenditure of **7.2m** across platforms. The gender split shows a heavy male dominance at **66%**, compared to **32% female** players.
* **Age & Engagement:** The distribution of gaming time by age group is tightly balanced, with **Young Adults leading at 35%**, followed closely by **Teenagers (34%)** and **Adults (31%)**.
* **Game Popularity by Hours:** *Elden Ring* commands the highest engagement with **369 total hours**, closely followed by *Starcraft II* (**355 hours**) and *Dota 2* (**332 hours**). Mobile titles like *Mobile Legends* and *Fortnite* occupy the lower tier of total hours within this specific cohort.
* **Financial Spending:** Monetization is highly successful in the **Strategy, MOBA, and MMO genres**, with each pulling in **1.1m** in total spending, while Role-Playing Games (RPGs) follow at **999.5k**.

---

### 2️⃣ Addiction Risk & Mental Health Dashboard
*Analyzes the deep correlations between gaming addiction levels, social isolation, and emotional stability.*

<img src="excel/Excel Dashboard 2.png" alt="Addiction Dashboard" width="100%">

#### 🔍 Deep Insights & Analytics:
* **Addiction Levels by Age:** The **Young Adult** segment exhibits the highest vulnerability to psychological strain, recording **312 players categorized with Low-to-Moderate addiction risks** and a noticeable surge in severe cases compared to Older Adults. Teenagers follow as the second most vulnerable group.
* **Social Impact (F2F vs. Isolation):** There is a clear, quantifiable inverse relationship between face-to-face (F2F) social interaction and gaming intensity. On average, the cohort retains **7.7 F2F social hours** against a **3.9 social score**. However, as addiction risk scales from "Low" to "Severe", the average social isolation score spikes dramatically while actual F2F hours drop down.
* **Mood & Spending Behavior:** Financial expenditure acts as an emotional coping mechanism; total spending shows an upward trajectory, peaking significantly when players experience emotional states like **Anxious, Irritable, and Depressed**.
* **Emotional Gaming Triggers:** Negative emotional states directly prolong sessions. Players suffering from **Anxiety, Irritability, Restlessness, and Depression** average the maximum limit of **7 hours of gaming time**, using games as an escapism mechanism, whereas "Excited" or "Normal" states account for only **4 hours**.

---

### 3️⃣ Healthcare & Physical Well-being Dashboard
*Tracks physical health indicators including sleep quality, physical pain metrics, and lifestyle balances.*

<img src="excel/Excel Dashboard 3.png" alt="Healthcare Dashboard" width="100%">

#### 🔍 Deep Insights & Analytics:
* **Sleep Deprivation:** The average sleep duration across the entire player base sits at a restrictive **6 hours**, mirroring the average **6.15 daily gaming hours**. Sleep quality metrics reveal that a vast majority of heavy gamers report "Insomnia", "Poor", or "Very Poor" sleep cycles, with "Good" sleep being a minority.
* **Physical Strain & Ergonomics:** A staggering **43% of the analyzed population is at High Risk for Physical Pain** (specifically back and neck strain), with **37% at Moderate Risk**, leaving only 20% with No Risk. 
* **Platform Strain Comparison:** When evaluating physical discomfort by platform, **Mobile and PC platforms show the highest frequency of physical pain reporting (TRUE)**, exceeding Console and Multi-platform setups due to prolonged static postures and smaller screen focus.
* **The Exercise/Mood Correlation:** Physical activity acts as a major buffer; data mapping reveals that players with higher **weekly exercise hours (averaging up to 6.9 hours)** maintain significantly lower restlessness and anxiety levels, stabilizing their overall mood state.

---

## 📂 Project Structure
```text
├── excel/
│   ├── Excel Final.xlsx             # Main Excel Workbook with Data Model & Dashboards
│   ├── Excel Schema.png             # Star Schema Diagram
│   ├── Excel Dashboard 1.png        # Player Dashboard Screenshot
│   ├── Excel Dashboard 2.png        # Addiction Dashboard Screenshot
│   └── Excel Dashboard 3.png        # Healthcare Dashboard Screenshot
├── gaming_mental_health.csv         # Raw Dataset
├── Gaming_Mental_Health_A...        # Python Notebook for EDA & Modeling
└── README.md                        # Project Documentation
