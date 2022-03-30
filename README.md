# School District Analysis

## Overview
This analysis aims to evaluate a school district data to identify if budget, size, and school types affect the students performance. The dataset contains information of 9th to 12th grade students in reading and math. In the data cleansing step, it was necessary remove data from 9th graders from one of the schools in the district, Thomas High School, due to evidences of academic dishonesty. Thus, results will compare the dataframes before and after the data cleansing step. This analysis was made using python library pandas and jupyter notebook. The complete analysis can be found on [PyCitySchools_Challenge.ipynb](PyCitySchools_Challenge.ipynb).

## Results

- In the district summary the affected values were 

![District_Summary_before_cleansing.png]("analysis/District_Summary_before_cleansing.png)
![District_Summary_Final.png]("analysis/District_Summary_Final.png)

- The school summary was the data frame with the most relevant changes, in the images below is possible to compare the data from TRhomas High School before and after removing the 9th graders’ scores
![School_Summary_before_cleansing.png]("analysis/School_Summary_before_cleansing.png)
![School_Summary_Final.png]("analysis/School_Summary_Final.png)

- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?


- How does replacing the ninth-grade scores affect the following:
    - Math and reading scores by grade
    ![Math_score_by_grade_before_cleansing.png]("analysis/Math_score_by_grade_before_cleansing.png)
    ![Math_score_by_grade_final.png]("analysis/Math_score_by_grade_final.png)

    ![Reading_score_by_grade_before_cleansing.png]("analysis/Reading_score_by_grade_before_cleansing.png)
    ![Reading_score_by_grade_final.png]("analysis/Reading_score_by_grade_final.png)

    - Scores by school spending
    ![School_Spending_before_cleansing.png]("analysis/School_Spending_before_cleansing.png)
    ![School_spending_final.png]("analysis/School_spending_final.png)
    
    - Scores by school size

    ![School_size_before_cleansing.png]("analysis/School_size_before_cleansing.png)
    ![School_size_final.png]("analysis/School_size_final.png)
    
    - Scores by school type
    ![School_type_before_cleansing.png]("analysis/School_type_before_cleansing.png)
    ![School_type_final.png]("analysis/School_type_final.png)


## Summary
Some crucial changes made in the code to meet the new requirements are:
    - A new 'count' was included to identify the students that wouldn't be considered in the analysis. As a result, 461 students were removed, and 38709 was the total of students used to calculate passing percentages. 
    - Scores from 9th grade students from Thomas high School were replaced by "NaN" using numpy.na, which means that they were not considered when calculating averages. 
    - The method 'loc' was used to filter data from 10th - 12th grade students from Thomas High School in order to calculate new averages scores for math and reading, as well passing percentages for both subjects and overall. 
    - Finally, the new values for Thomas High School replaced the old ones on the School Summary data frame, affecting all data frames that used data from per_school_summary_df.