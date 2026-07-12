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
