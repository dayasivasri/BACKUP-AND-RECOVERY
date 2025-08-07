# BACKUP-AND-RECOVERY
*Company*: Codetech IT Solutions
*Name*:DAYA SIVASRI
*Intern-ID*:CT04DH2291
*domain*: SQL
*duration*: 4 weeks
*Mentor*: Neela Santhosh
*Description*:In any database system, ensuring the safety and availability of data is critical. Backup and recovery are the two most essential components of database maintenance. A backup is a copy of the database that can be used to restore the original data in case of accidental deletion, corruption, or system failure. Recovery refers to the process of restoring that data from a backup file. In this task, we learned how to automate both backup and recovery for a MySQL database using simple command-line scripts on a Windows system. We used mysqldump, a utility provided with MySQL, to export the contents of the database into a .sql file. This backup file contains both the structure and data of the database and can be re-imported at any time to recreate the database exactly as it was at the time of backup.

To begin, we created a sample database named internship_db and added a table called students with a few rows of sample data. Once the database was ready, we wrote a script named backup.bat which contained the following command: mysqldump -u root -p internship_db > C:\backup\internship_db_backup.sql. This command, when run from the Windows Command Prompt, prompts the user for the MySQL password and then creates a backup file in the specified location. If successful, no errors are shown, and the .sql file will contain all the necessary commands to recreate the database. To test recovery, we simulated a failure by dropping the database using the command DROP DATABASE internship_db;. After confirming the database was deleted, we ran another script named restore.bat, which contained the command mysql -u root -p < C:\backup\internship_db_backup.sql. This command reads the backup file and restores the entire database to its original state, including tables and data.

While attempting to run these scripts, we initially encountered an error: 'mysql' is not recognized as an internal or external command. This happened because the MySQL executable files were not added to the Windows system’s PATH variable. To fix this, we located the MySQL bin folder (usually at C:\Program Files\MySQL\MySQL Server 8.0\bin) and added it to the system’s environment variables under PATH. Once this was done and the command prompt was restarted, both mysql and mysqldump commands worked globally from any directory. This made it easy to run our backup and restore scripts from anywhere in the system.

In conclusion, automating MySQL database backup and recovery using .bat scripts on Windows is a powerful and simple way to protect critical data. These scripts save time, reduce the risk of human error, and ensure that databases can be quickly recovered after unexpected problems. This task was valuable in learning how to manage real-world data safely and efficiently using practical tools and scripting techniques
#output:<img width="149" height="97" alt="Image" src="https://github.com/user-attachments/assets/1cd68194-76d8-4d33-8206-837b99c1c3d2" />


