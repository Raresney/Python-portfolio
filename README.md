# 🧠 Math Problem Retrieval System (RAG + Embeddings)

A Python project that builds a semantic search and code generation pipeline for mathematical problems using vector embeddings, FAISS, ChromaDB, and a RAG chain powered by OpenAI.

> Copyright (c) 2026 Bighiu Rares — [github.com/Raresney](https://github.com/Raresney)

---

## 📋 Features

| Step                    | Description                                                                           |
| ----------------------- | ------------------------------------------------------------------------------------- |
| 🧹 Dataset Cleaning     | Load from HuggingFace, normalize text, remove duplicates, export to CSV               |
| 🔢 Embedding Generation | Convert problems to vectors using `all-MiniLM-L6-v2` and `BAAI/bge-base-en-v1.5`      |
| 🔍 Similarity Search    | FAISS index for K-nearest neighbor retrieval with Hit Rate, Precision, Recall metrics |
| 🗄️ Vector Database      | Store and query embeddings with ChromaDB via LangChain                                |
| 🤖 RAG Pipeline         | Retrieve similar problems + generate Python code via OpenAI GPT-3.5-turbo             |

---

## ⚙️ Requirements

- Python 3.8+
- Google Colab (recommended) or local environment with GPU/CPU

```bash
pip install datasets sentence-transformers faiss-cpu torch
pip install langchain langchain-community langchain-openai chromadb pandas
```

For the RAG step, an **OpenAI API key** is required — set it as a Colab secret or environment variable:

```bash
export OPENAI_API_KEY=your_key_here
```

---

## 🚀 Pipeline

```
Load dataset (HuggingFace)
        ↓
Clean & deduplicate problems
        ↓
Export to CSV
        ↓
Generate embeddings (SentenceTransformers)
        ↓
Build FAISS index + evaluate models
        ↓
Store vectors in ChromaDB
        ↓
RAG chain: retrieve similar problems → generate Python code (GPT-3.5-turbo)
```

---

## ▶️ Run

Open and run `Proiect.ipynb` in Google Colab — the notebook executes the full pipeline sequentially.

At the final step, you will be prompted to enter a math problem in natural language:

```
>>> Introduceți problema matematică (în limbaj natural) și apăsați Enter:
calculate the area of a circle with radius 5
```

Output:

```python
import math
radius = 5
area = math.pi * radius ** 2
print(area)
```

---

## 📊 Output Files

| File                              | Description                                             |
| --------------------------------- | ------------------------------------------------------- |
| `math_python_dataset_curatat.csv` | Cleaned dataset — problem statements + Python solutions |
| `./chroma_db_math/`               | Persisted ChromaDB vector store                         |

---

## 🛠️ Technologies

Python, HuggingFace Datasets, SentenceTransformers, FAISS, LangChain, ChromaDB, Pandas, PyTorch, OpenAI API

---

## 🎯 Purpose

Experimental project for learning semantic search, vector embeddings, and RAG-based code generation.
