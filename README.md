# PyCitySchools with Pandas

## Overview of the School District Analysis
Maria, the chief data scientist for a city school district, wants help analyzing data on student funding and students' standardized test scores. Aggregating the data and showcasing trends in school performances will assist the school board and superintendent in making decisions regarding the budget allotments.

The school board has notified Maria that the students_complete.csv file shows evidence of academic dishonesty. The math and reading scores for Thomas High School ninth graders need to be replaced with NaNs while keeping the rest of the data intact. Maria also wants a report describing how these changes affected the overall analysis. 

*She is tasked with preparing all standardized testing data for analysis, reporting, and presentation to provide insights about performance trends and patterns. 
These insights are used to inform disucussions and strategic decisions at the school and district level.
With access to every student's math and reading socres as well as various information on the schools they attend. 
Your task is to aggregate the data and showcase trends in school performance.
This analysis will assist the school board and superintendent in making decisions regarding the school budgets and priorities*

## Results
- The Average Math Score, % Passing Math, % Passing Reading, and % Overall Passing columns are all affected in the district summary. Before replacing the ninth grade scores from Thomas High School, the average math score was 79.0, 75% of students were passing math, 86% were passing reading, and 65% were passing overall. After replacing the data with NaNs, all four of those statistics decreased. Below is the updated district summary.

<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/district_summary_df.png">

- In the school summary, only the Thomas High School row was affected. The Average Reading Score increased? The % Passing Math, % Passing Reading, and % Overall Passing values all decreased significantly. Before replacing the ninth grade scores, %93 of Thomas High School students were passing math, 97% were passing reading, and 91% were passing overall. After updating the summary, these percentages decreased to 67%, 70% and 65%, respectively. An updated version of the school summary can be seen below:

<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/by_school_summary_df.png" width="600">

- How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to other schools?

<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/bottom_schools.png" width="700">

- How does replacing ninth-grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type

## Summary
*Summarize four major changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs*

### Resources
- Data Sources: schools_complete.csv, students_complete.csv
- Software: Python 3.7.6, Anaconda 4.8.3
