# Navigation Flow

**Project:** Automated Employee Onboarding & Offboarding System
**Phase:** Navigation & User Interaction Flow

---

## Description

The Navigation Flow explains how users interact with the ServiceNow portal to submit onboarding or offboarding requests. Users access the Service Portal, navigate to the required catalog item, submit a request, and receive confirmation through generated request numbers and email notifications.

---

## Procedure

### Step 1: Login to ServiceNow

* Login to your **ServiceNow Personal Developer Instance (PDI)**.

---

### Step 2: Copy Instance Domain

* Copy the instance domain URL.
  Example:

```
https://dev190678.service-now.com
```

---

### Step 3: Access the Service Portal

* Paste the copied URL into a new browser tab.
* Add **/sp** at the end of the URL.

Example:

```
https://dev190678.service-now.com/sp
```

This will open the **Service Portal**.

---

### Step 4: Search for Catalog Request

* In the Service Portal search bar, search for **Network Requests** or the required catalog request item.

---

### Step 5: Fill Request Details

* Open the request form.
* Enter all required information such as:

  * Employee Name
  * Employee ID
  * Department
  * Request Type (Onboarding / Offboarding)
  * Joining Date or Exit Date

---

### Step 6: Submit the Request

* After filling all required details, click **Submit**.

---

### Step 7: Request Generation

* A **new request record** will be generated in the system.
* The request will have a **unique request number** for tracking.

---

### Step 8: Email Notification

* The user will receive an **email notification** confirming the request submission.
* The request will proceed to the **approval and workflow process**.

---

## Expected Outcome

* Users can easily submit onboarding or offboarding requests through the Service Portal.
* Requests are automatically generated with unique request numbers.
* Users receive confirmation emails for submitted requests.
* The workflow process begins automatically after submission.

---

