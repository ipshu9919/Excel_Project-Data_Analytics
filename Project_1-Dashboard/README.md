Excel Salary Dashboard

Introduction

This Excel Salary Dashboard was created as Project 1 of my journey toward becoming a Data Analyst. As an MBA graduate specializing in Marketing and International Business, I am building my analytical skills to turn raw data into meaningful insights that support better career and business decisions.

The purpose of this project is to explore salary trends across different data-related job titles, countries, and employment types. The interactive dashboard allows users to compare salaries and better understand the data job market.

Through this project, I applied my Excel skills to a practical analytical task and strengthened my understanding of data visualization, formulas, data validation, and interactive dashboard design.

Dashboard File

My completed dashboard is available here: 1_Salary_Dashboard.xlsx.

Excel Skills Used

The following Excel skills were applied in this project:

* Charts and Data Visualization
* Formulas and Functions
* Data Validation
* Data Analysis
* Interactive Dashboard Design

Data Jobs Dataset

The dataset used in this project contains data-related job information from 2023, including:

* Job Titles
* Salaries
* Locations
* Skills

This dataset provides a foundation for exploring salary differences across job roles and geographical locations.

Dashboard Build

Charts

Data Job Salaries — Bar Chart

<img src="/0_Resources/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary Dashboard Bar Chart">

* Excel Features: Used Excel’s bar chart functionality with formatted salary values.
* Design Choice: Selected a horizontal bar chart to make salary comparisons across job titles easier.
* Data Organization: Sorted job titles by descending salary for improved readability.
* Insights Gained: The visualization makes it easier to compare median salaries across data-related job roles and identify differences in earning potential.

Country Median Salaries — Map Chart

* Excel Features: Used Excel’s map chart feature to visualize median salaries by country.
* Design Choice: Applied color coding to distinguish salary levels across geographical regions.
* Data Representation: Displayed median salaries for countries with available data.
* Visual Enhancement: Made geographical salary comparisons easier to understand.
* Insights Gained: The map helps users explore international salary differences and understand how location can influence earning potential.

Formulas and Functions

Median Salary by Job Title

=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)

* Multi-Criteria Filtering: Evaluates job title, country, employment type, and salary availability.
* Array Formula: Uses the MEDIAN() function with a nested IF() statement to calculate the median salary for matching records.
* Targeted Analysis: Allows salary comparisons based on the selected job title, country, and employment type.
* Formula Purpose: Populates the salary table with the median salary for the selected criteria.

Background Table

Dashboard Implementation

<img src="/0_Resources/Images/1_Salary_Dashboard_Job_Title.png" width="400" height="500" alt="Salary Dashboard Job Title">

Count of Job Schedule Types

=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))

* Unique List Generation: Uses the FILTER() function to exclude entries containing “and” or commas and omit zero values.
* Formula Purpose: Generates a list of job schedule types for use in the dashboard.

Background Table

Dashboard Implementation

<img src="/0_Resources/Images/1_Salary_Dashboard_Type.png" width="350" height="500" alt="Salary Dashboard Schedule Type">

Data Validation

Filtered List

Data validation was implemented for the Job Title, Country, and Type selection fields to make the dashboard interactive.

* Improved User Experience: Allows users to select from predefined options.
* Data Consistency: Helps prevent invalid or inconsistent selections.
* Interactive Analysis: Enables users to explore salary data using different combinations of job titles, countries, and employment types.

<img src="/0_Resources/Images/1_Salary_Dashboard_Data_Validation.gif" width="425" height="400" alt="Salary Dashboard Data Validation">

Key Takeaways

Through this project, I gained practical experience in using Excel to organize and analyze data, calculate median salaries, create visualizations, and build an interactive dashboard.

The project helped me understand how data can be presented in a clear and meaningful way to support decision-making. It also strengthened my foundation in Excel as I continue developing my skills for Data Analyst and Business Analyst roles.

Conclusion

This Salary Dashboard is my first project in my Data Analyst learning journey. It demonstrates my ability to apply Excel features to explore salary trends across different data-related job titles and countries.

I look forward to building more projects using Excel, SQL, Power BI, and Python as I continue developing my analytical skills and building my data analytics portfolio.
