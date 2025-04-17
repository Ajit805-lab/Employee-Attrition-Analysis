# 📌 Employee-Attrition-Analysis 📢✨
## 📖 1. Introduction

        Employee attrition refers to the gradual reduction of a workforce due to employees leaving an organization over time. 
        
        It can occur due to voluntary resignations, retirements, layoffs, or involuntary terminations. This project analyses the 
        
        key factors of employee attrition such as salary, job-statisfaction, enviorment of company etc.
        
## 🎯 2. Objectives 

        ✅ What the causes of employee attrition

## 📌 3. Project Details

        📛 Project Name: Employee Attrition
        
        👨‍💻 Author: Ajit Kumar Samal
        
        📅 Date: 06-03-2025

        🛠 Tools Used: Power BI, Excel, Power Query
        
## 📌 4. Report Link :
        
        https://1drv.ms/u/c/be2c82aa9bfb8a04/ESClV8M3ySxIuR-em9yLLOMB3MNbTzmWOIGEMNTgo2UfjQ?e=1j0TqW
        
## 📷 Report Preview 

  ![Screenshot 2025-03-07 122554](https://github.com/user-attachments/assets/b1e56052-fd6b-458f-957e-2c534755ed49)
  
## 📊 5. Dataset Information :

    🟢 Source : Kaggle.com
    
    🔵 Data Type : CSV 
    
    🟡 Key features : 
    
        • 🎂 Age – Employee's age 
            
        • ❌ Attrition – Employee turnover status 
        
        • ✈️ BusinessTravel – Frequency of business travel
        
        • 💰 DailyRate – Daily earnings of the employee  
        
        • 🏢 Department – Department of the employee 
        
        • 📍 DistanceFromHome – Distance from home to workplace 
        
        • 🎓 Education – Education level  
        
        • 📚 EducationField – Field of study  
        
        • 👥 EmployeeCount – Number of employees  
        
        • 🆔 EmployeeNumber – Unique employee ID  
        
        • 🌿 EnvironmentSatisfaction – Workplace environment satisfaction 
        
        • 🚻 Gender – Gender of the employee  
        
        • ⏳ HourlyRate – Hourly wage  
        
        • 💼 JobInvolvement – Level of job involvement  
        
        • 📊 JobLevel – Job position level 
        
        • 👨‍💻 JobRole – Job designation  
        
        • 😊 JobSatisfaction – Satisfaction with the job  
        
        • 💍 MaritalStatus – Marital status of the employee  
        
        • 💵 MonthlyIncome – Monthly salary  
        
        • 🏷️ Salary_Slab – Salary category  
        
        • 💳 MonthlyRate – Monthly salary rate 
        
        • 🏢 NumCompaniesWorked – Number of previous companies worked at  
        
        • 🔞 Over18 – Employee is over 18 or not  
        
        • ⏰ OverTime – Overtime status 
        
        • 📈 PercentSalaryHike – Salary increment percentage  
        
        • ⭐ PerformanceRating – Employee performance rating  
        
        • 💑 RelationshipSatisfaction – Satisfaction with workplace relationships  
        
        • ⏳ StandardHours – Standard working hours  
        
        • 📦 StockOptionLevel – Stock option level 
        
        • 🔄 TotalWorkingYears – Total years of work experience  
        
        • 🎯 TrainingTimesLastYear – Training sessions attended last year  
        
        • ⚖️ WorkLifeBalance – Balance between work and personal life  
        
        • 🏢 YearsAtCompany – Years spent in the company  
        
        • 🔄 YearsInCurrentRole – Years in the current role  
        
        • ⏳ YearsSinceLastPromotion – Time since the last promotion 
        
        • 👨‍💼 YearsWithCurrManager – Years working with the current manager  

## 🛠️ 6. Data Transformation & ETL process :

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
## ⚙️ 7. Technical implementation :  

    ⚪ Step 1 : After doing all these things then i load this data into Power BI Desktop for creating reports
    
    🟡 Step 2 : in Power BI Desktop some measures are created for reports like count of employee, count of attrition, attrition rate, average age of employee etc.
    
Following some Dax expression was written:

        🔸Count of employee = count(Attrition[ID])
        
        A card visual used to represent the count of employees.
 
 ![Screenshot 2025-04-17 132802](https://github.com/user-attachments/assets/70208dde-9696-4ab6-81f6-b42425e6dfca)
         
        🔸 Count of Attrition = count(Attrition[Attrition])      
        
         A card visual used to represent count of employee attrition.
 
 ![Screenshot 2025-04-17 133431](https://github.com/user-attachments/assets/52332cce-1087-4230-8f85-317aceb28394)

        🔸 Attrition rate = count(Attrition[Attrition])/count(Attrition[ID])*100
        
         A card visual used to represent the attrition rate.

![Screenshot 2025-04-17 133503](https://github.com/user-attachments/assets/3c03632e-f335-4338-9c71-a8441de85d61)
ℹ️ Note-[The name of table and one of the column of table is same "Attrition"]

        🔸 Average age of employees = Average(Attrition[Age])
        
         A card visual to represent the average age.

![Screenshot 2025-04-17 133539](https://github.com/user-attachments/assets/53f6f020-11f8-4b57-a64e-57ce220a177c)

        🔸 Average monthly-rate of employees = Average(Attrition[MonthlyRate])
        
         A card visual to represent the average monthly-rate.

![Screenshot 2025-04-17 133639](https://github.com/user-attachments/assets/5022828b-35c3-43e7-84e8-9003b9d2bb9d)

        🔸 Average monthly-income of employees = Average(Attrition[MonthlyIncome])
        
         A card visual to represent the average monthly-income.

![Screenshot 2025-04-17 133750](https://github.com/user-attachments/assets/e45ef642-1dcd-4b13-b5de-e2d494fd2e8a)

        🔸 Average years at company of employees = Average(Attrition[YearsAtCompany])
        
         A card visual to represent the average monthly-income.

![Screenshot 2025-04-17 133836](https://github.com/user-attachments/assets/0ee841e3-c1c1-4a62-a49d-848aa0be7d77)

        🔸 Attrition_Count by Education
        
![Screenshot 2025-04-17 134319](https://github.com/user-attachments/assets/437df79e-caa0-476c-bf8f-16f5c2772843)

## 📊 8. Dashboard Features & Insights :
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
        
## 🔚 9. Conclusion : 
        In this project i successfully analysed the dataset using Power BI, transforming raw data into meaningful insights.
        The dashboards provides a clear visualisation of key matrics, enabling better descision making. By using power query-
        for data cleaning, DAX for advance calculation and interactive visuals.

        As per my analysis the key factor of employees attrition is salary. This isue raise for market competitation, Performance based and  
        sometimes the enviorment also effect to the employee attrition.
        Some ratings are given by the employees below :
        
![Screenshot 2025-03-08 125223](https://github.com/user-attachments/assets/cf462034-1074-4d98-9a0a-f730cf9f06a4)

## 📊 How to use the report :
        🔸 Download the .pbix file by given link.
        🔸 Open it in Power BI Desktop
        
## 📞 Conatct Information : 
        📧 Email: ajitkumarofficial79@gmail.com
        📱 Phone: 7978992711
## 🎉 Thank You!  
    We appreciate your time and interest in this project.  
    If you like it, consider giving a ⭐ to support the work!  

                
    
