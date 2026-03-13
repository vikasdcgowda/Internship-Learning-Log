

# Data Engineering Internship Learning Log

## Intern Information

**Name:** Vikas Gowda D
**Role:** Python Developer Intern
**Organization:** Datamatter Technologies
**Focus Area:** Data Migration & Data Engineering
**Start Date:** 12 March 2026

---

# Daily Learning Tracker

## Day 1 – Basics of Data and Data Migration

**Date:** 10 March 2026

On the first day, I started learning the fundamental concepts related to **data and data migration**. Data refers to information stored in digital form. It can exist in various formats such as databases, Excel sheets, CSV files, APIs, or cloud storage. For example, a table containing customer names, email addresses, and phone numbers is a simple form of data.

I learned that **data migration** is the process of transferring data from one system to another. Organizations usually perform data migration when they move from older systems to newer platforms such as **Salesforce**, or when they upgrade their technology infrastructure.

Companies migrate data for several reasons such as improving system performance, moving their infrastructure to cloud platforms, integrating systems after mergers, or replacing outdated applications with modern solutions.

Another key concept I explored was the **ETL process**, which stands for Extract, Transform, and Load. This process describes the typical workflow used in data migration and data engineering pipelines.

During the **Extract** stage, data is collected from the source systems such as databases, spreadsheets, APIs, or CRM platforms.
In the **Transform** stage, the extracted data is cleaned and organized by removing duplicates, correcting formats, and fixing missing values.
Finally, in the **Load** stage, the processed data is inserted into the destination system, which could be a database, a data warehouse, or a CRM system like Salesforce.

I was also introduced to **Salesforce**, a cloud-based CRM platform that organizations use to manage customer relationships, sales opportunities, leads, and support requests.

CRM stands for **Customer Relationship Management**, which refers to systems that help businesses manage and track interactions with their customers.

---

### Skills and Understanding Gained

* Basic understanding of how data is stored in different formats
* Awareness of how data moves between systems during migration
* Introduction to Salesforce and CRM platforms

---

# Day 2 – Salesforce Data Migration and Datamatter Platform

**Date:** 13 March 2026

On the second day, I continued learning about **Salesforce data migration concepts and the tools used to move data into Salesforce systems**.

Salesforce organizes business data using structures called **objects**. These objects function similarly to tables in a database. Some of the commonly used Salesforce objects include Accounts, Contacts, Leads, Opportunities, and Cases. These objects allow organizations to store and manage customer information, sales activities, and support records.

An important concept I learned is **field mapping**, which is required during data migration. Field mapping ensures that fields from the source system correctly correspond to the appropriate fields in Salesforce. For example, a "Name" column in an Excel sheet might be mapped to the "First Name" field in Salesforce.

Several tools commonly used for migrating data into Salesforce. These include **Salesforce Data Import Wizard**, **Data Loader**, and ETL platforms such as MuleSoft, Talend, and Informatica. Data Loader is widely used when working with large datasets, as it allows users to import, export, update, or delete records in Salesforce using **CSV files**.

Another concept I learned is the difference between **batch data migration** and **real-time integration**. In batch migration, data is transferred in scheduled groups, such as daily or nightly updates. In contrast, real-time integration allows data to move instantly when an event occurs, such as when a user submits a form on a website and a new lead is immediately created in Salesforce.

Additionally, I learned about common issues that may occur during data migration. These include duplicate records, inconsistent data formats, missing information, and incorrect field mappings. Another important aspect is understanding the **order of migration**, because Salesforce objects are often related to each other. For example, an Account must be created before a Contact since contacts are associated with accounts.

---

### Key Concepts Learned

* Salesforce Objects
* Field Mapping
* Data Import Wizard
* Data Loader
* CSV Files
* Batch Data Migration
* Real-Time Data Integration
* Migration Challenges
* Migration Order in Salesforce
---



---

# day - 3 --> Introduction to Datamatter: Gravity

## 1.1 What is Datamatter: Gravity?

**Datamatter: Gravity** is a **data migration platform**.

### First understand: What is Data Migration?

Data migration means **moving data from one system to another system**.

Example:

Old system → New system

* Old **ERP database** → **Salesforce**
* **Excel files** → **Cloud database**
* **Legacy CRM** → **Modern CRM**

Example company scenario:

| Old System          | New System |
| ------------------- | ---------- |
| Oracle Database     | Salesforce |
| Excel Customer Data | CRM System |
| Legacy ERP          | Cloud ERP  |

Manually moving this data is very difficult because:

* Different **data formats**
* Different **field names**
* Dirty or incorrect data
* Relationships between tables
* Risk of losing data

So **Datamatter: Gravity automates the entire migration process**.

You can think of it as:

**A smart ETL platform for data migration**

ETL =

* **E**xtract
* **T**ransform
* **L**oad

Gravity handles this entire process **automatically and safely**.

---

# 1.2 Key Capabilities

## 1.2.1 Intelligent Data Processing

Gravity uses **automation + AI + metadata analysis**.

### 1️⃣ AI-Powered Mapping

When moving data between systems, fields are different.

Example:

| Old System | New System   |
| ---------- | ------------ |
| cust_name  | customerName |
| cust_id    | customerId   |
| addr       | address      |

Normally developers manually map these.

Gravity **automatically suggests mapping**.

Example:

Source Field → Target Field

```
cust_name  → customerName
cust_phone → phoneNumber
cust_mail  → email
```

How it works:

Gravity analyzes:

* field names
* metadata
* data types
* sample values

and suggests the **best mapping automatically**.

This saves **hours or days of manual work**.

---

### 2️⃣ Data Quality Management

Real-world data is usually **dirty**.

Example problems:

| Problem          | Example             |
| ---------------- | ------------------- |
| Duplicate data   | Same customer twice |
| Missing values   | phone = null        |
| Incorrect format | date = 12/45/2022   |
| Wrong characters | name = @@John       |

Gravity has **data cleansing tools**.

Example operations:

* Remove duplicates
* Fix date formats
* Trim spaces
* Standardize values
* Remove invalid records

Example:

Before:

```
Name:  John
Email: john@gmail
Phone: 987654
```

After cleaning:

```
Name: John
Email: john@gmail.com
Phone: 9876543210
```

---

### 3️⃣ Transformation Engine

Sometimes **data structure must change**.

Example:

Old system:

```
FirstName
LastName
```

New system:

```
FullName
```

Transformation:

```
FullName = FirstName + LastName
```

Another example:

Old:

```
DOB = 2000-05-01
```

New:

```
Age = 25
```

Gravity allows:

* Data calculations
* Format changes
* Field combinations
* Field splitting

This is called **data transformation**.

---

# 1.2.2 Complete Migration Lifecycle

Gravity manages the **full lifecycle** of migration.

### Step 1 — Extract

Data is **collected from source systems**.

Examples:

* Oracle database
* MySQL database
* CSV files
* Excel files
* APIs

Example extracted data:

```
customer.csv
orders.csv
products.csv
```

Gravity loads these into its **workspace for analysis**.

---

### Step 2 — Transform

Now data is:

* cleaned
* converted
* formatted
* mapped

Example:

```
cust_name → customerName
cust_id → id
```

---

### Step 3 — Load

After transformation, data is **loaded into the target system**.

Example:

```
Salesforce CRM
Cloud database
Data warehouse
```

Gravity also supports:

* **backup**
* **rollback**

Rollback means:

If migration fails → system returns to **previous safe state**.

---

### Step 4 — Validate

After loading data, Gravity checks:

* Did all records migrate?
* Are values correct?
* Any missing records?

Example:

| Check          | Result |
| -------------- | ------ |
| Source records | 10,000 |
| Target records | 10,000 |
| Errors         | 0      |

Validation ensures **data integrity**.

---

# 1.2.3 Enterprise-Grade Features

These features make Gravity suitable for **large companies**.

---

### 1️⃣ Environment Management

Large projects use different environments:

| Environment | Purpose                |
| ----------- | ---------------------- |
| DEV         | development testing    |
| QA          | quality testing        |
| UAT         | user testing           |
| PROD        | real production system |

Gravity supports all these.

Example migration flow:

```
DEV → QA → UAT → PROD
```

This prevents **production failures**.

---

### 2️⃣ Pipeline Orchestration

Gravity creates **migration pipelines**.

Pipeline = **automated workflow**

Example pipeline:

```
Extract → Clean → Transform → Map → Validate → Load
```

Pipelines are:

* version controlled
* reusable
* automated

Example:

```
pipeline_v1
pipeline_v2
pipeline_v3
```

---

### 3️⃣ Audit Trail

Every action is recorded.

Example log:

```
10:30 AM – Extract started
10:45 AM – Transform completed
11:10 AM – Load completed
11:15 AM – Validation successful
```

Audit trail helps with:

* compliance
* debugging
* security
* reporting

---

### 4️⃣ Error Handling

Migration always has errors.

Example:

```
Invalid email
Missing ID
Duplicate key
```

Gravity:

* detects errors
* logs them
* suggests fixes
* retries migration

Example error log:

```
Row 245 → Invalid email
Row 910 → Duplicate customer ID
```

---

# 1.3 Why Choose Datamatter: Gravity?

## 1️⃣ Reduced Complexity

Traditional migration requires:

* custom scripts
* SQL coding
* manual mapping
* manual validation

That can take **months**.

Gravity automates these steps so migration becomes **weeks instead of months**.

---

## 2️⃣ Minimized Risk

Data migration can destroy data if done wrong.

Gravity reduces risk with:

* validation
* backups
* rollback
* error detection

---

## 3️⃣ Scalable Solution

Gravity works for:

Small migration:

```
Excel → CRM
```

Medium migration:

```
MySQL → Salesforce
```

Enterprise migration:

```
Legacy ERP → Cloud ERP
Millions of records
```

It scales automatically.

---

# 1.4 Core Components

## 1.4.1 Migration Workspace

This is the **main dashboard**.

Think of it as the **control center** of migration.

In the workspace you can:

* upload datasets
* configure pipelines
* monitor migration
* track errors
* validate data

---

## 1.4.2 Pipeline Tabs

Gravity divides migration into **tabs**.

Each tab represents a **step in migration**.

---

### Summary Tab

Overview of project.

Shows:

* uploaded files
* record count
* migration status
* progress

---

### Extract Tab

Used to:

* explore data
* preview datasets
* analyze structure

Example:

```
customer.csv
10000 records
20 columns
```

---

### Relationship Tab

Shows **relationships between datasets**.

Example:

```
Customers → Orders
Orders → OrderItems
Products → OrderItems
```

This is important because data must be loaded in the correct order.

---

### Filter Tab

Allows filtering records.

Example:

```
Only migrate active customers
```

Filter example:

```
status = active
```

---

### Cleanup Tab

Used for **data cleaning**.

Example:

* remove duplicates
* fix invalid formats
* remove null records

---

### Transform Tab

Used for **data transformation**.

Example:

```
FullName = FirstName + LastName
```

or

```
CountryCode = +91
```

---

### Mapping Tab

Maps fields between systems.

Example:

| Source     | Target |
| ---------- | ------ |
| cust_name  | Name   |
| cust_phone | Phone  |
| cust_email | Email  |

Gravity can **auto-suggest mappings**.

---

### Validation Tab

Checks migration rules before execution.

Example checks:

* required fields
* duplicate records
* data type mismatch

---

### Load Tab

Executes the migration.

Gravity pushes data to:

* Salesforce
* Dynamics
* databases
* APIs

---

### Error Handling Tab

Displays errors after migration.

Example:

```
Row 21 → Email missing
Row 87 → Invalid ID
```

Users can fix and re-run migration.

---

### Pipeline Tab

Shows the **complete workflow**.

Example:

```
Extract
 ↓
Clean
 ↓
Transform
 ↓
Map
 ↓
Validate
 ↓
Load
```

---

# 1.4.3 Application Menus

### Dashboard

Project overview.

Shows:

* migration progress
* success rate
* error rate
* pipeline status

---

### Entities

Entities represent **objects or tables**.

Example:

```
Customers
Orders
Products
Invoices
```

Each entity must be mapped between systems.

---

### Management

Used for:

* project planning
* migration estimation
* resource allocation

Example:

```
Estimated records: 2 million
Migration time: 5 hours
```

---

# 1.5 Supported Systems

Gravity supports many systems.

---

## Source Systems

Data can come from:

ERP systems:

```
SAP
Oracle ERP
```

CRM systems:

```
Salesforce
Zoho
HubSpot
```

Databases:

```
MySQL
PostgreSQL
SQL Server
Oracle
```

Files:

```
CSV
Excel
XML
```

Cloud services.

---

## Target Systems

Data can migrate to:

* Salesforce
* Microsoft Dynamics
* Cloud databases
* Data warehouses
* Custom applications via API

---

# 1.6 Getting Started

Typical workflow:

### Step 1 — Create Project

Create migration project inside Gravity.

Example:

```
Project: CRM Migration
```

---

### Step 2 — Define Entities

Define objects.

Example:

```
Customers
Orders
Products
```

---

### Step 3 — Upload Data

Upload source files.

Example:

```
customers.csv
orders.csv
products.csv
```

---

### Step 4 — Configure Pipeline

Configure migration steps:

```
Extract
Transform
Mapping
Validation
Load
```

---

### Step 5 — Execute Migration

Run pipeline.

Gravity will:

* migrate data
* validate results
* generate reports

---

# 1.7 Key Benefits

## Speed

Automation reduces manual work.

Features helping speed:

* AI mapping
* automation pipelines
* parallel processing

---

## Accuracy

AI reduces errors.

Validation ensures:

* no missing records
* no wrong formats
* no duplicate keys

---

## Visibility

You can track everything.

Example dashboard:

```
Total Records: 100000
Migrated: 98000
Errors: 2000
Success Rate: 98%
```

---

## Reliability

Migration safety features:

* backup
* rollback
* retry mechanism
* environment testing

---

# Final Quick Revision (Important Concepts)

Key concepts learned:

Datamatter Gravity is a **data migration platform** that automates the **ETL process (Extract, Transform, Load)**. It provides **AI-powered field mapping, data cleaning, transformation tools, validation systems, and automated pipelines** to move data safely between systems like **ERP, CRM, databases, and cloud platforms**. The platform manages the entire migration lifecycle through structured **pipeline tabs such as Extract, Transform, Mapping, Validation, and Load**. It also includes **enterprise features like environment management, audit trails, rollback systems, and error handling**. Gravity supports many **source systems (ERP, CRM, databases, files)** and **target systems (Salesforce, Dynamics, cloud databases)**. Its main benefits are **speed, accuracy, visibility, and reliability**, making complex enterprise data migrations much easier and safer.

---

