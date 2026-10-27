# Excel Salary Dashboard

![1_Salary_Dashboard.png](/0_Resources/Images/1_Salary_Dashboard_Final_Dashboard.gif)

## Introduction

This Excel Salary Dashboard was created as Project 1 of my journey toward becoming a Data Analyst. As an MBA graduate specializing in Marketing and International Business, I am building my analytical skills to turn raw data into meaningful insights and support better career and business decisions.

The purpose of this project is to explore salary trends across different data-related job titles, countries, and employment types. The interactive dashboard allows users to compare salaries and better understand the data job market.

Through this project, I applied my Excel skills to a practical analytical task and strengthened my understanding of data visualization, formulas, data validation, and interactive dashboard design.

### Dashboard File

My final dashboard is in [1_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts and Data Visualization**
- **🧮 Formulas and Functions**
- **❎ Data Validation**
- **📊 Data Analysis**
- **🎯 Interactive Dashboard Design**

### Data Jobs Dataset

The dataset used for this project contains data-related job information from 2023. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Job Salaries - Bar Chart

<img src="/0_Resources/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary Dashboard Chart1">

- 🛠️ **Excel Features:** Utilized Excel's bar chart feature with formatted salary values.
- 🎨 **Design Choice:** Selected a horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This visualization helps compare median salaries across data-related job roles and identify differences in earning potential.

#### 🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Chart2.png](/0_Resources/Images/1_Salary_Dashboard_Country_Map.gif)

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries by country.
- 🎨 **Design Choice:** Used color coding to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and understanding of geographical salary trends.
- 💡 **Insights Gained:** Helps explore global salary differences and understand how location can influence earning potential.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```excel
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

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, employment type, and excludes unavailable salary values.
- 📊 **Array Formula:** Utilizes the `MEDIAN()` function with a nested `IF()` statement to analyze matching records.
- 🎯 **Tailored Insights:** Provides salary information based on the selected job title, country, and employment type.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on the selected criteria.

🍽️ Background Table

![1_Salary_Dashboard_Screenshot1.png](/0_Resources/Images/1_Salary_Dashboard_Screenshot1.png)

📉 Dashboard Implementation

<img src="/0_Resources/Images/1_Salary_Dashboard_Job_Title.png" width="400" height="500" alt="Salary Dashboard Title">

#### ⏰ Count of Job Schedule Type

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** Uses the `FILTER()` function to exclude entries containing "and" or commas and omit zero values.
- **🔢 Formula Purpose:** Generates a list of job schedule types for use in the dashboard.

🍽️ Background Table

![1_Salary_Dashboard_Type.png](/0_Resources/Images/1_Salary_Dashboard_Screenshot2.png)

📉 Dashboard Implementation

<img src="/0_Resources/Images/1_Salary_Dashboard_Type.png" width="350" height="500" alt="Salary Dashboard Type">

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implemented data validation for the `Job Title`, `Country`, and `Type` selection fields to make the dashboard interactive.
    - 🎯 Allows users to select from predefined options.
    - 🚫 Helps prevent incorrect or inconsistent selections.
    - 👥 Improves dashboard usability and makes salary comparisons easier.

<img src="/0_Resources/Images/1_Salary_Dashboard_Data_Validation.gif" width="425" height="400" alt="Salary Dashboard Data Validation">

## Conclusion

This Salary Dashboard is Project 1 of my Data Analyst learning journey. Through this project, I gained practical experience in using Excel to analyze salary trends, compare median salaries, create visualizations, and build an interactive dashboard.

The project helped me understand how data can be transformed into meaningful insights to support decision-making. I will continue building my analytical skills through projects using Excel, SQL, Power BI, and Python as I work toward my goal of becoming a Data Analyst or Business Analyst.
