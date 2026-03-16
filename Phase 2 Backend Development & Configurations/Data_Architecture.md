# Data Architecture

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Data Architecture Design

---

## Description

The project uses a custom **Employee Lifecycle** table to store onboarding and offboarding details such as Employee ID, Department, Dates, and Status.

Service Catalog variables are mapped to this table to capture employee information during request submission. **Flow Designer** automates approval workflows and departmental task assignments for HR, IT, Facilities, and Security teams.

Role-Based Access Control (RBAC) and **Access Control Lists (ACLs)** ensure that stakeholders only access data relevant to their responsibilities. Dashboards and reports provide visibility into request status, SLA tracking, and overall employee lifecycle progress.

---

## Subtasks

### 1. Creation of Tables

**Objective**
Create a custom table to store employee onboarding and offboarding data.

**Tasks**

* Create a table named **Employee Lifecycle**.
* Define the purpose of the table for storing lifecycle data.
* Enable record creation for onboarding and offboarding requests.

---

### 2. Creation of Groups

**Objective**
Create user groups representing departments involved in the process.

**Tasks**

* Create groups for **HR**, **IT**, **Facilities**, and **Security**.
* Assign users to their respective groups.
* Use these groups for workflow task assignments.

---

### 3. Creation of Table Records

**Objective**
Allow the system to create records for each onboarding and offboarding request.

**Tasks**

* Configure the table to store request records.
* Ensure records capture employee lifecycle details.
* Link catalog request submissions to table records.

---

### 4. Creation of Fields

**Objective**
Add fields to store required employee lifecycle information.

**Fields**

* Employee ID
* Employee Name
* Department
* Joining Date
* Exit Date
* Request Type (Onboarding / Offboarding)
* Status

**Tasks**

* Configure appropriate data types for each field.
* Map catalog variables to table fields.
* Ensure proper data storage and retrieval.

---

## Expected Outcome

* Structured data storage for employee lifecycle management.
* Automated workflow integration with stored data.
* Secure access to data through role-based permissions.
* Improved visibility through reporting and dashboards.
