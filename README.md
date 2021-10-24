# School_District_Analysis
### Overview
The purpose of this analysis was to create a disctrict analysis that showed state testing results of multiple high schools. The results showed an anomaly with Thomas High School where the test scores were not accurate. A re-analysis was done to display any changes with the results and configure any affected data. 


#### How is the district summary affected?
- The district summary was affected by a change in scoring for both reading and math. Specificially, ninth grader results were replaced with "NaNs" to show the shift of score results in Thomas High School. 
 ###### Affected District Summary: 
 
 ![district_summary_NANS_ths](https://user-images.githubusercontent.com/90741799/138537401-18b12f99-be25-488f-ba50-09fc0032de8f.png)


#### How is the school summary affected?
- There was a shift in math and reading scores that affected the school summary. When looking at the dataframe, it appears that very little changed. 
- Looking closely at the percentage of passing reading, math, and overall passing; we can see the increase displayed below. The intial percentages ranged from 65-69 percent, wheras, the repalced school summary percentages had increased by almost 25 percent.
###### Before
![school_summary_before](https://user-images.githubusercontent.com/90741799/138536613-8e863bad-84a6-4279-b421-415e1fc7fc9e.png)
###### After
![school_summary_after_ths](https://user-images.githubusercontent.com/90741799/138581170-7d2fbf72-3257-4dee-9b0a-0aa0648e5c64.png)


#### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
- Replacing the ninth graders of Thomas High School math and reading scores affected their perfomance signficantly. When reviewing their initial results, it appeared that they weren't performing as well compared to other schools. After replacing the ninth graders' results, it is clear that Thomas High School's performance had ranked a bit higher. 
```# Calculate the students who passed both reading and math.
passing_math_reading = students_passing_math_reading_df.loc[(students_passing_math_reading_df["math_score"] >= 70)
                                               & (students_passing_math_reading_df["reading_score"] >= 70)]
# Calculate the num of students who passed both math and reading
overall_passing_math_reading_count = passing_math_reading["student_name"].count()



# Calculate the overall passing percentage with new total student count.
overall_passing_percentage = overall_passing_math_reading_count / ten_to_twelve_count * 100
print(overall_passing_percentage)# Calculate the students who passed both reading and math.
```
#### How does replacing the ninth-grade scores affect the following:
- There wasn't any apparent affects for scoring of each grade besides the scoring for ninth graders. 
- The only affect that was evident during the calculations of total percentages for all students who passed math and reading.

###### Math scores by grade:
 ![math_score_by_grade](https://user-images.githubusercontent.com/90741799/138537125-fd3ed4c8-2ae3-4c4e-899f-46f63a36f401.png)
###### Reading scores by grade:
 ![reading_scores_by_grade](https://user-images.githubusercontent.com/90741799/138537182-e835b240-31ae-43a2-ba0c-3dc8324242e1.png)

#### Scores by school spending, size, type:




- Shifting the attention to how ninth grade scores affected school spending, size, and type. We can see that there were certain areas of the dataframe that were not affected. The math and reading averages were the same as well as per student budget, total school budget, and student count.
 ![thomas_hs_summary](https://user-images.githubusercontent.com/90741799/137820255-c4bc07c7-3980-4133-be55-428a56a6d35c.png)
- School size had also remained the same throughout the analysis and replacing the scores did not have an affect on the size. 
- The only change that occured regarding school type was the slight increase in the percentages but the averages of both math and reading scores remained the same.
###### Scores by school type
![scores_by_school_type](https://user-images.githubusercontent.com/90741799/138536913-358fa0b2-e68a-419d-bd6a-0a3f232b124f.png)

#### Summary: 
The first change in the data after replacing the NaNs of ninth grade scores was the overall passing percentage. The passing percentage had increased once the scores were replaced. The second change was the ranking of the top performing and low performing schools. Once the scores were replaced, Thomas High School had a better ranking compared to it's initial data. The third change was that the math passing percentage for Thomas High  school had increased by 27 percent after replacing the scores. The last change that occured was the reading percentage for Thomas High School, which had increased by roughly 28 percent.





