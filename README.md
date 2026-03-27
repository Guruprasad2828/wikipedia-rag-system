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
<img width="1678" height="1047" alt="image" src="https://github.com/user-attachments/assets/8abcc479-5470-4a2d-89e2-349fe78dae4f" />
<img width="1673" height="1049" alt="image" src="https://github.com/user-attachments/assets/05d5115a-8507-4ae0-8cc7-af6aabd88dbf" />
<img width="1679" height="1008" alt="image" src="https://github.com/user-attachments/assets/90dc844d-505d-43f6-a550-f83ccac4f0ea" />


