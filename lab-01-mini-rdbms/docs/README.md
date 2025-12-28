# Design & Documentation - Lab 01

This document explain the design decisions, assumptions, and limitations of the Mini RDBMS Simulation Lab.

---

## 1. Design Decisions

-Google Sheets was chosen to simulate relational tables due to its structured tabular nature.
-Google Apps Scrippt was used to implement event-driven behaviour similar to database triggers.
-History tables were implemented seperately to maintain immutability and traceability.
-JSON snapshots were used to store full record state efficiently in a single column.

---

## 2. Constraint Simulation Strategy

-Primary keys are enforced using uniqueness checks on ID columns. 
-Foreign keys are simulated using dropdown validations referencing parent tables.
-Composite uniqueness (User_ID + Project_ID) is enforced using a derived key column.

---

### 3. Limitations

-This system does not support concurrent multi-user conflict resolution.
-Query performance is limited by spreadsheet size and script execution time.
-Automation depends on Google Apps Script and does not execute in exported Excel files.

----

## 4. Future Enhancements 

-Migration to a SQL-based backend (MySQL / PostgreSQL).
-Web-based frontend using Flask or Django.
-Role-based access control for admin and non-admin users.
-Visualization dashboards for audit and history data.
