# Functional Overview

**Project:** Automated Employee Onboarding & Offboarding System

---

## Description

The Automated Employee Onboarding & Offboarding System is designed to streamline the employee lifecycle using the ServiceNow platform. The system replaces manual processes with automated workflows that manage request submission, approvals, departmental task assignments, and lifecycle tracking.

The solution integrates **Service Catalog forms, Flow Designer automation, role-based access controls, and lifecycle tracking tables** to ensure a secure and efficient process.

---

## Core Functionalities

### 1. Request Submission

* Users submit onboarding or offboarding requests through the **Service Portal**.
* The request form collects required employee information using catalog variables.
* Submitted requests generate unique request numbers for tracking.

---

### 2. Automated Approval Workflow

* Requests are automatically routed to the **assigned manager** for approval.
* Approval is required before further workflow steps are triggered.
* Manager decisions determine the next stage of the process.

---

### 3. Departmental Task Automation

After approval, the system automatically generates tasks for relevant departments:

* **HR** – Handles employee documentation and onboarding/offboarding processes.
* **IT** – Provides or revokes system access and user accounts.
* **Facilities** – Allocates or collects physical assets and workspace.
* **Security** – Manages physical access permissions.

Each department receives tasks related to their specific responsibilities.

---

### 4. Lifecycle Data Tracking

* All request data is stored in the **Employee Lifecycle custom table**.
* The table tracks:

  * Employee details
  * Request type
  * Approval status
  * Task completion status
  * Final request closure

This enables centralized lifecycle tracking.

---

### 5. Dynamic Form Behavior

* **UI Policies** dynamically show or hide fields depending on the request type.
* Example:

  * If **Request Type = Onboarding → Joining Date appears**.
  * If **Request Type = Offboarding → Exit Date appears**.

This improves form usability and reduces errors.

---

### 6. Notifications and SLA Monitoring

* Automated **email notifications** inform users at each workflow stage.
* **Service Level Agreements (SLAs)** track task completion timelines.
* Managers and administrators can monitor progress through reports.

---

## Expected Outcome

* Automated employee lifecycle management.
* Faster onboarding and offboarding processes.
* Improved collaboration between HR, IT, Facilities, and Security teams.
* Secure handling of employee data with role-based access control.

---
