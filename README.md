# WebScrapping
---

# 📄 RAG PDF Question Answering System

A **Retrieval-Augmented Generation (RAG)** application that extracts knowledge from research papers (PDFs), stores embeddings in a local vector database, and answers questions using a local LLM.

The project uses:

* **LangChain** for building the RAG pipeline
* **Chroma** for storing embeddings
* **Streamlit** for the user interface
* **Ollama** for running local models

---

# 🚀 Project Overview

This project implements a **complete RAG pipeline**:

```
PDF Papers
   ↓
Text Extraction
   ↓
Chunking
   ↓
Embeddings
   ↓
Chroma Vector Database
   ↓
Retriever
   ↓
Local LLM (Mistral)
   ↓
Answer Generation
```

Users can ask questions about the PDFs, and the system retrieves the most relevant chunks before generating the answer.

---

# 🧠 Key Features

✅ PDF downloading and ingestion
✅ Recursive text chunking
✅ Embedding generation
✅ Vector database storage (Chroma)
✅ Retrieval-Augmented Generation (RAG)
✅ Streamlit UI for question answering
✅ Local LLM inference using Ollama
✅ Agentic Chunking

---

# 📂 Project Structure

```
rag-pdf-qa/
│
├── pdf_.py
│   └── Downloads research papers from the internet
│
├── chunking.py
│   └── Extracts text from PDFs
│   └── Splits text into chunks
│   └── Generates embeddings
│   └── Stores embeddings in Chroma vector database
│
├── Streamlit.py
│   └── Loads stored embeddings
│   └── Runs the RAG pipeline
│   └── Provides a UI to ask questions
│
├── chroma_db/
│   └── Local vector database storing embeddings
│
└── README.md
```

---

# ⚙️ How the System Works

## 1️⃣ Download Research Papers

The script downloads PDFs from online sources.

```
python pdf_.py
```

This will save the files as:

```
file_pdf1.pdf
file_pdf2.pdf
```

---

## 2️⃣ Extract Text and Create Embeddings

The `chunking.py` script:

* Extracts text from the PDFs
* Splits the text into chunks using **RecursiveCharacterTextSplitter**
* Converts chunks into embeddings
* Stores them inside **Chroma vector database**

```
python chunking.py
```

This will create the folder:

```
chroma_db/
```

Which contains the stored embeddings.

---

## 3️⃣ Ask Questions Using Streamlit

The Streamlit app loads the stored embeddings and performs retrieval + generation.

```
streamlit run Streamlit.py
```

A browser window will open where you can ask questions about the documents.

---
##  How to use the application
```
1. have to install all the packages
2. have to get the api key from huggingface or any other AI model
3. this code contains recursive chunking as well code for agentic chunking
4. In agentic chunking there is limit to query the agents in free plan , and the code  is commented out can use it after buying the tokens
5. to run you have to use the command (pytohn chunking.py) for embeding into vector db
6. to use the streamlit application, command you have to use is (streamlit run streamlit.py)
```
# OUTPUT _ IMAGE

# 🖥 Example Usage

### User Question

```
What is the main idea behind reasoning models?
```

### System Workflow

```
User Question
      ↓
Embedding Conversion
      ↓
Similarity Search in Chroma
      ↓
Relevant Context Retrieved
      ↓
Mistral LLM Generates Answer
```

---

# 📦 Dependencies

Install all required libraries:

```
pip install langchain
pip install langchain-community
pip install langchain-ollama
pip install chromadb
pip install streamlit
pip install pymupdf
pip install requests
pip install rich
pip install python-dotenv
```

---

# 🧾 Required Models

This project uses the **Mistral model via Ollama**.

Install Ollama and pull the model:

```
ollama pull mistral
```

The embedding model used:

```
nomic-embed-text
```

---

# 📊 Vector Database

Embeddings are stored locally using **Chroma**.

Directory created:

```
chroma_db/
 ├── chroma.sqlite3
 ├── collections
 └── index
```

This allows **fast similarity search during retrieval**.

---

# 🖥 Example UI

The Streamlit interface allows users to:

* Enter a question
* Retrieve answers from the PDFs
* Measure query response time

Displayed information:

```
Answer
Query Time
```

---

# 📚 Learning Concepts

This project demonstrates:

* Retrieval-Augmented Generation (RAG)
* Vector databases
* Embeddings
* Document chunking
* Local LLM inference
* Semantic search

---

# 👨‍💻 Author

**Snigdh Chamoli**

Interested in:

* AI / Machine Learning
* Backend Engineering
* System Design
* Distributed AI Systems

---

⭐ If you found this project useful, consider **starring the repository**.

---

