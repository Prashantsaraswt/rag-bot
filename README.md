# 🚀 RAG-Bot

A modular, scalable, and industry-ready **chat + document upload** application powered by **React, Vite, Tailwind CSS (Frontend)** and **FastAPI, PostgreSQL, Gemini API (Backend)**.  
Built for modern **Retrieval-Augmented Generation (RAG)** use cases with semantic search, chunking, and real-time AI chat.

---

## ✨ Features

- Modern **chat UI** with sticky header & footer  
- **File upload & preview** (PDF, images)  
- Responsive design with **dark theme**  
- WhatsApp-style **message status**  
- **Custom scrollbars & gradients** for smooth UX  
- Accessible, simple, and fast  
- **FastAPI backend** with semantic search & Gemini-powered chat  
- **PostgreSQL + pgvector** for vector storage  
- **Chunking & Deduplication** with SHA256  
- **Hybrid Search** (semantic + lexical with RRF)  
- **Streaming Chat (SSE)** with inline citations  
- Optional **Rate Limiting & Auth**  
- **Structured Logging** for observability  
- **Dockerized** for easy deployment  

---

## 📂 Project Structure

rag-bot/
├── Frontend/
│ ├── src/
│ │ ├── components/
│ │ ├── App.tsx
│ │ ├── index.css
│ │ ├── main.tsx
│ │ └── vite-env.d.ts
│ ├── dist/
│ ├── package.json
│ ├── tailwind.config.js
│ ├── postcss.config.js
│ ├── tsconfig.json
│ ├── vite.config.ts
│ └── .github/workflows/deploy.yml
├── backend/
│ ├── app/
│ │ ├── main.py
│ │ ├── api/ (routes)
│ │ ├── db/ (database models/sessions)
│ │ ├── core/ (config/cors)
│ │ ├── models/, repositories/, schemas/, services/, utils/
│ ├── Dockerfile
│ ├── docker-compose.yml
│ ├── requirements.txt
│ └── README.md
├── requirements.txt
└── README.md

yaml
Copy code

---

## 🖥️ Frontend Setup

```sh
cd Frontend
npm install
npm run dev   # Run development server
npm run build # Build for production
⚡ Backend Setup
sh
Copy code
# (inside your Python venv)
pip install -r requirements.txt

# Copy env file and add your GEMINI_API_KEY
cp .env.example .env
Run with Docker
sh
Copy code
docker-compose up --build
API Docs available at 👉 http://localhost:8000/docs

🏗️ Backend Architecture
FastAPI – High-performance API framework

PostgreSQL + pgvector – Vector storage for embeddings

Gemini API – Embeddings & chat responses

Hybrid Search – Semantic + lexical (Reciprocal Rank Fusion)

Chunking + Deduplication – Efficient document processing

Streaming (SSE) – Real-time AI chat with citations

Auth & Rate Limiting – Optional security layer

Structured Logging – JSON logs for observability

Dockerized – Easy containerized deployment

🚀 Deployment
Frontend
Automated via GitHub Actions (deploy.yml)

Deployable to GitHub Pages or static hosting

Backend
Run with Docker/Docker Compose

Requires PostgreSQL with pgvector extension

📌 Roadmap / Improvements
 Add multi-modal RAG (text + image)

 Enhance auth with JWT & RBAC

 Improve query ranking with rerankers

 Add monitoring (Prometheus + Grafana)

 Deploy backend to cloud (AWS/GCP/Azure)



