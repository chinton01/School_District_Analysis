# School_District_Analysis
### Overview
The purpose of this analysis was to create a disctrict analysis that showed statetasting results of multiple high schools. The results showed an anomaly with Thomas High School where the test scores were not accurate. A re-analysis was done to display any changes with the results and configure affected data. 


#### How is the district summary affected?
- The district summary was affected by
 ###### Affected District Summary: 
 
 ![district_summary_NANS_ths](https://user-images.githubusercontent.com/90741799/138537401-18b12f99-be25-488f-ba50-09fc0032de8f.png)


#### How is the school summary affected?
- There was a shift in math and reading scores that affected the school summary.

![school_summary_before](https://user-images.githubusercontent.com/90741799/138536613-8e863bad-84a6-4279-b421-415e1fc7fc9e.png)
![school_summary_after](https://user-images.githubusercontent.com/90741799/138536672-e9bec74a-182c-4d4b-8601-ff2880bad61f.png)

#### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

#### How does replacing the ninth-grade scores affect the following:
###### Math scores by grade:
 ![math_score_by_grade](https://user-images.githubusercontent.com/90741799/138537125-fd3ed4c8-2ae3-4c4e-899f-46f63a36f401.png)
###### Reading scores by grade:
 ![reading_scores_by_grade](https://user-images.githubusercontent.com/90741799/138537182-e835b240-31ae-43a2-ba0c-3dc8324242e1.png)

###### Scores by school spending
![scores_by_school_spending](https://user-images.githubusercontent.com/90741799/138536777-48806776-b40f-40f5-8a60-fbccbec873c0.png)

###### Scores by school size
![scores_by_school_size](https://user-images.githubusercontent.com/90741799/138536712-c6ff12b7-f981-4887-bf55-4fb6e3004ed7.png)

###### Scores by school type
![scores_by_school_type](https://user-images.githubusercontent.com/90741799/138536913-358fa0b2-e68a-419d-bd6a-0a3f232b124f.png)

Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

Images:
![thomas_hs_summary](https://user-images.githubusercontent.com/90741799/137820255-c4bc07c7-3980-4133-be55-428a56a6d35c.png)

###### For ten-twelfth grade: passing math 
![93 185](https://user-images.githubusercontent.com/90741799/137820698-1ed12295-a220-4e28-b2a7-2a54c0388f28.png)
 
 ###### 10-12th passing reading percentage: 
 ![97](https://user-images.githubusercontent.com/90741799/137820800-a31ac897-cd14-4fd9-9db5-c33e113a2da9.png)
###### Overall Passing math & reading 10-12th: 
![90](https://user-images.githubusercontent.com/90741799/137820874-7ab0fc3c-9b6c-45c1-99ab-bf0b25c50c06.png)

###### 9thGrade:
![9th_grade_data](https://user-images.githubusercontent.com/90741799/138536493-e3ab9c8a-515c-4730-bf2a-1f6738a3926a.png)








Step 12- 14:
``` # Step 12. Replace the passing math percent for Thomas High School in the per_school_summary_df.
passing_math_count = len(school_data_complete_df.loc[(school_data_complete_df["school_name"] == "Thomas High School") & (school_data_complete_df["math_score"] >= 70),])

ten_to_twelfth_math_percentage =  passing_math_count / float(ten_to_twelve_count) * 100
print(ten_to_twelfth_math_percentage) ```


 # Step 13. Replace the passing reading percentage for Thomas High School in the per_school_summary_df.
passing_reading_count = len(school_data_complete_df.loc[(school_data_complete_df["school_name"] == "Thomas High School") & (school_data_complete_df["reading_score"] >= 70),])

ten_to_twelfth_reading_percentage =  passing_reading_count / float(ten_to_twelve_count) * 100
print(ten_to_twelfth_reading_percentage)


# Step 14. Replace the overall passing percentage for Thomas High School in the per_school_summary_df.
# Calculate the students who passed both reading and math.
passing_math_reading = students_passing_math_reading_df.loc[(students_passing_math_reading_df["math_score"] >= 70)
                                               & (students_passing_math_reading_df["reading_score"] >= 70)]
# Calculate the num of students who passed both math and reading
overall_passing_math_reading_count = passing_math_reading["student_name"].count()



# Calculate the overall passing percentage with new total student count.
overall_passing_percentage = overall_passing_math_reading_count / ten_to_twelve_count * 100
print(overall_passing_percentage)# Calculate the students who passed both reading and math.

