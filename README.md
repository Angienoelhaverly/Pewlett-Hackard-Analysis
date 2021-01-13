# Pewlett-Hackard-Analysis
## Overview of the analysis
The goal behind the analysis of Pewlett Hackard data is to help the management team plan and develop a strategy to identify employees who are ready retire in the near future. We will use PostgreSQL to create a database with new tables in order to determine the number of retiring employees by title and identify employees who are eligible to participate in a mentorship program. 
### Background & Program Setup
The initial data for the project came from six CSV files. These files contained data on thousands of employees from Pewlett Hackard. Their column headers and relationships are diagrammed in the ERD (Entity Relationship Diagram) shown below. The ERD was created using Quick DBD. The ERD maps the relationships between the files which will be used to create the database and join tables to view the data in the required schema. Primary keys and foreign keys are also determined in the ERD. After the schema is created, we run queries on the tables to isolate the requested employee information. Query results are then turned into tables and exported as CSV files. 
#### ERD: Entity Relationship Diagram
![EmployeeDB](https://user-images.githubusercontent.com/73972332/104393837-3f91a980-54fa-11eb-9cfe-2aa2adcb2676.png)
## Results 
* A total of 90,398 employees are about to retire from the company. This data can be found by viewing the "unique_titles" table in the database or in the exported csv "unique_titles.csv"
* The majority of the staff ready to retire are Senior Engineers, and Senior Staff. This data can be found by viewing the "retiring_titles" table in the database or in the exported csv "retiring_titles.csv"
* There are 1,549 employees eligible for the mentorship program. This data can be found by viewing the "mentorship_eligibility" table in the database or in the exported csv "mentorship_eligibilitys.csv"

![unique_titles](https://user-images.githubusercontent.com/73972332/104394605-ceeb8c80-54fb-11eb-8755-549b40433061.png)

![retiring_titles](https://user-images.githubusercontent.com/73972332/104395018-a7e18a80-54fc-11eb-9e1f-99a10596d946.png)

![mentorship_eligibility](https://user-images.githubusercontent.com/73972332/104404149-dd8f6f00-550e-11eb-83d1-0913cedcf444.png)

## Summary
Provide high-level responses to the following questions, then provide two additional queries or tables that may provide more insight into the upcoming "silver tsunami."
* How many roles will need to be filled as the "silver tsunami" begins to make an impact?
* Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
