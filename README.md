# Case Study: Analyzing Job Market Data in Power BI

![](https://github.com/yanny-alt/Job-Market-Analysis-with-Power-BI/blob/main/Images/Job%20Market%20Analysis.jpg)

## Background

In this project, I’ll be analyzing a real-world job posting dataset to find insights for DataSearch, a fictional recruiting firm. I’ll explore and clean the data with Power Query to see what skills are most in demand for data scientists, analysts, and engineers. I’ll then use DAX to build insightful visualizations of my findings. Finally, I’ll bring it all together using everything Power BI has to offer to create a business dashboard so that I can answer questions for the DataSearch team.

## Data Analytics Pipeline

1. **Data Integrity Check**: I ensured the data’s integrity before beginning exploratory data analysis.
2. **Business Questions**: I formulated business questions about the job market trends.
3. **Visualizations**: I employed a variety of visuals and fundamental DAX calculations for investigation.
4. **Dashboard Development**: I created user-friendly visuals for key stakeholders.

## Problem to Solve

DataSearch, an employer recruiting agency, needs insight into data science employment market trends. I’ll be tasked with identifying trends in top data science jobs and their associated skills using a dataset of job posts.

[Link to The Interactive Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiN2U1MWRiY2YtNGQwYS00ZDUyLWI5MmUtYjQxYmNhMTkzNmYzIiwidCI6IjQ5MWM2ZTNhLTA3MjItNDhmMi1iMDFhLWFhMzliODc0MGYxNiJ9)

## The Data

The dataset is fictitious, comprising job postings in the data science industry over the last five years, with 19 attributes per posting. It includes both qualitative and quantitative columns, such as:

- **Qualitative**: Job ID, title, type, level, required skills.
- **Quantitative**: Posting dates, experience level, salary range, number of applicants.

## Exploratory Data Analysis (EDA) Questions

1. What is the average salary in data science?
2. What are the most popular jobs in data science?
3. Which data analytical skills correlate to job postings?
4. How frequent are job postings being posted?

## Initial EDA with Power Query

- Less than 1% of data is missing for Company Name.
- High percentage of empty values in salary and applicant columns.
- 70% of the Job title additional information column is empty.

## Job Posting Trend Analysis

- **Experience vs. Position Level**: Higher experience correlates with higher job positions.
- **Trends over Time**: Notable decrease in job listings in March 2020 due to COVID-19.

## Data Cleanup of Job Titles

I focused on key positions: Data Scientist, Data Analyst, Data Engineer, Machine Learning Engineer, and Data Science Manager.

## Insights from EDA

1. **Empty Salary Values**: There are many empty values for the salary information, indicating that salary details are often not disclosed in job postings.
2. **Experience and Salary Correlation**: As years of experience increase for a job, so does the associated salary, reflecting the value of experienced professionals in the industry.
3. **Job Postings Trend**: Job postings over the past five years are trending upwards, suggesting a growing demand for data science professionals.
4. **Demand for Data Engineers**: Data Engineers are the most popular and in-demand role in data science, highlighting a critical area for recruiters to focus on.

## Market Insight Analysis

1. **Increasing Job Openings**: The number of job openings is increasing with time, which is great news for DataSearch. The rise in demand for data science roles presents opportunities for growth.
2. **Top Positions**: Data Engineers, Scientists, and Analysts are among the most in-demand positions. To optimize our efforts, we should concentrate on these roles in our next examination.
3. **High Demand in Tech Industry**: Data science positions are in high demand in the technology industry, offering well-paying and growing career opportunities.

## Diving Deeper into the Dataset

Although I was able to perform a high-level analysis of the data earlier, I will now delve deeper into some columns to uncover additional insights. Using compelling visuals will aid in this discovery process. I aim to determine if there’s any link between skills and specific job titles, and identify the top industries and companies hiring for these positions. Finally, I will make recommendations to stakeholders based on these findings.

## Key Insights to Focus On

- Are certain companies targeting particular job types, experience, or skills?
- Is there a minimum expected experience level for certain roles or skills?
- What are the top skills needed for entry-level data scientists?
- Which industries have the most competitive salaries?

## Cleanup and Skill Analysis

### Skill Column Preparation

- **Job Skills Column**: The Job Skills column contains values in a list (e.g., ['python', 'power_bi', …]). This column needed to be cleaned up before further analysis.
- **Duplication and Renaming**: I duplicated the current job posting table, renamed the duplicated column to 'job skills', and removed all columns except Job Posting ID & Job Skills.
- **Cleanup Process**: I cleaned up the Job Skills column by removing brackets, quotes, and spaces, leaving only the comma as the delimiter.
- **Splitting Column**: I split the Job Skills column by the delimiter to make a row for each skill along with the associated Job Posting ID.
- **Removing Blanks**: I removed rows with blank values in the Job Skills column.

### Skill Analysis

- **Power BI Skills**: I noticed that Power BI was categorized under two entries, 'powerbi' and 'power_bi'. I standardized this by replacing 'powerbi' with 'power_bi'.

## Likelihood of Skills in Job Posting

Using DAX, I created a measure called 'posting counts' that counts the job posting IDs, and a measure called 'skill count' that counts the number of skills. The ratio (skill count / posting count) = %skill in posting provided insights on the likelihood of particular skills being featured in job postings. 

### Key Findings

- **Python**: Python is a top skill for Data Scientists and Data Science Managers.

## Trends in Skills Over Time

I explored how skills in job postings have trended over time. For Data Analysts, Engineers, and Scientists, the metrics have shown fluctuations on a short-term basis but have maintained relative consistency over the past few years.

## Deep Dive into Key Job Descriptions

For DataSearch, I performed an in-depth analysis of the top companies and industries hiring data scientists. Using a visualization that includes both Posting Count and Job Position Level, I filtered down to the top 10 industries by the number of job posts, with a specific focus on mid-level roles in the internet industry.

### Key Insight

- **Topal**: This company appears to be employing a large number of Data Engineers and Data Scientists, a significant finding for DataSearch.

## Other Job Recommendations

I explored job titles with similar requirements to the five key job titles analyzed earlier. For example, I found that both business analyst and data analyst roles require skills in SQL, Excel, Tableau, database, and cloud.

## Job Posting by Company Size

Most job postings came from smaller sized companies, indicating that smaller firms are actively seeking data science professionals.

## Dashboard Development

### Begin Dashboard Template

I structured the dashboard with slicers on the left, a header, and charts below.

### Interactive Dashboards

Ensuring the slicers were responsive, I verified that questions like "What was the average years of experience for data scientists in the computer software industry in 2021?" could be answered.

### Skill Dashboard

Including visuals from the skill analysis, I verified the cards worked properly by checking questions like "How many job postings for a data analyst list SQL as a required skill?" (1425 postings).

### Salary Analysis Dashboard

I created a gauge for salary visualization, including average pay, average minimum pay, and average maximum pay. To test the gauge, I asked "What is the typical compensation for an entry-level data scientist in the computer software industry?" ($97.75K).

## Conclusion

I have completed all major portions of the data analytics pipeline, progressing from integrity checks and exploration to identifying insights in the data science job market. Additionally, I created an interactive dashboard for DataSearch to utilize in future recruiting efforts. This final dashboard helps communicate insights effectively, allowing recruiters to better inform their clients about the most in-demand roles, skills, and companies.

## Dashboard Snapshots

- **Homepage**
  ![](https://github.com/yanny-alt/Job-Market-Analysis-with-Power-BI/blob/main/Images/DataSearch%20Homepage.png)
- **Job Page**
  ![](https://github.com/yanny-alt/Job-Market-Analysis-with-Power-BI/blob/main/Images/DataSearch%20Jobs%20Overview.png)
- **Skill Page**
  ![](https://github.com/yanny-alt/Job-Market-Analysis-with-Power-BI/blob/main/Images/DataSearch%20Skills%20Overview.png)
- **Company Page**
  ![](https://github.com/yanny-alt/Job-Market-Analysis-with-Power-BI/blob/main/Images/DataSearch%20Company%20Overview.png)

## Call to Action

Thank you for reading! Your feedback is appreciated. If you are interested in learning more about my work or discussing potential opportunities, please feel free to connect with me:

- [LinkedIn](https://www.linkedin.com/in/favourokechukwu/)
- [Medium](https://medium.com/@favour.okechukwu)
- [Portfolio Website](https://favourigwezeke.vercel.app/)
