# 📅 Automatic Event Creation in Google Calendar from Google Sheets Data

🚀 This workflow streamlines the process of creating events in **Google Calendar** using event data stored in a **Google Sheet**.

## 🌟 Overview
🔹 The process begins by **retrieving the latest event entry** from Google Sheets, ensuring only the most recent event details are processed.  
🔹 A **Function Node** formats the event date to align with Google Calendar's required format—ensuring consistency and preventing date-related errors.  
🔹 The structured event details are then **sent to Google Calendar**, where an event is created with essential information such as:
   - 📌 **Event Title (Summary)**
   - 📝 **Description**
   - 📅 **Date**
   - 📍 **Location**
🔹 Customization options include:
   - ✅ **Setting event status** (Busy/Available)
   - 🎨 **Assigning event colors** for better visibility

✨ By automating this process, you **eliminate manual event creation**, ensuring seamless **synchronization** between Google Sheets and Google Calendar—**boosting efficiency, accuracy, and productivity**! 🎯

---

## ⚙️ Prerequisites
Before setting up this workflow, ensure the following:
✅ You have an active **Google account** connected to **Google Sheets** and **Google Calendar**.  
✅ The **Google Sheets API** and **Google Calendar API** are **enabled** in the **Google Cloud Console**.  
✅ **n8n** has the necessary **OAuth2 authentication** configured for both **Google Sheets** and **Google Calendar**.  
✅ Your **Google Sheet** has the required columns for event details:  

### 📊 Example Google Sheet Structure
| 📌 Event Name  | 📝 Event Description | 📅 Event Start Date | 📍 Location |
|--------------|----------------|------------------|----------|
| 🎂 Birthday  | Celebration    | 27-Mar-1989     | City     |
| 💑 Anniversary | Celebration    | 10-Jun-2015     | City     |

---

## 🎨 Customization Options
🛠 Modify the **Google Sheets Trigger** to track updates in specific columns.  
🛠 Adjust the **data formatting function** to support:
   - ⏳ **Different date/time formats**
   - 🌍 **Time zone settings**
   - 🎨 **Custom event colors**
   - 📩 **Attendee invitations**

---

## 🔧 Steps to Implement the Workflow

### 🟢 Step 1: Add the Google Sheets Trigger Node
1️⃣ Click **"Add Node"** and search for **Google Sheets**.  
2️⃣ Select **"Google Sheets Trigger"** and add it to the workflow.  
3️⃣ Authenticate using your **Google account** (select an existing account if already authenticated).  
4️⃣ Select the **Spreadsheet** and **Sheet Name** to monitor.  
5️⃣ Set the **Trigger Event** to **"Row Added"**.  
6️⃣ Click **"Execute Node"** to test the connection.  
7️⃣ Click **"Save"**.  

### 🟡 Step 2: Process Data with Function Node
1️⃣ Click **"Add Node"** and search for **Function**.  
2️⃣ Add the **Function Node** and connect it to the **Google Sheets Trigger Node**.  
3️⃣ In the function editor, **write a script** to extract and format data.  
4️⃣ Ensure the required fields (**title, location, date**) are properly structured.  
5️⃣ Click **"Execute Node"** to verify the formatted output.  
6️⃣ Click **"Save"**.  

### 🔴 Step 3: Add the Google Calendar Node
1️⃣ Click **"Add Node"** and search for **Google Calendar**.  
2️⃣ Select **"Create Event"** operation.  
3️⃣ Authenticate with **Google Calendar**.  
4️⃣ Map the required fields:
   - 📌 **Title**
   - 📝 **Description**
   - 📍 **Location**
   - 📅 **Start time**
5️⃣ (Optional) Set **Event Status** and **Event Colors**.  
6️⃣ Click **"Execute Node"** to test event creation.  
7️⃣ Click **"Save"**.  

### ✅ Step 4: Final Steps
1️⃣ Connect all nodes in sequence (**Google Sheets Trigger → Function Node → Google Calendar Node**).  
2️⃣ **Test the workflow** by adding a sample row in **Google Sheets**.  
3️⃣ Verify that the event is **created in Google Calendar** with the correct details.  

---

## 🤝 About WeblineIndia
This workflow was built by the **AI development team** at **WeblineIndia**. We help businesses **automate processes**, **reduce repetitive work**, and **scale faster**.  
💡 Need something custom? You can **hire AI developers** to build workflows tailored to your needs.  
🚀 Let's innovate together! 💡
