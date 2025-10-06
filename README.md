> Oracle PDB and OEM Configuration
> Oracle PDB and OEM Configuration

> Student Information
Name: uwitonze pacific  
Student ID: 26983  
Course: PL/SQL  
Assignment Title: Oracle PDB and OEM Configuration  
Date: 06/10/2025 

> Overview of Tasks
This report summarizes the practical exercises conducted on October 06, 2025, using Oracle Database 21c Express Edition. The tasks focused on creating, managing, and monitoring pluggable databases (PDBs), as well as configuring Oracle Enterprise Manager (OEM) for monitoring. The activities included:

Task 1: Create a new Pluggable Database (PDB)
Task 2: Create and delete a PDB
Task 3: Configure and access Oracle Enterprise Manager (OEM)
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
> Task 1: Creating a New Pluggable Database (PDB)

A new pluggable database was created using the following name:

plsql_class2025db

The username was generated following the required naming convention:

pacific_plsqlauca_26983

A simple password was used for authentication.  
This database was successfully created and opened for use in classwork.

A pluggable database was created with the name:
plsql_class2025db
The admin username followed the required naming convention:
pacific_plsqlauca_26983
A simple password (mypassword) was assigned for authentication. The PDB was created in the root container and opened for storing classwork.

PDB creation confirmation attached below as shown on the image.

<img width="1903" height="966" alt="image" src="https://github.com/user-attachments/assets/34ac8db4-1430-4a92-b1a2-e62032e866de" />

> task2: Creating and Deleting a PDB

FirstTwoLettersOfName_to_delete_pdb_StudentID

Hence, the database name was:

pa_to_delete_pdb_26983

After creating the PDB, it was successfully deleted to demonstrate proper lifecycle management.

the below screenshoot below shows Creation confirmation attached.

<img width="1864" height="550" alt="image" src="https://github.com/user-attachments/assets/e0c0ed0e-4f6b-42e2-818d-39a8712a34a6" />

the screenshoot  below shows the Deletion confirmation .

<img width="1353" height="461" alt="image" src="https://github.com/user-attachments/assets/a5b1df38-428d-4900-bbf5-56b528a73d19" />

> Task 3: Oracle Enterprise Manager (OEM) Configuration

Oracle Enterprise Manager (EM Express) was configured and accessed via:

https://localhost:5500/em

Configuration Steps:

step 1: Enabled HTTP port by EXEC DBMS_XDB_CONFIG.SETHTTPPORT(5500);

step 2: Restarted the listener by lsnrctl reload;

Login Details

Logged in as SYS with the SYSDBA role using the system password, verifying the dashboard reflected:

Database: XE (21.3.0.0.0 Express Edition)

Type: Single Instance (CDB with 1 PDB: plsql_class2025db)

Metrics: CPU usage, memory allocation, data storage

Schema Visible: pacific_PLSQLAUCA_26983


<img width="1919" height="966" alt="image" src="https://github.com/user-attachments/assets/35cc507c-c988-47f5-82fb-81a52bf67fe5" />


> Issues Encountered and Solutions

Issue: OEM not loading

Cause: Listener not started

Solution: Ran lsnrctl start


Issue: PDB not opening

Cause: Database in MOUNT mode

Solution: Executed ALTER PLUGGABLE DATABASE ALL OPEN;




Issue: Login failed

Cause: Incorrect credentials

Solution: Re-entered correct SYS password




Issue: ORA-65096 error

Cause: User creation attempted in root container

Solution: Switched to PDB with ALTER SESSION ...;





> Conclusion

ll tasks were successfully completed on October 06, 2025. This exercise enhanced my understanding of Oracle multitenant architecture, including PDB creation, deletion, and monitoring via OEM. It also reinforced database administration and PL/SQL skills.
