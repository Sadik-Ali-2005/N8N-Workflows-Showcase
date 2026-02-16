# **Results Downloader (n8n + Playwright Automation)**

## **Overview**
This workflow automates the retrieval and structuring of student examination results by combining n8n orchestration with a custom Playwright browser automation service. It processes pending student records, retrieves result data from a college portal, extracts structured marks using AI, and updates a centralized spreadsheet.

---

## **Workflow Architecture**
Manual Trigger → Sheet Read → Conditional Filter → Loop → Playwright API → AI Parsing → JSON Conversion → Sheet Update → Status Update

---

## **Node-by-Node Breakdown**

### 1. Manual Trigger
Starts the workflow when executed manually.

### 2. Google Sheets – Read
Fetches student records containing:
- Register Number
- Date of Birth
- Processing Status

### 3. IF Node
Filters rows based on processing status (e.g., “Not yet”).

### 4. Loop Over Items
Processes each student record individually to avoid bulk failures.

### 5. HTTP Request (Playwright Service)
Sends student credentials to a custom Playwright backend that:
- Logs into the college results portal
- Enters credentials
- Scrapes raw result content
- Returns extracted result text

### 6. Router
Handles branching logic depending on API response success or failure.

### 7. Edit Fields
Normalizes and prepares returned result data for AI processing.

### 8. AI Agent (Text Organizer)
Uses a structured prompt to extract:
- Course names
- Subject-wise marks
- Final totals

Enforces strict JSON output formatting.

### 9. Convert to JSON (Code Node)
Parses and validates AI output for safe structured storage.

### 10. Update the Result (Append Sheet)
Writes structured marks into the results spreadsheet.

### 11. Status Handling
- Marks row as `Done` if successful.
- Marks row as `Not Done` if retrieval fails.

---

## **Key Features**
- Hybrid automation (Browser Automation + Workflow Engine)
- Batch student processing
- Conditional routing
- AI-enforced structured JSON extraction
- Spreadsheet-driven orchestration
- Status-based tracking and retry capability

---

## **Technical Stack**
- n8n Workflow Automation
- Playwright (Browser Automation Service)
- HTTP Integration Layer
- Google Sheets Integration
- Google Gemini Model
- AI Agent Architecture
- JavaScript Post-Processing

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.
All credentials, endpoints, student data, and portal details have been removed.