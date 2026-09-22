Oracle Pluggable Databases (PDB) Management

Overview of Tasks
This repository contains the practical evidence and documentation for Oracle Pluggable Databases (PDB) management.
The assignment demonstrates a practical understanding of Oracle multitenant architecture, creation and deletion of Pluggable Databases (PDBs), user creation and management inside a PDB, the usage of Oracle Enterprise Manager (OEM), and professional technical documentation

 Oracle Environment Used
Database Management System: Oracle Database (Multitenant Container Database architecture)
Environment Tooling: SQL*Plus and Oracle Enterprise Manager (OEM) Database Express 
Explanation of Each Task
Task 1: Create a New Pluggable Database & User
  Created a permanent Pluggable Database named qu_pdb_29354 from the seed database using the FILE_NAME_CONVERT clause
   Opened the PDB in READ WRITE mode and saved its open state so it persists across restarts
   Created a dedicated user account inside the PDB named queen_plsqlauca_29354 to be reused for future class work).
Task 2: Create and Delete a PDB
  Created a temporary Pluggable Database named qu_to_delete_pdb_29354 from CDB$ROOT).
  Verified its existence, closed it using CLOSE IMMEDIATE, and completely removed it along with its datafiles using the DROP PLUGGABLE DATABASE  INCLUDING DATAFILES command).
Task 3: Oracle Enterprise Manager (OEM) Setup
  Accessed Oracle Enterprise Manager (OEM) Database Express to monitor the database server environment
  Verified that the dashboard accurately reflects the multitenant environment and completed PDB configurations).
Task 4: Documentation & Reporting
   Organized all execution evidence screenshots neatly into designated folders (screenshots/pdb_creation, screenshots/pdb_deletion, and screenshots/oem_dashboard) within this public GitHub repository

Challenges Faced and Solutions
Challenge 1 (ORA-65005): Encountered an invalid file name pattern error when creating the PDB directly from the seed database.
  Solution: Explicitly specified the directory mappings using the FILE_NAME_CONVERT clause pointing to the correct datafiles directory
Challenge 2 (ORA-65040): Received an operation not allowed error when trying to create a temporary PDB while already logged into a pluggable database container.
  Solution: Switched the session back to the root container using ALTER SESSION SET CONTAINER = CDB$ROOT; before executing root-level PDB management commands


Submission Details  
Repository Link: https://github.com/queenineza18-boop/oracle_pdb_ass_II_29354_queen/

PDB Name Created: qu_pdb_29354
 Issues Encountered: Yes
