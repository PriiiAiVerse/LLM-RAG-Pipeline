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

    
🎯 Why is this Useful?

   Many real-world PDFs are long and unstructured. This tool allows you to:
- Extract clean text from PDFs.
- Query that text with a lightweight LLM (like Google's Gemma).
- Get answers grounded in the document — without needing massive GPUs or external APIs.

---

💡 Example Use Cases

📘 Turn Entire Textbooks into Conversational Mentors

  * Effortlessly ask questions and get concise answers from academic material — like chatting with a textbook.

🧠 Transform Manuals into Instant Know-It-Alls

   * Convert dense user guides or medical documents into interactive Q&A companions for quick insights.

🧾 Make Sense of Legalese with AI Clarity

   * Analyze lengthy terms, policies, and reports with AI that highlights what really matters.

---

 🎯 Project Goals

-  Demonstrate a simple RAG-style pipeline using open-source tools.
-  Allow GPU-aware model loading (Gemma 2B / 7B).
-  Make PDF question answering accessible to all.
-  Provide a starting point to extend with embeddings, vector search, and UI.

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

| Tool/Library          | Role                               |
|-----------------------|------------------------------------|
| `PyMuPDF` (`fitz`)    | PDF text extraction                |
| `torch`               | GPU memory detection               |
| `transformers`        | Loading and using LLMs (Gemma)     |
| `bitsandbytes`        | Efficient 4-bit model loading      |
| `accelerate`          | Fast inference support             |
| `Google Colab`        | Runtime environment (GPU-enabled)  |


---

 🧱 Project Structure

pdf-llm-rag/

├── pdf_llm_rag_workflow.ipynb # Main notebook with full workflow

├── sample_pdfs/ # Optional folder for storing sample PDFs

├── README.md # Project documentation

└── requirements.txt # Python dependencies

---

 📦 How to run 

 > ⚠️ Recommended: Use Google Colab if you don't have a GPU locally.

1. Clone the repository:
```bash
    git clone https://github.com/yourusername/pdf-llm-rag.git
    cd pdf-llm-rag
```
2. Create a virtual environment:
```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. Install dependencies:
```bash
    pip install -r requirements.txt
```

---

🌐 External Links

  * Gemma on Hugging Face
    
  * PyMuPDF Docs

---

🔌 Extendable Ideas 

1. Add embedding + FAISS/Chroma for full retrieval support.

2. Add Gradio or Streamlit UI for interactive querying.

3. Replace Gemma with Phi-2, Mistral, or LLaMA if preferred.

4. Enable multi-PDF support or metadata-based filtering.


>  NOTE : looking forward to use these ideas with upcomming project ..


----

🧑‍💻 Author  - PriiiAiVerse


📝 License
This project is licensed under the MIT License – see the LICENSE file for details.
