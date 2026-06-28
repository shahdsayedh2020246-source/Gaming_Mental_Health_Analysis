# 🎮 Gaming & Mental Health Data Analysis

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Engineering-orange?style=for-the-badge&logo=pandas" alt="Pandas">
  <img src="https://img.shields.io/badge/Database-Star%20Schema-green?style=for-the-badge" alt="Star Schema">
</p>

## 👥 The Team: The Outliers
* **Members:** Mohamed Bedier, Belal Elkhamisy, Shahd Mohamed, Youssef Talaat, Ebrahim Elnemr
* **Supervised by:** 💌 Dr. Amal Mahmoud 💌

---

## 📌 1. Project Introduction
This project performs an advanced data analysis lifecycle on a comprehensive dataset mapping the intersection between video gaming habits and human psychological, behavioral, and physical well-being. The core mission is to unveil empirical evidence on how intensive gaming correlates with physical strain, sleep architecture, academic/professional productivity, and potential addiction risks.

---

## 📊 2. Dataset Overview & Star Schema Architecture
To optimize the data for business intelligence and efficient querying, the flat dataset was re-engineered into an optimized **Star Schema Relational Database Engine**.

### 🔲 Central Fact Table
* **`Fact_Gaming_Mental_Health`**: Holds quantitative metrics (`Daily_Gaming_Hours`, `Sleep_Hours`, `GPA_or_Productivity_Score`, `Financial_Loss_Risk`) linked via foreign keys to the surrounding dimension tables.

### 📐 Dimension Tables
1. **`Dim_Platform`**: Contains device specs, online features, and primary controller setups.
2. **`Dim_Game`**: Holds detailed game genres, release studios, monetization structures, and core gameplay types.
3. **`Dim_Player`**: Encompasses demographic clusters (Age, Gender, Region, Employment Status).
4. **`Dim_Sleep`**: Tracks sleep hygiene, bedtime stability, latency, and sleep quality indexes.
5. **`Dim_Addiction`**: Maps behavioral traits (Compulsive engagement, escapism triggers, social withdrawal scores).
6. **`Dim_PhysicalStatus`**: Logs physical side-effects (Repetitive strain injuries, optical strain, posture scores).

---

## 🛠️ 3. Pipeline & Data Engineering Code
Below is the core technical pipeline implemented to process the data, handle missing values, and construct the Star Schema database structure:

```python
import pandas as pd
import numpy as np

# 1. Load Dataset
df = pd.read_csv('Gaming & Mental_Health.csv')

# 2. Advanced Data Cleaning & Imputation Pipeline
def clean_gaming_data(data):
    cleaned_df = data.copy()
    
    # Handle missing numeric values with Median to prevent outlier distortion
    numeric_cols = cleaned_df.select_dtypes(include=[np.number]).columns
    for col in numeric_cols:
        cleaned_df[col] = cleaned_df[col].fillna(cleaned_df[col].median())
        
    # Handle categorical missing fields with Mode
    categorical_cols = cleaned_df.select_dtypes(include=['object']).columns
    for col in categorical_cols:
        cleaned_df[col] = cleaned_df[col].fillna(cleaned_df[col].mode()[0])
        
    return cleaned_df

processed_df = clean_gaming_data(df)

# 3. Generating Unique Dimensional Primary Keys
processed_df['Player_ID'] = range(1, len(processed_df) + 1)
processed_df['Game_ID'] = range(101, 101 + len(processed_df))
processed_df['Platform_ID'] = range(501, 501 + len(processed_df))

# Example of Extracting Dimension Tables
dim_player = processed_df[['Player_ID', 'Age', 'Gender', 'Region', 'Employment_Status']].drop_duplicates()
dim_game = processed_df[['Game_ID', 'Game_Genre', 'Game_Name', 'Monetization']].drop_duplicates()

print("✅ Data Pipeline Executed: Star Schema generated successfully.")
📈 4. Explanatory Data Analysis (EDA) Highlights
The analytical framework covers critical behavioral patterns extracted from the dataset:

🔍 Key Analysis Sections:
Correlation Metrics: Investigating how Daily_Gaming_Hours directly impacts Sleep_Hours and Productivity.

Addiction Triggers: Analyzing structural monetization setups (e.g., microtransactions) against the Financial_Loss_Risk.

Academic/Professional Impact: Evaluating the variance in GPA between casual gamers (<2 hours) vs. hardcore gamers (>6 hours).
# Sample Analysis Code snippet for Data Insights
correlation_matrix = processed_df[['Daily_Gaming_Hours', 'Sleep_Hours', 'Productivity_Score']].corr()
print("Correlation Insights:\n", correlation_matrix)
💡 5. Data-Driven Strategic Recommendations
Based on the empirical insights derived from the models, the following actionable strategies are proposed:

🚀 Implement Context-Aware Gaming Boundaries Gamers showing escalating signs of escapism should utilize automated application blockers during peak productivity hours to protect academic performance.

💤 Adopt Sleep Hygiene & Ergonomic Break Protocols Enforce a strict "No-Screen Buffer Hour" before bedtime to ensure better sleep quality, alongside practicing the 20-20-20 rule during active gaming sessions.

🤝 Foster Offline Social Integration Universities and local communities should create hybrid or physical social clubs that align with esports interests, directly helping high-risk gamers convert online screen time into real-world connections.

💳 Establish Automated Micro-transaction Caps Players experiencing high impulse spending should set up automated boundaries directly inside their banking or payment applications to avoid financial stress.

⚙️ How to Run the Project Local
1- Clone the repository:
git clone [https://github.com/YOUR_USERNAME/Gaming_Mental_Health_Analysis_python.git](https://github.com/YOUR_USERNAME/Gaming_Mental_Health_Analysis_python.git)
2- Install dependencies:
pip install pandas numpy matplotlib seaborn sqlalchemy
3- Run the Jupyter Notebook or open it in Google Colab to see the full interactive execution.
