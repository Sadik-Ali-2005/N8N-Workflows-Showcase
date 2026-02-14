# **Questions Extractor and Answer Creator (n8n)**

## **Overview**
This workflow automates the extraction of questions from uploaded documents and generates intelligent answers using AI. It processes submitted files, performs OCR when necessary, structures extracted text, generates contextual responses, and uploads the final output file for further use.

---

## **Workflow Architecture**
Form Submission → File Processing → OCR Extraction → Data Aggregation → AI Answer Generation → File Creation → Upload

### **1. Triggers**
- **Form Submission Trigger** – Activates when a user submits a form containing document input.
- Supports batch processing through looping over submitted items.

### **2. Core Logic / Agent / Processing**
- Uploaded documents are sent for OCR processing to extract text content.
- The workflow retrieves signed URLs and OCR results.
- Extracted text is aggregated and processed using JavaScript for structured formatting.
- An AI Agent powered by a chat model generates answers based on extracted questions.
- Additional formatting and processing steps refine the output.
- The final file is generated and uploaded to cloud storage.

### **3. Integrated Tools**
- **Form Trigger** – Captures user-submitted documents.
- **HTTP Requests (OCR Service)** – Uploads files and retrieves OCR results.
- **Aggregation Node** – Consolidates extracted data.
- **JavaScript Processing Nodes** – Formats and structures text.
- **AI Agent + Google Gemini Chat Model** – Generates intelligent answers.
- **Google Drive (Upload)** – Stores the processed output file.

---

## **Key Features**
- Automated document-based question extraction
- OCR integration for scanned or image-based files
- AI-powered answer generation
- Structured text aggregation and transformation
- Batch processing support
- End-to-end document-to-answer automation

---

## **Use Cases**
- Educational content generation
- Automated assignment solution drafts
- Question bank creation
- Study material generation
- Document-based knowledge extraction workflows

---

## **Technical Stack**
- n8n Workflow Automation
- Form-Based Triggering
- OCR API Integration
- JavaScript Data Processing
- AI Agent Architecture
- Google Gemini Chat Model
- Google Drive Integration

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.  
No workflow JSON files, credentials, API keys, or production data are included in this repository.