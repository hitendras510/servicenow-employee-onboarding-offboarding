# Access Control

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Security & Access Management

---

## Description

Role-Based Access Control is implemented to protect sensitive employee lifecycle data. When a custom table is created in ServiceNow, four default Access Control Rules (ACLs) are generated automatically. In this project, the default ACLs are used and configured to ensure proper access restrictions.

ACLs are configured to control **read, write, create, and delete** permissions for records in the **Employee Lifecycle** table. Access is granted based on user roles to ensure that only authorized stakeholders can view or modify specific data.

---

## Role-Based ACL Configuration

### Default ACLs

When the **Employee Lifecycle custom table** is created, the following ACLs are automatically generated:

* Create
* Read
* Write
* Delete

These ACLs are used to manage access permissions for the table records.

---

## Access Control Rules (ACLs)

ACLs are configured to restrict access to sensitive data based on user roles.

### Key Access Rules

* **HR Role**

  * Can create onboarding and offboarding requests.
  * Can view and update employee lifecycle records.

* **Manager Role**

  * Can view employee lifecycle records related to their team.
  * Can approve onboarding or offboarding requests.

* **IT Role**

  * Can access tasks related to system access and account creation.
  * Limited access to lifecycle records.

* **Facilities Role**

  * Can view tasks related to workspace or asset allocation.

* **Security Role**

  * Can manage access permissions and monitor security policies.

---

## ACL Implementation Steps

1. Navigate to **System Security → Access Control (ACL)**.
2. Click **New** to create or modify an access control rule.
3. Select the **Employee Lifecycle table**.
4. Define the operation type:

   * Read
   * Write
   * Create
   * Delete
5. Assign the required **roles** to control access.
6. Save and test the ACL configuration.

---

## Expected Outcome

* Secure access to employee lifecycle records.
* Protection of sensitive employee information.
* Controlled access based on user roles and responsibilities.
* Improved system security and compliance.

---
