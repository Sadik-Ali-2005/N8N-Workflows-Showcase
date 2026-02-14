# **Content Generator (n8n)**

## **Overview**
This workflow automates AI-powered content generation using structured data from a spreadsheet and external enrichment sources. It retrieves input data, enhances it through API integration, generates intelligent content using an AI model, and updates the results back into a structured sheet.

---

## **Workflow Architecture**
Manual Trigger → Data Retrieval → External API Enrichment → AI Processing → Sheet Update

### **1. Triggers**
- **Manual Execution Trigger** – The workflow starts when the user clicks “Execute workflow”.
- Designed for controlled batch processing or testing environments.

### **2. Core Logic / Agent / Processing**
- Retrieves rows from a spreadsheet containing structured input data.
- Sends data to an external API for enrichment or preprocessing.
- Passes enriched information to an AI Agent powered by a chat model.
- The AI Agent generates refined, structured, or enhanced content.
- Generated output is written back to the spreadsheet.

### **3. Integrated Tools**
- **Google Sheets (Read)** – Fetches input data.
- **HTTP Request** – Connects to external APIs for data enrichment.
- **AI Agent + Chat Model (Gemini)** – Generates AI-driven content.
- **Google Sheets (Update)** – Writes generated output back into the sheet.

---

## **Key Features**
- AI-driven content automation
- Spreadsheet-based batch processing
- External API enrichment before generation
- Structured output storage
- Modular design for scalable content workflows
- Suitable for semi-automated publishing pipelines

---

## **Use Cases**
- Automated blog or article generation
- Marketing content creation
- Product description generation
- Data-driven content pipelines
- Batch AI content enrichment

---

## **Technical Stack**
- n8n Workflow Automation
- Google Sheets Integration
- HTTP API Integration
- AI Agent Architecture
- Google Gemini Chat Model

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.  
No workflow JSON files, credentials, API keys, or production data are included in this repository.