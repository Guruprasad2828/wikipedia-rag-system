#  Wikipedia RAG System

A **Retrieval-Augmented Generation (RAG)** system built on a Wikipedia corpus using **Hybrid Search (FAISS + BM25 + RRF)** and powered by **Zephyr-7B**, with an interactive **Gradio UI**.

---

##  Overview

This project combines **dense retrieval**, **sparse retrieval**, and **LLM generation** to produce accurate, source-grounded answers from Wikipedia.

- Dense search → FAISS  
- Sparse search → BM25  
- Fusion → Reciprocal Rank Fusion (RRF)  
- Generation → Zephyr-7B LLM  

---

##  Architecture

```
Query
  │
  ▼
Embeddings (MiniLM)
  │
 ├── FAISS (Dense)
 └── BM25 (Sparse)
        │
        ▼
     RRF Fusion
        │
        ▼
 Top Relevant Chunks
        │
        ▼
   Zephyr-7B LLM
        │
        ▼
 Answer + Sources 
```

---

##  Tech Stack

- Python  
- Transformers (HuggingFace)  
- Sentence-Transformers  
- FAISS  
- BM25 (rank-bm25)  
- PyTorch  
- Gradio  

---

##  Project Structure

```
wikipedia-rag-system/
│
├── app.py
├── requirements.txt
│
├── data/
│   ├── corpus.pkl
│   ├── chunks.pkl
│   ├── faiss_index.bin
│   └── bm25_index.pkl
│
└── README.md
```
