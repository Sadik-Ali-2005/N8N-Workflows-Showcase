# **RAG System using Supabase (n8n)**

## **Overview**
This workflow implements a Retrieval-Augmented Generation (RAG) system using Supabase as a vector store. It consists of two coordinated pipelines: one for ingesting and embedding documents into a vector database, and another for enabling an AI chatbot to retrieve relevant context and generate accurate responses.

---

## **Workflow Architecture**
Document Ingestion Pipeline + Chat-Based Retrieval Pipeline

### **1. Triggers**
- **Google Drive Trigger** – Activates when new documents are uploaded for ingestion into the knowledge base.
- **Chat Trigger** – Activates when a user sends a message to the chatbot interface.

### **2. Core Logic / Agent / Processing**

#### **RAG Ingestion Pipeline**
- Downloads newly uploaded documents.
- Loads document content using a data loader.
- Splits text into smaller chunks using a recursive text splitter.
- Generates embeddings using an AI embeddings model.
- Stores vectorized documents inside Supabase Vector Store.

#### **Chatbot Retrieval Pipeline**
- Receives user messages via chat trigger.
- AI Agent retrieves relevant contextual chunks from Supabase Vector Store.
- Uses embeddings similarity search for context matching.
- Generates grounded responses using a large language model (LLM).
- Maintains conversational continuity through memory integration.

### **3. Integrated Tools**
- **Google Drive (Trigger + Download)** – Handles document ingestion.
- **Default Data Loader** – Processes raw document content.
- **Recursive Character Text Splitter** – Breaks documents into manageable chunks.
- **Embeddings Model (Gemini)** – Converts text into vector representations.
- **Supabase Vector Store** – Stores and retrieves embeddings.
- **AI Agent + LLM** – Generates context-aware responses.
- **Simple Memory** – Maintains conversational state.

---

## **Key Features**
- Full Retrieval-Augmented Generation (RAG) architecture
- Dual pipeline design (Ingestion + Chatbot)
- Vector-based semantic search
- Context-aware AI responses
- Memory-enabled conversational continuity
- Scalable knowledge base ingestion
- Modular and extensible design

---

## **Use Cases**
- AI-powered knowledge base chatbot
- Document-driven Q&A systems
- Internal company assistant
- Academic or research document querying
- Context-aware support automation

---

## **Technical Stack**
- n8n Workflow Automation
- Supabase Vector Store
- Google Drive Integration
- Recursive Text Splitting
- Embeddings Model (Gemini)
- Large Language Model (LLM)
- AI Agent Architecture
- Conversational Memory Handling

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.  
No workflow JSON files, credentials, API keys, or production data are included in this repository.