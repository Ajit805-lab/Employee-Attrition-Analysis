# 📊 Employee-Attrition-Analysis
# 📌 Project Details
    📛 Project Name: Employee Attrition

    👨‍💻 Author: Ajit Kumar Samal

    📅 Date: 06-03-2025

    🛠 Tools Used: Power BI, Excel, Power Query
# 📂 Project Overview
    This project provides insights of employee attrition rate as per department wise, salary wise and other informations about employee attrition. This report helps to HR managers make data driven decisions 
    regarding workforce planning and retention strategies.   
# 📌 Report Link 
# 📷 Report Preview 
  ![Screenshot 2025-03-07 122554](https://github.com/user-attachments/assets/b1e56052-fd6b-458f-957e-2c534755ed49)
# 📌 Steps Followed
    🟢 Step 1 : Load data in Microsoft Power Query Editor.
    🔵 Step 2 : After loading data in power query editor trying to understand the 'Columns quality', 'Columns distribution' and 'Column profile option'.
    🟡 Step 3 : Also since by default, profile will be opened for 1st 1000 rows so you need column profiling based on entire dataset.
    🟠 Step 4 : After doing above setps clean the dataset like remove null values, duplicate values and giving a appropriate data type to the columns.
    🔴 Step 5 : Adding the conditional columns are 'Age Group', 'Salary Slab', And 'Attrition Count'.
                Expressios are:
                Age Group = if(Attrition[Age] < 20, "Below 20",
                            else if(Attrition[Age] <= 30, "20-30",
                            else if(Attrition[Age] <= 40, "30-40",
                            else if(Attrition[Age] <= 50, "40-50",
                            else "50-60"
                Salary slab=
                
    
