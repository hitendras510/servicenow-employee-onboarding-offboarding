# Data Handling

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Data Handling & Process Automation

---

## Description

The Employee Onboarding Project manages request data by storing onboarding and offboarding details in a custom table called **Employee Lifecycle**. This table maintains structured records containing employee information, request details, and lifecycle status.

Catalog variables from the **Onboard/Offboard Employee** catalog item are automatically captured and mapped to fields in the **u_employee_lifecycle** table using automation in Flow Designer.

---

## Data Storage

Employee lifecycle data is stored in the **Employee Lifecycle custom table** with references to user details and catalog variables.

### Key Data Fields

* Employee ID
* Employee Name
* Department
* Manager
* Request Type (Onboarding / Offboarding)
* Joining Date
* Exit Date
* Assigned Assets
* Access Revocation Details
* Request Status

This structured storage enables efficient tracking and reporting of employee onboarding and offboarding activities.

---

## Variables to Custom Table Records

Process automation is used to capture catalog variables from the **Onboard/Offboard Employee** catalog item and automatically map them to fields in the **u_employee_lifecycle** table.

This ensures that every submitted request creates or updates a structured record in the Employee Lifecycle table.

---

## Process to Map Variables

### Step 1: Create a Flow in Flow Designer

* Open **Flow Designer** in ServiceNow.
* Create a new flow to handle onboarding/offboarding requests.

### Step 2: Configure the Trigger

* Set the trigger to run when the **catalog item is submitted**.
* Select the catalog item **Onboard/Offboard Employee**.

### Step 3: Retrieve Catalog Variables

* Add the **Get Catalog Variables** action.
* Retrieve submitted variable values such as:

  * Employee ID
  * Manager
  * Department
  * Joining Date / Exit Date
  * Assets
  * Access Revocation Details

### Step 4: Create or Update Table Records

* Add the **Create/Update Record** action.
* Select the **Employee Lifecycle (u_employee_lifecycle)** table.

### Step 5: Map Variables to Fields

* Click **Add Fields (+)**.
* Map each catalog variable to the corresponding table field.

Example mappings:

* Employee ID → Employee ID field
* Department → Department field
* Manager → Manager field
* Joining Date → Joining Date field
* Exit Date → Exit Date field

---

## Expected Outcome

* Structured storage of onboarding and offboarding request data.
* Automatic creation or update of lifecycle records.
* Accurate tracking of employee lifecycle activities.
* Improved reporting and workflow automation.

---
