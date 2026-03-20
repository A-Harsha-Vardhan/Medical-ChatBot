## Architecture – Medical AI Chatbot (RAG-Based System)

The system follows a Retrieval-Augmented Generation (RAG) architecture to deliver context-aware medical responses.

1. User Interface (Client Layer)
   The user submits a medical query through a web interface or API client.

2. Backend API (Flask)
   The Flask server receives the request, validates input, and forwards the query to the processing pipeline.

3. Embedding Layer (HuggingFace)
   The user query is converted into vector embeddings using a HuggingFace embedding model.

4. Vector Database (Pinecone)
   The generated embeddings are used to perform similarity search in Pinecone.
   Relevant medical documents are retrieved based on semantic similarity.

5. Retrieval-Augmented Generation (LangChain)
   LangChain combines the user query with retrieved context to construct a prompt for the LLM.

6. Large Language Model (Gemini API)
   The Gemini model generates a response using the provided context and query.

7. Response Handling
   The generated response is returned through the Flask API to the user interface.

8. Deployment (Render)
   The Flask application is deployed on Render, handling incoming requests and integrating with external services (Pinecone and Gemini API).

Tech Stack:

* Backend: Flask (Python)
* LLM: Gemini API
* Embeddings: HuggingFace
* Vector Database: Pinecone
* Framework: LangChain
* Deployment: Render

Architecture Type:

* Retrieval-Augmented Generation (RAG)
* API-based Microservice Integration
