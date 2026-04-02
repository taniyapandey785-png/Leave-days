# Leave Approval Automation using n8n

## 📌 Project Overview
This project is an **automation workflow built using n8n** that automatically processes employee leave requests. The system uses **Google Sheets to track leave requests** and **Gmail to send automated approval or rejection emails**.

The workflow checks the number of leaves taken by an employee and automatically decides whether the leave should be approved or rejected.

This project demonstrates how **automation can simplify HR processes and reduce manual work**.

---

## ⚙️ How the Workflow Works

1. Employee submits leave request through **Google Form / Google Sheet**
2. **Google Sheets Trigger** detects a new entry in the sheet
3. The workflow checks the **number of leaves taken**
4. If the number of leaves is **greater than 3**, the leave is rejected
5. If the number of leaves is **3 or less**, the leave is approved
6. The system sends an **automated email to the employee**
7. The result is **stored back in Google Sheets**

---

## 🔄 Workflow Architecture

---

## 🧰 Technologies Used

- **n8n** – Workflow automation platform  
- **Google Sheets API** – To monitor leave requests  
- **Gmail API** – To send automated emails  
- **Google Forms** – To collect leave requests  

---

## 📊 Input Data Example

| Name | Email | No of Leave Taken |
|-----|-----|-----|
| John | john@email.com | 2 |
| Alex | alex@email.com | 4 |

---

## 📧 Email Automation

### Approved Leave

Subject: Approved

Message: yayy your leave is approved

---

## 📸 Project Screenshots

### n8n Workflow Dashboard

This screenshot shows the automation workflow created in **n8n** including triggers, conditions, and email actions.

![n8n Workflow](images/n8n-workflow.png)

---

### Google Sheets Leave Data

This screenshot shows how employee leave data is stored and processed in **Google Sheets**.

![Google Sheets Dashboard](images/google-sheets-dashboard.png)

---

## 📂 Project Structure

---

## 🚀 How to Run This Project

### Step 1
Install **n8n**

### Step 2
Start n8n

### Step 3
Import the **workflow JSON file** into n8n.

### Step 4
Connect credentials:

- Google Sheets OAuth
- Gmail OAuth

### Step 5
Activate the workflow.

Now whenever a new leave request is added to the sheet, the automation will run automatically.

---

## 🚀 Future Improvements

This project can be extended with more advanced features:

- 🔹 **Admin Dashboard**
  Create a dashboard for HR managers to monitor leave requests.

- 🔹 **Database Integration**
  Replace Google Sheets with databases like **MySQL or PostgreSQL**.

- 🔹 **Slack / Microsoft Teams Notifications**
  Send instant notifications to workplace communication tools.

- 🔹 **Leave Balance Tracking**
  Automatically update employee leave balances.

- 🔹 **Multi-Level Approval System**
  Manager → HR → Final approval workflow.

- 🔹 **AI-based Leave Insights**
  Analyze employee leave patterns using AI.

- 🔹 **Web Dashboard**
  Build a dashboard using **React or Streamlit** to visualize leave analytics.

---

## 🎯 Use Case

This project is useful for **HR teams and organizations** that want to automate leave management and reduce manual approval processes.

---

## 👩‍💻 Author

**Taniya Pandey**

Automation & AI Enthusiast  
Exploring workflow automation and AI-powered solutions.
