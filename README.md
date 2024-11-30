# Introduction

This is a SQL to Tableau Project using fictional real work healthcare data.

# Quick Link
[flu_jabs](flu_jabs.sql)
[Dashboard](https://public.tableau.com/views/FluJabs2022/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

# Scenario
As a Junior Data Analyst, I worked on a project to analyze flu jab data from 2022, focusing on vaccination trends and compliance rates. Using SQL for data extraction and Tableau for visualization, I developed a comprehensive dashboard to provide actionable insights into the flu jab campaign’s performance.

# Process
## Querying the dataset
The SQL is to address specific objectives listed in the comment section within the SQL script. There are three components in the script: two Common Table Expression (CTE), and a final query.

The first CTE is active_patients. This identifies patients who were:
1. Active in the hopsital between 2020-01-01 and 2022-12-31
2. Not deceased (pat.deathdate is null)
3. At least six months old as of 2022-12-31
Also, this CTE ensures no duplicate patients (select distinct patient)

The second CTE is flu_shot_2022. This filters records for patients who received flu jabs in 2022, and captures the earliest date each patient received the flu jabs within 2022.

The last query is the final query. It likely combines patient demographic details (e.g. birthdate, race, county, and full name) with information about whether they received the flu jabs. It also integrates results from the active_patients and flu_shot_2022 CTEs.

## Creating Dashboard
After querying the dataset, [flu_jabs](flu_jabs.csv) is generated. Then the csv file is imported to Tableau. To create the dashboard, seven different visuals are made. 

1. A bar graph showing flu jabs by age. 
2. A similar bar graph showing flu jabs by race. 
3. A map showing the geographical data of flu jabs. 
4. A name list showing the full name, age, and whether the person has received flu jabs.
5. The total percentage of compliancing flu jabs.
6. The toal number of flu jabs given.
7. The running sum of flu jabs.

# Key insights
- Vaccination rates were highest among age group 50-64, reflecting strong outreach efforts to this high-risk group.
- Certain racial groups had lower vaccination rates, suggesting potential barriers to access or outreach effectiveness.
- The running sum of jabs revealed a significant Q4 slowdown, indicating a need for additional promotional efforts during that time.

# Recommendations
- Develop outreach programs tailored to underrepresented racial groups, addressing potential barriers like language or mistrust.
- Implement incentives or campaigns during Q4 to sustain momentum and improve overall compliance rates.
- Allocate more resources to underperforming counties based on vaccination percentage data.

# Conclusion
This project demonstrates my ability to work with healthcare data, extract insights using SQL, and build actionable dashboards in Tableau. The insights and recommendations I developed highlight my analytical approach to supporting public health initiatives.