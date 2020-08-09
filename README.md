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
- Replacing ninth-grade scores at Thomas High School affects the Average Math Score, % Passing Math, % Passing Reading, and % Overall Passing columns in the district summary. Before replacing the ninth grade scores from Thomas High School, the average math score was 79.0, 75% of students were passing math, 86% were passing reading, and 65% were passing overall. After replacing the data with NaNs, all four of those statistics decreased. Below is the updated district summary.

<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/district_summary_df.png">

- In the school summary, only the Thomas High School row is affected. The first 5 values were unchanged. The average reading score increased from 83.8 to 83.9 and the % Passing Math, % Passing Reading, and % Overall Passing values all decreased significantly. Before replacing the ninth-grade scores, 93% of Thomas High School students were passing math, 97% were passing reading, and 91% were passing overall. After updating the summary, these percentages decreased to 67%, 70% and 65%, respectively. An updated version of the school summary can be seen below:

<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/by_school_summary_df.png" width="600">

- Replacing the ninth graders' math and reading scores affects Thomas High School's performance relative to other schools by removing it from the top 5 schools based on the percentage of students passing overall. After making the necessary adjustments to the data, Thomas High School becomes the 8th best performing school in this category. Holden High School is 7th with 89% of their students passing overall and Bailey High School is 9th with 55%.

- Average school scores based on school spending, size, and type were affected in the following manner:
- How does replacing ninth-grade scores affect the following:
  - For the average math and reading scores by grade, the ninth grade values for Thomas High School are NaN.
  - For averages by school spending, the row containing Thomas High School was affected ($630-644 Per Student). The average math and reading scores were unchanged. The % Passing Math, % Passing Reading, and % Overall Passing values all decreased. Before replacing the ninth-grade scores, 73% of students attending schools in this range were passing math, 84% were passing reading, and 63% were passing overall. The upated percentages can be seen in the dataframe printed below.
  
<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/spending_summary_df.png" width="750">
  
  - Scores by school size
  - Scores by school type

## Summary
*Summarize four major changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs*

### Resources
- Data Sources: schools_complete.csv, students_complete.csv
- Software: Python 3.7.6, Anaconda 4.8.3
