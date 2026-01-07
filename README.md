# Simple and Hybrid Retrieval-Augmented Generation (RAG)
## > **Note:** If GitHub fails to render the notebook, please download and run it locally or open it in Google Colab.

## Overview

This repository provides a practical and comparative implementation of **Simple RAG** and **Hybrid RAG** architectures using **LangChain**, **ChromaDB**, **BM25 lexical retrieval**, and **Mistral large language models**.

The objective of this project is to demonstrate how combining **dense semantic retrieval** with **sparse lexical retrieval** improves answer quality, robustness, and factual grounding in Retrieval-Augmented Generation systems.

---

## Objectives

- Implement a baseline **Simple RAG** pipeline
- Implement a **Hybrid RAG** pipeline combining dense and sparse retrieval
- Apply LLM-based re-ranking for improved context selection
- Compare Simple RAG vs Hybrid RAG performance
- Provide a reusable reference for research and production prototyping




## Repository Structure

```text
simple-hybrid-rag/
├── README.md
├── Simple_and_Hybrid_RAG.ipynb
├── requirements.txt
├── .gitignore
└── assets/
    └── architecture_diagrams/

```


## Technology Stack

| Component          | Technology             |
|-------------------|------------------------|
| LLM               | Mistral                |
| Framework         | LangChain              |
| Vector Store      | ChromaDB               |
| Sparse Retrieval  | BM25                   |
| Embeddings        | LangChain Embeddings   |
| Document Loader   | PyPDF                  |
| Language          | Python 3.10+           |


## Install Required dependencies

```
pip install -r requirements.txt
```

## This Project Uses Mistral AI API

Your your own AI API Keys for better output, we have used the mistral ai api free for research.

```
from google.colab import userdata
mistral_api_key = userdata.get("Mistral_API")
```

## RAG Architectures

### Simple RAG

#### Pipeline
- Load and chunk documents  
- Generate dense embeddings  
- Store embeddings in ChromaDB  
- Retrieve top-k relevant chunks  
- Generate response using an LLM  

#### Strengths
- Simple to implement  
- Strong semantic recall  

#### Limitations
- Weak on exact keyword matching  
- Higher hallucination risk  

---

### Hybrid RAG

#### Pipeline
- Dense retrieval (Embeddings + ChromaDB)  
- Sparse retrieval (BM25)  
- Combine results from both retrievers  
- LLM-based re-ranking  
- Context-aware response generation  

#### Strengths
- Handles both semantic and keyword queries  
- Improved factual grounding  
- Reduced hallucination  

---

## Re-ranking Strategy

Hybrid retrieval results are re-ranked using an LLM to:
- Select the most relevant context chunks  
- Remove redundant or noisy passages  
- Improve answer precision and faithfulness  

## Comparison Summary

| Aspect              | Simple RAG | Hybrid RAG |
|---------------------|------------|------------|
| Semantic Recall     | High       | High       |
| Keyword Precision   | Low        | High       |
| Robustness          | Medium     | High       |
| Hallucination Risk  | Higher     | Lower      |
| Query Coverage      | Limited    | Broad      |

---

## Use Cases

- Document-based Question Answering  
- Research on Retrieval-Augmented Generation  
- Enterprise Knowledge Assistants  
- Foundation for Agentic RAG systems  
- Academic benchmarking and experimentation  

---

## Future Work

- Agentic RAG integration  
- Multi-modal document support  
- Faithfulness and citation evaluation  
- Multi-vector and hierarchical retrieval  
- Production-ready modularization  

---

## Author

**Nagbhushan Subbapurmath**    
Data Scientist – Dassault Systèmes  

**Research Focus:**  
RAG, Multimodal AI, Text Summarisation, Multimodal RAG, Faithfulness Evaluation


