# 🧠 Math Problem Retrieval System (RAG + Embeddings)

A Python project focused on **processing mathematical datasets and building a semantic search system** using modern AI tools such as **SentenceTransformers, FAISS, and LangChain**.

The goal of this project is to experiment with **vector embeddings and retrieval techniques** for mathematical problem solving.

---

# 🚀 Features

🔹 Dataset cleaning and preprocessing from HuggingFace  
🔹 Duplicate removal from math problem dataset  
🔹 Generation of sentence embeddings for problems  
🔹 Semantic similarity search using FAISS  
🔹 Embedding model evaluation (precision, recall, hit rate)  
🔹 Vector database creation with ChromaDB  
🔹 Retrieval-Augmented Generation (RAG) style pipeline

---

# 📂 Project Workflow

The project follows several main steps:

### 1️⃣ Dataset Processing

The dataset is loaded from HuggingFace and cleaned:

- normalize problem text
- remove special characters
- remove duplicates
- export cleaned dataset to CSV

Dataset used:

**sdiazlor/math-python-reasoning-dataset**

---

### 2️⃣ Embedding Generation

Each math problem is converted into vector embeddings using:

- `all-MiniLM-L6-v2`
- `BAAI/bge-base-en-v1.5`

Libraries used:

- SentenceTransformers
- PyTorch

---

### 3️⃣ Similarity Search

Semantic search is implemented using **FAISS**.

The system retrieves the **K most similar math problems** to a given query.

Evaluation metrics used:

- Hit Rate@K
- Precision@K
- Recall@K
- Average search time

---

### 4️⃣ Vector Database

A vector database is created using:

- LangChain
- ChromaDB

This allows storing and querying embeddings efficiently.

---

# 🛠️ Technologies

- 🐍 Python
- 🤗 HuggingFace Datasets
- 🤖 SentenceTransformers
- ⚡ FAISS
- 🔗 LangChain
- 🗄️ ChromaDB
- 📊 Pandas
- 🔥 PyTorch

---

# 📊 Example Workflow

```
Load dataset
     ↓
Clean problem statements
     ↓
Remove duplicates
     ↓
Generate embeddings
     ↓
Create FAISS index
     ↓
Run similarity search
     ↓
Evaluate embedding models
     ↓
Store vectors in ChromaDB
```

---

# ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/python-portfolio.git
cd python-portfolio
```

Install dependencies:

```bash
pip install datasets sentence-transformers faiss-cpu torch
pip install langchain langchain-community chromadb pandas
```

---

# ▶️ Running the Project

Run the notebook or Python script:

```
Proiect.ipynb
```

The pipeline will:

1. download and clean the dataset
2. generate embeddings
3. evaluate embedding models
4. build a FAISS index
5. create a Chroma vector database

---

# 📁 Output

The project generates:

```
math_python_dataset_curatat.csv
```

which contains:

- cleaned math problems
- associated Python solutions

---

# 🎯 Purpose

This project was created to explore:

- semantic search
- vector embeddings
- retrieval systems
- AI-assisted problem solving

It is mainly an **experimental project for learning modern AI retrieval techniques.**

---

# 👤 Author

**Rares Bighiu**

Student — Mathematics & Computer Science  
Alexandru Ioan Cuza University of Iași

Interests:

- Cybersecurity
- Artificial Intelligence
- Data Science
- Machine Learning

---

# 📜 License

© 2026 Rares Bighiu  
All rights reserved.
