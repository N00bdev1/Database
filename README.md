SQL Fundamentals for Healthcare Data

This repository contains two Jupyter Notebooks (.ipynb) that demonstrate fundamental and intermediate SQL operations, simulating a basic database structure common in a clinic or healthcare management system.

The database schema revolves around Patients, Appointments, Encounters, and Prescriptions.

Repository Structure

The repository contains the following files:

01_SQL_BASICS.ipynb: Covers Data Definition Language (DDL) for creating tables and basic Data Manipulation Language (DML) operations (SELECT, INSERT, UPDATE, DELETE).

Focus: DDL & Basic DML

02_JOINS.ipynb: Demonstrates all major types of SQL JOIN operations, essential for querying relational data.

Focus: Intermediate DML (JOINs)

README.md: (This file) Overview and usage instructions for the repository.

01_SQL_BASICS.ipynb: Core Operations

This notebook establishes the foundation of the database and introduces the core CRUD (Create, Read, Update, Delete) operations.

Database Schema

The following tables are created and populated with sample data:

patients: Stores demographic and contact information. Primary Key: patient_id.

appointments: Tracks scheduled visits. Primary Key: appointment_id. Foreign Key: patient_id.

encounters: Logs actual patient visits, reasons, and outcomes. Primary Key: encounter_id. Foreign Key: patient_id.

prescriptions: Links medication orders to specific patient visits. Primary Key: prescription_id. Foreign Keys: encounter_id, patient_id.

Key SQL Topics Covered:

Table Creation (CREATE TABLE): Defining columns, data types (INT, VARCHAR, DATE, TEXT), and constraints (PRIMARY KEY, FOREIGN KEY).

Data Insertion (INSERT INTO): Adding new records to the tables.

Data Retrieval (SELECT):

Selecting all columns (SELECT *).

Selecting specific columns.

Filtering data using the WHERE clause (e.g., filtering by gender or visit_type).

Sorting results using ORDER BY.

Checking for missing values using IS NULL.

Data Modification (UPDATE): Changing existing records, both single and multiple fields.

Data Deletion (DELETE): Removing specific rows from a table.

02_JOINS.ipynb: Connecting Data

This notebook focuses on relational queries, demonstrating how to combine data from two or more tables using various JOIN techniques.

Key SQL JOINs Demonstrated:

INNER JOIN

Description: Returns only rows where there is a match in both tables.

Use Case Example: Finding appointments that definitely have a corresponding patient record.

LEFT JOIN

Description: Returns all rows from the left table, and the matched rows from the right table. Outputs NULL for the right table where no match is found.

Use Case Example: Listing all patients, even those who have not yet scheduled an appointment.

RIGHT JOIN

Description: Returns all rows from the right table, and the matched rows from the left table. Outputs NULL for the left table where no match is found.

Use Case Example: Listing all appointments, even if the patient record was somehow missing.

FULL OUTER JOIN

Description: Returns all records when there is a match in either left or right table.

Use Case Example: Listing every patient and every appointment, showing matches where they exist, and NULL where they don't.

CROSS JOIN

Description: Returns the Cartesian product of the tables—all possible combinations of rows.

Use Case Example: Used for generating test data or complex scenarios.

SELF JOIN

Description: A regular join where a table is joined to itself (requires aliasing).

Use Case Example: Finding pairs of patients who share the same doctor.

Getting Started

To run the SQL code in these notebooks, you will need a suitable environment:

Jupyter/VS Code: Open the .ipynb files in a Jupyter environment or VS Code.

SQL Kernel/Extension: You will need an environment capable of executing SQL directly, such as a local SQLite setup, or a database connection extension for your preferred SQL database (e.g., PostgreSQL, MySQL).

Execution Order: Run the cells in 01_SQL_BASICS.ipynb first to create and populate the tables before executing the JOIN queries in 02_JOINS.ipynb.

Note: The SQL syntax used is generally standard and should be compatible with most popular relational database systems.
