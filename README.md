# RAG-AI_PDFBOT

# RAG Project: PDF Question Answering with LangChain

This project demonstrates how to build a Retrieval-Augmented Generation (RAG) system using LangChain, HuggingFace embeddings, and Groq LLMs. The system reads a PDF, splits it into chunks, creates a vector store for semantic search, and allows you to ask questions about the PDF content interactively.

## Features
- Reads and processes a PDF document
- Splits text into manageable chunks
- Creates a FAISS vector store for efficient retrieval
- Uses HuggingFace embeddings for semantic search
- Integrates with Groq LLM (Llama 3) for answer generation
- Interactive Q&A in the terminal

## Requirements
See `requirements.txt` for all dependencies. Install them with:

```bash
pip install -r requirements.txt
```

## Setup
1. **Clone the repository** and navigate to the project directory.
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Set up your environment variables:**
   - Create a `.env` file in the project root.
   - Add your Groq API key:
     ```env
     GROQ_API_KEY=your_groq_api_key_here
     ```
4. **Add your PDF:**
   - Place the PDF you want to query in the project directory.
   - By default, the notebook expects a file named `1. dietary supplements - for whom.pdf`. You can change this in the code.

## Usage
You can run the notebook (`RAG_Project.ipynb`) or convert it to a Python script. The main workflow is:

1. **Read the PDF:** Extracts text from the PDF file.
2. **Split the text:** Divides the text into overlapping chunks for better retrieval.
3. **Create vector store:** Embeds the chunks and stores them in a FAISS vector database.
4. **Ask questions:** Enter your questions in the terminal. Type `quit` to exit.

## Example
```
Enter your question (or 'quit' to exit): What are dietary supplements?

Processing...

Answer: According to the provided context, dietary supplements are products that are concentrated sources of vitamins, minerals, or other substances with a nutritional or physiological effect, intended to supplement the regular diet. ...
```

## Notes
- Make sure your Groq API key is valid and has access to the Llama 3 model.
- For large PDFs, processing may take some time.
- If you encounter issues with embeddings, ensure you have the correct versions of `torch` and `transformers` installed.

## License
This project is for educational purposes. 
