# School_District_Analysis
## Overview

Standardized test data for mathematics and reading were analyzed for PyCity Schools to provide the school board with information to assist in making decisions regarding school budget allotments. Analysis includes a summary of performance by the overall district and an aggregation by school within the district. Performance in relation to student funding, school size, and school type is reported. 

After examination of original data files, a suspicion of academic dishonesty of altered scores for 9th grade math and reading at Thomas High School arose.  As such, the affected data were removed, and remaining data reanalyzed. This report describes the impact of redacting this data on the overall district summary and the corresponding aggregations. Data were analyzed and reported using Pandas and Jupyter Notebook.

## Results

The first analysis included all the math and reading scores provided in the data set. The second analysis included the data that remained after ninth grade math and reading scores for Thomas High School were removed. The code used to remove reading scores is pictured below. The same process was used to removed math scores.

![Loc Code](/Resources/Loc_Code.png)


Each point below addresses how the removal of this data impacts various reporting of the results.

* *District Summary* 

  The overall passing percentage is defined as the percentage of students who earn a passing score in both math and reading. The performance levels shown   in each figure below indicate that the removal of the ninth-grade data for Thomas High School bears little impact when examining the district as a       whole. This decrease in overall passing percentage is minimal.
  
  Initial Analysis: 
  
  ![District Summary](/Resources/District_Summary.png)
  
  Modified Analysis:
  
  ![District Summary Modified](/Resources/District_Summary_Modified.png)
  
  
  
  
  
  

* *School Summary*

  When aggregating the data by school, only the data for Thomas High School is impacted by removing the data. At first glance, it appears that the         overall passing rate for Thomas High School decreases significantly. However, the analysis of the data at this point has had the data points replaced     with NaN but the students are still in the data set. The students were counted by school name so when calculating the percentage of the overall           passing, the 9th grade students are still included in the total students at Thomas High School.  Thus, this result is unreliable.
  
  ![Per School Summary](/Resources/Per_School_Summary.png)
  

  The code was refactored to replace each percentage on the Thomas High School summary with percentages using only data points from tenth, eleventh, and   twelfth grade students. After this analysis, it appears that the overall passing rate does not change significantly. However, when using this school     summary to compare to other schools, it should be noted that all other schools were analyzed using grade levels 9 – 12 whereas Thomas High School         accounted for only 10 –   12 grades.

* *Thomas High School Performance*



* *Grade Level Scores*

   Removing the 9th grade math and reading scores at Thomas High School only impacts the grade level scores for that grade at that school. All scores at
   other locations remain the same as well as the remaining grade levels at Thomas High School.

* *Scores by School Spending*

  Thomas High School falls in the $631-$645 spending range (per student) so this is the only row that has the potential to change.  As represented in the   tables below, the data has actually not changed with the new analysis. This data is calculated by taking the budget and dividing by the number of
  students in the school. The data modification only changed the original scores for 9th grade to NaN, however, the students were not removed from the 
  data set so the total students stayed the same. The only calculation that took into consideration the adjusted student total excluding 9th grades were 
  the percentages in per school summary for Thomas High School.


* *Scores by School Type*

  Thomas High School is classified as a Charter school so this is the only row that has the potential to change. Again, this analysis was completed using
  the total student count, consequently, there is no difference among the results of each analysis.
  
## Summary

In summary, there was little change in the school district analysis after the reading and math scores for the nigth grade at Thomas High School were reaplaced with NaNs. The following observations can be made:

1. The overall passing percentage for Thomas High School decreased 0.3%.
2. The overall passing percentage for district also decreased by 0.3%
3. The average math score for the district decrease 0.1 points. 
4. 

