# Pewlett-Hackard-Analysis
## Project Overview
Data needs to live somewhere—and that’s where databases come in. SQL is the standard language for working with databases, whether it’s storing data, transforming it, or retrieving it. Anyone who works with data needs to know SQL. Specific roles that focus on it are data engineers, ETL developers, and database administrators.

In the data pipeline, every tool available to us depends on having reliable data. Databases and database languages are used not just to store data, but to extract it from various sources and serve it to the analysis tools that need it. Databases make sure that multiple users can access data at the same time without sacrificing data integrity.

## Overview of the Analysis
The goal behind the analysis of Pewlett Hackard data is to help the management team plan and develop a strategy to identify employees who are ready retire in the near future, thus preparing for a "silver tsunami". We will use PostgreSQL to create a database with new tables in order to determine the number of retiring employees by title and identify employees who are eligible to participate in a mentorship program. 
### Project Overview
The initial data for the project came from six CSV files. These files contained data on thousands of employees from Pewlett Hackard. Their column headers and relationships are diagrammed in the ERD (Entity Relationship Diagram) shown below. The ERD was created using Quick DBD. 
In this analysis we use three separate tools: 
* QuickDBD to create quick database design for better visualization,
* PostreSQL a database system to load, build and host company’s data, and
* pgAdmin a GUI, using SQL Language to explore, manipulate and extract the data.

The ERD maps the relationships between the files which will be used to create the database and join tables to view the data in the required schema. Primary keys and foreign keys are also determined in the ERD. After the schema is created, we run queries on the tables to isolate the requested employee information. Query results are then turned into tables and exported as CSV files. 

### Data & Queries
[Queries](Queries/Employee_Database_challenge.sql)

[Data](Data)


#### ERD: Entity Relationship Diagram
![EmployeeDB](https://user-images.githubusercontent.com/73972332/104393837-3f91a980-54fa-11eb-9cfe-2aa2adcb2676.png)
## Results 
* A total of 90,398 employees are about to retire from the company. This represents 30% of the company's total 300,024 employees. 
    * This is a staggering number of employees who will be retiring soon and definitely confirms that HR needs to put into action immediate strategy to prepare for their replacement. 
    * This data can be found by viewing the "unique_titles" table in the database or in the exported csv "unique_titles.csv". 
* The majority of the staff ready to retire are Senior Engineers (33% of total retiring), and Senior Staff (32% of total retiring). 
    * This outcome will leave quite a gap in the technical department and high level skill. These positions are also ones that require a higher portion of training, development, and skill. The company indeed has a challenge ahead. 
    * This data can be found by viewing the "retiring_titles" table in the database or in the exported csv "retiring_titles.csv"
* The least amount of employees who need replacing include Assistant Engineers and Managers. 
    * Hopefully this smaller number for Assistant Engineers will provide the company with some wiggle room to quickly train up the Assistant Engineers to become promoted to Senior Engineers. 
* There are 1,549 employees eligible for the mentorship program to act as mentees. In comparison to the total number of employees eligible to retire, this is not a very high percentage. Less than 2% in fact. These are current employees whose birth dates are between January 1, 1965 and December 31, 1965. This means they are exactly ten years younger than the current youngest who plan to retire soon.  
    * However, this is still better than nothing, and at least still a plan to move forward in some level of replacement planning. 
    * If Pewlett Hackard decides to expand the mentorship program by increasing the age rage to 
    * This data can be found by viewing the "mentorship_eligibility" table in the database or in the exported csv "mentorship_eligibilitys.csv"
### Potential Retirees Sum
![unique_titles](https://user-images.githubusercontent.com/73972332/104394605-ceeb8c80-54fb-11eb-8755-549b40433061.png)

### Potential Retirees by Title
![retiring_titles](https://user-images.githubusercontent.com/73972332/104395018-a7e18a80-54fc-11eb-9e1f-99a10596d946.png)

### Employees eligible to participate in a Mentorship Program
![mentorship_eligibility](https://user-images.githubusercontent.com/73972332/104404149-dd8f6f00-550e-11eb-83d1-0913cedcf444.png)

## Summary
### High Level Overview
* How many roles will need to be filled as the "silver tsunami" begins to make an impact?: 
    * According to the database, 90,398 roles will have to be filled in the next few years. 
    * The HR department should intially focus on Senior Enginner and Senior Staff roles as 29,414 and 28,254 positions will need to be filled. 
* Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
    * There are more people retiring than there are potential mentors, which means that the company would have to create an efficient program that can cover the disparity between the number of people retiring and the number of people who can be trained to fill these positions. 
    However, there are only 1,549 eligible employees to participate in the actual mentorship program as mentees and for this reason, there actually are enough mentors to mentor through only the mentorship program. 


## Additional Queries & Tables - Further Insight

### Retiring Employees by Department
* In viewing the employees who may retire soon by department, we can see that clearly the production and development departments will see the biggest knowledge gap with the largest amount of potential retirees. 
* Query can be found: [Queries](Queries/Employee_Database_challenge.sql)

![retire_dept_count](https://user-images.githubusercontent.com/73972332/104488508-4d3f4180-5583-11eb-8f80-dfac4240257e.png)

### Eligible Mentors by Department
* In viewing the eligible mentors by department, we can see that development and production departments have the most amount of employees who can participate in the mentorship program. This is a positive for the company and program given that the development and production departments stand to lose the greatest amount of staff to retirement. 
* Query can be found: [Queries](Queries/Employee_Database_challenge.sql)

![eligible mentors by dept](https://user-images.githubusercontent.com/73972332/104874029-bd90ee80-5906-11eb-9b40-d3bcb84873a6.png)



