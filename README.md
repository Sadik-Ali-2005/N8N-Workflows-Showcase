# n8n Workflow Showcase

This repository showcases multiple automation workflows built using n8n.

## Included Workflows
- Invoice Management
- Content Generator
- Questions Extractor and Answering
- College Route Emailing
- Customer Email Support
- RAG System using Supabase

## Tools & Technologies
- n8n
- AI / LLMs
- Email Automation
- Databases & Vector Stores

# All Workflows
## 1. Rag System using the Supabase
![](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/blob/main/Workflow_Images/1.%20Rag%20System%20using%20the%20Supabase.png)

### **Overview**
This workflow implements a Retrieval-Augmented Generation (RAG) system using Supabase as a vector store. It consists of two coordinated pipelines: one for ingesting and embedding documents into a vector database, and another for enabling an AI chatbot to retrieve relevant context and generate accurate responses.

### **Link to Workflow:** 
[1_Rag_System_using_the_Supabase](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/tree/main/Workflows/1.%20Rag%20System%20using%20the%20Supabase)

## 2. Content Generator
![](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/blob/main/Workflow_Images/2.%20Content%20Generator.png)

### **Overview**
This workflow automates the creation of newsletter-ready content by combining structured topic management, real-time news retrieval, and AI-powered summarization. It pulls pending topics from a spreadsheet, gathers relevant current articles, synthesizes the information into a concise student-friendly newsletter piece, and updates the content back into the sheet.

### **Link to Workflow:** 
[2_Content_Generator](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/tree/main/Workflows/2.%20Content%20Generator)

## 3. Customer Email Support
![](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/blob/main/Workflow_Images/3.%20Customer%20Email%20Support.png)

## **Overview**
This workflow implements an AI-powered customer support automation system that classifies incoming emails, retrieves relevant knowledge from a vector database, and generates contextual, friendly replies automatically. It combines intent detection, Retrieval-Augmented Generation (RAG), and structured response formatting within a fully automated Gmail workflow.

### **Link to Workflow:** 
[3_Customer_Email_Support](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/tree/main/Workflows/3.%20Customer%20Email%20Support)

## 4. Invoice Management
![](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/blob/main/Workflow_Images/4.%20Invoice%20Management.png)

### **Overview**
This workflow automates invoice intake and processing by monitoring a designated Google Drive folder, extracting structured invoice data from PDFs using AI, updating a centralized invoice database, and generating professional internal notifications automatically.

### **Link to Workflow:** 
[4_Invoice_Management](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/tree/main/Workflows/4.%20Invoice%20Management)

## 5. Question Extractor and Answers Generator
![](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/blob/main/Workflow_Images/5.%20Questions%20Extractor%20and%20Answer%20Creator.png)

### **Overview**
This workflow automates the ingestion, processing, consolidation, and restructuring of multiple question papers into a single, unified, deduplicated exam document. It uses OCR to extract text from uploaded files, applies AI-driven semantic processing to merge and clean content, removes duplicate questions across papers, and generates a structured HTML exam paper ready for distribution.

### **Link to Workflow:** 
[5_Questions_Extractor_and_Answer_Creator](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/tree/main/Workflows/5.%20Questions%20Extractor%20and%20Answer%20Creator)

## 6. Results Downloader
![](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/blob/main/Workflow_Images/6.%20Resuts%20Downloader.png)

### **Overview**
This workflow automates the retrieval and structuring of student examination results by combining n8n orchestration with a custom Playwright browser automation service. It processes pending student records, retrieves result data from a college portal, extracts structured marks using AI, and updates a centralized spreadsheet.

### **Link to Workflow:** 
[6_Results_Downloader](https://github.com/Sadik-Ali-2005/N8N-Workflows-Showcase/tree/main/Workflows/6.%20Results%20Downloader)
