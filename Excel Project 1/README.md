# Excel Salary Dashboard

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/b2627746-851c-4196-960d-0eece8dc3256)

## Introduction  
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  
This data is from Luke Barousse's Excel for Data Analytics Course. so the majority of data is concentrated in the US

### Dashboard file
My final Dashboard is in [Excel Project 1](https://github.com/YashLaxmanSharma/Excel_Project-Data_Anallytics/blob/main/Excel%20Project%201/Excel%20Project%201.xlsx)

### Excel Skills Used  
The following Excel skills were utilized for analysis:

- 📉 Charts  
- 🧮 Formulas and Functions  
- ❎ Data Validation  

### Data Jobs Dataset  
The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- 👨‍💼 Job titles  
- 💰 Salaries  
- 📍 Locations  
- 🛠️ Skills

## Dashboard Build  
### 📉 Charts  
📊 Data Science Job Salaries - Bar Chart

![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/4e892e78-2650-416b-8cbe-668f0269f010)

- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

### 🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/81b0f08b-8047-4faf-a1d4-c3cdeb0eb597)

- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

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
- 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- 📊 Array Formula: Utilizes ``MEDIAN()`` function with nested ``IF()`` statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table  
![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/e3676da3-bcc5-48e4-abb1-79e0288e6429)

📉 Dashboard Implementation  
![1_Salary_Dashboard_Job_Title](https://github.com/user-attachments/assets/272b5277-31dd-4f23-a968-bf5ad22c481a)

### ⏰ Count of Job Schedule Type  
```=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))```
- 🔍 Unique List Generation: This Excel formula below employs the ``FILTER()`` function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table  
![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/fa72c9bb-1848-496f-9648-8e970c09470c)

📉 Dashboard Implementation:  
![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/4d648289-9ded-4733-8903-12afc87b037b)


## ❎ Data Validation

### 🔍 Filtered List  
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the ``Job Title``, ``Country``, and ``Type`` option in the Data tab ensures:
- 🎯 User input is restricted to predefined, validated schedule types
- 🚫 Incorrect or inconsistent entries are prevented
- 👥 Overall usability of the dashboard is enhanced

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/e3211b70-700a-4028-9f2b-982181a1b578)

# Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. 
Utilizing data from Luke Barousse's Excel course, this dashboard allows users to make informed decisions about their career paths. 
Exploring the functionalities to understand how location and job type influence salaries.

