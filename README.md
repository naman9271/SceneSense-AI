<div align="center">

# SceneSense AI

**AI-Powered Intelligent Image Search Platform**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.111.1-009688.svg)](https://fastapi.tiangolo.com/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.36.0-FF4B4B.svg)](https://streamlit.io/)


</div>

---

## 🎯 Overview

Scene Sense is an AI-powered image search platform that transforms how you interact with your photo collections. Instead of scrolling through endless folders or relying on manual tags, simply describe what you're looking for in natural language and let AI find it for you.

## ✨ Key Features

- **🔍 Natural Language Search** - Search images using conversational queries like "sunset over mountains" or "people at a beach"
- **🤖 AI-Powered Understanding** - Utilizes OpenAI's CLIP model for semantic comprehension of image content
- **👥 Multi-User Support** - Secure authentication with isolated storage per user
- **🔒 Enterprise Security** - bcrypt password hashing and JWT-based authentication
- **☁️ Cloud Infrastructure** - Built on Google Cloud Platform for scalability
- **⚡ Fast Retrieval** - Pinecone vector database enables millisecond-level search responses
- **🎨 Modern Interface** - Clean, intuitive UI built with Streamlit

## 🏗️ Architecture

```
┌─────────────┐
│ Streamlit UI│ ◄── User Interface
└──────┬──────┘
       │
┌──────▼──────┐
│ FastAPI API │ ◄── Backend Logic
└──────┬──────┘
       │
   ┌───┴───┬────────┬─────────┐
   │       │        │         │
┌──▼──┐ ┌─▼─┐ ┌────▼────┐ ┌──▼───┐
│Mongo│ │GCP│ │Pinecone │ │ CLIP │
│ DB  │ │   │ │ Vector  │ │Model │
└─────┘ └───┘ └─────────┘ └──────┘
```

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **Backend**: FastAPI, Python 3.8+
- **AI/ML**: OpenAI CLIP, PyTorch
- **Databases**: MongoDB (Auth), Pinecone (Vectors)
- **Cloud**: Google Cloud Storage
- **Security**: JWT, bcrypt, OAuth2
- **Deployment**: Docker, Docker Compose

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Docker & Docker Compose (optional)
- Google Cloud Platform account
- MongoDB instance
- Pinecone account

### Installation

```bash
# Clone the repository
git clone https://github.com/naman9271/SceneSense-AI.git
cd SceneSense-AI

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Configure environment variables
cp .env.example .env
# Edit .env with your credentials

# Run the application
streamlit run scene_sense_app.py
```

### Docker Deployment

```bash
# Start all services
docker-compose up --build

# Access the application
# Streamlit UI: http://localhost:8501
# FastAPI Docs: http://localhost:8000/docs
```

## 📖 How It Works

1. **Upload Images** - Add your photos to the platform
2. **AI Processing** - CLIP model generates semantic embeddings
3. **Vector Storage** - Embeddings stored in Pinecone for fast retrieval
4. **Natural Search** - Describe what you're looking for in plain English
5. **Smart Results** - AI matches your query with relevant images

## 🔐 Security Features

- Password hashing with bcrypt
- JWT token-based authentication
- Per-user storage isolation
- Environment-based credential management
- HTTPS recommended for production

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenAI CLIP](https://github.com/openai/CLIP) for the vision-language model
- [FastAPI](https://fastapi.tiangolo.com/) and [Streamlit](https://streamlit.io/) communities
- Google Cloud Platform and Pinecone for infrastructure

<div align="center">

## Demo

https://github.com/user-attachments/assets/783a367b-66b1-4698-af5d-0461d3fb2c87


</div>

