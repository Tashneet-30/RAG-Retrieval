# trag

`trag` is a Python project scaffold for experimenting with document processing,
embeddings, and retrieval-augmented generation (RAG) workflows.

At the moment, this repository is in an early setup stage: the dependency stack
for document loading and vector search is present, the project structure is in
place, and a notebook is included for experimentation.

---

## Overview

This project is intended to support workflows such as:

- loading and parsing documents
- generating embeddings from text
- storing and searching vectors
- experimenting with retrieval pipelines
- prototyping ideas in notebooks before turning them into code

The current executable entry point is minimal and prints a startup message, but
the repository is already configured with the libraries commonly used for
building RAG-style systems.

---

## Tech Stack

The project currently includes:

- **Python 3.11+**
- **LangChain**
- **LangChain Community / Core**
- **sentence-transformers**
- **FAISS**
- **ChromaDB**
- **PyPDF**
- **PyMuPDF**
- **Jupyter / IPython kernel**

---

## Project Structure

```text
.
├── main.py
├── notebook/
│   └── document.ipynb
├── pyproject.toml
├── README.md
├── requirements.txt
├── src/
└── uv.lock
```

### Files

- **`main.py`**  
  Minimal project entry point.

- **`notebook/document.ipynb`**  
  Notebook for testing document ingestion and retrieval ideas interactively.

- **`pyproject.toml`**  
  Project metadata and dependency configuration.

- **`requirements.txt`**  
  Alternative dependency installation list for `pip`.

- **`src/`**  
  Source package directory for future application code.

- **`uv.lock`**  
  Lockfile for reproducible installs with `uv`.

---

## Requirements

Before running the project, make sure you have:

- **Python 3.11 or newer**
- one of the following package managers:
  - [`uv`](https://github.com/astral-sh/uv) (recommended), or
  - `pip`

---

## Installation

### Option 1: Install with `uv` (recommended)

```bash
uv sync
```

This installs the project dependencies based on `pyproject.toml` and `uv.lock`.

### Option 2: Install with `pip`

```bash
pip install -r requirements.txt
```

---

## Running the Project

Run the main entry point with:

```bash
python main.py
```

Expected output:

```text
Hello from trag!
```

---

## Working in the Notebook

To explore the notebook-based workflow, start Jupyter after installing
dependencies:

```bash
jupyter notebook
```

Then open:

```text
notebook/document.ipynb
```

This is the best place to prototype document loading, embedding generation, and
vector store experiments while the main application structure is still being
built.

---

## Current Status

This repository is currently a **starter scaffold** rather than a finished
application.

What is already present:

- project metadata and dependency configuration
- packages for PDF/document parsing
- packages for embeddings and vector databases
- a notebook for interactive experimentation
- a simple Python entry point

What is not yet implemented in the main codebase:

- document ingestion pipeline
- chunking and preprocessing flow
- embedding generation pipeline
- vector store indexing logic
- retrieval/query interface
- CLI or API layer

---

## Dependencies

The project is set up around the following library groups:

### Document Processing

- `pypdf`
- `pymupdf`

### Embeddings and Retrieval

- `sentence-transformers`
- `faiss-cpu`
- `chromadb`

### Orchestration

- `langchain`
- `langchain-core`
- `langchain-community`

### Notebook Support

- `ipykernel`

---

## Development Notes

If you plan to extend this repository, a good next step would be to add modules
inside `src/` for:

- document loaders
- text chunking
- embedding creation
- vector index management
- query/retrieval helpers

A possible future layout could look like this:

```text
src/
├── loaders/
├── embeddings/
├── retrievers/
├── vectorstores/
└── utils/
```

---

## Example Next Steps

Some practical improvements you may want to add next:

1. Load PDF files from a local folder
2. Extract and clean document text
3. Split text into chunks
4. Generate embeddings with `sentence-transformers`
5. Store vectors in FAISS or ChromaDB
6. Build a simple retrieval function
7. Add a CLI or notebook demo for question answering over documents

---


## Summary

`trag` is currently a clean starting point for building a Python-based document
retrieval or RAG project. The repository already includes the right dependency
foundation for parsing documents, generating embeddings, and experimenting with
vector search, while leaving the application architecture open for further
development.
