
# 🤖 RAG Chatbot with Azure/OpenAI

## 📌 Overview

This project is a simple Retrieval-Augmented Generation (RAG) chatbot that allows users to ask questions based on the content of a PDF document.

The chatbot retrieves relevant information from the document and uses an AI model to generate accurate answers.

---

## 🎯 Problem

Reading and searching through long documents manually is time-consuming.

Users need a way to quickly extract information from PDFs.

---

## 💡 Solution

This project builds a chatbot that:

* Loads a PDF document
* Splits it into smaller chunks
* Converts text into embeddings
* Stores embeddings in a vector database
* Retrieves relevant context based on user query
* Generates answers using an AI model

---

## 🧠 Architecture

User → Chatbot → Vector Search → AI Model → Response

---

## ⚙️ Tech Stack

* C#
* OpenAI API
* LangChain
* FAISS (Vector Database)

---

## 🚀 Features

* Ask questions from PDF
* Context-aware answers
* Simple CLI interface

---

## 📷 Demo

(Add screenshot here after running the project)

---

## 🛠️ How to Run

```bash
pip install openai langchain faiss-cpu pypdf python-dotenv
python chatbot.py
```

---

## 📂 Project Structure

```
rag-chatbot/
├── chatbot.py
├── data/
│   └── sample.pdf
├── demo.png
└── README.md
```

---

## 🔥 Future Improvements

* Add web UI (Streamlit)
* Deploy on Azure
* Use Azure OpenAI instead of OpenAI
* Store embeddings in Azure AI Search

---

## 👨‍💻 Author

Cao Van Bach – Azure Cloud & AI Engineer (AI-102)
