# LangChain Multi-Agent Q&A Project

This Jupyter notebook project demonstrates how to build a **Retrieval-Augmented Generation (RAG)** based Question Answering (QA) system using **LangChain** and **multiple data sources** such as:

- Wikipedia
- LangSmith Documentation
- Arxiv Papers

---

## Features

- Query Wikipedia using LangChain's WikipediaQueryRun tool
- Load and chunk web documentation from LangSmith using FAISS and HuggingFace embeddings
- Use Arxiv tool to retrieve and answer research paper-related questions
- Compose all tools into a multi-source question answering agent

---
## Technologies Used

- [LangChain](https://www.langchain.com/) – Framework for building LLM-powered applications with tools, memory, and agents
- [FAISS via LangChain](https://python.langchain.com/docs/integrations/vectorstores/faiss) – In-memory vector store for document search
- [HuggingFace Embeddings via LangChain](https://python.langchain.com/docs/integrations/text_embedding/huggingfacehub/) – Text embedding model (e.g., `all-MiniLM-L6-v2`)
- [LangSmith](https://smith.langchain.com/) – Optional for observability, tracing, and debugging
- Wikipedia & Arxiv access via [LangChain Community Tools](https://python.langchain.com/docs/integrations/tools/)

---

## What is RAG?

This project follows the **Retrieval-Augmented Generation (RAG)** architecture:

- **Retrieve**: Pulls relevant chunks from Wikipedia, LangSmith docs, or Arxiv
- **Augment**: Adds retrieved context to the prompt
- **Generate**: Uses an LLM to answer the question using the context

RAG allows the LLM to answer more accurately using **live, relevant, and external data**.

---

## Project Structure

```
rag-qa-agent-langchain.ipynb     # Enhanced Jupyter Notebook
README.md                      # This file
requirements.txt               # Dependencies
.env                           # API keys (not included in repo)
```

---

## Environment Variables

Create a `.env` file with the following keys:

```env
# For Groq
GROQ_API_KEY=your_groq_key

# Optional if using LangSmith logging and monitoring
LANGCHAIN_API_KEY=your_langchain_api_key
LANGCHAIN_PROJECT=LangChain-QA-Project
LANGSMITH_TRACING="true"
```

---

## How to Run

### 1. Clone the repository and enter the directory:

```bash
git clone https://github.com/yourname/langchain-multi-agent-qa.git
cd langchain-multi-agent-qa
```

### 2. Install dependencies

#### Option A: Using pip
```bash
pip install -r requirements.txt
```

#### Option B: Using uv (faster)
```bash
uv pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook agents_with_comments.ipynb
```

---

## Example Questions to Try

- "What is LangGraph and how does it work?"
- "Give me the latest Arxiv papers on large language models."
- "Who is the founder of LangChain?"
- "Explain memory in LangChain."


---

