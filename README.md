# PyCitySchools with Pandas

## Overview of the School District Analysis
Maria, the chief data scientist for a city school district, wants help analyzing data on student funding and students' standardized test scores. Aggregating the data and showcasing trends in school performances will assist the school board and superintendent in making decisions regarding the budget allotments.

The school board has notified Maria that the students_complete.csv file shows evidence of academic dishonesty. The math and reading scores for Thomas High School ninth-grade students need to be replaced with NaNs while keeping the rest of the data intact. Maria wants a report describing how these changes affected the overall analysis. 

## Results
- In the district summary, the Average Math Score, % Passing Math, % Passing Reading, and % Overall Passing columns are all affected. Before replacing the ninth grade scores from Thomas High School, the average math score is 79.0, 75% of students were passing math, 86% were passing reading, and 65% were passing overall. After replacing the data with NaNs, all four of those statistics decreased. Below is the updated district summary:

<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/district_summary_df.png">

- In the school summary, only the Thomas High School row is affected. The first 5 values are unchanged. The average reading score increased from 83.8 to 83.9 and the % Passing Math, % Passing Reading, and % Overall Passing values all decreased significantly. Before replacing the ninth-grade scores, 93% of Thomas High School students were passing math, 97% were passing reading, and 91% were passing overall. After updating the summary, these percentages decreased to 67%, 70% and 65%, respectively. An updated version of the school summary can be seen below:

<img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/by_school_summary_df.png" width="600">

- Replacing the ninth graders' math and reading scores affects Thomas High School's performance relative to other schools by removing it from the top 5 schools based on the percentage of students passing overall. After making the necessary adjustments to the data, Thomas High School becomes the 8th best performing school in this category. Holden High School is 7th with 89% of their students passing overall and Bailey High School is 9th with 55%.

- Average school scores based on school spending, size, and type are affected in the following manner:
- Replacing ninth-grade scores also affects averages by grade, school spending, school size, and school type:
  - For the average math and reading scores by grade, the ninth grade values for Thomas High School are NaN.
  - For averages by school spending, the row containing Thomas High School is affected ($630-644 Per Student). The average math and reading scores are unchanged. The % Passing Math, % Passing Reading, and % Overall Passing values all decreased. Before replacing the scores, 73% of students attending schools in this range were passing math, 84% were passing reading, and 63% were passing overall. The upated percentages can be seen in the dataframe printed below:
  <img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/spending_summary_df.png" width="700">
  
  - For averages by school size, the Medium (1,000-1,999) row is affected. The average math and reading scores are unchanged. Before replacing the ninth-grade scores, 94% of students attending medium sized schools were passing math, 97% were passing reading, and 91% were passing overall. The updated percentages can be seen below:
  <img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/size_summary_df.png" width="700">
  
  - For averages by school type, the Charter row is affected. The average math and reading scores are unchanged. Before replacing the scores, 94% of students attending charter schools were passing math, 97% were passing reading, and 90% were passing overall. The updated percentages can be seen in the dataframe below:
  <img src="https://github.com/npantfoerder/school-district-analysis/blob/master/Resources/type_summary_df.png" width="700">

## Summary
- One major change in the updated school district analysis is the Thomas High School row in the school summary. Although the first 5 values do not change and the average reading score increased by 0.1, all of the passing percentages decreased significantly. Replacing all of the ninth-grade scores with NaNs decreases these percentages since the total number of students does not change, but none of ninth-grade scores are greater than 70.

- A second major change in the updated analysis is how Thomas High School is ranked in comparison to the other schools in the district. In the results, we saw that Thomas High School moved from being one of the top 5 schools based on % Passing Overall, to the 8th school. When sorting the school summary by % Passing Reading, Thomas High School goes from being the top school to the 8th school. Thomas High School also moves from the 7th to the 9th ranked school based on % Passing Math. 

- Another big change in the updated analysis is the $630-644 row in the dataframe grouped by school spending per student. Thomas High School was one of 4 schools in this spending range. Once again, the % Passing Math, % Passing Reading, and % Overall Passing values all decreased. 

- A fourth big change in the updated analysis after the ninth-grade scores are replaced is the Medium (1,000-1,999) row in the dataframe grouped by school size. Thomas High School was one of three medium sized schools. Here, the % Passing Math, % Passing Reading, and % Overall Passing values all decreased by 6. 

### Resources
- Data Sources: schools_complete.csv, students_complete.csv
- Software: Python 3.7.6, Anaconda 4.8.3
