# School_District_Analysis
Overview of the school district analysis: Explain the purpose of this analysis.

Results: Using bulleted lists and images of DataFrames as support, address the following questions.

How is the district summary affected?
How is the school summary affected?
How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
How does replacing the ninth-grade scores affect the following:
Math and reading scores by grade
Scores by school spending
Scores by school size
Scores by school type
Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
Images:
![thomas_hs_summary](https://user-images.githubusercontent.com/90741799/137820255-c4bc07c7-3980-4133-be55-428a56a6d35c.png)
![93 185](https://user-images.githubusercontent.com/90741799/137820698-1ed12295-a220-4e28-b2a7-2a54c0388f28.png)
![97](https://user-images.githubusercontent.com/90741799/137820800-a31ac897-cd14-4fd9-9db5-c33e113a2da9.png)
![90](https://user-images.githubusercontent.com/90741799/137820874-7ab0fc3c-9b6c-45c1-99ab-bf0b25c50c06.png)


Step 12- 14:
# Step 12. Replace the passing math percent for Thomas High School in the per_school_summary_df.
passing_math_count = len(school_data_complete_df.loc[(school_data_complete_df["school_name"] == "Thomas High School") & (school_data_complete_df["math_score"] >= 70),])

ten_to_twelfth_math_percentage =  passing_math_count / float(ten_to_twelve_count) * 100
print(ten_to_twelfth_math_percentage)


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

