# Technical Blueprint

**Project:** Automated Employee Onboarding & Offboarding System

---

## Description

The technical blueprint outlines the core technical architecture and implementation details of the Automated Employee Onboarding & Offboarding system in ServiceNow. It documents workflow automation, data structures, approval logic, and SLA configurations that enable efficient employee lifecycle management.

---

## Included Components

### 1. Flow Designer Workflow

The automation logic is implemented using **ServiceNow Flow Designer**.

**Documentation Includes:**

* Workflow screenshots showing the flow execution.
* Step-by-step explanations of onboarding and offboarding processes.
* Flow triggers based on catalog item submissions.

**Key Flow Steps**

1. Catalog request submission trigger.
2. Manager approval request.
3. Conditional routing based on request type.
4. Task creation for HR, IT, Facilities, and Security teams.
5. Status update in the Employee Lifecycle table.
6. Email notification and request closure.

---

### 2. Variable-to-Field Mapping Logic

Catalog variables from the **Onboard/Offboard Employee catalog item** are mapped to the custom lifecycle table.

**Mapping Flow**
Catalog Item Variables → Flow Designer → Employee Lifecycle Table Fields

**Example Variables**

* Employee ID
* Request Type
* Department
* Manager
* Joining Date / Exit Date
* Asset Details
* Access Requirements

These variables are automatically stored in the lifecycle table for structured tracking.

---

### 3. Custom Table Schema

A custom table named **`u_employee_lifecycle`** is created to manage employee lifecycle records.

**Table Fields Include**

* Employee ID
* Request Type
* Department
* Manager
* Joining Date
* Exit Date
* Request Status
* Task Completion Status
* SLA Status

**Purpose**

* Centralized storage of onboarding and offboarding data.
* Lifecycle tracking and reporting.

---

### 4. Approval Routing Logic

Approval routing is configured directly within **Flow Designer**.

**Approval Conditions**

* All onboarding and offboarding requests require **manager approval**.
* Approval is dynamically assigned based on the **Manager reference field**.

**Approval Outcomes**

* **Approved → Workflow continues with task creation.**
* **Rejected → Request status updated and workflow terminated.**

---

### 5. SLA Configuration

Service Level Agreements (SLAs) are configured to monitor task completion timelines.

**Departments with SLA Tracking**

* IT Tasks
* Facilities Tasks
* Security Tasks

**SLA Monitoring Includes**

* Task start time
* Task completion time
* SLA breach detection
* Performance reporting

---

## Expected Outcome

* Clear documentation of system architecture and workflow design.
* Structured understanding of automation logic.
* Improved maintainability and scalability of the ServiceNow implementation.

---
