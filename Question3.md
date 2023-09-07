---
layout: default
title: Question Three
---

<style> 
    body { -webkit-user-select: none; /* Chrome, Safari and Opera */ 
    -moz-user-select: none; /* Firefox */ 
    -ms-user-select: none; /* IE and Edge */ 
    user-select: none; /* standard syntax */ } 
</style>

## Problem Statement:
---

You are given a dataframe (**‘table_data.csv’**) with five columns: ID, CSE1, CSE2, CSE3, CSE4, and SECTION. 

[Get the file](https://drive.google.com/file/d/1-Ez5aLv2IynzkAR-pFpD-f5LzuPktYRL/view?usp=sharing)

- The ID represents the student's identity. 
- The CSE1, CSE2, CSE3, and CSE4 columns represent four different subjects and contain the respective scores of students with a prefix and suffix garbage values.
- The SECTION represents the section of students with four unique sections ('A', 'B', 'C' and 'D').

Your task is to perform the following operations on the dataset:

1. **Data Cleansing:** Clean the marks present in the CSE1, CSE2, CSE3, and CSE4 columns by removing the prefixed and suffixed garbage values and ensure they are numeric.

2. **Average Calculation:** Calculate the average mark of each student across the four subjects (CSE1-4). Store this average in a new dataframe column, 'AVG_MARK'.

3. **Grade Assignment:** Based on the student's 'AVG_MARK', assign a corresponding grade. The grade determination criteria is as follows:
    - 0 <= 'AVG_MARK' <= 29, assign 'F'
    - 30 <= 'AVG_MARK' <= 49, assign 'D'
    - 50 <= 'AVG_MARK' <= 69, assign 'C'
    - 70 <= 'AVG_MARK' <= 79, assign 'B'
    - 80 <= 'AVG_MARK' <= 89, assign 'A-'
    - 90 <= 'AVG_MARK' <= 100, assign 'A'
    
    Store these grades in a new DataFrame column 'GRADE'.

4. **Highest and Lowest Marked Subjects:** Find the highest and lowest marked subject for each student. Create two new columns, 'LOWEST_MARKED_SUBJECT' and 'HIGHEST_MARKED_SUBJECT', and store the name of the respective subject in these columns for each student.

5. **Section-Wise Highest Average Mark:** Make a new column named "MAX_AVG_MARK_SECTION" and assign the highest mark based on each section to the rows.

**Note:**

- Make sure to handle any potential exceptions or errors in the dataset during the execution of the above tasks.
- Comment your code appropriately for better understanding.
- Your solution should have optimal time and space complexity.
- Submit the updated csv file


---

### Input Demo
<img src="https://cdn.discordapp.com/attachments/945567201518317581/1149026039280959518/image.png" alt="input1" style="display:inline-block; height:auto;"> 
### Output Demo
<img src="https://cdn.discordapp.com/attachments/945567201518317581/1149025986264977498/image.png" alt="output" style="display:inline-block; height:auto;">