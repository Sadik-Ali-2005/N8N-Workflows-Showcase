# **Invoice Management (n8n)**

## **Overview**
This workflow automates invoice intake and processing by monitoring a designated Google Drive folder, extracting structured invoice data from PDFs using AI, updating a centralized invoice database, and generating professional internal notifications automatically.

It transforms unstructured invoice documents into structured, actionable financial records.

---

## **Workflow Architecture**
Drive Folder Trigger → File Download → PDF Text Extraction → AI Structured Data Extraction → Database Update → AI Email Generation → Notification Delivery

### **1. Triggers**
- **Google Drive Trigger (Folder Monitoring)** – Polls a specific folder for newly uploaded invoice files.
- Designed for continuous invoice intake automation.

### **2. Core Logic / Agent / Processing**
- Newly uploaded invoice files are downloaded automatically.
- PDF content is extracted and converted into raw text.
- An AI-powered Information Extractor identifies structured fields such as:
  - Invoice Number
  - Client Details
  - Total Amount
  - Invoice Date
  - Due Date
- Extracted data is appended or updated in a Google Sheets-based invoice database.
- A second AI model generates a structured internal email notification in JSON format.
- A JavaScript node safely parses the structured output before sending.
- A formatted notification email is delivered to the accounts team.

### **3. Integrated Tools**
- **Google Drive (Trigger + Download)** – Detects and retrieves invoice files.
- **PDF Extraction Node** – Converts invoice documents into readable text.
- **AI Information Extractor (Gemini Model)** – Extracts structured invoice fields.
- **Google Sheets (Append or Update)** – Maintains the invoice database.
- **AI Message Generation Model** – Produces structured notification emails.
- **JavaScript Processing Node** – Parses and validates AI-generated JSON.
- **Gmail** – Sends automated internal notifications.

---

## **Key Features**
- Event-driven document ingestion
- AI-based structured field extraction
- Append-or-update database logic (deduplication by Invoice Number)
- JSON-enforced AI output formatting
- Automated financial record synchronization
- AI-generated professional email notifications
- End-to-end document processing pipeline

---

## **Use Cases**
- Accounts payable automation
- Invoice intake and tracking systems
- Finance operations workflow automation
- AI-powered document processing
- Automated internal financial notifications

---

## **Technical Stack**
- n8n Workflow Automation
- Google Drive Integration
- PDF Text Extraction
- Google Gemini Models
- AI Information Extraction
- Google Sheets Database
- JavaScript Post-Processing
- Gmail Integration

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.  
No workflow JSON files, credentials, API keys, or production data are included in this repository
