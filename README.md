# 🚢 Titanic Survival Analysis: Socio-Economic & Demographic Drivers

A comprehensive data science project exploring the factors that influenced survival outcomes during the 1912 Titanic disaster.

## 📌 Project Overview
The sinking of the Titanic is one of the most infamous shipwrecks in history. This project analyzes the passenger manifest to determine which groups of people were more likely to survive, focusing on **Socio-Economic Status (Class)**, **Gender**, **Age**, and **Family Composition**.

### Key Research Questions:
* Did passenger class (wealth) act as a significant gateway to survival?
* To what extent did the "women and children first" protocol manifest in the data?
* Did traveling solo versus in a family group change a passenger's odds?

## 📊 Dataset Summary
* **Source:** Titanic Passenger Manifest (891 records)
* **Target Variable:** `Survived` (Binary: 0 = No, 1 = Yes)
* **Key Features:** Pclass, Sex, Age, SibSp, Parch, Fare, and Title (Engineered).
* **Baseline Survival Rate:** ~38.4%

## 🛠️ Technical Workflow
1.  **Exploratory Data Analysis (EDA):** Identified missing values in `Age` (19.9%) and `Cabin` (77.1%).
2.  **Data Cleaning:**
    * Dropped the sparse `Cabin` column.
    * Imputed `Age` using the **median** to remain robust against outliers.
    * Imputed `Embarked` using the **mode**.
3.  **Feature Engineering:**
    * **Title Extraction:** Extracted social titles (Mr, Mrs, Master, etc.) from names.
    * **Family Grouping:** Created categories for Solo, Small (2–4), and Large (5+) families.
    * **Life Stage Buckets:** Segmented passengers into Minor, Adult, and Senior.
4.  **Visualization:** Utilized Matplotlib and Seaborn for correlation heatmaps, survival matrices, and distribution plots.

## 📈 Key Insights
* **The Gender Gap:** Women had **3.9x higher odds** of survival than men (74.2% vs 18.9%).
* **Socio-Economic Disparity:** 1st Class passengers had a **63% survival rate**, while 3rd Class passengers only had **24.2%**.
* **The "Sweet Spot" for Families:** Small families (2-4 members) had the highest survival rate (**57.9%**), suggesting a coordination advantage. Large families (5+) struggled significantly (**16.1%**).
* **The Ultimate Advantage:** A **1st Class Female** had a **96.8%** chance of survival, whereas a **3rd Class Male** had only a **13.5%** chance.



## 💡 Strategic Recommendations
* **Equitable Access:** Analysis suggests a ~39% survival gap between classes driven by deck proximity. Future safety designs should prioritize standardized lifeboat access across all tiers.
* **Coordinated Evacuation:** Data shows small groups fare better than individuals. Emergency protocols should focus on family-unit evacuation to improve coordination and speed.

## 🚀 How to Run
1. Clone this repository.
2. Ensure you have the following libraries installed:
   ```bash
   pip install pandas matplotlib seaborn numpy
