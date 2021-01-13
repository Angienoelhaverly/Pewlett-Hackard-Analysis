# Pewlett-Hackard-Analysis
## Overview of the analysis
The goal behind the analysis of Pewlett Hackard data is to help the management team plan and develop a strategy to identify employees who are ready retire in the near future. We will use PostgreSQL to create a database with new tables in order to determine the number of retiring employees by title and identify employees who are eligible to participate in a mentorship program. 
### Background & Program Setup
The initial data for the project came from six CSV files. These files contained data on thousands of employees from Pewlett Hackard. Their column headers and relationships are diagrammed in the ERD (Entity Relationship Diagram) shown below. The ERD maps the relationships between the files which will be used to create the database and join tables to view the data in the required schema. Primary keys and foreign keys are also determined in the ERD. After the schema is created, we run queries on the tables to isolate the requested employee information. Query results are then turned into tables and exported as CSV files. 
#### ERD: Entity Relationship Diagram
![EmployeeDB](https://user-images.githubusercontent.com/73972332/104393837-3f91a980-54fa-11eb-9cfe-2aa2adcb2676.png)
## Results 
* A total of 90,398 employees are about to retire from the company. This data can be found by viewing the "unique_titles" table in the database or in the exported csv "unique_titles.csv"
![unique_titles](https://user-images.githubusercontent.com/73972332/104394605-ceeb8c80-54fb-11eb-8755-549b40433061.png)
## Summary
