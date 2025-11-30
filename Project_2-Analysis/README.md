# My Salary Analysis Project  

## Introduction  
This project analyzes trends in the 2023 data job market using Excel. As someone exploring the data and finance industry, I wanted to understand:  

* What skills employers value the most
* How skills influence salaries
* Differences in salary between regions
* Which skills provide the highest salary advantage

Using a dataset of real-world job postings, I applied Excel’s advanced analytics features—including Power Query, PivotTables, Power Pivot, and DAX—to extract insights about salaries, skills, and job market expectations.  

### Questions to Analyze  
To understand the data science job market, I asked the following:  

1) Do more skills get you better pay?
2) What’s the salary for data jobs in different regions?
3) What are the top skills of data professionals?
4) What’s the pay for the top 10 skills?

### Excel Skills Used  
The following Excel skills were utilized for analysis:  

* 📊 Pivot Tables
* 📈 Pivot Charts
* 🧮 DAX (Data Analysis Expressions)
* 🔍 Power Query
* 💪 Power Pivot


### Data Jobs Dataset  
The dataset used for this project contains real-world data science job information from 2023. The dataset is available via Luke Barousse Excel Data Analytic courses, which provides a foundation for analyzing data using Excel.  

It includes detailed information on:

* 👨‍💼 Job titles
* 💰 Salaries
* 📍 Locations
* 🛠️ Skills

## 1️⃣ Do more skills get you better pay?  

### 🔍 Skill: Power Query (ETL) 

📥 Extract  

A) I first used Power Query to extract the original data ``` (data_salary_all.xlsx) ``` and create two queries:

* 🗃️ First one with all the data jobs information.
* 🔧 The second listing the skills for each job ID.

🔄 Transform  

B) Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.  

* 📊 data_jobs_all

<img width="244" height="312" alt="image" src="https://github.com/user-attachments/assets/5087c563-0da1-4e27-a5ea-177118cbfe3b" />  

### 

* 🛠️ data_job_skills

<img width="243" height="328" alt="image" src="https://github.com/user-attachments/assets/8d33c7ce-a6df-461c-b54d-47677b13f355" />  

###  

🔗 Load  

C) Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.  

* 📊 data_jobs_all


<img width="1916" height="649" alt="image" src="https://github.com/user-attachments/assets/6aaa8a19-868e-40fe-8f9c-d7e8234a7dea" />  

### 

* 🛠️ data_job_skills

<img width="1914" height="702" alt="image" src="https://github.com/user-attachments/assets/74399462-a9c7-4727-8775-6a77f83f8844" />  

###  

### 📊 Analysis  

💡 Insights  

* 📈 There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.
* 💼 Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.

###  
<img width="874" height="537" alt="image" src="https://github.com/user-attachments/assets/16a1b43d-1e91-4ad2-87f4-b535a54d2fe0" />   

###  

🤔 So What  

This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.  

## 2️⃣ What’s the salary for data jobs in different regions?  

### 🧮 Skills: PivotTables & DAX  

📈Pivot Table  

* 🔢 I created a PivotTable using the Data Model I created with Power Pivot
* 📊 I moved the ``` job_title_short ``` to the rows area and ``` salary_year_avg  ``` into the values area.
* 🧮 Then I added new measure to calculate the median salary for United States jobs.

  ```
  =CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States")
  ```

🧮 DAX  
* To calculate the median year salary I used DAX.

``` 
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```

### 📊 Analysis  

💡 Insights  

* 💼 Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.
* 💰 The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.

###   

<img width="1776" height="738" alt="image" src="https://github.com/user-attachments/assets/d5a0fbd2-afd7-43fd-909a-cbe4739e18c5" />  

###  

🤔 So What  

* These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards while considering geographical variations.


## 3️⃣ What are the top skills of data professionals?  

### 🔧 Skill: Power Pivot  

💪 Power Pivot  

* 🔗 I created a data model by integrating the ``` data_jobs_all ``` and ``` data_jobs_skills ``` tables into one model.
* 🧹 Since I had already cleaned the data using Power Query; Power Pivot created a relationship between these two tables.

🔗 Data Model  

* I created a relationship between my two tables using the ``` job_id ``` column.

###  

<img width="1788" height="1264" alt="image" src="https://github.com/user-attachments/assets/1c807475-6668-4253-b07d-397d9b783a2b" />  

### 

📃 Power Pivot Menu  

* The Power Pivot menu was used to refine my data model and makes it easy to create measures.

###  

<img width="1918" height="742" alt="image" src="https://github.com/user-attachments/assets/8482cf85-cac3-44a8-ad70-ee97463d48ff" />  

###  

### 📊Analysis  

💡Insights

* 💻 SQL and Python dominate as top skills in data-related jobs, reflecting their foundational role in data processing and analysis.
* ☁️ Emerging technologies like AWS and Azure also show significant presence, underlining the industry's shift towards cloud services and big data technologies.

###  

<img width="759" height="513" alt="image" src="https://github.com/user-attachments/assets/80208673-697b-4c30-8be8-db34398ffff2" />  

###  

🤔So What  

* Understanding prevalent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.



## 4️⃣ What’s the pay of the top 10 skills?

### 📊 Skill: Advanced Charts (Pivot Chart)  

📈 PivotChart  

a) I created a combo PivotChart to plot median salary and skill likelihood (%) from my PivotTable.
* 🪙 Primary Axis: Median Salary (as a Clustered Column)
* 👍 Secondary Axis: Skill Likelihood (as a Line with Markers)


b) To customize the chart, I added a title axis title, removed the lines (skill likelihood), and changed the markers to diamonds.  


### 📊 Analysis  

💡Insights  

* 💰 Higher median salaries are associated with skills like Python, Oracle, and SQL, suggesting their critical role in high-paying tech jobs.

* 📉 Skills like PowerPoint and Word have the lowest median salaries and likelihood, indicating less specialization and demand in high-salary sectors.

###

<img width="862" height="452" alt="image" src="https://github.com/user-attachments/assets/06ed635a-52bb-49d5-ac7d-085c90e421bd" />  

###  

🤔So What  

* This chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.


# Conclusion  

This project uses Excel as a full analytics tool—beyond basic spreadsheets—to explore job market dynamics in the data industry. Through data modeling, DAX calculations, Power Query transformations, and dashboard visuals, I uncovered clear trends:

* More skills = more pay
* Core technical skills (Python, SQL, cloud) dominate demand
* US roles pay far higher than global roles
* High-value skills significantly impact salary potential  

This analysis helped me understand the skill sets driving today’s data job market and sharpened my Excel, analytical thinking, and data storytelling skills.














