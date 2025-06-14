# HR-Analysis

## Overview
This project involves the design and implementation of an interactive Power BI dashboard for monitoring of key HR metrics. The dashboard enables data-driven analysis to assess the impact of various organizational and employee-related factors on HR performance indicators.
## Objectives
Develop a dynamic and interactive Power BI dashboard to visualize key HR metrics such as employee turnover, retention rate, and headcount trends.

Identify and analyze correlations between HR performance indicators (e.g., employee satisfaction) and potential influencing factors such as department, tenure.

Enable data-driven decision-making by providing insights into workforce demographics, recruitment pipeline.

Monitor diversity and inclusion metrics (e.g., gender distribution, minority representation) to support organizational DEI (Diversity, Equity, and Inclusion) initiatives.

Conduct comparative analysis across different business units, locations, or teams to highlight areas requiring HR intervention or policy adjustments.

## Dataset
This is an HR dataset including 311 rows and 35 columns.</br>
</br>
Columns Data Types:
- Employee Name	Text
- EmpID	Text
- MarriedID (1 or 0 for yes or no)	Binary
- MaritalStatusID	Integer
- EmpStatusID	Integer
- DeptID Integer
- PerfScoreID Integer
- FromDiversityJobFairID (1 or 0 for yes or no)	Binary
- Salary	Float
- Termd	Binary
- PositionID Integer
- Position	Text
- State	Text
- Zip	Text
- DOB	Date
- Sex Text
- MaritalDesc	Text
- CitizenDesc	Text
- EmployeeID	Integer
- EmployeeName	Text
- Department	Text
- JobRole	Text
- Location	Text
- Age	Integer
- Gender	Text
- Tenure	Decimal
- PerformanceRating	Integer
- AttritionFlag	Boolean
- TerminationDate	Date
- HireDate	Date
- Salary	Decimal
- Bonus	Decimal
- TrainingHours	Integer
## Data Wrangling
- Reformating: replacing "M" by "Male" and "F" by "Female" in Sex column.
- Binning: added column Salary Bins and assigned each salary value to a bin.
- Renaming Column: renamed column EngagementSurvey to EngagementScore which is more descriptive.
## Dax Measures
Below is a description of each Hr Metric implemented as Dax measures, which allows flexible and insightful analysis based on different data contexts. 
- Number of Employees: Total number of employees either active or terminated.
- Headcount: Number of active employees.
- Male %: percentage of males from headcount.
- Female %: percentage of females from headcount.
- Retention Rate (%): percentage of employees who remained employed over a specific period, in this case measured annualy.
- Number of Terminations: Number of employees who no longer work for this company.
- Terminated Voluntarily %: Percentage of employees who no longer work for this company by their choice.
- Terminated for a Cause %: Percentage of employees who are terminated for a cause.
- Employee Turnover Rate (%): Percentage of employees who left the company to average number of emplyees over a specific period in our case its measured annualy.
- High Performing Employees: Number of employees who's performance score field is either "fully meets" or "exceeds".
- Average Engagement Score: Average of employee's engagement score.
- Average Employee Satisfaction: Average of emploeyee's satisfaction score.
## Dashboard
This is a 3-page dashboard (Employee Overview - Attrition - Performance) that gives insights into:</br>
</br>
1- Employee Overview:
- Headcount.
- Male Percentage.
- Female Percentage.
- Annual Retention Rate.
- Headcount by Citizen Description.
- Headcount by State.
- Headcount by Marital Status.
- Headcount by Department.
- Headcount by Recruitment Source.
- 
2- Attrition:
- Number of Terminations.
- Terminated Voluntarily Percentage.
- Terminated for a Cause Percentage.
- Annual Retention Rate.
- Number of Terminations by Department.
- Top 3 Termination reasons and their count.
- Number of Terminations by Performance Score.
- Number of Terminations by Employee Satisfaction.
- Number of Terminations by Salary.
-
3- Performance:
- Number of High Performing employees.
- Average Engagement Score.
- Average Employee Satisfaction.
- Performance Score Distribution.
- Employees Needing Improvement (Performance) across Departments distribution.
- Average Engagement Survey by Department.
- Average Employee Satisfaction by Department.
- Average Employee Score by Department.
## Insights
- There is a total of 207 employees who currently work for the company, 44% of them are males and 56% females.
- Retention Rate across the years is relatively good (> 90%) and the lowest Retention Rates are for years 2011, 2016 which is exactly 90%.
- 96% of employees are citizens adn around 4% are non-citizens.
- Massachusetts state has the highest number of employees (177 employees).
- 126 employees (60%) are in production department and the rest are distributed between IT/IS, sales, admins, software engineering and 1 employee in executive office.
- Indeed and Linkedin together are the sources for recruiting 144 of our current employees (around 70%).
- Total number of terminations is 104 employees 85% was volantarily and 15% was for a cause.
- Turnover Rate across the years is usually 10% or less except for year 2011 which was 15% and 2015 which was 11%.
- 83 employees (80%) of employees are from production department.
- Top 3 termination reasons are for another position, more money or because they were unhappy.
- 83 terminated employees fully met the performance expectations.
- 100 terminated employees had satisfaction score of 3 or more.
- 81 terminated employees had salaries between range 50k-100k and almost non who had salaries between 150k-250k were terminated.
- 191 of current employees are high performing .
- Average engagement score is 4.1.
- Average employee satisfaction is 3.9.
- Employees who's performance needs distribution are distributed between Production, IT/IS, software engineering, sales . Production has 15 employees needing performance which is more tha other departments.
- Executive office and admin offices have highest average engagement score which is 4.8 and 4.6.
- Average employee satisfaction is the lowest in executive office which is 3.0
- Non Citizens have higher employee satifaction score (>4.0) than citizens 3.87.
