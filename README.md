Titanic: Socio-Economic Survival Analysis
This project performs a comprehensive exploratory data analysis (EDA) on the Titanic passenger manifest to determine how socio-economic status, gender, and family structures influenced survival rates during the 1912 disaster.

📊 Executive Summary
The analysis reveals that survival was not random but heavily dictated by institutional protocols ("women and children first") and socio-economic privilege.

Key Finding: There was an 83.3% survival gap between the most advantaged group (1st Class Females: 96.8%) and the least advantaged group (3rd Class Males: 13.5%).

🛠️ Data Engineering & Cleaning
Missing Values: Dropped the Cabin column (77.1% missing) and used median imputation for Age to ensure robustness against outliers.

Feature Engineering: Created high-signal variables including:

Title: Extracted from names to capture social status beyond just passenger class.

FamilyGroup: Categorized passengers into Solo, Small (2–4), and Large (5+) cohorts.

AgeGroup: Categorized by life stage (Minor, Adult, Senior).

📈 Key Insights
Gender: Women survived at a rate of 74.2% compared to just 18.9% for men.

Class (SES): 1st Class passengers had a 63.0% survival rate, while 3rd Class passengers had only 24.2%.

Family Dynamics: Small families (2–4 members) showed a "coordination advantage," achieving higher survival rates than solo travelers or very large families.

Age: Minors had a clear survival advantage, consistent with emergency evacuation priority.

🚀 Recommendations
Infrastructure: Standardize lifeboat access across all deck tiers to close the 39-point survival gap between 1st and 3rd class.

Protocols: Implement evacuation strategies that support family coordination, as small groups showed higher resilience.

📂 Project Structure
Titanic_Socioeconomic_Analysis.ipynb: The complete Python analysis including data cleaning, feature engineering, and Seaborn/Matplotlib visualizations.

README.md: Project overview and summary of findings.
