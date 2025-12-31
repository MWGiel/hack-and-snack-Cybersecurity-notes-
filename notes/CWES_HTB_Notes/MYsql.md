## HTB – SQL Basics: Finding Department Information in the employees Database
**Objective**
Retrieve the department number (dept_no) for the department named "Development" from the MySQL/MariaDB employees database.

---
**1. List all databases**
> SHOW DATABASES
> employees

---
**2. Select the target database**
> USE employees

---
**3. List all tables in the database**
> SHOW TABLES

---
**Inspect the departments table structure**
> DESCRIBE departments

---
**5. Query the department number for "Development"**
> SELECT * FROM departments WHERE dept_name = 'Development'

---
## Answer
> Department number: d005
