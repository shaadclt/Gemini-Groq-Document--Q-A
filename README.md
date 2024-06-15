# Gemini Groq Document Q&A

This project is a Streamlit application that leverages language models and vector embeddings to perform document-based Q&A. It uses LangChain, FAISS, and Google Generative AI embeddings to process and retrieve information from documents stored in a directory.

## Features
- Upload and process PDF documents from a specified directory.
- Create vector embeddings from document content.
- Perform Q&A based on the processed documents using a large language model (LLM).

## Requirements
- Python 3.7+
- Required Python packages (listed in `requirements.txt`)

## Installation

1. **Clone the repository:**

```bash
git clone https://github.com/shaadclt/Gemini-Groq-Document--Q-A.git
cd Gemini-Groq-Document--Q-A
```

2. **Install the required packages:**
```bash
pip install -r requirements.txt
```

3. **Set up environment variables:**
Create a .env file in the root directory of the project and add your API keys:
```bash
GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
```

## Usage
1. Run the Streamlit app:
```bash
streamlit run app.py
```
2. Use the application:
- The app's title "Gemini Groq Document Q&A" will be displayed at the top.
3. To embed documents, click the "Documents Embedding" button.
- Once the vector store DB is ready, enter your query in the text input field and press enter.
4. The response will be displayed based on the processed documents.

## Main Components
**Vector Embedding:**

The vector_embedding function loads PDF documents from the specified directory, splits them into chunks, and creates vector embeddings using Google Generative AI embeddings.

**Q&A Retrieval:**

The application uses a language model (ChatGroq) to answer questions based on the document content. The retrieval chain fetches relevant document chunks and passes them to the language model to generate responses.

## Key Libraries and Tools
1. Streamlit: For creating the web interface.
2. LangChain: For managing and chaining different components such as loaders, splitters, and language models.
3. FAISS: For efficient similarity search and clustering of vector embeddings.
4. Google Generative AI Embeddings: For creating vector representations of document chunks.
5. dotenv: For loading environment variables from a .env file.

### Sample .env File
```bash
GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
```

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.
