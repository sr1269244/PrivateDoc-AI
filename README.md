<<<<<<< HEAD
Local RAG Pipeline with Ollama, LangChain, and Docker
A fully local, containerized Retrieval-Augmented Generation (RAG) pipeline built for high-performance privacy, featuring local model serving, persistent vector search, and structured Jupyter notebooks.
Architecture & Tech Stack
 * Inference Engine: Ollama running locally inside a standalone Docker container (serving models like smollm2 on port 11434)
 * Orchestration: LangChain
 * Vector Database: ChromaDB (with local persistence)
 * Environment: Python managed via Jupyter Notebooks and standard project tooling (pyproject.toml)
Project Structure
RAG_Pipeline_SHEETAL/
│
├── src/
│   ├── Vector/                  # ChromaDB vector store files (git-ignored for clean state)
│   ├── 2.0.ipynb                # Document loading and preprocessing
│   ├── 3.0_RAG_LOCAL_PERSIST.ipynb # Local persistence implementation
│   ├── 4.0_RAG_Add_Documents.ipynb # Incremental document embedding
│   ├── DOCKER_Model_Runner.ipynb # Container orchestration notes
│   ├── fabric-onelake.pdf       # Sample reference documentation
│   └── UNIT 2 E Commerce.pdf    # Sample reference documentation
│
├── 1.0 RAG_WITH_OWN_TEXT.ipynb  # Core pipeline introduction
├── .env.example                 # Environment variable template
├── .gitignore                   # Excludes local artifacts (.venv, Vector/, .env)
├── pyproject.toml               # Project dependencies and configuration
└── README.md                    # Project documentation

Step-by-Step Tutorial Chapters
 * 1.0 RAG_WITH_OWN_TEXT.ipynb: Introduction to processing text inputs and configuring basic retrieval mechanics.
 * 2.0.ipynb: Document ingestion, parsing, and text splitting strategies.
 * 3.0_RAG_LOCAL_PERSIST.ipynb: Setting up local persistence using ChromaDB to retain embeddings across sessions.
 * 4.0_RAG_Add_Documents.ipynb: Expanding the knowledge base dynamically by adding new documents to the existing store.
 *  DOCKER_Model_Runner.ipynb: Guide on containerizing and executing local model runners via Docker for seamless environment parity.
     
Getting Started
Prerequisites
 * Docker Desktop installed and running
 * Python environment (Jupyter Notebook support)
Setup Instructions
 * Clone the repository:
   git clone https://github.com/sr1269244/RAG_Pipeline_SHEETAL.git
cd RAG_Pipeline_SHEETAL

 * Start the Ollama Docker Container:
   docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama

 * Pull your target model:
   docker exec -it ollama ollama pull smollm2

 * Open the project in VS Code and explore the tutorial sequence starting from 1.0 RAG_WITH_OWN_TEXT.ipynb.
=======
# PrivateDoc AI: Local RAG Document Intelligence Engine
>>>>>>> 43396baca81ec6980987c0f41887a37268f126a3
