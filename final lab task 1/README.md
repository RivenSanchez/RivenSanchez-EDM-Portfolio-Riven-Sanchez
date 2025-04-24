## Finals Lab Task 1. MySQL Basics
<!-- task needed to complete and instructions -->
The following are the tasks that need to be implemented using MySQL statements. Make sure to complete them in the order specified:
- ### Task 1:
  Create table named `employees` with the following fields:  
  - `employee_id` UNIQUE, INTEGER, AUTO-INCREMENT, PRIMARY KEY
  -  `employee_name` VARCHAR(255) and NOT NULL
  -  `manager_id` INTEGER, FOREIGN KEY referencing `employee_id` in the same table (`employees`) 
- ### Task 2:
  Create table named `departments` with the following fields:
  - `department_id`  UNIQUE, INTEGER, AUTO-INCREMENT, PRIMARY KEY
  - `department_name` VARCHAR(255), NOT NULL
- ### Task 3:
  Create table named `employee_departments` with the following fields:
  - `employee_id` INTEGER, FOREIGN KEY referencing `employee_id` in table (`employees`)
  - `department_id` INTEGER, FOREIGN KEY referencing `department_id` in table (`department`)
- ### Task 4
  Create table named `employee_projects` with the following fields:
  - `employee_id` INTEGER, FOREIGN KEY referencing `employee_id` in table (`employees`)
  - `project_name` VARCHAR(255), NOT NULL
- ### Task 5
  Create table named `managers` with the following fields:
  - `manager_id` UNIQUE, INTEGER, AUTO-INCREMENT, PRIMARY KEY
  - `employee_id` INTEGER, FOREIGN KEY referencing `employee_id` in table (`employees`)



 <!-- required output-->
## Required output per Test Cases:
1. Query statements (Task 1-5)
2. Table Structure (Task 1-5)
3. And 1 ER Diagram or Relational schema from phpMyAdmin or Workbench (pdf or jpg file)
4. Sql copy of the database and table sturctures


<!-- step by step -->
## STEP 1:
- Open XAMPP and start the Apatche and MySQL then open MySQL workbench
- Add a new connection
- Click the connection made
## STEP 2:
- Create a DATABASE BY using  
 `CREATE DATABE database_name`
- Use the database that has created by using  
  `USE database_name`

  <!-- screenshots and code  -->
## HERE IS THE SCREENSHOT OF TASK 1 TO TASK 4 
### task 1
![](image/task%201.1.png)  
- code  
  `CREATE TABLE employees_tbl (employee_id INT(10) UNIQUE AUTO_INCREMENT PRIMARY KEY,
 employee_name VARCHAR(255) NOT NULL, 
 manager_id INT(10), FOREIGN KEY(manager_id) REFERENCES employees_tbl(employee_id));`
### task 2
![](image/task%201.2.png)
- code  
  `CREATE TABLE departments_tbl (department_id INT(10) UNIQUE AUTO_INCREMENT PRIMARY KEY,
 department_name VARCHAR(255) NOT NULL);`
### task 3
![](image/task%201.3.png)
- code  
`CREATE TABLE employee_departments_tbl (employee_id INT(10), FOREIGN KEY (employee_id) REFERENCES employees_tbl(employee_id), 
department_id INT(10), FOREIGN KEY(department_id) REFERENCES departments_tbl(department_id));`
### task 4
![](image/task%201.4.png)
- code  
  `CREATE TABLE employee_projects_tbl (employee_id INT(10), FOREIGN KEY(employee_id) REFERENCES employees_tbl(employee_id),
 project_name VARCHAR(255) NOT NULL);`


<!-- ER Diagram -->
## HERE IS THE SCREENSHOT OF ER DIAGRAM
![](image/erd.png)

<!--SQL FILES-->
## HERE IS MY SQL FILE
[employees Table](file/multi_level_company_employee_projects_tbl.sql)  
[departments Table](file/multi_level_company_departments_tbl.sql)  
[employee departments Table](file/multi_level_company_employee_departments_tbl.sql)  
[employee projects Table](file/multi_level_company_employee_projects_tbl.sql)  
[managers Table](file/multi_level_company_managers_tbl.sql)  
