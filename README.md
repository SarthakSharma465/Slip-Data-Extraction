# Slip Data Extraction Project

This project automates the extraction, validation, and processing of slip data using the Microsoft Power Platform, including Power Apps, Power Automate, AI Builder, and SharePoint. It streamlines the process of document submission, data extraction, review, and policy creation, enhancing accuracy and reducing manual effort in underwriting workflows.

---

## 📊 Solution Overview

### Architecture Approaches:

#### 1. **Mailbox-Based Extraction (Legacy Approach)**
- Emails are sent to an Extraction Mailbox.
- Power Automate triggers the extraction process and invokes AI Builder for data extraction.
- Extracted data is stored in SharePoint Lists and Excel files.
- Processed emails are automatically archived.

#### 2. **UI-Based Extraction (Enhanced Approach)**
- Users upload documents via a **Power Apps Data Extraction UI**.
- Documents are stored in a SharePoint Document Library.
- Power Automate triggers AI Builder to extract data automatically.
- Extracted data is reviewed, corrected, and approved within Power Apps.
- Data is then submitted back to SharePoint for storage.
- Optionally, the user can initiate **Policy Generation** via RPA (Desktop Flow).

---

### 💻 **Extended Integration: Desktop Flow Automation (VM-Based)**
After successfully completing the data extraction proof of concept (POC), we extended the solution by integrating a **Virtual Machine (VM)** to run **Power Automate Desktop Flows**.

- Once the extracted and validated data is submitted, a **Desktop Flow** (attended/unattended) runs on a dedicated VM.
- This Desktop Flow automates filling the extracted slip data into a **third-party application** to create insurance policies automatically.
- This closes the loop between data extraction and actual policy generation, enabling true end-to-end automation.

---

## 🖥️ Solution Components

### Power Apps (User Interface)
#### Screen 1: Document Upload & Review Dashboard
- **Upload files** (triggers backend automation).
- View and search uploaded documents from SharePoint Document Library.
- Auto-refresh functionality for real-time updates.

#### Screen 2: Data Extraction Review
- **PDF Viewer** to review uploaded documents.
- Editable form to review and adjust extracted data.
- Submit button updates SharePoint List with validated data.
- “Create Policy” button triggers VM-based Desktop Flow for policy creation.

---

### Power Automate (Workflow Automation)
- Document upload, AI model execution, and data archiving.
- Triggers Desktop Flows for automated policy creation.

---

### AI Builder (AI-Powered Data Extraction)
- Custom AI model extracts key fields:
  - Insured Name
  - Inception Date
  - Sum Insured
  - Total Insured Value (TIV)
- No-code/low-code setup.

---

### SharePoint (Data Storage)
- **Document Library**: Stores uploaded slip documents.
- **SharePoint List**: Stores extracted structured data linked to uploaded files.

---

## ⚙️ Tech Stack
- **Power Apps** (UI & Low-Code App Development)
- **Power Automate Cloud & Desktop Flows** (Automation)
- **AI Builder** (Document AI Extraction)
- **SharePoint** (Document & Data Storage)
- **Virtual Machine (VM)** (Desktop Flow Host for Third-Party Integration)

---

## 📂 Solution Architecture Diagrams

### Mailbox-Based Approach:
![Mailbox Approach](Solution%20Architecture%20-%20Mailbox%20Approach.jpg)

### UI-Based Approach:
![UI Approach](Solution%20Architecture%20-%20UI%20Approach.jpg)

---

## ✅ Key Features
- Fully automated slip data extraction workflow.
- User-friendly Power Apps for data upload, review, and validation.
- AI-powered extraction with low-code/no-code setup.
- End-to-end automation: from document upload to third-party policy creation via Desktop Flow.

---

## 📄 License
This repository is for personal portfolio demonstration purposes only. No confidential or proprietary information is included.

---

## 🙋‍♂️ Author
Sarthak Sharma  
*Low-Code Developer | AI Automation/Innovation Engineer*

---

