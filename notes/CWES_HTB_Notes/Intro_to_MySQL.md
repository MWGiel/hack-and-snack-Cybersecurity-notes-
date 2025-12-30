## This module introduces SQL injection through MySQL
and it is crucial to learn more about MySQL and SQL to understand how SQL injections work and utilize them properly. Therefore, this section will cover some of MySQL/SQL's basics and syntax and examples used within MySQL/MariaDB databases.
# Structured Query Language (SQL)
SQL syntax can differ from one RDBMS to another. However, they are all required to follow the ISO standard for Structured Query Language. We will be following the MySQL/MariaDB syntax for the examples shown. SQL can be used to perform the following actions:

- Retrieve data
- Update data
- Delete data
- Create new tables and databases
- Add / remove users
- Assign permissions to these users

---
## Command Line
The mysql utility is used to authenticate to and interact with a MySQL/MariaDB database. The -u flag is used to supply the username and the -p flag for the password. The -p flag should be passed empty, so we are prompted to enter the password and do not pass it directly on the command line since it could be stored in cleartext in the bash_history file.
