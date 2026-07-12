# 🗄️ Gaming & Mental Health — Relational Database, Modeling & Analysis

## 📌 Section Overview
This section contains the comprehensive **SQL Infrastructure** developed for the Gaming and Mental Health project. The process covers the entire backend lifecycle: from raw data ingestion and data cleaning, through advanced feature engineering, to restructuring a flat dataset into an optimized, high-performance **Star Schema (1 Fact Table & 6 Dimension Tables)**. Finally, deep business analysis and behavioral insights were extracted using advanced SQL functionalities.

---

## 📐 Data Modeling & Architecture (ERD)

To eliminate data redundancy and optimize analytical query execution times, the dataset was normalized into a scalable relational model. 

### 🗺️ Entity-Relationship Diagram (ERD)
![ERD Diagram](ERD%20Diagram.png)

### 🧩 Schema Design Details:
* **Fact Table:** `Fact_Gaming_Mental_Health` (Contains all descriptive metrics, KPIs, and maps out surrogate keys connecting to all surrounding lookups).
* **Dimension Tables:**
  * `Dim_Player`: Tracks dynamic player demographics (`age`, `gender`, `Age_Group`, `Educational_State`).
  * `Dim_Platform`: Normalizes client gaming environments.
  * `Dim_Game`: Contains structural metadata for genres and specific titles.
  * `Dim_Sleep`: Stores sleep quality markers, distribution brackets, and disruption logs.
  * `Dim_Addiction`: Isolates psychological symptoms and maps custom behavioral risk tiers.
  * `Dim_PhysicalStatus`: Isolates systemic occupational hazards (e.g., eye strain, musculoskeletal pain attributes).

---

## 🛠️ SQL Script Directory Breakdown

The analytical workflow inside this directory is organized into sequential scripts:

### 🧼 1. Database Setup & Structural Cleaning (`01_database_setup_and_cleaning.sql`)
* Focuses on physical table adjustments and environment configuration.
* Handles data type alignment and enforces operational constraints.
* Neutralizes blank entries (`''`) converted dynamically into strict relational `NULL` values for non-applicable criteria (e.g., student GPAs for full-time workers).
* Runs comprehensive validation sweeps ensuring absolute structural integrity across all records (`record_id`).

### ⚙️ 2. Advanced Feature Engineering (`02_feature_engineering.sql`)
* Implements robust conditional categorization models using specialized threshold distributions:
  * **Outlier-Aware Discretization:** Leverages session variables (`@avg_spent`, `@std_spent`) to compute dynamic standard deviation offsets for spending and game-time profiles rather than rigid static intervals.
  * **Behavioral Buckets:** Encodes calculated classifications for `sleep_states`, `Physical_Pain` thresholds, and educational tracking matrices (`Student`, `Worker`, `Working_Student`).

### 🏗️ 3. Star Schema Ingestion (`03_data_modeling.sql`)
* Houses structural DDL statements deployed with fully configured transactional rules (`ON UPDATE CASCADE`, `ON DELETE SET NULL`).
* Orchestrates target lookups populating surrogate auto-increment identifiers.
* Executes the final data pipeline loading data into the central Fact table using high-efficiency analytical `LEFT JOIN` maps.

### 🔎 4. Exploratory & Metric Queries (`04_exploratory_data_analysis.sql` & `05_kpis_and_metrics.sql`)
* Contains strategic queries computing operational performance baselines (e.g., precise demographic breakdowns, average financial indices, precise health and physical risk ratios).

### 🎯 5. Business Insight Resolutions (`06_answering_business_questions.sql`)
* Synthesizes complex answers using core advanced concepts such as **Window Functions**, Subqueries, and **Common Table Expressions (CTEs)** to unlock hidden behavioral insights.

---

## 💡 Key Analytical Findings Derived via SQL

* ⏳ **The Performance Tax:** A stark, near-linear inverse relationship was proven between continuous screen exposure and performance metrics; individuals categorized with a **'Failing'** academic status logged an average of **8.52 daily gaming hours**, more than double that of **'Excellent'** performers (**3.94 hours**).
* 🧠 **Addiction Correlates:** Elevated addiction risk metrics directly map severe real-world social impacts. **Severe Risk** profiles demonstrated an average isolation score of **6.5**, with real-world social contact plunging down to a mere **3.2 hours weekly**.
* 🩺 **Physical Symptom Scaling:** Gamers classified in the severe **'High Risk'** physical pain category averaged **8.3 daily gaming hours**, proving a sharp escalating physical cost as screen-time thresholds cross average boundaries.
