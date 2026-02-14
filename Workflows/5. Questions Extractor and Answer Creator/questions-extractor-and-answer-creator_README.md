# **Questions Extractor and Answer Creator (n8n)**

## **Overview**
This workflow automates the ingestion, processing, consolidation, and restructuring of multiple question papers into a single, unified, deduplicated exam document. It uses OCR to extract text from uploaded files, applies AI-driven semantic processing to merge and clean content, removes duplicate questions across papers, and generates a structured HTML exam paper ready for distribution.

---

## **Workflow Architecture**
Form Submission → File Upload → OCR Processing → Content Aggregation → AI Deduplication & Structuring → HTML Generation → Cloud Storage Upload

### **1. Triggers**
- **Form Trigger** – Users upload one or more question paper files.
- Supports batch processing via loop control.

### **2. Core Logic / Agent / Processing**
- Uploaded documents are sent to Mistral’s OCR API for text extraction.
- A signed URL is generated for secure OCR processing.
- Extracted markdown content from all papers is aggregated.
- JavaScript processing combines multiple papers into a single structured dataset.
- An AI Agent:
  - Cleans OCR artifacts
  - Merges sections by mark value (2, 5, 10, etc.)
  - Semantically deduplicates similar questions
  - Renumbers questions sequentially
  - Tracks source papers
  - Generates a unified, clean HTML exam paper
- The final HTML output is converted to base64 format.
- The generated exam file is uploaded to Google Drive.

### **3. Integrated Tools**
- **Form Trigger** – Accepts file submissions.
- **HTTP Requests (Mistral API)** – Handles file upload, signed URL retrieval, and OCR processing.
- **Aggregation Node** – Consolidates multiple document outputs.
- **JavaScript Processing Nodes** – Combines and formats extracted data.
- **AI Agent + Google Gemini Model** – Performs semantic deduplication and structured HTML generation.
- **Google Drive (Upload)** – Stores the final consolidated exam file.

---

## **Key Features**
- Multi-document ingestion
- OCR-based text extraction
- Semantic duplicate detection across papers
- Mark-based section merging
- Automated renumbering and restructuring
- Clean, strict HTML generation
- Batch file handling with loop control
- End-to-end document automation

---

## **Use Cases**
- Academic exam consolidation
- Question bank normalization
- Study material standardization
- Institutional exam restructuring
- Large-scale document cleanup automation

---

## **Technical Stack**
- n8n Workflow Automation
- Mistral OCR API
- HTTP API Integration
- Google Gemini Model
- AI Agent Architecture
- JavaScript Data Processing
- Google Drive Integration
- Semantic Deduplication Logic

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.  
No workflow JSON files, credentials, API keys, or production data are included in this repository.
