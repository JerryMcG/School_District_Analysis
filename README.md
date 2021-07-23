# School_District_Analysis
## Overview

In this assignment we are working with Maria, who is a chief data scientist for City School Districts. She analyzes student funding and standard test data which is used to report and present insights around performance trends and budget allocations. This analysis then feeds into strategic decisions which are made at the school and district level. Our task is to look at the Student funding and test score data, aggregate and identify trends while adhering to FERPA requirements. Once the initial analysis is complete, Maria has been informed that Grade 9 math and reading scores from Thomas High School appear to have been altered. This data now needs to be eliminated from our analysis to maintain the integrity of our overall analysis. 

## Results

* How is the district summary affected?

We can see that the % for passing Math, Reading and overall have all dropped:
|Metric|Before|After|
|% passing math|74.981|74.760|
|% passing reading|85.805|85.660|
|% overall passing|65.172|64.856|

* How is the school summary affected?

We can see that the % for passing Math, Reading and overall have all dropped:
|Metric|Before|After|
|% passing math|93.272|93.186|
|% passing reading|97.309|97.019|
|% overall passing|90.948|90.630|

* How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
Thomas High School remains in the same position within the top 5 schools after we adjusted the overall % by recalculating with ninth graders removed from total student counts. 

* How does replacing the ninth-grade scores affect the following:
** Math and reading scores by grade
*** Only impact is that Thomas High School now shows nan for 9th grade scores for Math and Reading
** Scores by school spending
Scores in range $585-629 & $630-644  have increased as a result of replacing these grades. 
** Scores by school size
no impact to the data
** Scores by school type
no impact to the data

## Summary

Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

* Per School Summary scores change significantly before we factored in the new student count (removing 9th grade count) to calculate the scores. If we had not factored in this change it would have unfairly represented a significant change in Thomas High School Summary level data. Scores dropped from within 90% range to 60% range but once we factored in the new student count, %'s still changed but these were marginal changes of a few decimal points. 

* District Summary. Overall each percentage dropped by 2-3 tenths of a % for each of the percentages calculated. This was a marginal change in relation to the large amount of students who were included in the analysis. 

* Math and Reading Scores Per Grade. Now when we look at the grade level scores for each school, we can clearly see there was an issue with 9th grade data from Thomas High School. This is indicated by the NaN value which is now held in the table.
* Scores by School Spending. When we run this analysis again we can see that the scores in ranges $585-629 & $630-644 have increased as a result of replacing the altered data. This double change is not what i had expected. Since Thomas High School is a Medium School which has a spending range of $630-644 per student, I would not have expected changes in the $585-629 data. However I have come to the conclusion that there may be a variance in the data somewhere which i have overlooked to result in this change. I believe only the $630-644 value should be altered by our replaced values. 
