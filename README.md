# 🎬 AI Video Assistant

AI-powered meeting intelligence platform that transcribes videos, generates summaries, extracts key insights, and allows users to chat with meeting content using RAG (Retrieval-Augmented Generation).

Built using Whisper, Mistral AI, LangChain, ChromaDB, and Streamlit.

---

## ✨ Features

- 🎙️ Audio extraction from YouTube videos
- 📝 Speech-to-text transcription using Whisper
- 🌐 Hinglish → English transcription using Sarvam AI
- 📋 Automatic meeting summarization
- 🏷️ Meeting title generation
- ✅ Action item extraction
- 🔑 Key decision extraction
- ❓ Open question detection
- 🧠 RAG-powered meeting chatbot
- 🎨 Interactive Streamlit dashboard

---

## 🔄 Workflow

```text
YouTube URL / Audio File
            │
            ▼
     Audio Extraction
            │
            ▼
      Audio Chunking
            │
            ▼
      Transcription
   (Whisper / Sarvam)
            │
            ▼
        Transcript
            │
   ┌────────┼────────┐
   ▼        ▼        ▼
Summary  Decisions  Action Items
   │
   ▼
Vector Embeddings
   │
   ▼
 ChromaDB Store
   │
   ▼
 RAG Chat Assistant
```

---

## 🏗️ Tech Stack

### AI & LLM
- Mistral AI
- LangChain (LCEL)

### Speech Processing
- OpenAI Whisper
- Sarvam AI

### RAG Pipeline
- ChromaDB
- Sentence Transformers
- all-MiniLM-L6-v2

### Frontend
- Streamlit

### Audio Processing
- yt-dlp
- FFmpeg
- pydub

---

## 📁 Project Structure

```text
AI-Video-Assistant/
│
├── app.py
├── main.py
├── requirements.txt
│
├── core/
│   ├── extractor.py
│   ├── rag_engine.py
│   ├── summarizer.py
│   ├── transcriber.py
│   └── vector_store.py
│
├── utils/
│   └── audio_processor.py
│
└── vector_db/
```

---

## ⚙️ Installation

```bash
git clone <your-repo-url>

cd AI-Video-Assistant

uv venv

source .venv/bin/activate

uv pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file:

```env
MISTRAL_API_KEY=your_key

SARVAM_API_KEY=your_key

WHISPER_MODEL=small

SARVAM_STT_MODEL=saaras:v2.5
```

---

## ▶️ Run Application

### Streamlit UI

```bash
streamlit run app.py
```

### CLI Version

```bash
python main.py
```
