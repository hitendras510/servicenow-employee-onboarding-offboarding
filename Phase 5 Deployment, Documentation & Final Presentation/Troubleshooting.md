# Troubleshooting

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Troubleshooting & Issue Resolution

---

## Description

Troubleshooting was performed during development and testing to identify and resolve issues related to workflow execution, notifications, catalog variables, and form behavior. ServiceNow system logs, Flow Designer execution details, and form testing were used to diagnose and fix problems to ensure smooth system operation.

---

## Common Issues and Resolutions

### 1. Flow Execution Logs

**Issue**

* Workflow steps not executing correctly during onboarding or offboarding requests.

**Troubleshooting Method**

* Used **Flow Designer → Execution Details** to trace the flow execution.

**Actions Taken**

* Verified trigger conditions for catalog submission.
* Checked approval routing and task generation steps.
* Confirmed that notification actions were triggered correctly.

**Outcome**

* Ensured all flow steps executed successfully and workflows completed as expected.

---

### 2. Email Notification Logs

**Issue**

* Users not receiving email notifications for approvals or task assignments.

**Troubleshooting Method**

* Checked email logs in:

  **System Logs → Email → Sent / Received**

**Actions Taken**

* Verified email notifications for:

  * Manager approvals
  * Departmental task assignments
  * Request closure notifications

**Outcome**

* Confirmed that all email notifications were successfully triggered and delivered.

---

### 3. Variable Population Issues

**Issue**

* Catalog variables were not correctly populating fields in the Employee Lifecycle table.

**Troubleshooting Method**

* Debugged variable sets and catalog configurations.

**Actions Taken**

* Checked variable mappings in Flow Designer.
* Verified catalog variable names and table field mappings.
* Updated catalog client scripts where necessary.

**Outcome**

* Ensured accurate mapping of catalog variables to table fields.

---

### 4. Form Behavior Testing

**Issue**

* Dynamic form fields not appearing correctly in the Service Portal.

**Troubleshooting Method**

* Tested UI policies and catalog client scripts.

**Actions Taken**

* Verified UI policy conditions.
* Ensured correct configuration of show/hide logic.

**Example Behavior**

* If **Request Type = Onboarding → Joining Date field is displayed**.
* If **Request Type = Offboarding → Exit Date field is displayed**.

**Outcome**

* Dynamic form behavior works correctly and improves user experience.

---

## Expected Result

* Smooth execution of onboarding and offboarding workflows.
* Proper delivery of system notifications.
* Accurate data population in lifecycle tables.
* Improved reliability and usability of ServiceNow forms.

---

