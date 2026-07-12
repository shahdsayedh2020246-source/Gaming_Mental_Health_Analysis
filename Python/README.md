# 🐍 Advanced Python Data Science & Streamlit Analytics Workspace

This directory houses the core Python engineering, predictive analytics, and interactive web application artifacts for the **Gaming & Mental Health Project**. It showcases a complete data science workflow—ranging from programmatic Exploratory Data Analysis (EDA) in Jupyter Notebooks to a live, production-ready dashboard built using Streamlit and Plotly.

---

## 🛠️ Python Tech Stack & Libraries
* **Data Manipulation:** `Pandas`, `NumPy`
* **Data Visualization:** `Plotly Express`, `Seaborn`, `Matplotlib`
* **Web Application Framework:** `Streamlit`
* **Statistical Analysis:** `Scikit-Learn` / `SciPy` (for correlation and feature tracking)

---

## 📐 Relational Database Schema Design
To replicate scalable data warehouse environments, the flat dataset was systematically programmatically separated into an optimized **Star Schema** architectural design consisting of distinct dimensions joined to a centralized transaction fact table.

### 🗺️ Data Model Schema Diagram
<img src="Python Schema.png" alt="Python Star Schema Design" width="100%">

---

## 🖥️ Streamlit Web App & Interactive Viewports

The Python application leverages **Streamlit** for the frontend UI and **Plotly Express** for responsive, modern dark-themed neon charts. The web app is structured into three synchronized analytical viewports:

### 1️⃣ Viewport A: Player Profile & Financial Matrix
*Programmatically parses general user demographics, total revenue footprints across game genres, and engagement counts.*

<img src="Player Dashboard Python.png" alt="Python Player Dashboard" width="100%">

#### 🔍 Granular Insights:
* **The Revenue Engines:** Strategy, MOBA, and MMO genres represent the primary financial drivers, with each cracking **1.1M in total transaction volume**, while RPG titles hold strong at **999.5K**.
* **Daily Engagement:** Total captured playtime stands at **6.2K collective daily hours**, heavily anchored across an evenly distributed age demographic where Young Adults marginally lead at 35%.

---

### 2️⃣ Viewport B: Psychological Strain & Addiction Behavioral Analytics
*Maps the behavioral regressions between explicit gaming addiction classifications and critical mental health triggers.*

<img src="Addiction Dashboard Python.png" alt="Python Addiction Dashboard" width="100%">

#### 🔍 Granular Insights:
* **The Escapism Phenomenon:** There is an empirical ceiling where negative mood states like **Anxiety, Irritability, and Depression** drive daily playtime to its maximum value (**7 hours average**), demonstrating a heavy reliance on video games as emotional coping mechanisms.
* **Social Decay Quantification:** The application captures a steep drop-off in face-to-face (F2F) weekly social interaction hours as players transition into High and Severe addiction categories, simultaneously driving up their computed social isolation indexes.

---

### 3️⃣ Viewport C: Ergonomics, Sleep Architecture & Physical Strain
*Evaluates systemic biological impacts, tracking postural risks across platforms and sleep disruption indexes.*

<img src="Health Dashboard Python.png" alt="Python Health Dashboard" width="100%">

#### 🔍 Granular Insights:
* **Sleep Squeeze:** Average sleep duration is restricted to **6 hours**, running almost identical to the average daily gaming duration (**6.15 hours**). Sleep quality tracking indicates a dominant distribution of "Insomnia" and "Poor" flags among heavy active users.
* **Biomechanical Risk:** A staggering **43% of the cohort registers at High Risk for Physical Pain** (specifically back and neck strain). Grouped distribution analysis confirms that **PC and Mobile platform users** report significantly higher rates of physical pain compared to traditional console setups due to static ergonomic positioning.

---

## 📂 Directory Contents & Execution
* **`Final_Project_Python.ipynb`**: The foundational Jupyter Notebook containing data preprocessing, outlier extraction, programmatic cleaning pipelines, and exploratory visualizations.
* **`dashboard.py`**: The production script containing the native Streamlit application structure, interactive Plotly layout themes, and dynamic cross-filtering queries.
* **`Gaming and Mental Health.csv`**: The fully cleaned tabular master dataset feeding the application.
* **`Python Schema.png`**: Database structural relational blueprint.
* **`Player Dashboard Python.png`**, **`Addiction Dashboard Python.png`**, **`Health Dashboard Python.png`**: High-resolution interface captures of the working web application.

---

## 🚀 How to Run the Live App Locally

To spin up the dynamic dashboard on your local machine, follow these steps:

1. **Install required dependencies:**
   ```bash
   pip install streamlit pandas numpy plotly
