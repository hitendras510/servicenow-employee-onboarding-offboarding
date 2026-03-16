# QA Testing

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Quality Assurance Testing

---

## Description

Quality Assurance (QA) testing was performed to verify the complete request lifecycle for onboarding and offboarding processes. Real-world scenarios were simulated to ensure that the system correctly handles request creation, approval routing, task assignment, SLA tracking, notifications, and request closure.

Testing also included verification through **ServiceNow system logs and audit history** to confirm that each workflow step executed correctly.

---

## QA Testing – Request Lifecycle Verification

The following processes were tested:

### 1. Request Creation

* Submitted onboarding and offboarding requests through the Service Portal.
* Verified that requests were successfully created in the **Employee Lifecycle table**.

### 2. Manager Approval Routing

* Confirmed that requests were automatically routed to the **assigned manager** for approval.
* Verified that approval actions triggered the next workflow stage.

### 3. Task Assignment

* Ensured tasks were automatically generated for the relevant departments:

  * IT Team
  * Facilities Team
  * Security Team
* Verified that each team received the appropriate task.

### 4. SLA Tracking

* Confirmed that **Service Level Agreements (SLAs)** were applied to tasks.
* Verified that task completion timelines were monitored correctly.

### 5. Email Notifications

* Checked that automated **email notifications** were sent at key stages:

  * Request submission
  * Approval completion
  * Task assignment
  * Request closure

### 6. Status Updates and Ticket Closure

* Verified that request status updated automatically during each workflow stage.
* Confirmed that the ticket was **closed automatically after all departmental tasks were completed**.

---

## System Verification

To validate correct system execution, the following tools were used:

* **ServiceNow System Logs**
* **Audit History**
* **Request Records**

These tools helped confirm that each process step executed successfully.

---

## Report Verification

To verify request records:

1. Navigate to **Reports → All**.
2. Search for **sc_request**.
3. Open the report to view generated request records and their status.

---

## Expected Outcome

* Successful creation of onboarding and offboarding requests.
* Proper approval routing to managers.
* Automatic task assignment to relevant departments.
* SLA monitoring for task completion.
* Email notifications for workflow updates.
* Proper closure of requests after task completion.

---

