# **Customer Email Support (n8n)**

## **Overview**
This workflow implements an AI-powered customer support automation system that classifies incoming emails, retrieves relevant knowledge from a vector database, and generates contextual, friendly replies automatically. It combines intent detection, Retrieval-Augmented Generation (RAG), and structured response formatting within a fully automated Gmail workflow.

---

## **Workflow Architecture**
Gmail Polling → Intent Classification → Conditional Routing → Knowledge Retrieval → AI Response Generation → Email Labeling → Automated Reply

### **1. Triggers**
- **Gmail Trigger (Polling every minute)** – Detects new incoming emails in real time.
- Designed for continuous inbox monitoring.

### **2. Core Logic / Agent / Processing**
- Incoming email text is analyzed using an AI-based text classifier.
- Emails are categorized into:
  - *Customer Support*
  - *Other*
- Only support-related emails proceed through the AI response pipeline.
- The AI Agent uses:
  - A structured system prompt to enforce tone and formatting
  - A vector database tool for knowledge retrieval
- Relevant contextual information is retrieved from Pinecone using embeddings.
- The AI generates a contextual, friendly response.
- Non-support emails follow a no-operation branch.

### **3. Integrated Tools**
- **Gmail Trigger** – Monitors new incoming emails.
- **Text Classifier (Gemini Model)** – Categorizes email intent.
- **Embeddings Model (Gemini)** – Converts text into vector representations.
- **Pinecone Vector Store** – Retrieves contextual newsletter knowledge.
- **AI Agent** – Generates structured responses using RAG.
- **Gmail (Add Label)** – Marks processed emails as important.
- **Gmail (Reply to Message)** – Sends automated replies within the same thread.

---

## **Key Features**
- Real-time email monitoring
- AI-powered intent classification
- Retrieval-Augmented Generation (RAG)
- Vector-based semantic search
- Structured response formatting
- Conditional workflow branching
- Automatic email labeling
- Thread-aware reply automation

---

## **Use Cases**
- Automated helpdesk systems
- Newsletter support automation
- FAQ-based response generation
- AI-assisted inbox management
- Scalable customer support workflows

---

## **Technical Stack**
- n8n Workflow Automation
- Gmail Integration
- Google Gemini Chat Model
- AI Text Classification
- Embeddings Model
- Pinecone Vector Database
- Retrieval-Augmented Generation (RAG)
- AI Agent Architecture

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.  
No workflow JSON files, credentials, API keys, or production data are included in this repository.
