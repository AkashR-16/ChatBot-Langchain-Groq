# ChatBot-Langchain-Groq
This project demonstrates a simple implementation of a chatbot using **Streamlit**, **LangChain**, and **FAISS** for document retrieval. The bot utilizes **ChatGroq** as the LLM and performs similarity searches on pre-loaded documents.

## Features

- Load documents from the web.
- Split documents into manageable chunks.
- Perform document similarity searches using FAISS.
- Retrieve and answer questions based on context.

## Prerequisites

- Python 3.8+
- A valid **Groq API key**.
- The following Python libraries:
  - `streamlit`
  - `langchain`
  - `langchain_community`
  - `langchain_groq`
  - `dotenv`
  - `faiss-cpu` (or `faiss-gpu` for better performance with GPU)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AkashR-16/ChatBot-Langchain-Groq.git
   cd ChatBot-Langchain-Groq
2. Create a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate
3. Setup Environmental variables:
     Add the Groq API key

## Usage
1. Run the streamlit app
   ```bash
   streamlit run app.py
2. Enter your prompt in the text input field, and the chatbot will answer based on the loaded documents.
3. Use the Document similarity search expander to view the relevant document chunks.

## How It Works
1. Document Loading: Documents are fetched from a specified URL using WebBaseLoader.
2. Text Splitting: The documents are split into smaller chunks using RecursiveCharacterTextSplitter.
3. Vector Store: FAISS indexes the document chunks for efficient retrieval.
4. Chatbot Workflow:
   - A user's query is passed through the retrieval chain.
   - Relevant chunks are retrieved and used as context for generating the response.
5. LLM Integration: ChatGroq generates responses using the retrieved context.

