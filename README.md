# Introduction:
Dive into the data job market! Focusing on data analyst roles, this project explores & top-paying jobs, in-demand skills, and where high demand meets high salary in data analytics.

SQL quaries? Check them out here : [projects_sql](/projects_sql/)

# Background 

Driven by a quest to navigate the data analyst job market more effectively, this project was born from a desire to pinpoint top-paid and in-demand skills, streamlining others work to find optimal
jobs. Data hails from my [sql_load](//sql_load/lukebarousse.com/sql). It's packed with insights on job titles, salaries, locations, and essential
skills.

### The questions I wanted to answer my SQL queries were 

    1. What are the top-paying data analyst job?
    2. What skills are required for these top-paying jobs?
    3. What skills are most in demand for data analysts?
    4. Which skills are associated with higher salaries?
    5. What are the most optimal skills to learn?

# Tools I Used

For my deep dive into the data analyst job market, I harnessed the power of several key tools:

- **SQL**: The backbone of my analysis, allowing me to query the database and unearth critical insights.

- **PostgreSQL**: The chosen database management system, ideal for handling the job posting data.

- **Visual Studio Code**: My go-to for database management and executing SQL queries.

- **Git & GitHub**: Essential for version control and sharing my SQL scripts and analysis, ensuring collaboration and project tracking.

# The Analysis

Each query for this project aimed at investigating specific aspects of the data analyst job market. Here's how I approached each question:


### 1. Top paying Data Analysis Jobs 

To identify the highest-paying roles II filtered data analyst positions by average yearly salary and location, focusing on remote jobs. This query highlights the high paying opportunities in the field.

```sql

 SELECT
    job_id,
    job_title,
    job_location,
    salary_year_avg,
    job_posted_date,
    name AS company_name 
FROM 
    job_postings_fact
LEFT JOIN company_dim ON job_postings_fact.company_id = company_dim.company_id
WHERE
    job_title_short = 'Data Analyst' AND 
    job_location = 'Anywhere' AND 
    salary_year_avg IS NOT NULL
ORDER BY 
    salary_year_avg DESC
LIMIT 10

```
Here's the breakdown of the top data analyst jobs
in 2023:
- **Wide Salary Range:** Top 10 paying data
analyst roles span from $184,000 to $650,000,
indicating significant salary potential in the
field.

- **Diverse Employers:** Companies like
SmartAsset, Meta, and AT&T are among those
offering high salaries, showing a broad interest
across different industries.

- **Job Title Variety:** There's a high diversity
in job titles, from Data Analyst to Director of
Analytics, reflecting varied roles and
specializations within data analytics.

![Top Paying Roles](assets\1_top_paying_roles.png)
#  What I Learned 

Throughout this adventure, I've turbocharged my SQL toolkit with some serious firepower:

🧩 **Complex Query Crafting**: Mastered the art of advanced SQL, merging tables like a pro and wielding WITH clauses for ninja-level temp table maneuvers.

📊 **Data Aggregation**: Got cozy with GROUP BY and turned aggregate functions like COUNT() and AVG() into my data-summarizing sidekicks.

💡 **Analytical Wizardry**: Leveled up my real-world puzzle-solving skills, turning questions into actionable, insightful SQL queries.


# Conclusion 

From the analysis, several general insights emerged:

1. **Top-Paying Data Analyst Jobs** : The highest-paying remote data analyst jobs offer a wide range of salaries, with the top positions reaching up to $650,000.

2. **Skills for Top-Paying Jobs**: High-paying data analyst jobs require advanced proficiency in SQL, suggesting it’s a critical skill for earning a top salary.

3. **Top In-Demand Skills**: SQL is crucial for job seekers as it is the most demanded skill in the data analyst job market.

4. **High-Paying Skills** : Niche expertise in specialized skills like SVN and Solidity commands the highest average salaries, highlighting their premium value.

5. **Optimal Skills for Job Market Value**: SQL leads in demand and offers for a high average salary, positioning it as one of the most optimal skills for data analysts to learn to maximize their market value.


# Closing Thought 

This project improved my SQL skills and offered valuable insights into the data analyst job market. The analysis results serve as a guide for prioritizing skill development and job search efforts. By concentrating on high-demand, high-salary skills, aspiring data analysts can better position themselves in a competitive job market. This exploration underscores the importance of continuous learning and staying updated with emerging trends in data analytics.











