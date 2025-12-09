# Automated User Check Workflow (n8n)

This repository contains an n8n workflow that automatically checks user data from an internal API, evaluates conditions, and performs different actions based on the results.

---

## 🚀 Workflow Overview

The workflow runs on a schedule and contains the following steps:

### 1. Schedule Trigger
The workflow starts automatically at a defined time (daily/hourly).  
This ensures continuous monitoring without manual execution.

### 2. HTTP Request
- Sends a GET request to:  
  `https://internal.users...`
- Fetches updated user or system data.
- Passes the response to the IF node.

### 3. IF Condition
The workflow checks a specific condition in the API response.  
Based on this condition:

#### ➤ TRUE branch:
- **Edit Fields**: Formats or prepares the API output.
- **Create Airtable Record**: Stores the cleaned data as a new record in Airtable.

#### ➤ FALSE branch:
- **Code Node**: Executes custom logic or transforms error data.
- **Discord Notification**: Sends an alert message to a specified Discord channel.

---

## 📌 Purpose of the Workflow

- Automate daily user checks  
- Log valid or matched data in Airtable  
- Notify via Discord when data does not meet required conditions  
- Reduce manual monitoring and errors  

---

## 🛠️ Technologies Used

- **n8n** (Workflow automation)
- **Airtable** (Record storage)
- **Discord** (Notifications)
- **REST API** (Internal data source)
- **JavaScript** (Custom Code Node)

---

## 📂 Files in Repository
- `/automation-user-check-workflow
.json` – Exported workflow file
- `/automation-user-check-workflow
.png` – Screenshot of workflow    
- `/README.md` – Documentation  
- Additional config files if needed

---

## 🔧 Setup Instructions
1. Import the workflow.json file into n8n.
2. Update API URL and authentication.
3. Connect Airtable credentials.
4. Connect Discord webhook or bot.
5. Enable the schedule trigger.

---

## 📬 Author
Rimsha Hanif

