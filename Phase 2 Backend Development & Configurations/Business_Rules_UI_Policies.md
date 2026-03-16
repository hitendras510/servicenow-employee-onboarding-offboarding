# Business Rules & Catalog UI Policy Configuration

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Business Logic & Form Configuration

---

## Business Rules

### Description

Business Rules are configured to enforce data consistency by updating request status automatically during onboarding and offboarding processes. They also prevent invalid submissions and trigger background updates, such as closing lifecycle records once all departmental tasks are completed.

### Purpose

* Maintain accurate employee lifecycle data.
* Automate request status updates.
* Ensure process completion before closing records.

### Key Functions

* Automatically update request status during onboarding/offboarding.
* Prevent invalid or incomplete submissions.
* Close lifecycle records once all departmental tasks are completed.
* Trigger background updates when workflow stages change.

### Expected Outcome

* Improved data consistency.
* Automated lifecycle record updates.
* Reduced manual intervention in status tracking.

---

# Catalog UI Policy Configuration

## Description

UI Policies dynamically control the visibility of fields in onboarding and offboarding forms based on user selections. Conditional logic ensures that only relevant information is displayed to users, reducing errors and improving form usability.

### Scenario

* If **Request Type = Onboarding**, then the **Joining Date** field should appear.
* If **Request Type = Offboarding**, then the **Exit Date** field should appear.

---

## Configuration Procedure

### Step 1: Navigate to Catalog Items

* Go to **Service Catalog → Catalog Definitions → Maintain Items**.

### Step 2: Open Catalog Item

* Open the catalog item **Onboard/Offboard Employee**.

### Step 3: Access Catalog UI Policies

* Scroll to the **Catalog UI Policies** related list.
* Click **New** to create a new UI Policy.

### Step 4: Configure UI Policy

**Applies To:** Catalog Item
**Catalog Item:** Onboard/Offboard Employee
**Short Description:** Show Joining Date for Onboarding
**Condition:** Request Type is Onboarding

* Save the UI Policy.

### Step 5: Configure UI Policy Actions

* After saving, navigate to **UI Policy Actions** (related list).
* Click **New** to create a new UI Policy Action.

**Configuration:**

* Variable: **Joining Date**
* Visible: **True**

### Step 6: Configure Exit Date Policy

Repeat the same process with the following configuration:

**Short Description:** Show Exit Date for Offboarding
**Condition:** Request Type is Offboarding

**UI Policy Action:**

* Variable: **Exit Date**
* Visible: **True**

---

## Testing

* Update and save all UI Policies.
* Open the form in **Service Portal**.
* Test both scenarios:

  * Select **Onboarding** → Joining Date should appear.
  * Select **Offboarding** → Exit Date should appear.

---

## Expected Outcome

* Dynamic form behavior based on request type.
* Reduced user input errors.
* Improved form usability and efficiency.

