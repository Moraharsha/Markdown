# UnifyApps Company Overview

[UnifyApps](https://www.unifyapps.com/) is an enterprise AI and automation platform company.

In simple terms, they help large companies connect different software systems, automate workflows, and build AI-powered business applications with minimal coding.

---

# What UnifyApps Does

Their platform mainly focuses on four major areas:

## 1. Data Integration
Connecting enterprise applications such as:
- Salesforce
- SAP
- Workday
- Databases
- Internal enterprise systems

This helps companies move and synchronize data between multiple platforms.

---

## 2. Workflow Automation
Automating repetitive business processes such as:
- Approval flows
- Employee onboarding
- Claims processing
- Ticket routing
- Notifications

---

## 3. AI Agents / Generative AI
Building enterprise AI assistants that can:
- Answer employee queries
- Automate support tasks
- Analyze enterprise data
- Trigger workflows intelligently

---

## 4. Low-Code Application Development
Helping organizations quickly create internal business applications without writing large amounts of code.

---

# Example Use Case

A bank may use UnifyApps to:

1. Collect customer data from multiple systems
2. Run fraud detection checks
3. Automate approvals
4. Use AI assistants for employee/customer support

---

# Company Background

UnifyApps was founded in 2023 by former leaders from Sprinklr.

The company operates in:
- India
- Dubai
- New York
- Hyderabad

Official Website:
- https://www.unifyapps.com/

---

# Industries They Serve

UnifyApps works with organizations in:
- Banking
- Retail
- Telecom
- Insurance
- Healthcare
- Government sectors

---

# Common Use Cases

Some common enterprise use cases include:
- Fraud detection
- Claims processing
- HR automation
- Supply chain optimization
- Customer support automation

---

# Technologies Commonly Used

Engineering work at UnifyApps commonly involves:

- Java
- Spring Boot
- APIs
- Distributed Systems
- Cloud Platforms
- Data Pipelines
- Workflow Automation
- AI Orchestration

---

# Why It Matches Java Backend Engineers

For Java backend developers, the company’s work aligns well with:
- Backend API development
- Microservices
- Integration systems
- Event-driven architecture
- Scalable enterprise applications

This makes it a good fit for engineers with experience in:
- Java
- Spring Boot
- REST APIs
- Kafka
- Databases
- Cloud technologies
  # Data Pipeline Overview & Settings

## Introduction

The UnifyApps Data Platform is mainly used to move, organize, and manage data between different systems like databases, applications, cloud storage, etc.

It contains 4 main modules:

- Data Pipelines
- Data Catalog
- Unified Data Model (UDM)
- Data Quality

---

# 1. Data Pipelines

This is the main part of the platform.

A data pipeline is a process that:

- Takes data from one system
- Processes or modifies it
- Sends it to another system

### Example

- Read customer data from MySQL
- Clean or transform the data
- Load it into Snowflake or another database

Think of it like a pipe carrying water from one place to another, but here the “water” is data.

---

# 2. Data Catalog

This helps users find and understand data.

It stores:

- Table names
- Column details
- Data descriptions
- Source information

### Example

If someone wants employee salary data, they can search the catalog and find where that data exists.

---

# 3. Unified Data Model (UDM)

Different systems store data in different formats.

The Unified Data Model creates:

- One common structure
- Standardized data format

### Example

One application stores:

```text
cust_id
```

Another application stores:

```text
customerId
```

UDM maps them into a single standard format.

---

# 4. Data Quality

This module checks whether the data is:

- Correct
- Complete
- Consistent
- Duplicate-free

### Example

If age is negative or email is missing, the system can detect it.

---

# What is ETL?

The platform mainly works using ETL.

## E → Extract

Get data from source systems.

### Examples

- Database
- API
- Excel file

---

## T → Transform

Modify or clean the data.

### Examples

- Remove duplicates
- Change formats
- Apply calculations

---

## L → Load

Store the processed data into the target system.

### Examples

- Data warehouse
- Cloud storage
- Another application

---

# Overall Flow

```text
Source System
     ↓
Extract Data
     ↓
Transform / Clean Data
     ↓
Load into Target System
```
# Simple Summary

The UnifyApps Data Platform helps companies move, clean, standardize, and manage data between multiple systems using data pipelines and ETL processes.

# Creating a Basic Pipeline

This topic guides students through the step-by-step process of creating their first data pipeline. Learners will master the pipeline creation workflow from naming conventions to source selection.

The curriculum covers the extensive range of supported data sources including databases, applications, and APIs. Students will learn how to leverage the connection manager for efficient connection reuse across projects.

Practical exercises will involve creating pipelines between popular databases like Oracle and Microsoft SQL Server. By completion, students will confidently create basic pipelines and understand the importance of proper connection management.

## What is a Data Pipeline?

A data pipeline is a process used to move data from one system to another automatically.

It follows the ETL methodology:

- **Extract** → Read data from the source system
- **Transform** → Process or modify the data if needed
- **Load** → Store the data into the target system

Example:
Oracle Database → Pipeline → Microsoft SQL Server

# Platform Components

The UnifyApps data platform has four main parts:

- **Data Pipelines** → Move data from one system to another  
- **Data Catalog** → Organize and manage all available data  
- **Unified Data Model** → Keep data in a common structure across systems  
- **Data Quality** → Check and improve data accuracy and consistency  

Together, these modules help companies manage their data in one complete platform.

---

# ETL Architecture

The platform uses the **ETL process**:

1. **Extract** → Collect data from different sources  
2. **Transform** → Clean, modify, or process the data  
3. **Load** → Send the processed data to the target system  

This helps organizations move and prepare data efficiently.

---

# Versatile Connectivity

The platform can transfer data between many types of systems, such as:

- Database to Database  
- Application to Database  
- Database to Application  
- Application to Application  

This flexibility allows organizations to connect different tools and systems easily.

# Schema Mapping and Configuration

## Manual Mapping

Manual mapping means choosing exactly how data should move from the source to the destination.

- You can decide which source fields should go to which destination fields.
- This gives better control over data migration based on business needs.
- If source and destination field names and data types are the same, the platform can automatically map them.
- One source table can also send data to multiple destination tables if needed.

### Example

| Source Field | Destination Field |
|---|---|
| customer_name | cust_name |
| phone_number | mobile_no |

Here, data from the source fields is manually connected to destination fields.

## Source Replication

Source replication means creating an exact copy of the source table in the destination system.

- The platform automatically scans the source table structure.
- It creates the same fields and data types in the destination table.
- If the destination database does not support a particular data type, the platform automatically chooses a compatible alternative.
- This is the simplest and fastest method when you want the destination to look exactly like the source.

### Example

If the source table has:
- Employee_ID
- Employee_Name
- Salary

The same structure will automatically be created in the destination database.

# Pipeline Settings and Configuration

## Pipeline Types

### Real-time Pipelines
These pipelines work continuously.  

Whenever data changes in the source system (insert, update, or delete), the changes are immediately copied to the destination system.

**Example:**  
If a new customer is added in the source database, it is instantly updated in the target database.
### Scheduled Pipelines
These pipelines run only at specific times based on a schedule.

They:
- Start automatically at the scheduled time
- Transfer data for a certain duration
- Stop after completion
- Wait for the next schedule

**Example:**  
A pipeline can run every day at 10 PM to move daily sales data.

---

### Schedule Configuration
Users can configure how often the pipeline should run:
- Every few minutes
- Hourly
- Daily
- Weekly

An optional end date can also be added for temporary projects.

---

# Ingestion Modes

## Historical Only
This mode transfers all existing old data one time.

After the data transfer is completed, the pipeline automatically stops.

**Used for:**  
Initial data migration or backup.

---

## Live Only
This mode transfers only new changes happening after the pipeline starts.

It monitors:
- New records
- Updated records
- Deleted records

It uses **upsert logic**, meaning:
- Update the record if it already exists
- Insert the record if it does not exist

---

## Historical and Live
This mode combines both approaches.

### Steps:
1. Transfer all old existing data
2. Continue monitoring and transferring new changes in real time

**Most commonly used mode** for production systems.

---

# Data Capture Settings

## Audit Logging
The platform keeps logs of all pipeline activities.

Logs include:
- Number of records transferred
- Success and failure details
- Event IDs
- Transfer history

This helps with monitoring and troubleshooting.

---

## Raw Record Capture
Users can store the actual data records during transfer.

This includes:
- Successful records
- Failed records
- Skipped records

Useful for:
- Debugging
- Auditing
- Compliance checks

---

## Selective Recording
By default, only failed records are stored.

But users can configure the system to capture:
- Only failed records
- All records
- Specific record types

based on business or audit requirements.
