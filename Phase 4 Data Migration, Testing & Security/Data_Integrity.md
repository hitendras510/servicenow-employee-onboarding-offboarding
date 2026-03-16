# Data Integrity

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Data Integrity & Validation

---

## Description

Data integrity ensures that employee lifecycle information remains accurate, consistent, and reliable throughout the onboarding and offboarding process. Validation rules, automation, and workflow conditions are implemented to prevent incomplete or incorrect data submissions.

The system enforces mandatory fields, auto-populates key information, validates date conditions, and ensures that approval processes are completed before requests progress.

---

## Field Validation and Automation

### Mandatory Fields

To prevent incomplete submissions, the following fields are configured as mandatory:

* Employee ID
* Request Type
* Department
* Manager

This ensures that all essential employee information is captured before a request is submitted.

---

### Auto-Populate Logic

Certain fields are automatically populated using **reference fields and dot-walking** in ServiceNow.

Auto-filled values include:

* Current User
* Manager
* Department

This reduces manual input, minimizes errors, and improves form usability.

---

### Date Validations

Date validation rules ensure logical and consistent data entry.

Validation checks include:

* **Joining Date must be earlier than Exit Date**.
* Prevent overlapping onboarding or offboarding requests for the same employee.

These validations help maintain accurate lifecycle tracking.

---

### Approval State Validation

Requests cannot proceed to the next stage until the **manager approval** is completed.

This is enforced using **Flow Designer conditions**, ensuring that:

* Manager approval is mandatory.
* Workflow actions are triggered only after approval.

---

# Data Integrity Implementation Summary

| Area               | Actions Taken                                                                                                                                                                 |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Data Handling**  | Catalog variables such as Employee ID, Department, Dates, Manager, and Assets are mapped to the **Employee Lifecycle custom table** for structured tracking.                  |
| **Access Control** | Implemented **role-based ACLs** where HR manages requests, IT/Facilities/Security handle tasks, and Managers approve requests only for their reporting employees.             |
| **QA Testing**     | Conducted **unit testing, integration testing, and user acceptance testing (UAT)** to validate request creation, approvals, SLA tracking, notifications, and task completion. |
| **Data Integrity** | Enforced mandatory validations, auto-populated fields (Department and Manager), date validation checks, and approval state enforcement.                                       |

---

## Expected Outcome

* Accurate and consistent employee lifecycle records.
* Reduced chances of incorrect or incomplete submissions.
* Improved workflow reliability.
* Strong data governance and validation controls.

---
