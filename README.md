# School District Analysis

## Overview of Project: 
Analyze school district results for city. 
### Purpose:
Perform data analytics on school and student information and present results in a format that helps reveal performance trends and patterns. This will help the school board and superintendent to make decisions for strategic budgeting based on standardized test scores and student funding.   

## Results:
Jupyter Notebook, the primary development environment used by Maria the chief data scientist and her team, was used to read, inspect, and clean .csv files for both the school information and student information (see below image for examples of code). Once cleansed and properly formatted Jupyter Notebook was used to merge data tables, perform calculations, and create tables.  
![]()
### Purging of Data: 
Unfortunately, during the analysis the school board informed us of academic dishonestly. More specifically the reading and math scores collected for the ninth graders at Thomas High School (THS) had been altered and we were asked to null out (NaN) all standardized test scores for that category.  
-How is the district summary affected?
	-Fortunately, the district summary table had minimal to no affected on the total outcome of the results as the number of ninth graders for THS represented a small portion of the total number of students for the district. See the below images for comparison of district summary.  

![]()![]()

-How is the school summary affected?
	-The same can not be said for the school summary table. As you can see from the images below, the “% Passing Reading, “% Passing Math”, and “% Overall Passing” for Thomas High School saw significant increases in values. Ranging anywhere from 17-25% mark up. This is due to the ninth-grade student being removed from the total student population for Thomas High. 
![]()![]()

-How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
	-Thanks to this adjustment in calculations for THS, the “% Overall Passing” values increased to 90.6% making them one of the top performing schools in the district. See the below image for top 5 performing schools. 
![]()![]()

-How does replacing the ninth-grade scores affect the following:
*Math and reading scores by grade
Similarly, to the district summary the math and reading scores by grade had no changes as the academic dishonestly only affected the overall outcome for the ninth grades at Thomas High School. See below images for comparison of the reading scores. 
![]()![]()
*Scores by school spending
Even though the ninth-grade scores for THS was nulled out, the spending per student stayed the same as the total number of students were considered for this table. The results of the recalculated math, reading, and overall passing categories did bolster and increase for the spending range “$630-644”. 
![]()
*Scores by school size
In addition to school spending, scores by school size saw an equivalent increase for math, reading and overall passing percent for each category within the “Medium (1000-2000)” range. 
![]()
*Scores by school type
As Thomas High School is a “Charter” school, when tabled by school type. The charter subset saw an increase for math and reading scores as well as the overall passing percent. 
![]()


## Summary: 
Due to the academic dishonest, we were required to add additional code to properly account for the requested changes in the dataset by the school board. 
-First, we needed to remove or null out the math and reading scores for all ninth grades at Thomas High School (see below image for updated code). This was mandated by the school board as they could not derive the level of tampering for 9th grade at THS. 
![]()
-Second, new code was needed to accurately reflect the number of students in the ninth grade at THS and remove that student count from the total student body at THS.
-Thirdly, more code was scripted to update the “% Passing Math”, “% Passing Reading”, and “% Overall Passing” for Thomas High to only include the 10th, 11th, and 12th grade scores. See below image for the code that was scripted for the ninth-grade count and recalculated scores. 
![]()
-Lastly, all these updated values had to be integrated back into the school summary table to accurately depict the school district analysis. 
