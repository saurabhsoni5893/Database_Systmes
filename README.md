# Database_Systmes

Semester project and Ad-Hoc Queries developed during course CSE 5330 - Database Systems I 

# Project: Inventory and Sales Management for an Online Business

Project comprises of total 5 phases which are as below:

# Phase 1: Problem Statement
Choose an interesting problem in a domain/area of your interest/expertise that requires data modeling and support for a database management system (DBMS). 
Designing the solution of the problem requires understanding of the problem domain or be able to get that info or research that.
It has 3 steps: 
1. General Problem Description
2. Business Goals or Functional Requirements
3. Data to be captured for your business

# Phase 2: EER (Extended Entity-Relationship) Modeling
Extended Entity Relationship (EER) diagram for the problem described in phase 1.

# Phase 3: Mapping the EER Modeling to Relations
Convert the EER Modeling of Phase 2 into Relations using the mapping steps.

# Phase 4: Creation of the Database and Execution of Complex SQL Queries
This phase has steps:
1. Normalize Relations of Phase 3 at least up to BCNF (Byce-Codd Normal Form)
2. Transform your relations into tables in a specific Relational-Database Management System (RDBMS) by using DDL.
3. Make sure all Functional Dependencies applicable to the Problem Statement of Phase 1 (based on the Data and Application Semantics) are captured by Database Schema design.
4. Transform all the constraints into appropriate constraints on the corresponding tables.
5. Define Triggers where appropriate for managing Referential Integrity constraints and other application specific situation monitoring.

Scripts need to be executed in following order:

**Step 1: DDL Script [myDBcreate.sql]**<br> 
It has a file containing the SQL statements that create entire database schema. 
This includes the tables with their constraints, and views, indexes, and other objects as per the application requirement.
Note: Tables have to be created in a specific order. Make sure to create the tables that do not reference any other tables first.

Step 2: DML Script [myDBinsert.sql]
It has a file containing INSERT statements that populate the tables created in step 1.
This script will contain SQL commands to fill data in the tables.

Step 3: DML Update Script [myDBupdate.sql]
Create a script that will update the database through a series of Insertions, Deletes, and Updates. 
This will allow to verify the correctness of the SQL queries when the database is updated/changed.

Step 4: Drop script [myDBdrop.sql]
Create a script that will drop all the tables that have created for the project. This will be useful to start from a clean slate after some inserts and deletes have been added to the application to check the correctness of ad hoc queries. 
One should be able to clean everything through this script and re-load the database instance using the above steps.
Note: Make sure to drop tables that are not referenced by other tables first (in the reverse order of create tables). 
If trying to drop a table that is being referenced by some other table, the DROP will fail.

Step 5: Ad-hoc SQL queries [myDBqueries.sql]
Create a script with ad-hoc queries on the database, say myDBqueries.sql. This script should contain at least 6 queries on the database.
1. At least 2 Queries on Multiple Relations containing GROUP BY, HAVING, and aggregate computations
2. At least 2 Queries that corresponds to Data Analysis (as in a Data Warehouse). Should have CUBE and/or ROLLUP clauses.
3. At least 2 Queries using an OVER clause for windowing operation.

# Phase 5: Application Development and Demo
In this phase, a front-end application will be developed that will interface with the DBMS on a server at the backend. 
The user will interact with the DBMS only through this interface. The GUI will be used by the user to retrieve and update the database without having to write SQL queries.
The interface you develop should have the following features-
1. Should be able to show relations in the database.
2. The contents of chosen relations, and updates to them.
3. Should be able to generate reports using parameters from the GUI (As an example, if it is a library database, one should be able to search for books on different parameter values or list all books that are overdue by a week.)
4. Should demonstrate the use of dynamic SQL with Prepare and Execute methods.
5. Should demonstrate the use of various dynamic SQL Queries including Aggregates, HAVING clause, GROUP BY, and ORDER BY, CUBE, ROLLUP clauses.
