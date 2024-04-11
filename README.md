# Data Engineer Code Test

Welcome to the code test for the Data Engineer position!  
This test aims to evaluate your skills in designing a cost-effective and secure data solution using Databricks.

## Objectives
- Define components for data storage, processing, and security, considering different data types.
- Incorporate suitable tools and technologies aligned with Databricks.
- Address cost-effectiveness, scalability, and resource utilization.
- Demonstrate data modeling design techniques with real-life scenarios

### Expected Time
Less than 8 hours

## Part 1 - Scenario
Imagine you are working on a large-scale data engineering project in Databricks.
Please provide the notebook code, along with an explanation of each step and function used, and appropriate diagrams to illustrate the architecture and
components of the scenario. In the explanation, please include your considerations for scalability and data security.

Guidelines:
1. Connect to the MySQL database using appropriate libraries or connectors available.
2. Retrieve the required data (Part 1 - Data) from the MySQL database.
3. Write the data to Parquet file(s), ensuring to partition the data appropriately.
4. Store the Parquet file(s) in blob storage (e.g. AWS S3, Azure Blob Storage) for data persistence and scalability.
5. Transform the data, if necessary.
6. Load the data with delta table format.
7. Create a workflow to automate the data extraction, transformation, and loading process.

## Part 1 - Data
Table: member

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


## Part 2 - Scenario
Please design (a) fact table(s) in delta table format to store invoice data in `invoice.pdf` and provide the table schema specification.


## Submission
- Please clone and recreate this repository as a **private repository**.
- Invite `matthewlam-lcjg` as a collaborator for submission.

Good luck!
