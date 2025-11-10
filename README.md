# **AI-Powered Document Summarizer & Chat Assistant**
### **Overview**
This project is an AI-powered **document understanding assistant** that allows users to upload reports, papers, or text files and interact with them conversationally.
It uses **Google Gemini 1.5 Pro**, **LangChain**, and **ChromaDB** to generate accurate, context-aware document summaries and intelligent responses — all through a clean conversational interface.

The system leverages **Retrieval-Augmented Generation (RAG)** to combine local document embeddings with Gemini’s generative reasoning for deep contextual insights.


### **Features**

* 📄 **Document Upload & Summarization**
  Upload PDFs, TXT, or Markdown files and get instant summaries.

* 💬 **Chat with Your Documents**
  Ask context-based questions and receive accurate answers extracted from your uploaded files.

* ⚙️ **RAG-Powered Retrieval**
  Uses chunked text embeddings stored in **ChromaDB** for precise context recall.

* 🤖 **Google Gemini Integration**
  Generates intelligent, structured, and medically/technically sound responses.

* 🧠 **Modular LangChain Pipeline**
  Separate stages for loading, chunking, embedding, retrieval, and conversation — easily extensible.

* 🛡️ **Secure Local Processing**
  Keeps all document embeddings and data local to your environment.

### **Tech Stack**
#### **1. Backend & Framework**

* **Python 3.11+**
* **LangChain** — Framework for RAG and chaining logic
* **ChromaDB** — Lightweight local vector database for embeddings
* **FastAPI or Flask** (optional) — For serving as an API backend

#### **2. AI & NLP**
* **Google Gemini 1.5 Pro** — Large language model for summarization and QA
* **LangChain Google GenAI** — Wrapper to connect Gemini with LangChain
* **RecursiveCharacterTextSplitter** — Efficient document chunking
* **PyPDFLoader / TextLoader** — Document parsing and preprocessing

#### **3. Environment & Configuration**
* **python-dotenv** — For managing API keys and configs
* **os** — For handling paths and file management

### **Project Structure**

app/
├── loaders/
│   └── file_loader.py         # Loads PDF/TXT/MD documents
├── utils/
│   ├── text_utils.py          # Handles document chunking
│   └── load_config.py         # Loads API keys and environment variables
├── retriever/
│   └── vector_store.py        # Builds and persists ChromaDB vector store
├── chains/
│   └── qa_chain.py            # Gemini-powered retrieval QA logic
├── interface/
│   └── cli.py                 # CLI chat interface
data/
└── sample_docs/               # Example PDFs/text files
```

### **How to Run**
#### **Step 01 — Clone the Repository**
```bash
git clone https://github.com/yourusername/AI-Document-Summarizer.git
cd AI-Document-Summarizer
```

#### **Step 02 — Create a Virtual Environment**
```bash
python3 -m venv myenv
source myenv/bin/activate    # (On macOS/Linux)
# OR
myenv\Scripts\activate       # (On Windows)
```

#### **Step 03 — Install Dependencies**

```bash
pip install -r requirements.txt
```

#### **Step 04 — Set Up Environment Variables**
```bash
cp .env.example .env
```

Then open `.env` and add your Gemini API key:
```
GOOGLE_API_KEY=your-gemini-api-key
```

#### **Step 05 — Run the Application**
```bash
python main.py
```

### **Example Query Flow**
1. Upload your documents to `./data`
2. Run the app
3. Type questions like:

   ```
   Summarize all the uploaded files.
   What does the blood test report indicate?
   ```
4. The AI retrieves the most relevant chunks and generates context-aware answers.


### **Future Enhancements**
* 🔍 Add **document-level insights dashboard** (visual summary cards)
* 🗣️ Voice query integration
* 🧾 Multi-document summarization with ranking
* 🧬 Medical report entity extraction (diagnosis, metrics, parameters)
* ☁️ Cloud deployment with persistent vector storage

# Summarist
