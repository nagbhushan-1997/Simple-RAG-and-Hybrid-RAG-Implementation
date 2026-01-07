# Simple and Hybrid Retrieval-Augmented Generation (RAG)

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



