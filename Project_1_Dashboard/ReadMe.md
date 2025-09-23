# Excel Salary Dashboard

<img width="1112" height="533" alt="Screenshot 2025-09-23 102101" src="https://github.com/user-attachments/assets/92e65a29-3b57-42bf-9e65-a5b89d2b43e3" />

## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detauked information on job titles, salaries, locations, and essential skills that are presented here.

## Dashboard File

My final dashboard is in [1_Salary_Dashboard.xlsx](https://github.com/levieitnerdba89-a11y/Excel_Project_Data_Analytics/tree/main/Project_1_Dashboard)

## Excel Skills Utilized

- 📊 Charts
- 📔 Formulas and Functions
- 🔧 Data Validation

## Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The datset is available through my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- 🤹 Job title
- 💰 Salaries
- 📍 Locations
- 📈 Skills

# Dashboard Build - Charts

## 📊 **Data Science Job Salaries - Bar Chart**

<img width="395" height="438" alt="Screenshot 2025-09-23 100758" src="https://github.com/user-attachments/assets/e2f1dd20-7893-4a40-ba37-40577bab7ad2" />

*VBA Language*

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

- **Criteria Filtering:** Checks job title, country, schedule type, and excludes blanks salaries.
- **Array Formula:** Uses `MEDIAN()` function with nested `IF()` statement to analyze array.
- **Filtered Insights**: Provides specific salary information for job title, regions, and schedule types.

*Background Table*

<img width="259" height="219" alt="Screenshot 2025-09-23 093848" src="https://github.com/user-attachments/assets/e99f9173-09ef-4934-b135-0c0232fd8ea1" />

- **Excel Features Used:** Utilized Excel's insert chart feature to transalte the raw data into a visually digestible bar chart.
- **Design Choice:** Simple bar chart to effectively quantify specific fields in the data science job market.
- **Data Representation:** Specific fields withing the Data Scientist job market.
- **Visual Enhancement:** Monochromatic color scheme to minimize distraction from the actual data and the selected parameter is unfaded to highlight selection.
- **Insights Gained:** Enables easy understanding of data science jobs and their respective compensations. 


## 🗺️ Map Chart

<img width="288" height="182" alt="Screenshot 2025-09-23 094315" src="https://github.com/user-attachments/assets/f08a12cb-e70e-49aa-be5c-4d44aebe7841" />

*VBA Language*

```
=SORT(FILTER(A2:B112, ISNUMBER(B2:B112)), 2, 1)
```
- **Unique List Generation:** This excel formula uses the `FILTER()` to exclude entries entries containing "and" or commas, and ommits zero values.
- **Formula Purpose:** This formula populates the table below to allow us to correlate between job country and the median salary within specified country.

*Background Table (Only 5/84 rows shown for example)*

<img width="226" height="99" alt="Screenshot 2025-09-23 102507" src="https://github.com/user-attachments/assets/39d8c8e9-6208-40b5-92fa-c0c99a184f4b" />

- **Excel Features Used:** Utilized Excel's map chart feature to plot median salaries across the globe.
- **Design Choice:** Color-coded map to visualize the differences in salaries across regions.
- **Data Representation:** Plotted median salary for each country with available data.
- **Visual Enhancement:** Improved readability of geographic salary trends.
- **Insights Gained:** Enables quick grasp of global salary differences and highlights the high and low salary trends of different regions.


# 📔 Schedule Chart - Bar Chart

<img width="337" height="438" alt="Screenshot 2025-09-23 095716" src="https://github.com/user-attachments/assets/208e36ed-378f-4a0c-be39-8d822317b8b6" />

*VBA Language*

```
=SORT(FILTER(A2:B6,ISNUMBER(B2:B6)), 2, 1)
```
- **Checks & Returns:** Collects rows where comlumn B contains a number using `FILTER()`
- **Sort:** Takes filtered results and sorts them by teh 2nd column of the filtered range, and then sorts them into ascending order using `SORT()`

```
=IF($D6<>type,$E6,NA())
```
- **Accurate Correlations:** Organizes schedule type with corresponding salary data.
- **Extended Context:** Provides additional data context by giving Excel additional data so that it doesnt plot values as zero.

*Background Table*

<img width="378" height="98" alt="Screenshot 2025-09-23 103423" src="https://github.com/user-attachments/assets/cdfecdb4-7878-4a8a-9a40-f9edda0b601b" />


- **Excel Features Used:** Excel's insert chart feature to convert the data into an easy to read bar chart.
- **Design Choice:** Basic and effectie bar chart to express specific data in regards to the job schedule type.
- **Data Representation:** Enables the user to specify their search even more by filtering for specific schedule types.
- **Visual Enhancement:** Another monochromatic choice using a faded and unfaded scheme to visualize selected data filter options.
- **Insights Gained:** Provides a fast an specific view into the options available across the data science job market globally.

 ## Conclusion
 
I made this dashboard to express insights into salary trends across various data-related job titles. Using data fom my Excel course, this dashboard allows users to make informed decisions about their career paths. Investigating the functionalities to undertand how job skills,job location, and job type influence salaries.









 
