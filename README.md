# School District Analysis

## Overview of Project

Using python code and pandas to perform an analysis of a school district with district, school, and class subject summary tables generated.

### Purpose

Python code and pandas are used to perform an analysis of a school district's data set.  This allows for quick processing and analysis of a large data set to develop summary tables that communicate findings to further analysis and deductions about the data.  Summary tables for the district, the schools in the district, and additional details for the schools were developed.  

While processing the data set, there was evidence that the ninth grader math and reading scores from Thomas High School appeared to be altered.  To not influence the analysis summaries, these scores were removed and Thomas High School percentages were replaced to only reflect the school's tenth through twelfth graders' scores.  

## Analysis Results and Challenges

### Analysis of Outcomes 

#### District Summary
The district summary for the math, reading, and overall passing percentages were minorly affected by removing the Thomas High School's ninth grader math and reading scores.  After score removal, the district summary math and reading percentages lowered by approximately 0.1% while the overall passing percentage rose by approximately 0.2%.  Since it was only one grade level from one school that was removed from the data set, the overall district summary was not significantly impacted but more focused school summary tables created from the dataset reflect the dataset modifications.

##### Updated District Summary
![](images/district_summary.png)

#### School Summary

The school summary row for Thomas High School was updated to reflect lower math, reading, and overall passing percentages when the ninth grader scores were removed.  When the ninth grade scores were removed, the passing percentages for math, reading, and overall need to be re-calculated to include only tenth through twelfth graders in the student count.  Before the student count for the percentage calculations was modified, significantly lower passing percentages could be seen.  Once the Thomas High School student count was modified to only reflect the tenth through twelfth graders since the ninth grader scores were removed, the school passing percentages were minorly lowered from when the ninth graders scores and counts were previously included. 

##### Updated School Summary
![](images/school_summary.png)


### Additional Results with Dataset Modification

When the ninth-grade scores were removed, the following affects are observed:

-- Math and reading scores by grade summary tables: the summary tables show that the ninth graders' math and reading scores where replaced to "NaN" (Not a Number) to reflect that their scores were not included in the math, reading, and overall percentage calculations.  Because they were removed, all ninth grade scores across schools in the district cannot be equally compared.  Also as a result of removing the ninth graders' scores, the Thomas High School student count was updated to remove the ninth graders in the math, reading, and overall percentage calculations so that the score removal impact is appropriately reflected in the performance related analysis.

-- Scores by school spending:  there was no impact to the scores by school spending, except to the passing percentages displayed as previously mentioned, because the true total number of students at Thomas High School was included for the spending categorization (ninth graders were not excluded from that student count).  Even though the Thomas High School student count was modified to remove the ninth grades in the passing percentage calculations, the number of ninth graders needed to be included in the overall spending calculations because money is still spent on them at the school.  It was only the ninth graders' subject scores that were in question and not their attendance at school. 

-- Scores by school size:  as with school spending, the Thomas High School ninth graders need to remain in the total school count to account for their attendance at the school. Removing the ninth graders' with the student count is relevant for their infuence on the passing percentages for math and reading but not relevant for comparing the categories of school sizes within the district.

-- Scores by school type:  the ninth graders' scores and impact on school passing percentages are irrelevant to the categorization of Thomas High School's school type as their scores would not change that Thomas High School is a Charter school.  And based on the precision used for these scores, no impact is visible following Thomas High School score modification.  

### Challenges and Difficulties Encountered

No challenges were encountered during the analysis. But assumptions or additional actions that needed to be made include:

*By removing the Thomas High School ninth graders' scores, the passing percentages (math, reading, and overall) were re-calculated to only include and reflect the passing percentages for the tenth through twelfth graders at the school (e.g. Thomas High School student count used to calculate a passing percentage only includes tenth through twelfth graders).  As a result of this modification for Thomas High School, all passing percentages were impacted.  But because the ninth graders' impact to Thomas High School overall percentages was minor, the summary dataframe values' precision (e.g. increasing or decreasing it) can reflect the modification impact.  Higher precision shows the modification impact while lower precision for those summary percentages values does not reflect the modifications made.

*No other evidence of academic dishonesty was found in other schools.

*To confirm some of the coding logic was correctly configured, addtional displays for new dataframes have been included in the cells.  Since many cells built upon each other, early verification on coding results avoided the need to debug large blocks of code to find/correct any errors encountered.

*In reviewing the included code, there are re-factoring opportunities available should this analysis need to be performed with any higher frequency or larger datasets in order to streamline the processing/analysis to produce the summary tables.


## Summary

In summary of this school district analysis, the following four major changes were found after reading and math scores for ninth graders at Thomas High School were replaced with NaNs:

1.  Thomas High School remained a top 5 performing school in the district based on their updated overall passing percentage.  To keep this result the total student count for the passing percentage calculations needed to be updated to reflect only the tenth through twelth graders and eliminating ninth graders scores and student count for the math, reading, and overall performance calculations.

2.  Prior to updating the passing percentages to only reflect tenth through twelfth graders' in the student count, Thomas High School's passing percentages where approximately 25-30% lower than the original school passing percentages (that included ninth graders' scores) since the ninth graders scores were removed.

3.  Once the ninth graders scores were removed and the passing percentages updated for Thomas High School, the overall impact for Thomas High School was a very small lowering in their passing percentages from original calculations that included ninth graders.  Once additional investigation is made into the Thomas High School ninth graders' scores, there is potential for greater impact if the ninth grader scores are determined to be higher or lower than originally recorded.  

4.  By removing the ninth graders scores, a per school ninth grader comparison cannot be made for the schools in the district.  But when factored into summary dataframes at the district or school type level (broader scope), lower value precision does not make the Thomas High School modification visible.
