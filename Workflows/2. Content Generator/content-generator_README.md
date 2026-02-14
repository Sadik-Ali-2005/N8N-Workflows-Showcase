# **Content Generator (n8n)**

## **Overview**
This workflow automates the creation of newsletter-ready content by combining structured topic management, real-time news retrieval, and AI-powered summarization. It pulls pending topics from a spreadsheet, gathers relevant current articles, synthesizes the information into a concise student-friendly newsletter piece, and updates the content back into the sheet.

---

## **Workflow Architecture**
Manual Trigger → Topic Retrieval → News API Fetch → AI Summarization → Sheet Update

### **1. Triggers**
- **Manual Execution Trigger** – Runs when “Execute workflow” is clicked.
- Designed for controlled batch content generation.

### **2. Core Logic / Agent / Processing**
- Retrieves a topic marked as “Todo” from Google Sheets.
- Uses an HTTP request to fetch current related news articles via an external news API.
- Extracts the top three relevant articles.
- Passes article content to an AI Agent with a structured system prompt.
- The AI synthesizes all sources into a single cohesive newsletter article.
- Ensures output is clear, concise, student-friendly, and professionally formatted.

### **3. Integrated Tools**
- **Google Sheets (Read)** – Fetches pending newsletter topics.
- **HTTP Request (News API)** – Retrieves current related articles.
- **AI Agent + Google Gemini Model** – Generates structured newsletter content.
- **Google Sheets (Update)** – Stores generated article, links, and marks status as “Finished”.

---

## **Key Features**
- Spreadsheet-driven topic management
- Real-time news enrichment
- Multi-source content synthesis
- Structured AI system prompt for consistent tone
- Automated status tracking
- End-to-end newsletter automation

---

## **Use Cases**
- College newsletter automation
- Weekly content pipelines
- AI-assisted journalism workflows
- Editorial content drafting
- Batch AI article generation

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
