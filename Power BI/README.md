# 🎮 Gaming and Mental Health Analytics Dashboard (Power BI)

## 📌 Project Overview
This project presents a comprehensive, data-driven analysis of the relationship between **Gaming Habits and Mental/Physical Health**. Using Power BI, the project transforms complex behavioral data into three interactive dashboards (**Player Profile, Addiction Insights, and Health Impact**). 

The goal of this project is to uncover how gaming hours, financial spending, and different platforms correlate with mental states (such as anxiety, depression, and irritability), sleep quality, and physical pain.

---

## 📊 Dashboards Breakdown

### 1. 👤 Player Dashboard (Demographics & General Stats)
![Player Dashboard](Player%20Dashboard%20Power%20BI.jpg)

This tab focuses on understanding the player base, their spending habits, and general gaming behavior.
* **Key Metrics (KPIs):**
  * **Total Players:** 1K players in the dataset.
  * **Total Spent:** $7M across different game genres.
  * **Total Gaming Hours:** 6.15K hours accumulated.
  * **Avg Work Score:** 5.39.
* **Visualizations & Insights:**
  * **Who Plays More? (By Gender):** Equal distribution among genders (35% Other, 33% Male, 32% Female).
  * **Who Plays More? (By Age Group):** Evenly spread across Young Adults (35%), Teenagers (34%), and Adults (31%).
  * **Top 5 Games by Gaming Hours:** *Apex Legends* leads (7.2 hrs), followed closely by *Fortnite*, *Civilization VI*, *Final Fantasy*, and *Clash of Clans*.
  * **Sum of Total Spent by Game Genre:** MMO ($1.15M) and Strategy ($1.12M) are the highest revenue-generating genres.
  * **Gaming Hours vs. Work Score:** A scatter plot showing the distribution of work scores against the number of gaming hours.

---

### 2. 🧠 Addiction Dashboard (Mental Health & Behavioral Analysis)
![Addiction Dashboard](Addiction%20Dashboard%20Power%20BI.jpg)

This tab deep dives into gaming addiction levels (Severe, High, Moderate, Low) and their direct impact on work productivity and psychological well-being.
* **Key Metrics (KPIs):**
  * **Avg Work Productivity:** 5.39
  * **Total Gaming Hours:** 6.15K
  * **Avg F2F (Face-to-Face) Hours:** 7.65 hours of real-world social interaction.
  * **Avg ISO (Isolation) Score:** 3.87 (measuring social withdrawal).
* **Visualizations & Insights:**
  * **Daily Gaming Hours by Exercise Time:** Shows an inverse relationship; as gaming addiction/hours increase, physical exercise hours drastically drop.
  * **Addiction by Platform:** Breaks down addiction levels across Console, PC, Mobile, and Multi-platform. PC and Mobile show distinct spikes in *Low* to *Severe* classifications.
  * **Does Spending Affect Mood States?:** A clear trend showing that high-spending players experience elevated levels of **Anxiety (10.2K)**, **Irritability (9.8K)**, and **Depression (7.3K)**.
  * **Who Spends More? (By Addiction Level):** **Severe (38%)** and **High (20%)** addiction groups contribute to more than half of the total financial spending.

---

### 3. 🩺 Health Dashboard (Physical Health & Sleep Quality)
![Health Dashboard](Health%20Dashboard%20Power%20BI.jpg)

This tab analyzes how intensive gaming affects the physical body, sleep cycles, and general mood.
* **Key Metrics (KPIs):**
  * **Avg Exercise Hours:** 6.95 hrs
  * **Avg Gaming Hours:** 6.15 hrs
  * **Avg Sleep:** 5.74 hrs (below the healthy average).
  * **High Risk Physical Pain:** 24% of players suffer from severe physical pain.
* **Visualizations & Insights:**
  * **Mood State by Avg Exercise Hours:** Higher exercise hours strongly correlate with positive emotional states like *Excited* and *Normal*, while lower exercise hours relate to *Anxious* and *Restless* states.
  * **Average of Sleep Hours by Sleep Quality:** Validates that individuals reporting *Insomnia* or *Very Poor* sleep get less than 5 hours of sleep on average.
  * **Average Exercise Hours by Sleep State:** Identifies that 41% of the sample experiences *Over_Sleep*, while 27% suffers from *Poor* sleep states.
  * **Physical Pain Risk Distribution:** A critical pie chart showing that **43%** of players are at **High Risk** of physical pain, and 37% are at Moderate Risk.

---

## 🐍 Advanced Customization: Python Integration for Tooltips

To elevate the user experience and create deeply customized, dynamic tooltips that Power BI's default visuals don't natively support, **Python (Matplotlib & Pandas)** was integrated directly inside the Power BI report. 

These Python scripts are triggered dynamically as a **Tooltip** when hovering over data points to provide instant, advanced breakdowns.

### 📝 1. Gender Distribution Tooltip Script
This script generates a clean, custom-colored bar chart showing the breakdown of players by gender for any filtered data segment.

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)
# dataset = dataset.drop_duplicates()

import matplotlib.pyplot as plt

# Initialize figure size
plt.figure(figsize=(6, 5))

# Group by gender and count the records
dataset.groupby("gender")["record_id"].count().plot(
    kind="bar",
    color=["#ff5266", "#4a37fa", "#b3b2b8"], # Customized theme matching dashboard colors
    rot=0, 
    fontsize=16,  
)

# Customize title and axis labels
plt.title("Distribution by Gender", fontsize=20) 
plt.xlabel("", fontsize=14) 
plt.ylabel("", fontsize=14) 

plt.tight_layout()  
plt.show()

Conversation with Gemini
عايزاك تعملي ريدمي ل ده بالتفصيل gaming and mental health _ power BI و اشرحه و اكتب في النهايدة اني استخدمت اكواد بايثون في باور بي اي زي # The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script:



# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)

# dataset = dataset.drop_duplicates()



# Paste or type your script code here:

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

plt.show() زي ده # The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script:



# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)

# dataset = dataset.drop_duplicates()



# Paste or type your script code here:



import matplotlib.pyplot as plt

import pandas as pd



plt.figure(figsize=(5,5))

dataset.groupby('gaming_addiction_risk_level')['record_id'].count().plot(

    kind='pie',

    autopct='%1.1f%%',

    colors=['#2ec4b6', '#ffbf69', '#e94560', '#a475fa'],

    textprops={"fontsize": 20}

)

plt.title('Addiction Risk Distribution',fontsize= 24)

plt.ylabel('')

plt.show() و ده عشان اعمل تول تيب و اربطه بالداش بورد

إليك ملف README.md احترافي ومفصل بالكامل لمشروعك على GitHub، يغطي جميع لوحات التحكم (Dashboards) الثلاثة المرفقة، ويشرح البيانات والرسوم البيانية بدقة، بالإضافة إلى كتابة الجزء الخاص باستخدام أكواد بايثون (Python Scripts) لبناء الـ Tooltips المخصصة في Power BI داخل ملف الـ README.

📁 README.md
Markdown
# 🎮 Gaming and Mental Health Analytics Dashboard (Power BI)

## 📌 Project Overview
This project presents a comprehensive, data-driven analysis of the relationship between **Gaming Habits and Mental/Physical Health**. Using Power BI, the project transforms complex behavioral data into three interactive dashboards (**Player Profile, Addiction Insights, and Health Impact**). 

The goal of this project is to uncover how gaming hours, financial spending, and different platforms correlate with mental states (such as anxiety, depression, and irritability), sleep quality, and physical pain.

---

## 📊 Dashboards Breakdown

### 1. 👤 Player Dashboard (Demographics & General Stats)
This tab focuses on understanding the player base, their spending habits, and general gaming behavior.
* **Key Metrics (KPIs):**
  * **Total Players:** 1K players in the dataset.
  * **Total Spent:** $7M across different game genres.
  * **Total Gaming Hours:** 6.15K hours accumulated.
  * **Avg Work Score:** 5.39.
* **Visualizations & Insights:**
  * **Who Plays More? (By Gender):** Equal distribution among genders (35% Other, 33% Male, 32% Female).
  * **Who Plays More? (By Age Group):** Evenly spread across Young Adults (35%), Teenagers (34%), and Adults (31%).
  * **Top 5 Games by Gaming Hours:** *Apex Legends* leads (7.2 hrs), followed closely by *Fortnite*, *Civilization VI*, *Final Fantasy*, and *Clash of Clans*.
  * **Sum of Total Spent by Game Genre:** MMO ($1.15M) and Strategy ($1.12M) are the highest revenue-generating genres.
  * **Gaming Hours vs. Work Score:** A scatter plot showing the distribution of work scores against the number of gaming hours.

---

### 2. 🧠 Addiction Dashboard (Mental Health & Behavioral Analysis)
This tab deep dives into gaming addiction levels (Severe, High, Moderate, Low) and their direct impact on work productivity and psychological well-being.
* **Key Metrics (KPIs):**
  * **Avg Work Productivity:** 5.39
  * **Total Gaming Hours:** 6.15K
  * **Avg F2F (Face-to-Face) Hours:** 7.65 hours of real-world social interaction.
  * **Avg ISO (Isolation) Score:** 3.87 (measuring social withdrawal).
* **Visualizations & Insights:**
  * **Daily Gaming Hours by Exercise Time:** Shows an inverse relationship; as gaming addiction/hours increase, physical exercise hours drastically drop.
  * **Addiction by Platform:** Breaks down addiction levels across Console, PC, Mobile, and Multi-platform. PC and Mobile show distinct spikes in *Low* to *Severe* classifications.
  * **Does Spending Affect Mood States?:** A clear trend showing that high-spending players experience elevated levels of **Anxiety (10.2K)**, **Irritability (9.8K)**, and **Depression (7.3K)**.
  * **Who Spends More? (By Addiction Level):** **Severe (38%)** and **High (20%)** addiction groups contribute to more than half of the total financial spending.

---

### 3. 🩺 Health Dashboard (Physical Health & Sleep Quality)
This tab analyzes how intensive gaming affects the physical body, sleep cycles, and general mood.
* **Key Metrics (KPIs):**
  * **Avg Exercise Hours:** 6.95 hrs
  * **Avg Gaming Hours:** 6.15 hrs
  * **Avg Sleep:** 5.74 hrs (below the healthy average).
  * **High Risk Physical Pain:** 24% of players suffer from severe physical pain.
* **Visualizations & Insights:**
  * **Mood State by Avg Exercise Hours:** Higher exercise hours strongly correlate with positive emotional states like *Excited* and *Normal*, while lower exercise hours relate to *Anxious* and *Restless* states.
  * **Average of Sleep Hours by Sleep Quality:** Validates that individuals reporting *Insomnia* or *Very Poor* sleep get less than 5 hours of sleep on average.
  * **Average Exercise Hours by Sleep State:** Identifies that 41% of the sample experiences *Over_Sleep*, while 27% suffers from *Poor* sleep states.
  * **Physical Pain Risk Distribution:** A critical pie chart showing that **43%** of players are at **High Risk** of physical pain, and 37% are at Moderate Risk.

---

## 🐍 Advanced Customization: Python Integration for Tooltips

To elevate the user experience and create deeply customized, dynamic tooltips that Power BI's default visuals don't natively support, **Python (Matplotlib & Pandas)** was integrated directly inside the Power BI report. 

These Python scripts are triggered dynamically as a **Tooltip** when hovering over data points to provide instant, advanced breakdowns.

### 📝 1. Gender Distribution Tooltip Script
This script generates a clean, custom-colored bar chart showing the breakdown of players by gender for any filtered data segment.

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)
# dataset = dataset.drop_duplicates()

import matplotlib.pyplot as plt

# Initialize figure size
plt.figure(figsize=(6, 5))

# Group by gender and count the records
dataset.groupby("gender")["record_id"].count().plot(
    kind="bar",
    color=["#ff5266", "#4a37fa", "#b3b2b8"], # Customized theme matching dashboard colors
    rot=0, 
    fontsize=16,  
)

# Customize title and axis labels
plt.title("Distribution by Gender", fontsize=20) 
plt.xlabel("", fontsize=14) 
plt.ylabel("", fontsize=14) 

plt.tight_layout()  
plt.show()
📝 2. Addiction Risk Distribution Tooltip Script
This script generates an advanced pie chart designed to act as an instant pop-up tooltip, showing the proportion of addiction risk levels dynamically.

Python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)
# dataset = dataset.drop_duplicates()

import matplotlib.pyplot as plt
import pandas as pd

# Initialize figure size
plt.figure(figsize=(5,5))

# Group by addiction risk level and create a detailed pie chart
dataset.groupby('gaming_addiction_risk_level')['record_id'].count().plot(
    kind='pie',
    autopct='%1.1f%%',
    colors=['#2ec4b6', '#ffbf69', '#e94560', '#a475fa'], # Dashboard UI matched palette
    textprops={"fontsize": 20}
)

plt.title('Addiction Risk Distribution', fontsize=24)
plt.ylabel('')
plt.show()
🔗 How to Connect Python Tooltips in Power BI:
Create a new page in Power BI and set its Page Type to Tooltip (under Page Information).

Insert a Python Visual onto the tooltip page.

Drag the required fields (gender, gaming_addiction_risk_level, record_id) into the Visual Data fields.

Paste the respective script above into the Power BI Python script editor and hit Run.

Go back to your main Dashboard, select your target visual, go to Properties > Tooltips, and select this Tooltip page. Now, hovering over any visual will render these dynamic Python charts instantly!

🛠️ Tools Used
Power BI Desktop: Dashboard design, DAX measures, and data modeling.

Python (Pandas & Matplotlib): Used for advanced data visualization and custom tooltip rendering.

UI/UX Design: Dark-themed dashboard optimized for accessibility and gaming aesthetics.


***

### ✨ مميزات هذا الـ README:
1. **منظم ومنسق:** يسهل على أي شخص يزور حسابك على GitHub فهم فكرة المشروع فوراً.
2. **شرح تفصيلي للـ Dashboards:** يوضح أرقامك والـ KPIs (مثل الـ 1K لاعب، الـ 7M مصاريف، الـ 6.15K ساعات لعب) والتحليلات المكتوبة في الصور بدقة.
3. **دمج كود بايثون بطريقة احترافية:** تم شرح الأكواد داخل الـ Block Code الخاص بالـ Markdown مع توضيح خطوات ربط الـ Tooltip داخل باور بي آي خطوة بخطوة بالإنجليزية لتبدو كمحترفة بيانات (Data Analyst).
حطيت صور لتلاتة داش بورد اللي بعتهم؟

لا، في الكود البرمجي (Markdown) السابق لم أقم بإدراج روابط الصور الفعالة لكي لا يظهر لك كود مكسور، ولكنني شرحت محتوى الثلاث لوحات بالتفصيل بناءً على الصور التي أرسلتها (Player Dashboard و Addiction Dashboard و Health Dashboard).

لكي تظهر الصور بشكل تلقائي واحترافي داخل صفحة الـ GitHub الخاصة بكِ، يمكنك رفع الصور الثلاثة في نفس المجلد (Repository) على جيتهاب وتحديث الجزء الخاص بالـ Dashboards في ملف الـ README ليكون كالتالي:

استبدلي الجزء الخاص بـ Dashboards Breakdown بهذا الكود الذي يحتوي على مسارات الصور:

Markdown
## 📊 Dashboards Breakdown

### 1. 👤 Player Dashboard (Demographics & General Stats)
![Player Dashboard](Player%20Dashboard%20Power%20BI.jpg)

This tab focuses on understanding the player base, their spending habits, and general gaming behavior.
* **Key Metrics (KPIs):**
  * **Total Players:** 1K players in the dataset.
  * **Total Spent:** $7M across different game genres.
  * **Total Gaming Hours:** 6.15K hours accumulated.
  * **Avg Work Score:** 5.39.
* **Visualizations & Insights:**
  * **Who Plays More? (By Gender):** Equal distribution among genders (35% Other, 33% Male, 32% Female).
  * **Who Plays More? (By Age Group):** Evenly spread across Young Adults (35%), Teenagers (34%), and Adults (31%).
  * **Top 5 Games by Gaming Hours:** *Apex Legends* leads (7.2 hrs), followed closely by *Fortnite*, *Civilization VI*, *Final Fantasy*, and *Clash of Clans*.
  * **Sum of Total Spent by Game Genre:** MMO ($1.15M) and Strategy ($1.12M) are the highest revenue-generating genres.
  * **Gaming Hours vs. Work Score:** A scatter plot showing the distribution of work scores against the number of gaming hours.

---

### 2. 🧠 Addiction Dashboard (Mental Health & Behavioral Analysis)
![Addiction Dashboard](Addiction%20Dashboard%20Power%20BI.jpg)

This tab deep dives into gaming addiction levels (Severe, High, Moderate, Low) and their direct impact on work productivity and psychological well-being.
* **Key Metrics (KPIs):**
  * **Avg Work Productivity:** 5.39
  * **Total Gaming Hours:** 6.15K
  * **Avg F2F (Face-to-Face) Hours:** 7.65 hours of real-world social interaction.
  * **Avg ISO (Isolation) Score:** 3.87 (measuring social withdrawal).
* **Visualizations & Insights:**
  * **Daily Gaming Hours by Exercise Time:** Shows an inverse relationship; as gaming addiction/hours increase, physical exercise hours drastically drop.
  * **Addiction by Platform:** Breaks down addiction levels across Console, PC, Mobile, and Multi-platform. PC and Mobile show distinct spikes in *Low* to *Severe* classifications.
  * **Does Spending Affect Mood States?:** A clear trend showing that high-spending players experience elevated levels of **Anxiety (10.2K)**, **Irritability (9.8K)**, and **Depression (7.3K)**.
  * **Who Spends More? (By Addiction Level):** **Severe (38%)** and **High (20%)** addiction groups contribute to more than half of the total financial spending.

---

### 3. 🩺 Health Dashboard (Physical Health & Sleep Quality)
![Health Dashboard](Health%20Dashboard%20Power%20BI.jpg)

This tab analyzes how intensive gaming affects the physical body, sleep cycles, and general mood.
* **Key Metrics (KPIs):**
  * **Avg Exercise Hours:** 6.95 hrs
  * **Avg Gaming Hours:** 6.15 hrs
  * **Avg Sleep:** 5.74 hrs (below the healthy average).
  * **High Risk Physical Pain:** 24% of players suffer from severe physical pain.
* **Visualizations & Insights:**
  * **Mood State by Avg Exercise Hours:** Higher exercise hours strongly correlate with positive emotional states like *Excited* and *Normal*, while lower exercise hours relate to *Anxious* and *Restless* states.
  * **Average of Sleep Hours by Sleep Quality:** Validates that individuals reporting *Insomnia* or *Very Poor* sleep get less than 5 hours of sleep on average.
  * **Average Exercise Hours by Sleep State:** Identifies that 41% of the sample experiences *Over_Sleep*, while 27% suffers from *Poor* sleep states.
  * **Physical Pain Risk Distribution:** A critical pie chart showing that **43%** of players are at **High Risk** of physical pain, and 37% are at Moderate Risk.
💡 ملاحظة هامة جداً لكي تظهر الصور بنجاح:
عند رفع الصور الثلاثة على GitHub، تأكدي أن أسماء ملفات الصور مطابقة تماماً للاسم المكتوب بين القوسين ( ) في الكود الأعلى (بما في ذلك المسافات والـ الحروف الكبيرة والصغيرة)، وهي كالتالي:

Player Dashboard Power BI.jpg

Addiction Dashboard Power BI.jpg

Health Dashboard Power BI.jpg

ادمج كلع و ابعت من جديد وحط صور الداش بورد

إليكِ ملف الـ README.md الكامل والجاهز للنسخ والمدمج فيه كافة الأجزاء (الوصف، التحليلات، روابط الصور، وأكواد بايثون لـ Tooltips) بشكل احترافي ومنظم:

📁 README.md
Markdown
# 🎮 Gaming and Mental Health Analytics Dashboard (Power BI)

## 📌 Project Overview
This project presents a comprehensive, data-driven analysis of the relationship between **Gaming Habits and Mental/Physical Health**. Using Power BI, the project transforms complex behavioral data into three interactive dashboards (**Player Profile, Addiction Insights, and Health Impact**). 

The goal of this project is to uncover how gaming hours, financial spending, and different platforms correlate with mental states (such as anxiety, depression, and irritability), sleep quality, and physical pain.

---

## 📊 Dashboards Breakdown

### 1. 👤 Player Dashboard (Demographics & General Stats)
![Player Dashboard](Player%20Dashboard%20Power%20BI.jpg)

This tab focuses on understanding the player base, their spending habits, and general gaming behavior.
* **Key Metrics (KPIs):**
  * **Total Players:** 1K players in the dataset.
  * **Total Spent:** $7M across different game genres.
  * **Total Gaming Hours:** 6.15K hours accumulated.
  * **Avg Work Score:** 5.39.
* **Visualizations & Insights:**
  * **Who Plays More? (By Gender):** Equal distribution among genders (35% Other, 33% Male, 32% Female).
  * **Who Plays More? (By Age Group):** Evenly spread across Young Adults (35%), Teenagers (34%), and Adults (31%).
  * **Top 5 Games by Gaming Hours:** *Apex Legends* leads (7.2 hrs), followed closely by *Fortnite*, *Civilization VI*, *Final Fantasy*, and *Clash of Clans*.
  * **Sum of Total Spent by Game Genre:** MMO ($1.15M) and Strategy ($1.12M) are the highest revenue-generating genres.
  * **Gaming Hours vs. Work Score:** A scatter plot showing the distribution of work scores against the number of gaming hours.

---

### 2. 🧠 Addiction Dashboard (Mental Health & Behavioral Analysis)
![Addiction Dashboard](Addiction%20Dashboard%20Power%20BI.jpg)

This tab deep dives into gaming addiction levels (Severe, High, Moderate, Low) and their direct impact on work productivity and psychological well-being.
* **Key Metrics (KPIs):**
  * **Avg Work Productivity:** 5.39
  * **Total Gaming Hours:** 6.15K
  * **Avg F2F (Face-to-Face) Hours:** 7.65 hours of real-world social interaction.
  * **Avg ISO (Isolation) Score:** 3.87 (measuring social withdrawal).
* **Visualizations & Insights:**
  * **Daily Gaming Hours by Exercise Time:** Shows an inverse relationship; as gaming addiction/hours increase, physical exercise hours drastically drop.
  * **Addiction by Platform:** Breaks down addiction levels across Console, PC, Mobile, and Multi-platform. PC and Mobile show distinct spikes in *Low* to *Severe* classifications.
  * **Does Spending Affect Mood States?:** A clear trend showing that high-spending players experience elevated levels of **Anxiety (10.2K)**, **Irritability (9.8K)**, and **Depression (7.3K)**.
  * **Who Spends More? (By Addiction Level):** **Severe (38%)** and **High (20%)** addiction groups contribute to more than half of the total financial spending.

---

### 3. 🩺 Health Dashboard (Physical Health & Sleep Quality)
![Health Dashboard](Health%20Dashboard%20Power%20BI.jpg)

This tab analyzes how intensive gaming affects the physical body, sleep cycles, and general mood.
* **Key Metrics (KPIs):**
  * **Avg Exercise Hours:** 6.95 hrs
  * **Avg Gaming Hours:** 6.15 hrs
  * **Avg Sleep:** 5.74 hrs (below the healthy average).
  * **High Risk Physical Pain:** 24% of players suffer from severe physical pain.
* **Visualizations & Insights:**
  * **Mood State by Avg Exercise Hours:** Higher exercise hours strongly correlate with positive emotional states like *Excited* and *Normal*, while lower exercise hours relate to *Anxious* and *Restless* states.
  * **Average of Sleep Hours by Sleep Quality:** Validates that individuals reporting *Insomnia* or *Very Poor* sleep get less than 5 hours of sleep on average.
  * **Average Exercise Hours by Sleep State:** Identifies that 41% of the sample experiences *Over_Sleep*, while 27% suffers from *Poor* sleep states.
  * **Physical Pain Risk Distribution:** A critical pie chart showing that **43%** of players are at **High Risk** of physical pain, and 37% are at Moderate Risk.

---

## 🐍 Advanced Customization: Python Integration for Tooltips

To elevate the user experience and create deeply customized, dynamic tooltips that Power BI's default visuals don't natively support, **Python (Matplotlib & Pandas)** was integrated directly inside the Power BI report. 

These Python scripts are triggered dynamically as a **Tooltip** when hovering over data points to provide instant, advanced breakdowns.

### 📝 1. Gender Distribution Tooltip Script
This script generates a clean, custom-colored bar chart showing the breakdown of players by gender for any filtered data segment.

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)
# dataset = dataset.drop_duplicates()

import matplotlib.pyplot as plt

# Initialize figure size
plt.figure(figsize=(6, 5))

# Group by gender and count the records
dataset.groupby("gender")["record_id"].count().plot(
    kind="bar",
    color=["#ff5266", "#4a37fa", "#b3b2b8"], # Customized theme matching dashboard colors
    rot=0, 
    fontsize=16,  
)

# Customize title and axis labels
plt.title("Distribution by Gender", fontsize=20) 
plt.xlabel("", fontsize=14) 
plt.ylabel("", fontsize=14) 

plt.tight_layout()  
plt.show()
📝 2. Addiction Risk Distribution Tooltip Script
This script generates an advanced pie chart designed to act as an instant pop-up tooltip, showing the proportion of addiction risk levels dynamically.
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(gaming_addiction_risk_level, record_id)
# dataset = dataset.drop_duplicates()

import matplotlib.pyplot as plt
import pandas as pd

# Initialize figure size
plt.figure(figsize=(5,5))

# Group by addiction risk level and create a detailed pie chart
dataset.groupby('gaming_addiction_risk_level')['record_id'].count().plot(
    kind='pie',
    autopct='%1.1f%%',
    colors=['#2ec4b6', '#ffbf69', '#e94560', '#a475fa'], # Dashboard UI matched palette
    textprops={"fontsize": 20}
)

plt.title('Addiction Risk Distribution', fontsize=24)
plt.ylabel('')
plt.show()
🔗 How to Connect Python Tooltips in Power BI:
Create a new page in Power BI and set its Page Type to Tooltip (under Page Information).

Insert a Python Visual onto the tooltip page.

Drag the required fields (gender, gaming_addiction_risk_level, record_id) into the Visual Data fields.

Paste the respective script above into the Power BI Python script editor and hit Run.

Go back to your main Dashboard, select your target visual, go to Properties > Tooltips, and select this Tooltip page. Now, hovering over any visual will render these dynamic Python charts instantly!

🛠️ Tools Used
Power BI Desktop: Dashboard design, DAX measures, and data modeling.

Python (Pandas & Matplotlib): Used for advanced data visualization and custom tooltip rendering.

UI/UX Design: Dark-themed dashboard optimized for accessibility and gaming aesthetics.
