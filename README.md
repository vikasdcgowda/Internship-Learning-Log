

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

# Internship Diary – Day 4
 
## Objective

The objective of the fourth day was to migrate **Customer object data** from the source dataset to Salesforce using the Datamatter Gravity platform and understand the mapping process between source fields and Salesforce fields.
 
---
 
## Work Done
 
### 1. Customer Data Migration Attempt

On this day, I worked on migrating the **Customer object dataset** into Salesforce. The migration pipeline included reviewing metadata, transformation rules, and especially the **mapping stage**, where each source field must be mapped to a corresponding Salesforce field.
 
---
 
### 2. Issue with Field Mapping

During the mapping process, we encountered a problem where some fields were being mapped incorrectly. The system automatically suggested mappings that linked certain source fields to unrelated Salesforce fields.
 
After analyzing the issue, we identified that this was actually a **bug in the mapping suggestion system**, which was incorrectly recommending target fields for some attributes.
 
This required manually reviewing and correcting the field mappings.
 
---
 
### 3. Mistake Identified During Migration

Another issue occurred due to a mistake from my side. I had included the **customer_id** field from the source dataset in the migration mapping.
 
However, Salesforce automatically generates a **unique system ID** for each record when data is inserted. Because of this, the `customer_id` field should not be migrated as a system identifier.
 
Including this field caused confusion during the migration process. Once we understood this behavior, we removed the `customer_id` field from the mapping configuration.
 
---
 
## Key Learnings
 
- Salesforce automatically generates record **IDs**, so they should not be migrated from external datasets.

- Careful review of **field mapping** is necessary before executing data migration.

- Automated mapping suggestions may not always be correct and should be validated manually.

- Understanding the **target system’s data model** is important for successful data migration.
 
---
 
## Outcome

By the end of the day, the issue with incorrect mapping was identified and the migration configuration was updated by removing the unnecessary `customer_id` field. This helped improve my understanding of how Salesforce handles record identifiers and how to properly configure migration pipelines.
 
---

# Internship Diary – Day 5
 
## Objective

The objective of the fifth day was to extend the migration process by attempting to migrate another object, **Order**, into Salesforce using the Datamatter Gravity platform.
 
---
 
## Work Done
 
### 1. Attempt to Add Order Object

On this day, I tried to configure and migrate a new object called **Order** to Salesforce. The goal was to understand how multiple objects can be migrated and how relationships between objects can be handled during migration.
 
---
 
### 2. Authentication Error During Connection

While attempting to connect Datamatter Gravity with Salesforce, I encountered an error during the connection process:

- Error Code: 424 (Authentication Failed)
 
This error prevented the system from establishing communication with Salesforce, and therefore the migration process could not proceed further.
 
---
 
### 3. Troubleshooting Steps

Initially, I was using **Amit Sir’s Salesforce credentials** to perform the connection. When the authentication issue occurred, I tried several troubleshooting steps.
 
First, I attempted to create my **own Salesforce account** and tried connecting again using my credentials. However, the same authentication error still occurred.
 
To resolve this issue, I discussed the problem with **Abhishek Sir and Vaishnavi Ma'am**. They suggested several modifications during the Salesforce setup process, including reviewing the connected app configuration, OAuth settings, and authentication parameters.
 
Following their suggestions, I carefully rechecked the setup and attempted the connection again.
 
---
 
### 4. Additional Troubleshooting

Even after implementing the suggestions from **Abhishek Sir**, I continued troubleshooting the issue by reviewing documentation and also consulting **ChatGPT** for possible configuration fixes.
 
Despite trying multiple solutions throughout the day, the authentication error persisted and the connection could not be successfully established.
 
---
 
## Key Learnings
 
- Understood how **Salesforce setup and connected app configuration** works.

- Learned about **OAuth authentication and API connection setup** in Salesforce.

- Gained practical experience in troubleshooting **authentication and integration errors**.

- Became more familiar with the **Salesforce setup environment and configuration process**.
 
---
 
## Outcome

Although the migration was not successfully completed due to the authentication error (424), the day was productive in terms of learning. I gained a better understanding of Salesforce setup.
 
---
 
# Internship Diary – Day 6
 
## Objective

The objective of the sixth day was to resolve the authentication issue encountered while connecting Datamatter Gravity with Salesforce and continue the work on migrating the **Order object**.
 
---
 
## Work Done
 
### 1. Authentication Error (Error 424)

At the beginning of the day, I was still facing the same authentication problem while connecting the system. The error message displayed was:

- Error 424 – Authentication Failed
 
This prevented Datamatter Gravity from establishing a connection with Salesforce.
 
---
 
### 2. Troubleshooting with Abhishek Sir

To resolve this issue, I discussed the problem with **Abhishek Sir**. He carefully analyzed the configuration and helped troubleshoot the issue step by step.
 
Before this discussion, I had created an **External Client App** in Salesforce. However, it turned out that for this integration I actually needed to create a **Connected App** instead.
 
Following this realization, I created the Connected App using the correct path in Salesforce:

Setup → Connected Apps → Manage Connected Apps → New Connected App
 
After configuring the Connected App, I attempted the connection again, but the same authentication error was still occurring.
 
---
 
### 3. Identifying the Missing Configuration

Based on Abhishek Sir’s suggestion, I then connected with **Ankit Sir** to further analyze the problem. He reviewed the Salesforce setup configuration and identified the exact issue.
 
The missing configuration was in the Salesforce settings:
 
After configuring the Connected App, I attempted the connection again, but the same authentication error was still occurring.
 
---
 
### 4. Progress on Order Object Migration

Once the connection issue was resolved, I proceeded with the next task of adding another object for migration, which was the **Order object**.
 
During this stage, I configured the object and worked on the **field mapping process**. The fields were mapped correctly today, and the migration setup for the Order object is currently **in progress**.
 
---
 
## Key Learnings
 
- Learned the difference between **External Client App and Connected App** in Salesforce integrations.

- Understood how **OAuth authentication settings** impact API integrations.

- Identified that enabling **OAuth Username-Password Flow** is necessary for certain authentication methods.

- Gained practical experience troubleshooting **integration and authentication errors** in Salesforce.

- Improved understanding of **object mapping during data migration**.
 
---
 
## Outcome

By the end of the day, the authentication issue that had been occurring for multiple days was successfully resolved. I was able to establish a connection with Salesforce and proceed with configuring the **Order object migration**, which is currently ongoing.
 
---
 
---
 
# 📘 Internship Learning – Day 7
 
## 🎯 Objective
 
Today, I worked on migrating multiple objects and understanding relationships between them in Salesforce using Datamatter.
 
---
 
## 🔧 Work Done
 
Today, I first attempted to migrate the **Customer (Contact) object**, and it was **successfully completed**. This helped me gain confidence in handling basic data migration.
 
After that, I tried working with another object, **Order (child object)**, to understand how relationships work between objects in Salesforce.
 
During this process, I faced multiple issues and errors:
 
* Incorrect field mapping (AI mapped fields wrongly, such as mapping external ID to Salesforce ID)

* Metadata issues (fields were not visible until I refreshed metadata)

* Data format issues (date vs datetime mismatch)

* Faced difficulty while working with **child object (Order)**
 
---
 
## ❗ Additional Issue Faced
 
While mapping fields for Order, I encountered another error:
 
```text

total_amount → Read-Only Field

```
 
### 🔍 Reason
 
* Some standard Salesforce fields are **read-only**

* These fields cannot be inserted or updated during migration
 
### ✅ Solution
 
* I created a **custom field** in Salesforce to store the value

* Then mapped the dataset field to this custom field instead
 
---
 
##Picklist Issue

* Salesforce Status field is dynamic

* But my dataset had fixed values:

```text

pending, completed, cancelled

```

✔ Solution: Need to match picklist values or create custom field
 
## ❗ Major Issue Faced
 
While trying to migrate the **orders.csv (Order object)**, I encountered the error:
 
```text

REQUIRED_FIELD_MISSING: Select an account

```
 
---
 
## 🔍 Root Cause Analysis
 
After analyzing the issue, I understood the actual reason:
 
👉 Salesforce requires **Account as a mandatory parent object**
 
* A **Contact (Customer)** must be linked to an Account

* An **Order** must also be linked to an Account
 
---
 
## 🧠 Key Concept Learned
 
```text

Salesforce Relationship Structure:

Account → Contact (Customer) → Order

```
 
👉 This means:
 
* We cannot directly create Orders without Account

* Proper **data hierarchy and order of migration** is required
 
---
 
## 🚫 Mistake Made
 
* Tried migrating **Order object without proper Account linkage**

* Did not follow correct migration sequence

* Faced difficulty in handling **child object migration**
 
---
 
## ✅ Correct Approach
 
```text

1. Create Account data  

2. Load Account into Salesforce  

3. Load Customer (Contact) linked to Account  

4. Load Orders linked to Customer (and Account)

```
 
---
 
## 📚 Key Learnings
 
* Salesforce enforces **strict parent-child relationships**

* **Account is mandatory** for Contact and Order

* External IDs are essential for linking data

* Migration must follow **correct sequence**

* Some fields are **read-only and require custom fields**

* Errors like `REQUIRED_FIELD_MISSING` indicate missing relationships

* Proper data modeling is crucial before migration

* Child object migration is more complex than parent object
 
---
 
## 🚀 Outcome
 
Although I was not able to successfully complete the Order migration today, I:
 
* Successfully migrated the **Customer object**

* Understood how to handle **read-only field issues**

* Gained clarity on **Salesforce data hierarchy and relationships**

* Learned the importance of **correct migration order and dependencies**

* Improved my understanding of handling **real-world migration errors**
 
---
 
# Internship Learning
 
# 📘 Learning – Salesforce Data Migration & Object Relationships
 
## 🧠 Overview

Today I worked on understanding Salesforce objects, data migration, and how different objects are connected in a real business scenario. I practiced using multiple objects such as Account, Contact (Customer), Opportunity, Order, and Case to simulate how a real company manages its sales and service processes.
 
---
 
## 🏢 Understanding Salesforce Structure
 
I learned that Salesforce follows a **structured data model**:

Account → Contact → Opportunity → Order → Case
 
 
- **Account** = Parent object (company/customer)

- **Contact** = Person (customer)

- **Opportunity** = Sales deal

- **Order** = Purchase

- **Case** = Support issue
 
👉 Data must always be inserted in this order.
 
---
 
## 🔗 Entity–Relationship (ER Concept)
 
- **Entity** = Object (like Account, Contact)

- **Relationship** = Connection between objects
 
Example:

- Contact belongs to Account  

- Order belongs to Account  
 
👉 This is how data is organized in Salesforce.
 
---
 
## ⚙️ Data Migration Practice
 
I worked on uploading datasets and mapping fields correctly.
 
### Key Learning:

- Account must exist first  

- Child objects must be linked to Account  

- Proper mapping is required for successful migration  
 
---
 
## 🔑 External ID
 
I understood that:
 
- External ID is used to store my system IDs (like `A001`)

- It helps Salesforce match records without using Salesforce-generated IDs
 
Example:

External_Account_ID__c = A001
 
 
👉 Used for linking data across systems
 
---
 
## 🔗 Foreign Key vs Lookup
 
### ✅ Foreign Key

- Used to **find and match records**

- Example:

- account_external_id → Account.External_Account_ID__c

- - Mandatory for migration
 
---
 
### ⚠️ Lookup

- Used to **create optional relationships**

- Not always required

- In my case, it was not needed
 
---
 
### 💡 Important Realization
 
In my tool:
 
> Foreign Key handled both **finding and linking**
 
So Lookup was not required in my scenario.
 
---
 
## ❌ Errors Faced & Fixes
 
### 1. REQUIRED_FIELD_MISSING: Select an account

- ❌ Cause: Account not linked

- ✅ Fix: Proper foreign key mapping
 
---
 
### 2. INVALID_FIELD_FOR_INSERT_UPDATE

- ❌ Cause: Trying to insert into system field

- ✅ Fix: Remove or use custom field
 
---
 
### 3. Wrong Mapping

- ❌ Used wrong field (Customer ID instead of Account ID)

- ✅ Fixed by matching correct IDs
 
---
 
### 4. Upload Order Issue

- ❌ Uploaded child before parent

- ✅ Correct order followed
 
---
 
## 🔄 Sales vs Service Understanding
 
### Sales Objects:

- Account

- Contact

- Opportunity
 
### Service Objects:

- Case

- Support-related data
 
### Common Objects:

- Account

- Contact
 
---
 
## 🧠 Key Takeaways
 
- Salesforce is both a **business system + database**

- Data must follow **parent-child structure**

- **Foreign Key is critical** for migration

- **External ID acts as bridge** between systems

- Lookup is optional and not always required

- Correct mapping and order are very important
 
---
 
## 🚀 Final Understanding
 
> Salesforce works on structured relationships.  
> If relationships are not properly defined, data migration will fail.
 
Today I gained a clear understanding of:

- Object relationships  

- Data migration process  

- Real-world Salesforce data flow  
 
---

- Mandatory for migration
 
---
 
### ⚠️ Lookup

- Used to **create optional relationships**

- Not always required

- In my case, it was not needed
 
---
 
### 💡 Important Realization
 
In my tool:
 
> Foreign Key handled both **finding and linking**
 
So Lookup was not required in my scenario.
 
---
 
## ❌ Errors Faced & Fixes
 
### 1. REQUIRED_FIELD_MISSING: Select an account

- ❌ Cause: Account not linked

- ✅ Fix: Proper foreign key mapping
 
---
 
### 2. INVALID_FIELD_FOR_INSERT_UPDATE

- ❌ Cause: Trying to insert into system field

- ✅ Fix: Remove or use custom field
 
---
 
### 3. Wrong Mapping

- ❌ Used wrong field (Customer ID instead of Account ID)

- ✅ Fixed by matching correct IDs
 
---
 
### 4. Upload Order Issue

- ❌ Uploaded child before parent

- ✅ Correct order followed
 
---
 
## 🔄 Sales vs Service Understanding
 
### Sales Objects:

- Account

- Contact

- Opportunity
 
### Service Objects:

- Case

- Support-related data
 
### Common Objects:

- Account

- Contact
 
---
 
## 🧠 Key Takeaways
 
- Salesforce is both a **business system + database**

- Data must follow **parent-child structure**

- **Foreign Key is critical** for migration

- **External ID acts as bridge** between systems

- Lookup is optional and not always required

- Correct mapping and order are very important
 
---
 
## 🚀 Final Understanding
 
> Salesforce works on structured relationships.  
> If relationships are not properly defined, data migration will fail.
 
Today I gained a clear understanding of:

- Object relationships  

- Data migration process  

- Real-world Salesforce data flow  

 ---
