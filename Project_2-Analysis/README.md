# Project 2: Data Jobs Market Analysis

## Introduction

As an MBA graduate specializing in Marketing and International Business, I am building my analytical skills to pursue a career as a Data Analyst. After completing my first Excel Salary Dashboard project, I wanted to explore the data job market in greater depth and understand which skills are in demand and how they relate to salary levels.

The purpose of this project is to analyze real-world data job postings to identify salary trends, compare opportunities across regions, and explore the most profitable skills in the data industry.

Through this project, I aim to strengthen my Excel-based data analysis skills and better understand the technical skills that can help me prepare for Data Analyst and Business Analyst roles.

### Questions to Analyze

To better understand the data job market, I explored the following questions:

1. **Do more skills get you better pay?**
2. **What are the salaries for data jobs in different regions?**
3. **What are the top skills required for data professionals?**
4. **What is the pay associated with the top 10 skills?**

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📊 PivotTables**
- **📈 PivotCharts**
- **🧮 DAX (Data Analysis Expressions)**
- **🔍 Power Query**
- **💪 Power Pivot**
- **🔗 Data Modeling**
- **📉 Data Visualization**

### Data Jobs Dataset

The dataset used for this project contains real-world data job information from 2023. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

This dataset provides a foundation for exploring salary patterns, regional differences, and skill demand across data-related roles.

## 1️⃣ Do More Skills Get You Better Pay?

### 🔍 Skill: Power Query (ETL)

#### 📥 Extract

- I used Power Query to extract the original data (`data_salary_all.xlsx`) and create two queries:
    - 🗃️ The first query contains data job information.
    - 🔧 The second query lists the skills associated with each job ID.

#### 🔄 Transform

- I transformed both queries by changing column data types, removing unnecessary columns, cleaning text, and trimming excess whitespace.
    - 📊 data_jobs_all

        ![2_Project_Analysis_Screenshot1.png](/0_Resources/Images/2_Project_Analysis_Screenshot1.png)

    - 🛠️ data_job_skills

        ![2_Project_Analysis_Screenshot2.png](/0_Resources/Images/2_Project_Analysis_Screenshot2.png)

#### 🔗 Load

- I loaded both transformed queries into the workbook to prepare the data for further analysis.
    - 📊 data_jobs_all

        ![2_Project_Analysis_Screenshot3.png](/0_Resources/Images/2_Project_Analysis_Screenshot3.png)

    - 🛠️ data_job_skills

        ![2_Project_Analysis_Screenshot4.png](/0_Resources/Images/2_Project_Analysis_Screenshot4.png)

### 📊 Analysis

#### 💡 Insights

- 📈 The analysis explores the relationship between the number of skills requested in job postings and median salary, particularly for specialized roles.
- 💼 Comparing roles such as Business Analyst, Data Scientist, and Senior Data Engineer helps examine differences in skill requirements and earning potential.

    ![2_Project_Analysis_Chart1.png](/0_Resources/Images/2_Project_Analysis_Chart1.png)

#### 🤔 So What?

- Understanding the relationship between skills and salary can help me prioritize relevant skills while preparing for Data Analyst and Business Analyst roles.

## 2️⃣ What Are the Salaries for Data Jobs in Different Regions?

### 🧮 Skills: PivotTables & DAX

#### 📈 PivotTable

- 🔢 I created a PivotTable using the Data Model built with Power Pivot.
- 📊 I placed `job_title_short` in the Rows area and `salary_year_avg` in the Values area.
- 🧮 I added a measure to calculate the median salary for jobs in the United States.

    ```dax
    =CALCULATE(
        MEDIAN(data_jobs_all[salary_year_avg]),
        data_jobs_all[job_country] = "United States")
    ```

#### 🧮 DAX

- I used DAX to calculate the median annual salary across the dataset.

    ```dax
    Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
    ```

### 📊 Analysis

#### 💡 Insights

- 💼 Comparing median salaries across job titles helps identify roles with higher earning potential in the United States and internationally.
- 💰 Regional salary differences provide a better understanding of how location can influence earning opportunities in the data job market.

    ![2_Project_Analysis_Chart2.png](/0_Resources/Images/2_Project_Analysis_Chart2.png)

#### 🤔 So What?

- These comparisons can support career planning by helping aspiring data professionals understand salary differences across roles and regions.

## 3️⃣ What Are the Top Skills Required for Data Professionals?

### 🔧 Skill: Power Pivot

#### 💪 Power Pivot

- 🔗 I created a data model by integrating the `data_jobs_all` and `data_jobs_skills` tables.
- 🧹 After cleaning the data in Power Query, I used Power Pivot to establish a relationship between the two tables.

#### 🔗 Data Model

- I created a relationship between the tables using the `job_id` column.

    ![2_Project_Analysis_Screenshot5.png](/0_Resources/Images/2_Project_Analysis_Screenshot5.png)

#### 📃 Power Pivot Menu

- I used the Power Pivot menu to manage the data model and create measures for analysis.

    ![2_Project_Analysis_Screenshot6.png](/0_Resources/Images/2_Project_Analysis_Screenshot6.png)

### 📊 Analysis

#### 💡 Insights

- 💻 The analysis explores the demand for technical skills such as SQL and Python across data-related job postings.
- ☁️ Cloud technologies such as AWS and Azure provide additional insight into the skills appearing in the data job market.

    ![2_Project_Analysis_Chart3.png](/0_Resources/Images/2_Project_Analysis_Chart3.png)

#### 🤔 So What?

- Identifying frequently requested skills helps me understand which technologies to prioritize while developing my analytical skill set and preparing for industry requirements.

## 4️⃣ What Is the Pay Associated with the Top 10 Skills?

### 📊 Skill: Advanced Charts (PivotChart)

#### 📈 PivotChart

- I created a combo PivotChart to compare median salary and skill likelihood (%) using data from my PivotTable.
    - 🪙 **Primary Axis:** Median Salary, displayed as a Clustered Column.
    - 👍 **Secondary Axis:** Skill Likelihood, displayed as a Line with Markers.
- I customized the chart by adding a title and axis titles, removing unnecessary gridlines, and changing the markers to diamonds for improved readability.

### 📊 Analysis

#### 💡 Insights

- 💰 Comparing median salaries across the top 10 skills helps identify skills associated with different salary levels.
- 📉 The comparison also highlights differences in skill likelihood, helping distinguish commonly requested skills from those with different levels of demand.

    ![2_Project_Analysis_Chart4.png](/0_Resources/Images/2_Project_Analysis_Chart4.png)

### 🤔 So What?

- This analysis helps me make more informed decisions about which technical skills to prioritize as I continue learning SQL, Excel, Power BI, and Python for analyst roles.

## Conclusion

This project is the second step in my Data Analyst learning journey. Building on my first Excel Salary Dashboard, I explored the data job market through multiple analytical questions involving skill requirements, salary trends, and geographical differences.

By using Excel features such as Power Query, PivotTables, DAX, Power Pivot, and PivotCharts, I developed a deeper understanding of data cleaning, data modeling, calculations, and visualization.

This project strengthened my ability to approach business questions analytically and present findings in a structured way. I will continue building my portfolio through projects that apply Excel, SQL, Power BI, and Python to practical data analysis problems.
