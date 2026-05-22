# 📚 RAG Chat Assistant

An end-to-end Retrieval-Augmented Generation (RAG) based AI chatbot built using **LangChain, FastAPI, Streamlit, ChromaDB, and Llama3**.

The system allows users to upload documents and interact with them through natural language queries. It uses vector embeddings and semantic search to retrieve relevant document context before generating AI-powered responses.

---

# 🚀 Features

- 📄 Upload PDF, DOCX, and HTML documents
- 🧠 Retrieval-Augmented Generation (RAG) pipeline
- 🔍 Semantic document search using ChromaDB
- 💬 Interactive chatbot interface
- ⚡ FastAPI backend APIs
- 🎨 Streamlit frontend UI
- 🗂️ Persistent vector database storage
- 📝 Chat history & metadata storage using SQLite
- 🔄 Multiple LLM model support
- 📚 LangChain-powered document processing

---

# 🛠️ Tech Stack

## Languages
- Python

## Frameworks & Libraries
- FastAPI
- Streamlit
- LangChain
- ChromaDB
- SQLite
- Pydantic
- Uvicorn

## LLM / AI
- Llama3
- Embedding-based semantic retrieval
- Retrieval-Augmented Generation (RAG)

---

# 📂 Project Structure

```bash
RAG-Chat-Assistant/
│
├── api/                              # FastAPI backend
│   ├── chroma_db/                    # ChromaDB vector storage
│   ├── app.log                       # Application logs
│   ├── chroma_utils.py               # ChromaDB helper functions
│   ├── db_utils.py                   # SQLite database utilities
│   ├── langchain_utils.py            # LangChain RAG pipeline
│   ├── main.py                       # FastAPI entry point
│   ├── pydantic_models.py            # Request/response schemas
│   └── rag_app.db                    # SQLite database
│
├── app/                              # Streamlit frontend
│   ├── api_utils.py                  # Backend API integration
│   ├── chat_interface.py             # Chat UI logic
│   ├── sidebar.py                    # Upload & model controls
│   └── streamlit_app.py              # Main Streamlit app
│
├── docs/                             # Sample uploaded documents
│
├── documentation/
│   ├── screenshots/                  # Project screenshots
│   ├── api_reference.md              # API documentation
│   └── user_guide.md                 # User guide
│
├── .env.example                      # Environment variable template
├── .gitignore
├── LICENSE
├── notes.txt
├── requirements.txt
└── README.md
```

---

# ⚙️ How It Works

1️⃣ User uploads documents  
2️⃣ Documents are processed and chunked using LangChain  
3️⃣ Embeddings are generated and stored in ChromaDB  
4️⃣ User asks a query through Streamlit UI  
5️⃣ Relevant chunks are retrieved using semantic similarity  
6️⃣ Llama3 generates contextual responses using retrieved data  

---

# 📸 Application Screenshots

## 🖥️ Chatbot Interface

### Document Upload + Chat Interaction

<img width="100%" alt="RAG Chatbot UI" src="documentation/screenshots/chat_interface_1.png">

---

### Multi-Query Conversation Example

<img width="100%" alt="RAG Chatbot Conversation" src="documentation/screenshots/chat_interface_2.png">

---

# ▶️ Run Locally

## 1️⃣ Clone Repository

```bash
git clone https://github.com/Rashi14111/RAG-Chat-Assistant.git
cd RAG-Chat-Assistant
```

---

## 2️⃣ Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4️⃣ Configure Environment Variables

Create a `.env` file in the root directory.

Example:

```env
OPENAI_API_KEY=your_api_key_here
```

(Only if required by your configured model/provider.)

---

## 5️⃣ Start FastAPI Backend

```bash
cd api
uvicorn main:app --reload
```

Backend runs on:

```bash
http://127.0.0.1:8000
```

---

## 6️⃣ Start Streamlit Frontend

Open a new terminal:

```bash
cd app
streamlit run streamlit_app.py
```

Frontend runs on:

```bash
http://localhost:8501
```

---

# 📌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/upload` | Upload documents |
| POST | `/query` | Ask chatbot queries |
| GET | `/documents` | Retrieve uploaded documents |
| DELETE | `/documents/{id}` | Delete documents |

---

# 📊 Key Highlights

✔ End-to-end RAG implementation  
✔ FastAPI + Streamlit integration  
✔ Persistent vector storage using ChromaDB  
✔ LangChain-powered retrieval pipeline  
✔ Semantic document understanding  
✔ Interactive AI chatbot interface  
✔ Modular backend/frontend architecture  

---

# 🔒 Notes

- `.env` file is excluded using `.gitignore`
- Virtual environment (`venv`) should NOT be pushed to GitHub
- ChromaDB generated files can be regenerated automatically
- Uploaded sample documents are only for testing/demo purposes

---

# 👩‍💻 Author

## Rashi Garg

- GitHub: https://github.com/Rashi14111

---

# 📜 License

This project is licensed under the MIT License.

