```markdown
# RAG Q&A Conversation With PDF

![License](https://img.shields.io/badge/license-GPL%20v3-blue)
![Language](https://img.shields.io/badge/language-Python%203.10%2B-blue)
![Framework](https://img.shields.io/badge/framework-Streamlit-orange)

A conversational Retrieval-Augmented Generation (RAG) application that allows users to upload PDF documents and interact with their content through natural language queries, maintaining chat history for context-aware responses.

## Description

This project implements a **conversational Q&A system over PDF documents** using a combination of:

- **LangChain** for orchestrating the RAG pipeline  
- **Groq's LLaMA 3.1 8B** as the language model  
- **Hugging Face Sentence Transformers** for dense document embeddings  
- **ChromaDB** for efficient vector storage and retrieval  
- **Streamlit** for an interactive web-based UI  

Users can upload one or more PDFs, ask questions about the content, and receive answers grounded in the document text — all while preserving session-based conversation history for richer context.

### Key Capabilities

- Upload and process PDF files dynamically  
- Ask follow-up questions leveraging previous interactions  
- Maintain separate chat sessions via unique session IDs  
- Retrieve relevant document chunks using semantic similarity search  
- Generate accurate, cited responses using a history-aware retriever  

## Installation

### Prerequisites

Before running the app, ensure you have:

- Python 3.10 or higher  
- A [Groq API key](https://console.groq.com/)  
- A Hugging Face token with access to embedding models (e.g., `all-MiniLM-L6-v2`)  

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/duttabikram/-RAG-Q-A-Conversation-With-PDF.git
   cd -RAG-Q-A-Conversation-With-PDF
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables in a `.env` file:

   ```env
   HF_TOKEN=your_huggingface_token_here
   ```

5. Run the Streamlit app:

   ```bash
   streamlit run app.py
   ```

## Usage

Once the app is running locally or deployed:

1. Enter your **Groq API key** when prompted.
2. Provide a **Session ID** (or use the default).
3. Upload one or more **PDF files**.
4. Start asking questions based on the uploaded content.

Example interaction flow:

```text
User: What are the main findings of the study?
Bot: According to the document...
User: Can you elaborate on section 3?
Bot: In section 3, it was noted that...
```

The system maintains context across messages within the same session.

## Tech Stack

| Category          | Technology                         |
|-------------------|------------------------------------|
| Language          | Python                             |
| Web Framework     | Streamlit                          |
| LLM               | Groq LLaMA 3.1 8B                  |
| Embeddings        | Hugging Face (all-MiniLM-L6-v2)    |
| Vector Store      | ChromaDB                           |
| Document Loaders  | PyPDFLoader (via LangChain)        |
| Text Splitting    | RecursiveCharacterTextSplitter     |
| Prompt Management | LangChain Prompt Templates         |
| Environment Mgmt  | python-dotenv                      |

## Features

- ✅ Conversational Q&A over PDF documents  
- 📚 Semantic retrieval using embeddings  
- 🔁 Session-aware chat history tracking  
- 💬 Follow-up question support  
- 🖥️ Interactive Streamlit interface  
- ☁️ Deploy-ready configuration  

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository  
2. Create a new branch (`git checkout -b feature/your-feature`)  
3. Commit your changes (`git commit -m 'Add some feature'`)  
4. Push to the branch (`git push origin feature/your-feature`)  
5. Open a pull request  

Please make sure to update tests as appropriate.

## License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for details.
```