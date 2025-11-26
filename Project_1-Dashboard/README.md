# Excel Salary Dashboard

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/a209400f-8c44-440b-ba92-53bb0facedb7)  
## Introduction  
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from Luke Barousse Excel Course, which provides a foundation in analyzing data using this powerful tool. The dataset contains detailed information on job titles, salaries, locations, and essential skills.
### Dashboard file  
My final dashboard is in [Project 1 (Salary Dashboard).xlsx](https://github.com/user-attachments/files/23767070/Project.1.Salary.Dashboard.xlsx)  
### Excel Skills Used  
The following Excel skills were utilized for analysis:  

📉 Charts  
🧮 Formulas and Functions  
❎ Data Validation  
### Data Jobs Datasets  
The dataset used for this project contains real-world data science job information from 2023. The dataset is available via Luke Barousse Excel Course, which provides a foundation for analyzing data using Excel. It includes detailed information on:  

👨‍💼 Job titles  
💰 Salaries  
📍 Locations  
🛠️ Skills  

## Dashboard Build  
### 📉 Charts  
📊 Data Science Job Salaries - Bar Chart 

<img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/4507c87d-9110-4570-acb7-2c8e10d7ee38" />         

###
* 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.   
* 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.    
* 📉 Data Organization: Sorted job titles by descending salary for improved readability.    
* 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.
###  
🗺️ Country Median Salaries - Map Chart  

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/0e5523c8-2fef-4b05-9f7d-b39caa2b500b)

###  
* 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.  
* 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.  
* 📊 Data Representation: Plotted median salary for each country with available data.  
* 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.  
* 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions  
💰 Median Salary by Job Titles  
```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```  
* 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.  
* 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.  
* 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.  
* 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.


🍽️ Background Table  

<img width="265" height="220" alt="image" src="https://github.com/user-attachments/assets/4a0d63ae-ab56-471f-8d39-9a2c582a4dbb" />  

###  
📉 Dashboard Implementation  

<img width="350" height="600" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/11313557-0747-4d62-a0fc-ee844f7ea9fd" />  

###  
⏰ Count of Job Schedule Type  

``` =FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0)) ```  
* 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.  
* 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.


🍽️ Background Table  

<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/3577d582-e10c-4db2-9a44-1a7b5fbb959f" />  

###  

📉 Dashboard Implementation  

<img width="350" height="650" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/bce6d141-c66b-48a0-bf71-62f672830df4" />  

###  

### ❎ Data Validation  
🔍 Filtered List  

🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures: 

* 🎯 User input is restricted to predefined, validated schedule types  
* 🚫 Incorrect or inconsistent entries are prevented   
* 👥 Overall usability of the dashboard is enhanced

### 

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/2ce5ec28-87b3-418f-b835-ecc3315e6902)  

### 

## Conclusion  

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from Luke Barousse Excel Course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.
















