# Project-2-Database-modeling
Designing tables and relationships

Project Overview
This project focuses on designing and implementing a relational database model to support sales analysis. Using real .csv datasets, a star schema was built in PostgreSQL, allowing for structured reporting, trend analysis, and scalable business intelligence solutions.
The project involved:
•	Building fact and dimension tables based on real data.
•	Defining primary and foreign keys to ensure data consistency.
•	Importing structured data into PostgreSQL.
•	Creating an Entity-Relationship Diagram (ERD) to illustrate table relationships.

Tools Used
•	PostgreSQL — Database creation, table management, and data loading.
•	pgAdmin — Query execution and database exploration.
•	dbdiagram.io — ERD visualization and design.
•	Excel — Data cleaning and format adjustments (UTF-8 conversion).

Project Structure
pgsql
/sales_dw_project
├── README.md
├── Code_create_tables_sql_sample.txt # SQL script to create tables
├──Relation_tables_foreign_keys.csv (export SQL)
├── Samples_Querys.doc
│
└── /diagrams
    └── ERD.pgerd              # ERD model file (.png export)

Database Design
•	Fact Table: fact_table — Connects to all dimensions and stores sales metrics (quantity, unit_price, total_price).
•	Dimension Tables: Each dimension table is linked to the fact table through a foreign key relationship.
o	customer_dim
o	item_dim
o	store_dim
o	time_dim
o	trans_dim

 How to Run This Project
•	Create the database in PostgreSQL:
•	CREATE DATABASE sales_dw;
•	Connect to the database and create all tables.
•	Import the data:
\copy customer_dim FROM 'path/to/customer_dim.csv' DELIMITER ',' CSV HEADER;
\copy item_dim FROM 'path/to/item_dim.csv' DELIMITER ',' CSV HEADER;
\copy store_dim FROM 'path/to/store_dim.csv' DELIMITER ',' CSV HEADER;
\copy time_dim FROM 'path/to/time_dim.csv' DELIMITER ',' CSV HEADER;
\copy trans_dim FROM 'path/to/trans_dim.csv' DELIMITER ',' CSV HEADER;
\copy fact_table FROM 'path/to/fact_table.csv' DELIMITER ',' CSV HEADER;
•	Explore the database using SQL queries or connect it to BI tools for visualization.

Author
Monica Prieto — Data Engineer



