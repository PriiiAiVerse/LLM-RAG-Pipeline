# 🧠 LLM-Powered PDF Analyzer using Gemma + RAG

<p align="center">
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExaHRqN242end4aG5lMnNkN2E3eGV2ZmNiOWoyNTd4OGE5YTdyZ2dtYyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/XP8kV1sQnHF9AL30GE/giphy.gif" width="400" alt="Anime" />
</p>
This project demonstrates how to process a PDF document and analyze its content using a lightweight Large Language Model (LLM) like Google's Gemma, following a RAG (Retrieval-Augmented Generation) inspired workflow. The setup is designed to be GPU-memory aware and works in constrained environments like Google Colab.

---

📌 Objective

Enable efficient, memory-aware question answering or text analysis on PDF documents by:
- Extracting structured text from PDFs.
- Embedding or chunking content for retrieval.
- Using an LLM (e.g., Gemma) to answer user queries with relevant context.

---

 🔁 RAG Workflow Overview

> Retrieval-Augmented Generation (RAG) combines document retrieval and text generation for more accurate and grounded answers.

 🔄 Simplified Workflow Followed:

1. 📥 PDF Input
   - Download or upload your own PDF (e.g., "Human Nutrition 2020").
2. 📄 Text Extraction
   - Use `PyMuPDF` (`fitz`) to extract raw text, page by page.
3. 🔍 Chunking & Embedding
   - Chunk text into paragraphs/pages for context retrieval.
   - Embed text using embedding models (planned or extendable).
4. ⚙️ Hardware Check
   - Detect GPU memory to select appropriate Gemma model (`2B` or `7B`, optionally quantized).
5. 🧠 LLM Inference
   - Use Gemma to answer queries, guided by extracted or retrieved context.
6. 🗣️ Output
   - Display generated answers to the user.

---

 🚀 Features

-  Lightweight RAG-style flow
-  Download or load your own PDFs
-  Page-wise text extraction via PyMuPDF
-  Model adaptation based on GPU availability
-  Option to switch between quantized and full-precision models
-  Extendable for use with vector stores like FAISS or ChromaDB

---

 🛠️ Technologies Used

| Tool/Library        | Role                              |
|---------------------|-----------------------------------|
| `PyMuPDF (fitz)`    | PDF text extraction               |
| `torch`             | GPU memory inspection             |
| `transformers`      | Load Gemma or other LLMs          |
| `requests`          | PDF download                      |
| `Google Colab`      | Runtime environment (GPU-enabled) |

---

 📦 Installation

Install required packages:

```bash
pip install pymupdf torch transformers

```

