# AgriMind — AI-Powered Crop Disease Diagnostic System

AgriMind is an end-to-end intelligent farming assistant that combines 
Computer Vision, LLMs, RAG pipelines, and Voice AI to help farmers 
diagnose crop diseases and get actionable treatment advice.

---

## Live Demo
[Try AgriMind on Hugging Face](https://huggingface.co/spaces/dedhaaryavrat/Agrimind)

---

## System Architecture

Leaf Image → MobileNetV2 Router → Crop-Specific Disease Classifier
→ LangChain LLM (Groq) → RAG Pipeline (ChromaDB) → Voice Response

---

## Features

- Two-stage CNN pipeline — MobileNetV2 router (99.4% accuracy) routes 
  to crop-specific specialist models (92.4% accuracy)
- Supports 8 crops and 9+ disease classes per crop
- LLM-powered Q&A grounded in agricultural knowledge base via RAG
- Hindi and English voice input via OpenAI Whisper
- Persistent ChromaDB vector store with cosine similarity retrieval

---

## Tech Stack

- Deep Learning: TensorFlow, Keras, MobileNetV2, CNN
- LLM and Agents: LangChain, LangGraph, Groq API (llama-3.1-8b-instant)
- RAG: ChromaDB, cosine similarity
- Voice AI: OpenAI Whisper, faster-whisper
- Frontend: Streamlit
- Deployment: Hugging Face Spaces

---

## Project Structure

agrimind/
├── app.py                 # Main Streamlit application
├── rag_engine.py          # RAG pipeline logic
├── bot_whisper/
│   └── ragbot.py          # Voice input handler
├── the_rag_one/
│   └── chat_engine.py     # LLM chat engine
├── data/
│   └── vector_store/      # ChromaDB persistent store
├── pdfs/                  # Agricultural knowledge base
├── *.keras                # Trained CNN models
└── requirements.txt

---

## Local Setup

git clone https://github.com/AryavratDedha/Agrimind.git
cd Agrimind
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
echo GROQ_API_KEY=your_key_here > .env
streamlit run app.py

---

## Supported Crops and Diseases

Tomato: Bacterial Spot, Early Blight, Late Blight, Leaf Mold,
        Septoria Leaf Spot, Spider Mites, Target Spot, Yellow Leaf Curl Virus
Apple: Apple Scab, Black Rot, Cedar Apple Rust
Corn: Common Rust, Gray Leaf Spot, Northern Leaf Blight
Potato: Early Blight, Late Blight
Rice: Brown Spot, Leaf Blast, Neck Blast
Sugarcane: Bacterial Blight, Red Rot
Bell Pepper: Bacterial Spot
Wheat: Brown Rust, Yellow Rust

---

## Author

Aryavrat Dedha
GitHub: https://github.com/AryavratDedha
Hugging Face: https://huggingface.co/dedhaaryavrat
LinkedIn: https://www.linkedin.com/in/aryavrat-dedha-02b3412ba
