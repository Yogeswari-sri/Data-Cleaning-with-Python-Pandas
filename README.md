# Data-Cleaning-with-Python-Pandas
Data Analyst in training, skilled in Python and Pandas for data cleaning and transformation.     Focused on building a professional portfolio that connects technical skills to real‑world analytics applications.

:

🧹 Data Cleaning with Python & Pandas

📌 Project Overview

This project demonstrates how to clean and transform raw datasets into recruiter‑ready formats using Python and Pandas.
The focus is on handling mixed date formats, missing values (NaT), and preparing clean data for Power BI and Excel dashboards.

⚡ Key Features
Standardized inconsistent date formats (Joining_Date, Last_Login_Time) using pd.to_datetime().

Applied error handling (errors="coerce") to safely convert invalid entries into NaT.

Implemented strategies for missing values:

Default replacements

Median/mean imputation

Department‑level hierarchical filling

Cleaned salary data by removing commas, quotes, and symbols for numeric conversion

.

🛠️ Tech Stack
Python (Pandas, NumPy)

Jupyter Notebook / Google Colab

Power BI / Excel for visualization

| Column | Before Cleaning | After Cleaning |
| --- | --- | --- |
| Joining_Date | ``Sep ``16, ``2023`` / ``29-Aug-22`` / ``02/14/23`` | ``2023-09-16`` / ``2022-08-29`` / ``2023-02-14`` |
| Last_Login_Time | ``16-04-2023`` / ``04/15/23`` | ``2023-04-16`` / ``2023-04-15`` |
| Salary | ``"70,000"`` / ``"45,500"`` | ``70000.0`` / ``45500.0`` |
| Missing Dates | Empty / Invalid entries | Filled with median/mean |

# Standardize Joining_Date
df["Joining_Date"] = pd.to_datetime(
    df["Joining_Date"],
    errors="coerce",
    dayfirst=True
)

# Clean Salary column
df["Salary"] = df["Salary"].replace(r'[",]', '', regex=True).astype(float)

🎯 Outcome
Clean, consistent datasets ready for analysis.

Recruiter‑friendly dashboards with accurate insights.

Portfolio project showcasing data cleaning, transformation, and visualization skills.


🚀 Next Steps
Extend cleaning pipeline to other HR/Finance datasets.

Automate imputation strategies for large‑scale data.

Integrate cleaned data directly into Power BI dashboards.

