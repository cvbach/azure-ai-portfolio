🧠 System Description
🔷 Overview

This system implements a Retrieval-Augmented Generation (RAG) architecture on Azure, enabling users to query and receive accurate answers based on internal document data.

📥 Data Ingestion & Indexing

Documents (PDF files such as reports, policies, and manuals) are stored in an Azure Storage Account.

These documents are then processed and indexed using Azure AI Search. During this process:

Text content is extracted from documents
The Azure OpenAI Service embedding model (text-embedding-3-small) is used to convert text into vector representations
The processed data is stored as a vector index in Azure AI Search

This enables semantic and vector-based retrieval.

🗂️ Knowledge Base (Vector Database)

Azure AI Search serves as the system’s vector database, responsible for:

Storing indexed document data
Supporting semantic and vector search
Retrieving relevant content based on user queries
🔍 Query & Retrieval (RAG)

When a user submits a query:

The query is sent to Azure AI Search
The system performs vector similarity search
Relevant document chunks are retrieved as context
🤖 Response Generation

The retrieved context is passed to the language model hosted on Azure OpenAI Service (e.g., GPT-4o).

The model:

Understands the context
Synthesizes a natural language response
Ensures answers are grounded in the retrieved data
⚙️ Orchestration (Azure AI Foundry)

The entire workflow is orchestrated using Azure AI Foundry, which:

Manages model deployment (GPT-4o)
Connects data sources (Azure AI Search)
Coordinates the RAG pipeline
Enables end-to-end AI application development
🔁 End-to-End Flow
Documents → Storage → AI Search (Indexing + Embedding)
        → User Query → AI Search (Retrieval)
        → Azure OpenAI (Generation)
        → Response
🎯 Key Benefits
Enables accurate, context-aware responses
Reduces hallucination by grounding answers in real data
Supports scalable and production-ready AI systems
Integrates multiple Azure AI services into a unified pipeline
