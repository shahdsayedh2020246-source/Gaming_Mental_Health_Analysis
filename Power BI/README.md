# 📊 Power BI Interactive Analytics & Hybrid Python Workspace

This directory contains the production-grade **Power BI (.pbix)** dashboard architecture for the **Gaming & Mental Health Project**. The solution transitions complex behavior metrics into an executive-facing interactive business intelligence suite, featuring custom dark-themed UI navigation, complex DAX measures, and **hybrid Python integration for advanced native tooltips**.

---

## 🛠️ Tech Stack & Advanced Features
* **Data Modeling:** Power BI Data Model (Star Schema) with optimized 1:N relationships.
* **ETL & Data Transformation:** Power Query for datatype correction, conditional column profiling, and schema generation.
* **Expression Language:** **DAX (Data Analysis Expressions)** for calculated metrics, tracking scores, and dynamic aggregations.
* **Python Scripting Integration:** Native Power BI Python Visuals used to programmatically render advanced **Custom Tooltips** using `Matplotlib` and `Pandas`.
* **UI/UX Design:** Custom interactive sidebar navigation, neon dark-theme aesthetics, and intuitive visual grouping.

---

## 🐍 Advanced Hybrid Feature: Python-Engineered Tooltips
Rather than relying solely on standard Power BI native charts, this project injects programmatic Python visualization scripts directly into the **Report Page Tooltips**. When hovering over data points, the Power BI context filters the underlying dataset, and a native Python engine dynamically renders specialized statistical distribution charts:

### 1️⃣ Tooltip Page 1: Addiction Risk Distribution (Pie Matrix)
Programmatically aggregates data to showcase the exact percentage slice of user dependency on hover using custom hex styling matching the global neon theme.
```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)
# dataset = dataset.drop_duplicates()

import matplotlib.pyplot as plt
import pandas as pd

plt.figure(figsize=(5,5))
dataset.groupby('gaming_addiction_risk_level')['record_id'].count().plot(
    kind='pie',
    autopct='%1.1f%%',
    colors=['#2ec4b6', '#ffbf69', '#e94560', '#a475fa'],
    textprops={"fontsize": 20}
)
plt.title('Addiction Risk Distribution', fontsize=24)
plt.ylabel('')
plt.show()
2️⃣ Tooltip Page 2: Demographic Gender Distribution (Bar Matrix)
Generates high-resolution categorical breakdowns across dynamic demographic segments directly within the tooltips to enrich user hover discovery.
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)
# dataset = dataset.drop_duplicates()

import matplotlib.pyplot as plt

plt.figure(figsize=(6, 5))

# Group by gender and count the records
dataset.groupby("gender")["record_id"].count().plot(
    kind="bar",
    color=["#ff5266", "#4a37fa", "#b3b2b8"], 
    rot=0, 
    fontsize=16,  
)

# Customize title and axis labels
plt.title("Distribution by Gender", fontsize=20) 
plt.xlabel("", fontsize=14) 
plt.ylabel("", fontsize=14) 

plt.tight_layout()  
plt.show()
🖥️ Executive Dashboards & Core Analytical Viewports
1️⃣ Viewport A: Player Profile & Financial Matrix
An overview of cohort demographics, global gaming volume, and comprehensive financial footprint analysis across various game genres.

🔍 Key Visual Data Points & Insights:
The High-Level Overview: Total population stands at 1K Players, driving a massive financial market of $7M in Total Spending, with an aggregate 6.15K Total Gaming Hours.

Financial Drivers by Genre: MMO titles lead the market at $1.15M, followed closely by Strategy ($1.12M) and MOBA ($1.11M). Mobile games represent the lowest spending tier at $0.85M.

Demographics & Distribution: Gender distribution is remarkably uniform (35% Female, 34% Teenager, 33% Male/Other). Age group segmentation shows balanced distribution across Young Adults (35%), Teenagers (34%), and Adults (31%).

2️⃣ Viewport B: Psychological Strain & Addiction Behavioral Analytics
Investigates behavioral anomalies, evaluating addiction density across platforms and the emotional cost of dynamic spending habits.

🔍 Key Visual Data Points & Insights:
Escapism & Emotional Triggers: A direct correlation is visible between emotional strain and financial spending. Negative mood states like Anxiety (10.2K) and Irritability (9.8K) heavily dominate active user spending compared to positive emotional states like Excitement (3.1K).

Addiction Segmentation by Platform: Severe/High Addiction levels are heavily prevalent on PC and Console setups.

Financial Concentration: Players classified within the Severe (38%) and High (20%) addiction parameters combined represent over half of the entire financial ecosystem's monetary flow.

The Social/Productivity Trade-Off: Average Work Productivity drops to a baseline of 5.39, while the cohort retains an Average Face-to-Face (F2F) Socialization score of 7.65 hours against an Average ISO (Isolation) Score of 3.87.

3️⃣ Viewport C: Health Architecture, Sleep & Physical Strain Metrics
Correlates hours of screen immersion against biological impacts, sleep quality deterioration, and musculoskeletal pain indicators.

🔍 Key Visual Data Points & Insights:
The Sleep Quality Squeeze: Average Sleep Duration is compressed to 5.74 Hours (juxtaposed against 6.15 average gaming hours). A linear decay is visualized where "Good" sleep stands at 6.8 hours, dropping drastically to 4.7 hours for users suffering from severe Insomnia.

Biomechanical Risk Distribution: A staggering 43% of the total cohort is flagged as High Risk for Physical Pain, with another 37% at Moderate Risk. Only 20% report a complete absence of pain (No Risk).

Active Balancing: Despite heavy gaming hours, the tracked cohort manages an Average Exercise metric of 6.95 hours, showing a downward regression curve as severe mental states shift from Excited/Normal down to Restless and Anxious.

📂 Repository Structural Contents
Gaming_and_Mental_Health_Analytics.pbix: The master Power BI Desktop application file containing full data models, visual canvases, custom DAX calculations, and integrated Python Tooltip pages.

Player Dashboard Power BI.jpg: Performance snapshot of the general cohort demographics interface.

Addiction Dashboard Power BI.jpg: Performance snapshot of the behavioral and spending regression analysis interface.

Health Dashboard Power BI.jpg: Performance snapshot of the physical strain, sleep metrics, and ergonomic impact interface.

🚀 How to Interact with the Desktop File
Download the .pbix file from this directory.

Ensure you have the latest version of Power BI Desktop installed.

Python Environment Setup: To enable the custom tooltips, make sure your Power BI Options point to your local Python installation with pandas and matplotlib installed (pip install pandas matplotlib).

Open the file to explore interactive cross-filtering, dynamic slicers, and custom tooltips.
