# ReplySmart – Intelligent Customer Support Assistant

ReplySmart is an **AI-powered customer support assistant** that integrates Gmail, OpenAI, Google Sheets, and **n8n workflows** to automatically classify, draft, and refine email responses with a **human-in-the-loop review process**.  

## 🚀 Features
- **Email Classification**: Detects and labels incoming emails as *Billing, Technical Support, General Inquiry,* or *Spam*.
- **Automated Drafting**: Generates AI-powered responses using OpenAI GPT models.
- **RAG-Powered Refinement**: Uses Retrieval-Augmented Generation (RAG) with a FAQ Vector Database for accurate, context-aware answers.
- **Human-in-the-Loop**: Customer support teams can fetch, review, revise, and approve responses before sending.
- **Google Sheets Database**: Stores all unresolved/resolved emails with labels, agent responses, and status tracking.
- **Web Dashboard (Lovable)**: Provides a clean interface to manage the support pipeline.

## 🛠️ Tech Stack
- **n8n** – Workflow automation
- **OpenAI GPT-4.1** – Drafting responses
- **OpenAI Embeddings** – Powering the FAQ Vector Database
- **Google Sheets** – Lightweight database for email tracking
- **Lovable** – Frontend interface/dashboard
- **Gmail API** – Email detection, classification, and replies

## 📂 Project Workflows
- **ReplySmart-ResponsePipeline** → Handles email detection, classification, response drafting, and database storage.
- **ReplySmart-Reviewer-Workflow** → Dashboard workflow for fetching unresolved emails, refining responses, and sending replies.

## 🌐 Live Demo
👉 [ReplySmart Dashboard](https://replysmart.lovable.app)  

## 📖 How It Works
1. New email detected via Gmail API → classified (Billing, Technical, Inquiry, Spam).  
2. AI drafts a response using GPT + FAQ Vector Database (RAG).  
3. Email + draft stored in Google Sheets (status = "Not Responded").  
4. Human reviewer fetches unresolved email in the dashboard.  
5. Reviewer can:
   - **Send** the draft as-is → status updated to "Responded".  
   - **Revise** with custom prompt → refinement agent improves it.  
   - **Ignore spam** → not stored.  

🔹 *ReplySmart makes customer support faster, smarter, and more reliable by combining AI automation with human oversight.*
