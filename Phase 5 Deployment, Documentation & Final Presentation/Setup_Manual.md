# Setup Manual

**Project:** Automated Employee Onboarding & Offboarding System

---

## Description

This document provides a **step-by-step guide to replicate the solution in a new ServiceNow Personal Developer Instance (PDI)**. It explains how to configure catalog items, variables, UI policies, workflows, access controls, and testing procedures to successfully implement the automated onboarding and offboarding system.

---

# Implementation Steps

## 1. Create the Catalog Item

### Navigation

ServiceNow → **Service Catalog → Catalog Definitions → Maintain Items**

### Steps

1. Click **New** to create a new catalog item.
2. Configure the following details:

| Field       | Value                                          |
| ----------- | ---------------------------------------------- |
| Name        | Onboard / Offboard Employee                    |
| Catalog     | Service Catalog                                |
| Category    | HR Services                                    |
| Description | Request for employee onboarding or offboarding |

3. Save the catalog item.

---

## 2. Configure Catalog Variables

Add variables to capture employee lifecycle information.

### Key Variables

* Request Type
* Employee ID
* Department
* Manager
* Joining Date
* Exit Date
* Assets
* Access Details

### Steps

1. Open the catalog item.
2. Navigate to **Variables** related list.
3. Click **New** and add the required variables.
4. Save all variables.

---

## 3. Configure UI Policies

UI Policies dynamically control field visibility based on request type.

### Example Policy

| Condition                  | Action            |
| -------------------------- | ----------------- |
| Request Type = Onboarding  | Show Joining Date |
| Request Type = Offboarding | Show Exit Date    |

### Steps

1. Open the catalog item.
2. Navigate to **Catalog UI Policies**.
3. Click **New** and configure the policy condition.
4. Add **UI Policy Actions** to show or hide relevant fields.
5. Save the configuration.

---

## 4. Configure Flow Designer Workflow

### Navigation

ServiceNow → **Flow Designer**

### Steps

1. Click **New Flow**.

2. Add a trigger:

   * **Service Catalog → Catalog Item Requested**

3. Configure workflow steps:

**Step 1:** Manager Approval

* Send approval request to the employee's manager.

**Step 2:** Department Task Creation

* HR Task
* IT Task
* Facilities Task
* Security Task

**Step 3:** Status Update

* Update record in **Employee Lifecycle table**.

**Step 4:** Notification

* Send email notifications for approvals and task completion.

---

## 5. Configure Roles and ACLs

### Roles

Create roles for different stakeholders:

* HR
* IT
* Facilities
* Security
* Manager

### ACL Configuration

Navigate to:

**System Security → Access Control (ACL)**

Configure ACL rules to control:

* Read access
* Write access
* Update permissions

Each role should only access data relevant to their responsibilities.

---

## 6. Test Request Submissions

### Steps

1. Open **Service Portal**.
2. Search for **Onboard / Offboard Employee** catalog item.
3. Fill in required details.
4. Submit the request.

### Verification Checklist

* Request record created.
* Manager approval triggered.
* Department tasks generated.
* Email notifications sent.
* Lifecycle record updated.

---

## Screenshots and Execution Flow

The setup documentation should include:

* Catalog item configuration screenshots.
* Variable setup screenshots.
* UI policy configuration.
* Flow Designer workflow steps.
* Request submission and task generation.

These screenshots help demonstrate the implementation sequence and system behavior.

---

## Expected Result

After completing the setup:

* Onboarding and offboa
