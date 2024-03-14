# Data Engineer Code Test

Welcome to the code test for the Data Engineer position!  
This test aims to evaluate your skills in designing a cost-effective and secure data solution using Databricks, as well as your ability to perform data extraction, transformation, and loading tasks.

## Objectives
- Define components for data storage, processing, and security, considering different data types.
- Incorporate suitable tools and technologies aligned with Databricks.
- Address cost-effectiveness, scalability, and resource utilization.
- Demonstrate data modeling design techniques with real-life scenarios

### Expected Time
Less than 10 hours

## Part 1 - Scenario
Please write code that can be run in Databricks and create workflows to fetch data from a MySQL database with the given table structure.  
Save the data to Parquet files using Databricks and store the files in object storage (AWS S3/Azure Blob Storage). Additionally, create another workflow to read the Parquet files and load the data into tables in Databricks.

Consider the following guidelines:
1. Prepare member table in PySpark Dataframe according to example code in `generate_member_data.py`
2. Load member data into MySQL table(s)
3. Connect to the MySQL database using appropriate libraries or connectors available in Databricks.
4. Write Spark Read/SQL queries to retrieve the required data from the MySQL database.
5. Transform the retrieved data, if necessary, to prepare it for storage in Parquet format.
6. Write the transformed data to Parquet files using Databricks, ensuring to partition the data appropriately.
7. Store the Parquet files in blob storage (e.g. AWS S3, Azure Blob Storage) for data persistence and scalability.
8. Create a workflow to automate the data extraction, transformation, and loading process, ensuring it runs at specified intervals or triggers.
9. For the second workflow, read the Parquet files from object storage into Databricks.
10. Load the data from the Parquet files into the member table(s) in delta table format in Databricks.

## Part 1 - Data
Table: Members

| Column Name       | Data Type | Description                              |
|-------------------|-----------|------------------------------------------|
| member_id         | string    | Unique identifier for each member         |
| first_name        | string    | First name of the member                  |
| last_name         | string    | Last name of the member                   |
| email             | string    | Email address of the member               |
| phone_number      | string    | Phone number of the member                |
| address           | string    | Address of the member                     |
| city              | string    | City where the member resides              |
| country           | string    | Country where the member resides           |
| registration_date | date      | Date when the member registered            |

The script to generate data in the member table can be found in the example file `generate_member_data.py`.  
Please note that you'll need to install the faker library in your Databricks environment for this script to work. You can install it using the command: `!pip install faker`

Although mock data is used in the task, please treat the code and workflow as running in production environment.


## Part 2 - Scenario
Please design (a) fact table(s) in delta table format to store invoice data in `invoice.pdf` and provide the table schema specification included but not limited to table name(s), table description, column names, data types, column definition/description, sample values, constraints (primary keys, unique, nullable, foreign keys, etc.), partitioning strategy, assumption, etc.

## Part 2 - SQL Test
Assume the fact table(s) above is created, please provide the Databricks SQL to query the following results:
1. Find the top 5 customers who have made the highest total purchase amount in Jan 2024.
2. Determine the number of invoices that contain at least one line item with a quantity greater than 10.
3. Find the date with the highest total purchase amount.


## Deliverables List
1. Python and/or SQL notebook, along with an explanation of each step and function used
2. Data Architecture Diagram/ System Design Diagram to illustrate the architecture and components of Part 1 scenario described above.
3. Screenshot of the Databricks Workflow and/or YAML/JSON of the job config of Part 1
4. Table Schema Specification of Part 2
5. SQL Queries of Part 2 SQL Test

Please include your considerations for scalability and data security in the given scenario.

## Submission
- Please clone and recreate this repository as a **private repository**.
- Invite `matthewlam-lcjg` as a collaborator for submission.

Good luck!
