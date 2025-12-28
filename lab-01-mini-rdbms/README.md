# Lab 01 - Mini RDBMS Simuation (Google Sheets + Apps Script)

##Overview
This lab is an individual project that simulates core Relational Database Management System (RDBMS) behaviors using **Google Sheets** and **Google Apps Script**.
The goal of the lab is to demonstrate database design principles, data integrity enforcement, audit logging, and versioned record history without using a traditional database engine.

---

## Key Features Implemented 

### 1. Relational Schema Design
-Users, Projects, and Assignments tables
-Many-to-many relationship implemented using a junction table (Assignments)
-Structured schema with clearly defined attributes

### 2. Database Constraints
-Primary key enforcement (unique indentifiers)
-Foreign key validation using controlled dropdowns
-Composite key enforcement to prevent duplicate User-Project assignments

### 3. Data Integrity & Validation
-Input validation rules to prevent invalid or inconsistent data
-Referential integrity checks across tables
-Controlled vocabularies for status and roles

### 4. Audit Logging (Event-Driven)
-Automatic logging of INSERT and UPDATE operations
-Field-level change tracking (old value -> new value)
-Permanent timestamps generated via Apps Script triggers

### 5. Versioned Record History
-Dedicated history tables for Users, Projects, and Assignments
-Incremental version numbers per record
-JSON-based snapshots capturing full row state and change metadata
-Enables traceability and historical reconstruction of data changes

### 6. DB Admin Console
-Centralized admin-style interface
-Search user by User_ID
-Search project by Project_ID
-View all project assignments for a selected user

---

## Data Volume
-Users: 30+ records
-Projects: 20+ records
-Assignments: 100+ records
-Audit logs and history tables populated through real edits

This data volume is intentionally used to simulate a realistic internal system rather than a minimal demo.

---

##Project Structure
