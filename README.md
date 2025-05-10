# 📄 RAG Document Q&A with Groq and LLaMA3

This Streamlit application enables users to perform question-answering over a collection of research papers using Retrieval-Augmented Generation (RAG). It leverages Groq's LLaMA3 model for language understanding and HuggingFace embeddings for document similarity.

---

## 🚀 Features

- **Document Ingestion**: Automatically loads and processes PDFs from the `research_papers` directory.
- **Vector Embeddings**: Utilizes HuggingFace's `all-MiniLM-L6-v2` model to generate embeddings.
- **Vector Store**: Stores embeddings in a FAISS vector database for efficient retrieval.
- **Language Model**: Employs Groq's LLaMA3-8b-8192 model for generating answers.
- **Interactive UI**: Built with Streamlit for an intuitive user experience.

---

## 🛠️ Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/ssarthak0/Rag-Document-Q-A-with-GROQ-API-and-LLAMA-3
   cd Rag-Document-Q-A-with-GROQ-API-and-LLAMA-3
   ```

2. **Create a Virtual Environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set Up Environment Variables**

   Create a `.env` file in the root directory and add your API keys:

   ```env
   GROQ_API_KEY=your_groq_api_key_here
   OPENAI_API_KEY=your_openai_api_key_here
   HF_TOKEN=your_huggingface_token_here
   ```

   Replace the placeholder values with your actual API keys.

---

## 📁 Directory Structure

```
rag-groq-qa/
├── app.py
├── research_papers/
│   ├── paper1.pdf
│   ├── paper2.pdf
│   └── ...
├── requirements.txt
└── README.md
```

- Place your PDF documents inside the `research_papers` directory.

---

## 🧾 Usage

Run the Streamlit application:

```bash
streamlit run app.py
```

Once running, open your browser and navigate to `http://localhost:8501`. Enter your query in the input box and click on "Document Embedding" to initialize the vector store. Then, ask questions related to the content of your research papers.

---

## 🔍 How It Works

1. **Document Loading**: Uses `PyPDFDirectoryLoader` to load all PDFs from the specified directory.
2. **Text Splitting**: Splits documents into chunks using `RecursiveCharacterTextSplitter`.
3. **Embedding Generation**: Generates embeddings for each chunk using HuggingFace's `all-MiniLM-L6-v2` model.
4. **Vector Store Creation**: Stores embeddings in a FAISS vector database.
5. **Retrieval**: Retrieves relevant document chunks based on user queries.
6. **Answer Generation**: Uses Groq's LLaMA3 model to generate answers based on the retrieved context.

---

## 📚 Dependencies

Below is the `requirements.txt` content:

```plaintext
langchain
langchain-community
langchain-openai
langchain-groq
langchain-chroma
langchain-huggingface
python-dotenv
ipykernel
pypdf
pymupdf
chromadb
faiss-cpu
sentence-transformers
pandas
openai
huggingface_hub
streamlit
```

To install these dependencies, run:

```bash
pip install -r requirements.txt
```

Ensure that your `requirements.txt` file is in the root directory of your project. If you have any specific version requirements or encounter any compatibility issues, feel free to specify the versions accordingly.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙋‍♀️ Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

---

## 🔗 Resources

- [LangChain Documentation](https://docs.langchain.com/)
- [Groq API Documentation](https://console.groq.com/docs)
- [Streamlit Documentation](https://docs.streamlit.io/)

---

Happy querying! 🎉
