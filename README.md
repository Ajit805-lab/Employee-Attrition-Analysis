# 📌 Employee-Attrition-Analysis 📢✨
## 📖 1. Introduction

        Employee attrition refers to the gradual reduction of a workforce due to employees leaving an organization over time. 
        
        It can occur due to voluntary resignations, retirements, layoffs, or involuntary terminations. This project analyses the 
        
        key factors of employee attrition such as salary, job-statisfaction, enviorment of company etc.
## 🎯 2. Objectives 

        ✅ What the causes of employee attrition

# 📌 Project Details
    📛 Project Name: Employee Attrition

    👨‍💻 Author: Ajit Kumar Samal

    📅 Date: 06-03-2025

    🛠 Tools Used: Power BI, Excel, Power Query
# 📂 Project Overview
    This project provides insights of employee attrition rate as per department wise, salary wise and 
    other informations about employee attrition. This report helps to HR managers make data driven decisions 
    regarding workforce planning and retention strategies.
    
   # 📌 Report Link : https://1drv.ms/u/c/be2c82aa9bfb8a04/ESClV8M3ySxIuR-em9yLLOMB3MNbTzmWOIGEMNTgo2UfjQ?e=1j0TqW
# 📷 Report Preview 
  ![Screenshot 2025-03-07 122554](https://github.com/user-attachments/assets/b1e56052-fd6b-458f-957e-2c534755ed49)
#### 📊 Dataset Information :
    🟢 Source : Kaggle.com
    
    🔵 Data Type : CSV 
    
    🟡 Key features : (Age, Attrition, BusinessTravel, DailyRate, Department, DistanceFromHome, Education,
     EducationField, EmployeeCount, EmployeeNumber, EnvironmentSatisfaction, Gender, HourlyRate, JobInvolvement, JobLevel,
     JobRole, JobSatisfaction, MaritalStatus, MonthlyIncome, Salary_Slab, MonthlyRate, NumCompaniesWorked, Over18, OverTime, 
     PercentSalaryHike, PerformanceRating, RelationshipSatisfaction, StandardHours, StockOptionLevel, TotalWorkingYears, TrainingTimesLastYear, 
     WorkLifeBalance, YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager)
    
# 📌 Steps Followed
#### 🛠️ Data Transformation & ETL process :
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
                            else "50-60"))))
                            
                Salary slab = if(attriition[Monthlyincome] <= 5000, "1k-5k",
                              else if(attrition[Monthlyincome] <= 1000, "5k-10k",
                              else if(Attrition[Monthlyincome] <= 15000, "10k-15k",
                              else "Above 15k")))
#### ⚙️ Technical implementation :                      
    ⚪ Step 1 : After doing all these things then i load this data into Power BI Desktop for creating reports
    
    🟡 Step 2 : in Power BI Desktop some measures are created for reports like count of employee, count of attrition, attrition rate, average age of employee etc.
Following some Dax expression was written:

🔸Count of employee = count(Attrition[ID])

A card visual used to represent the count of employees.
 
 ![Screenshot 2025-03-08 110358](https://github.com/user-attachments/assets/ceeee443-7ec2-4959-9402-89b9fdb98055)
 
🔸 Count of Attrition = count(Attrition[Attrition])      

 A card visual used to represent count of employee attrition.
 
 ![Screenshot 2025-03-08 110656](https://github.com/user-attachments/assets/7285b55b-04b1-47ed-994e-65630d1f3a8d)

🔸 Attrition rate = count(Attrition[Attrition])/count(Attrition[ID])*100

A card visual used to represent the attrition rate.

![Screenshot 2025-03-08 110630](https://github.com/user-attachments/assets/65b75794-cf51-4a5b-b49d-d811b7338e6c)
ℹ️ Note-[The name of table and one of the column of table is same "Attrition"]

🔸 Average age of employees = Average(Attrition[Age])

A card visual to represent the average age.

![Screenshot 2025-03-14 102215](https://github.com/user-attachments/assets/a98b4edb-073a-45c3-a588-e63f9269a711)

🔸 Average monthly-rate of employees = Average(Attrition[MonthlyRate])

A card visual to represent the average monthly-rate.

![Screenshot 2025-03-14 102227](https://github.com/user-attachments/assets/d6fbb37d-d90f-4527-903f-447da772bd6d)

🔸 Average monthly-income of employees = Average(Attrition[MonthlyIncome])

A card visual to represent the average monthly-income.

![Screenshot 2025-03-14 102322](https://github.com/user-attachments/assets/f2d431b0-f9c2-46c7-aeaf-f984a7df8cdd)

🔸 Average years at company of employees = Average(Attrition[YearsAtCompany])

A card visual to represent the average monthly-income.

![Screenshot 2025-03-14 102316](https://github.com/user-attachments/assets/79c48beb-c3ed-48b9-8d75-4ca03341273d)


# 📊 Dashboard Features & Insights :
    Total number of attrition : 237  
        🔸 Female = 87 (37%)
        🔸 Male = 150 (63%)
        
    Attrition count on monthly income :
       🔸 1k-5k = 163
       🔸 5k-10k = 49
       🔸 10k-15k = 20
       🔸 Above 15k = 05
       
    Attrition count on Age group : 
       🔸Below 20 = 10
       🔸20-30 = 90
       🔸30-40 = 85
       🔸40-50 = 34
       🔸50-60 = 18
       
    Attrition count on department : 237
       🔸 Human resources = 92 (38%)
       🔸 Research and devlopment = 133 (56%)
       🔸 Sale = 12 (6%)
       
    Average Monthly Income : 6.5k
        🔸 Female = 6.69k 
        🔸 Male = 6.38k
        
    Average Monthly Rate : 14.3k
        🔸 Female = 14.6k
        🔸 Male = 14.0k
# 🔚 Conclusion : 
        In this project i successfully analysed the dataset using Power BI, transforming raw data into meaningful insights.
        The dashboards provides a clear visualisation of key matrics, enabling better descision making. By using power query-
        for data cleaning, DAX for advance calculation and interactive visuals.

        As per my analysis the key factor of employees attrition is salary. This isue raise for market competitation, Performance based and  
        sometimes the enviorment also effect to the employee attrition.
        Some ratings are given by the employees below :
![Screenshot 2025-03-08 125223](https://github.com/user-attachments/assets/cf462034-1074-4d98-9a0a-f730cf9f06a4)

# 📊 How to use the report :
        🔸 Download the .pbix file by given link.
        🔸 Open it in Power BI Desktop
### 📞 Conatct Information : 
        📧 Email: ajitkumarofficial79@gmail.com
        📱 Phone: 7978992711
## 🎉 Thank You!  
    We appreciate your time and interest in this project.  
    If you like it, consider giving a ⭐ to support the work!  

                
    
