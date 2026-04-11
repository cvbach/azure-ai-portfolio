# ⚙️ Setup Guide – Azure AI RAG System

This guide describes how to set up an end-to-end RAG (Retrieval-Augmented Generation) system using Azure services.

---

## 🧱 Prerequisites

- Azure subscription
- Access to:
  - Azure OpenAI
  - Azure AI Search
  - Azure Storage Account
  - Azure AI Foundry

---

## 📦 1. Create Azure Storage (Data Source)

1. Go to Azure Portal  
2. Create a **Storage Account**  
3. Create a **Blob Container** (e.g., `documents`)  
4. Upload your PDF files  

📌 These documents will be used as the knowledge base.

---

## 🔍 2. Create Azure AI Search

1. Create an **Azure AI Search service**  
2. Configure:
   - Pricing tier (Basic or higher)
3. Create:
   - Data Source (connect to Storage)
   - Index
   - Indexer

---

## 🧠 3. Define Search Index

Create an index with fields such as:

- `id` (key)
- `content` (text)
- `vector` (embedding)
- `metadata` (optional)

📌 Make sure vector search is enabled.

---

## 🔄 4. Configure Indexer (Data Ingestion)

1. Create an **Indexer**
2. Connect:
   - Data Source → Blob Storage
   - Target → Search Index
3. Run the indexer

📌 This step extracts and indexes document content.

---

## 🤖 5. Deploy Azure OpenAI Models

Go to Azure OpenAI and deploy:

### 1. Chat Model
- Example: `gpt-41`

### 2. Embedding Model
- Example: `text-embedding-3-small`

📌 Embedding model is used for vector search.

---

## 🔗 6. Configure Vector Search

Ensure that:

- Embeddings are generated from document content  
- Vectors are stored in Azure AI Search  
- Queries are converted to embeddings before search  

---

## ⚙️ 7. Set up Azure AI Foundry

1. Create a project in Azure AI Foundry  
2. Configure:
   - Model (GPT-4.1)
   - Data source (Azure AI Search)
3. Build agent / flow:
   - User query → Search → GPT → Response  

📌 This is where orchestration happens.

---

## 💬 8. Test the System

1. Go to Foundry playground / agent  
2. Ask a question related to your documents  
3. Verify:
   - Relevant documents are retrieved  
   - GPT generates accurate answers  

---

## 🔐 9. Security (Recommended)

- Use managed identity or API key securely  
- Do NOT expose secrets in public repositories  
- Mask sensitive information in screenshots  

---

## ✅ Final Flow
