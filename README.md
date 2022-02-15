# Week_7
## Overview of the analysis
In this SQL lesson we looked a Pwelett Hackard and the large number of people that are available to retire soon. We also examined the idea of a mentorship program for those who would be leaving soon. Furthermore we broke down the analysis by title to see how many in each job would soon be retirement age.
## Results: Provide a bulleted list with four major points from the two analysis deliverables. Use images as support where needed.
* There are 72,458 people who are soon eligible for retirement and are currently employed by Pwelett Hackard.
* There are 50,842 senior staff (Senior Engineer and Senior Staff) soon eligible for retirement and are currently employed by Pwelett Hackard.
* There are 2 Mangers soon eligible for retirement and are currently employed by Pwelett Hackard.
* There is 1,549 staff members eligible to be a part of the mentorship program
![title_chart](https://user-images.githubusercontent.com/96025706/153967506-f2aa04c2-526d-49bb-9594-ccf985c6a6a7.png)
## Summary Questions
### 1. How many roles will need to be filled as the "silver tsunami" begins to make an impact?
72,458 roles will need to be filled as old employees begin to retire.
### 2. Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
There are 240,124 current employees of which 72,458 will soon be retiring. That leaves 167,666 employees of which 1,549 are eligible for the mentorship program. I would say no there are not enough as if every remaining employee were to go under mentorship it would be approximately 108 mentees to each mentor. We found these number by using the below queries.
```
SELECT COUNT(emp_no)
from mentorship_eligibility; 

SELECT COUNT(emp_no)
from dept_employees AS m
where (m.to_date = '9999-01-01');
