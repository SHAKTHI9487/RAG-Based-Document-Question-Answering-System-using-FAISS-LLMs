**RAG-Based Document Question Answering System**

**RAG-Based-Document-Question-Answering-System-using-FAISS-LLMs/**

├── ingest.py         
├── retriever.py       
├── requirements.txt   
├── README.md          
└── data/
    ├── pdf.1.WHO.pdf
    ├── pdf.2.EU.pdf
    └── pdf.3.US.pdf




 Overview
This project implements a Retrieval-Augmented Generation (RAG) pipeline that answers user questions by retrieving relevant content from real-world PDF documents and generating grounded responses using a Large Language Model.

The system avoids hallucinations by strictly generating answers based on retrieved document context.


 Problem Statement
Organizations store critical information in documents (PDFs), making it difficult to retrieve precise answers efficiently. This project solves that by combining vector search with LLM-based generation.

Tech Stack
- Python
- LangChain
- FAISS (Vector Database)
- Hugging Face Transformers
- Sentence-Transformers
- FLAN-T5 (Text-to-Text LLM)
  
 System Architecture
1. PDF document ingestion
2. Text chunking and embedding generation
3. Vector storage using FAISS
4. Semantic retrieval based on user query
5. Context-grounded answer generation using a text-to-text LLM

Workflow
1. PDFs are loaded and split into semantic chunks
2. Chunks are converted into embeddings
3. Embeddings are stored in FAISS
4. User query retrieves top relevant chunks
5. LLM generates an answer using retrieved context

**I built an end-to-end RAG system using FAISS and LLMs, with real PDF ingestion and grounded generation**


How to Run the Project

1. Clone the repository
```bash
git clone https://github.com/SHAKTHI9487/RAG-Based-Document-Question-Answering-System-using-FAISS-LLMs.git
cd RAG-Based-Document-Question-Answering-System-using-FAISS-LLMs

pip install -r requirements.txt

python ingest.py

python app.py

```md
## Example Query

```text
Question:
What is diabetes according to the WHO document?

Answer:
Diabetes is a chronic disease characterized by elevated blood glucose levels, which over time leads to serious damage to the heart, blood vessels, eyes, kidneys, and nerves.






