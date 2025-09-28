
# Document Analysis with LLMs (RAG, Q&A)

A clean, reproducible notebook for **question-answering over your documents**. It shows a minimal **RAG** (Retriever-Augmented Generation) pipeline: load documents → split into chunks → embed → index in a vector store → retrieve top passages → generate answers with sources. Built and tested in **Google Colab**, runs locally as well.

---

## ✨ What’s inside

- **Load & preprocess** PDFs/TXT/CSVs (Colab upload or `data/` folder)  
- **Chunking & embeddings** (Sentence-BERT / OpenAI)  
- **Vector stores**: **FAISS** or **ChromaDB**  
- **Retriever** with top-k similarity search  
- **LLM** inference: **OpenAI** or local **🤗 Transformers**  
- Clear cells to **switch providers** and experiment quickly  
- Optional stubs for a **Gradio / Streamlit** demo UI

---

## 🧩 Architecture (high level)

```
flowchart LR
  A[Documents (data/)] --> B[Loader & Text Splitter]
  B --> C[Embeddings (Sentence-BERT / OpenAI)]
  C --> D[Vector Store (FAISS / Chroma)]
  D --> E[Retriever (top-k)]
  E --> F[LLM (OpenAI or HF Transformers)]
  F --> G[Answer + Cited Passages]
```

## 🗂️ Data
Put files in a local data/ directory (git-ignore it) or upload/mount in Colab.
Example cell paths in the notebook already reference data/….
If you prefer Drive in Colab, mount it with


## 🚀 Run
In Google Colab
Click the Colab badge above.
Upload files or mount Drive.
Runtime → Run all.

##📦 Requirements
See requirements.txt in this repo.

## 🛡️ License
  MIT


