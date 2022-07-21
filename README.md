# School_District_Analysis
## Overview

Standardized test data for mathematics and reading were analyzed for PyCity Schools to provide the school board with information to assist in making decisions regarding school budget allotments. Analysis includes a summary of performance by the overall district and an aggregation by school within the district. Performance in relation to student funding, school size, and school type is reported. 

After examination of original data files, a suspicion of academic dishonesty of altered scores for 9th grade math and reading at Thomas High School arose.  As such, the affected data were removed, and remaining data reanalyzed. This report describes the impact of redacting this data on the overall district summary and the corresponding aggregations. Data were analyzed and reported using Pandas and Jupyter Notebook.

## Results

The first analysis included all the math and reading scores provided in the data set. The second analysis included the data that remained after ninth grade math and reading scores for Thomas High School were removed. The code used to remove reading scores is pictured below. The same process was used to removed math scores.

![Replacement_Code](https://user-images.githubusercontent.com/108107856/180306288-81244bf5-a4e4-458c-b0e2-b1bd8a5c5fdc.png)


Each point below addresses how the removal of this data impacts various reporting of the results.

* *District Summary* 

  The overall passing percentage is defined as the percentage of students who earn a passing score in both math and reading. The performance levels shown   in each figure below indicate that the removal of the ninth-grade data for Thomas High School bears little impact when examining the district as a       whole.This percentage decrease in overall passing is not enough to be of interest.
  
  
  
  
  

* *School Summary*

  When aggregating the data by school, only the data for Thomas High School is impacted by removing the data. At first glance, it appears that the         overall passing rate for Thomas High School decreases significantly. However, the analysis of the data at this point has had the data points replaced     with NaN but the students are still in the data set. The students were counted by school name so when calculating the percentage of the overall           passing, the 9th grade students are still included in the total students at Thomas High School.  Thus, this result is unreliable.

  The code was refactored to replace each percentage on the Thomas High School summary with percentages using only data points from tenth, eleventh, and   twelfth grade students. After this analysis, it appears that the overall passing rate does not change significantly. However, when using this school     summary to compare to other schools, it should be noted that all other schools were analyzed using grade levels 9 – 12 whereas Thomas High School         accounted for only 10 –   12 grades.

* *Thomas High School Performance*



* *Grade Level Scores*

   Removing the 9th grade math and reading scores at Thomas High School only impacts the grade level scores for that grade at that school. All scores at
   other locations remain the same as well as the remaining grade levels at Thomas High School.

* *Scores by School Spending*

  Thomas High School falls in the $631-$645 spending range (per student) so this is the only row that has the potential to change.  As represented in the   tables below, the data has actually not changed with the new analysis. This data is calculated by taking the budget and dividing by the number of
  students in the school. The analysis only changed the original scores for 9th grade to NaN, however, the students were not removed from the data set so   the total students stayed the same. The only calculation that took into consideration the adjusted student total excluding 9th grades were the 
  percentages in per school summary.


* *Scores by School Type*

