# RAG FastAPI Project

This project is a FastAPI application that handles document ingestion and query functionality for a retrieval-augmented generation (RAG) system. It includes endpoints for uploading and processing documents and querying them using embeddings.

## Features
- **Document Ingestion**: Upload and process documents.
- **Query Processing**: Query documents using embeddings.

## Technologies Used
- **FastAPI**: Web framework for building APIs.
- **Uvicorn**: ASGI server for running the FastAPI application.
- **Python**: Programming language used.

## Installation

### Prerequisites
- Python 3.6+
- Pip

### Steps

1. Clone the repository:  
   `git clone https://github.com/username/repository.git`  
   `cd rag_fastapi_project_`

2. Create and activate a virtual environment:  
   **Windows**:  
   `python -m venv venv`  
   `.\venv\Scripts\Activate`  
   **Mac/Linux**:  
   `python -m venv venv`  
   `source venv/bin/activate`

3. Install dependencies:  
   `pip install fastapi uvicorn`

4. Run the application:  
   `uvicorn app.main:app --reload`  
   The application will be running at `http://127.0.0.1:8000`.

## API Endpoints

- **POST /ingest**: Upload and process a document. The request must include a file, and the response will return a document ID.  
  Example response:  
  `{ "status": "success", "document_id": "12345" }`

- **POST /query**: Submit a query to retrieve relevant documents based on embeddings. The request includes a query string.  
  Example response:  
  `{ "status": "success", "results": [{ "document_id": "12345", "score": 0.95 }] }`

