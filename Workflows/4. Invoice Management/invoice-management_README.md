# **Invoice Management (n8n)**

## **Overview**
This workflow automates invoice processing by detecting newly uploaded invoice files, extracting structured information using AI, storing the data in a spreadsheet, and sending automated notifications. It transforms unstructured PDF invoices into organized, actionable records.

---

## **Workflow Architecture**
Drive Trigger → File Processing → AI Data Extraction → Spreadsheet Update → Notification Generation → Email Delivery

### **1. Triggers**
- **Google Drive Trigger** – Activates when a new invoice file is created in a specified folder.
- Designed for real-time invoice intake automation.

### **2. Core Logic / Agent / Processing**
- Downloads the newly uploaded invoice file.
- Extracts text content from PDF documents.
- Uses an AI-powered Information Extractor to identify structured invoice fields (e.g., invoice number, client details, amounts, dates).
- Updates or appends structured data into a spreadsheet.
- Generates a formatted notification message using an AI model.
- Processes structured output via a JavaScript node for clean formatting.
- Sends a notification email to the relevant team.

### **3. Integrated Tools**
- **Google Drive (Trigger + Download)** – Detects and retrieves invoice files.
- **PDF Extraction Node** – Converts invoice documents into readable text.
- **AI Information Extractor (Gemini Model)** – Extracts structured invoice fields.
- **Google Sheets** – Stores processed invoice records.
- **AI Message Generation** – Creates structured notification content.
- **JavaScript Node** – Parses and formats structured output.
- **Gmail** – Sends automated invoice notifications.

---

## **Key Features**
- Event-driven invoice automation
- AI-based structured data extraction
- PDF-to-structured-data transformation
- Automated spreadsheet synchronization
- AI-generated professional email notifications
- End-to-end automation pipeline
- Scalable for finance and accounting workflows

---

## **Use Cases**
- Accounts payable automation
- Invoice intake and tracking systems
- Financial operations workflows
- Document processing automation
- AI-assisted bookkeeping pipelines

---

## **Technical Stack**
- n8n Workflow Automation
- Google Drive Integration
- PDF Text Extraction
- Google Gemini Chat Model
- AI Information Extraction
- Google Sheets Integration
- JavaScript Processing Node
- Gmail Integration

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.  
No workflow JSON files, credentials, API keys, or production data are included in this repository.