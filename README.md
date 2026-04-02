# Leave Approval Automation using n8n

## 📌 Project Overview
This project is an HR Leave Approval Automation System built using **n8n, Google Sheets, and Gmail**. The workflow automatically processes employee leave requests and sends approval or rejection emails based on predefined conditions.

Whenever a new leave request is submitted through Google Sheets, the automation checks the **number of leaves already taken** and decides whether the request should be **approved or rejected**.

This project demonstrates how workflow automation can simplify HR operations, reduce manual work, and improve response time.

---

## ⚙️ Workflow Logic
1. A leave request is submitted and stored in **Google Sheets**.
2. The **Google Sheets Trigger** in n8n detects a new row.
3. The workflow checks the **number of leaves taken** by the employee.
4. If the number of leaves is **greater than 3**, the leave request is rejected.
5. If the number of leaves is **3 or less**, the leave request is approved.
6. An automated email notification is sent to the employee.
7. The result is logged back into **Google Sheets**.

---

## 🔄 Workflow Architecture

Google Form / Google Sheets  
↓  
Google Sheets Trigger (n8n)  
↓  
IF Condition (Check Leave Count)

If Leave > 3  
→ Send Rejection Email  
→ Append Data to Google Sheet  

If Leave ≤ 3  
→ Send Approval Email  
→ Append Data to Google Sheet  

---

## 🧰 Technologies Used
- n8n – Workflow automation platform  
- Google Sheets API – To track leave requests  
- Gmail API – To send automated email notifications  
- Google Forms – To collect leave requests  

---

## 📊 Example Input Data

| Name | Email | No of Leave Taken |
|------|------|------------------|
| John | john@email.com | 2 |
| Alex | alex@email.com | 4 |

---

## 📧 Email Automation

### Approved Leave
Subject: Approved  

Message:  
`[Employee Name] yayy your leave is approved`

### Rejected Leave
Subject: Not Approved  

Message:  
`[Employee Name] sorry not approved`

---

## 📸 Project Screenshots

### n8n Workflow Dashboard
This screenshot shows the automation workflow created in n8n including the trigger, condition logic, and email actions.
<img width="1920" height="1128" alt="Screenshot 2026-04-02 134253" src="https://github.com/user-attachments/assets/de9f8afa-636e-4ce8-bbd8-2f0986803c00" />

![n8n Workflow](images/n8n-workflow.png)
<img width="799" height="445" alt="Screenshot 2026-04-01 155549" src="https://github.com/user-attachments/assets/026b6d1c-39dd-426c-9980-b2725fce3254" />

### Google Sheets Leave Data
This screenshot shows how employee leave requests are stored and processed in Google Sheets.

![Google Sheets Dashboard](images/google-sheets-dashboard.png)

---

## 📂 Project Structure

leave-approval-automation  
│  
├── images  
│   ├── n8n-workflow.png  
│   ├── google-sheets-dashboard.png  
│  
├── workflow.json  
├── README.md  

---

## 🚀 How to Run This Project

### Step 1
Install n8n

npm install n8n -g

### Step 2
Start n8n

n8n start

### Step 3
Import the workflow JSON file into n8n.

### Step 4
Connect required credentials:
- Google Sheets OAuth
- Gmail OAuth

### Step 5
Activate the workflow.

Once activated, the automation will run automatically whenever a new leave request is added to the sheet.

---

## 🚀 Future Improvements
This project can be expanded with additional features such as:

- Admin dashboard for HR managers  
- Database integration using MySQL or PostgreSQL  
- Slack or Microsoft Teams notifications  
- Automatic leave balance tracking  
- Multi-level approval system (Manager → HR → Final approval)  
- AI-based leave pattern analysis  
- Web dashboard using React or Streamlit  

---

## 🎯 Use Case
This automation helps HR teams manage leave requests efficiently by reducing manual approval processes and ensuring faster communication with employees.

---

## 👩‍💻 Author
Taniya Pandey  
Automation & AI Enthusiast
