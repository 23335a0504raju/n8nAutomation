# WhatsApp-Controlled Google Drive Automation using n8n

This project demonstrates a fully automated workflow using **n8n**, **WhatsApp**, **Google Drive**, and **Supabase PostgreSQL**. The workflow allows you to control Google Drive files and folders directly via WhatsApp commands.

---

## 🌐 Live Workflow

You can explore the workflow live here: [n8n Automation on Render](https://n8n-s63m.onrender.com/workflow/LyOAkqTZdg3RD30v)

GitHub Repository: [https://github.com/23335a0504raju/n8nAutomation](https://github.com/23335a0504raju/n8nAutomation)

---

## 🛠 Tools and Stack

- **n8n** (Docker & Render deployment)
- **WhatsApp Sandbox / Twilio API** for messaging
- **Google Drive** for file/folder management
- **Supabase PostgreSQL** for logging and metadata storage
- **Render** to host n8n workflow for free (forever free plan)

---

## 📦 Workflow Overview

1. **Webhook Node**: Receives WhatsApp messages as POST requests.  
2. **Parse Command Node**: Extracts the command, folder, file, media, and sender info.  
3. **Switch Node**: Determines the command type (UPLOAD, DELETE, RENAME, SUMMARY, LIST).  
4. **Google Drive Nodes**: Perform file/folder operations like listing, renaming, uploading, or deleting.  
5. **Supabase Node**: Stores logs and file metadata for tracking.  
6. **Reply Node**: Sends confirmation back to WhatsApp (success/failure or invalid command).

---

## 📋 Supported WhatsApp Commands

| Command | Example | Description |
|---------|---------|-------------|
| **DELETE** | `DELETE/Reports/new` | Deletes the file `new` from the folder `Reports`. |
| **LIST** | `LIST /certificates` | Lists all files inside the folder `certificates`. |
| **RENAME** | `RENAME/certificates/Delloite.pdf newname Delloite` | Renames `Delloite.pdf` in `certificates` folder to `Delloite`. |
| **SUMMARY** | `SUMMARY /feeReceip` | Provides a summary of the contents of the folder `feeReceip`. |
| **UPLOAD** | `UPLOAD /folder file.pdf` | Uploads a new file `file.pdf` to the folder `folder`. |

---

## ⚡ Key Features

- Fully automated **WhatsApp to Google Drive operations**.
- Supports multiple commands with dynamic parsing.
- Hosted on a **forever free plan** using Render + n8n Docker.
- Integrated **Supabase PostgreSQL database** for logging.
- Sends real-time confirmation messages to WhatsApp.

---

## 🛠 Challenges Faced

- Parsing **nested JSON payloads** from WhatsApp messages.
- Handling **Google Drive API file/folder queries** reliably.
- Debugging workflow when **file IDs returned null** or commands were invalid.
- Implementing a robust **invalid command handler** for WhatsApp responses.

---

## ✅ Achievements

- Created a **fully operational WhatsApp bot** that manipulates Google Drive.  
- Developed a **scalable workflow in n8n** using free tools.  
- Integrated **Supabase PostgreSQL** for logging and debugging.  
- Learned advanced **n8n nodes and JavaScript code execution** within workflows.  
- Successfully deployed the workflow on **Render for continuous automation**.

---

## 📂 Future Improvements

- Add **authentication for multiple users**.  
- Enable **file content preview** via WhatsApp.  
- Extend to **other cloud storage platforms**.  
- Improve **error handling and logging** with analytics dashboards.
