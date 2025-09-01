# RAG-Bot

A modular, scalable, and industry-ready chat/document upload application built with React, Vite, Tailwind CSS (frontend) and FastAPI, PostgreSQL, Gemini API (backend).

## Features
- Modern chat UI with sticky header/footer
- File upload and preview (PDF, images)
- Responsive design and dark theme
- WhatsApp-style message status
- Custom scrollbars and gradients
- Accessible and easy to use
- Automated deployment via GitHub Actions
- FastAPI backend with semantic search, chunking, and Gemini-powered chat

## 📂 Project Structure

```
rag-bot/
├── Frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── App.tsx
│   │   ├── index.css
│   │   ├── main.tsx
│   │   └── vite-env.d.ts
│   ├── dist/
│   ├── package.json
│   ├── tailwind.config.js
│   ├── postcss.config.js
│   ├── tsconfig.json
│   ├── vite.config.ts
│   └── .github/workflows/deploy.yml
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── api/ (routes)
│   │   ├── db/ (database models/sessions)
│   │   ├── core/ (config/cors)
│   │   ├── models/, repositories/, schemas/, services/, utils/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── requirements.txt
│   └── README.md
├── requirements.txt
└── README.md
'''

## Frontend Setup
1. Install dependencies:
   sh
   cd Frontend
   npm install
   
2. Run the development server:
   sh
   npm run dev
   
3. Build for production:
   sh
   npm run build
   

## Backend Setup
1. Create/select a Python environment (venv or conda).
2. Install dependencies:
   sh
   pip install -r requirements.txt
   
3. Set up environment variables:
   sh
   cp .env.example .env  # Add your GEMINI_API_KEY
   
4. Run with Docker:
   sh
   docker-compose up --build
   
5. Access API docs at [http://localhost:8000/docs](http://localhost:8000/docs)

## Backend Architecture & Features
- *FastAPI*: Main API framework
- *PostgreSQL + pgvector*: Stores document embeddings for semantic search
- *Gemini API*: Used for embeddings and chat responses
- *Chunking & Deduplication*: Documents are normalized, chunked, and deduplicated using SHA256
- *Hybrid Search*: Combines vector and lexical search with Reciprocal Rank Fusion
- *Streaming Chat*: SSE endpoint with inline citations
- *Rate Limiting & Auth*: Optional bearer token authentication
- *Structured Logging*: JSON logs for observability
- *Docker*: Containerized for easy deployment

## Deployment
- *Frontend*: Automated via GitHub Actions (deploy.yml). Artifacts can be deployed to static hosting or GitHub Pages.
- *Backend*: Use Docker/Docker Compose for production deployment. Ensure PostgreSQL is set up with the vector extension.
