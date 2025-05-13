# 🧠 AI Chatbot Assistant

A full-stack chatbot built with **FastAPI** (backend) and **React** (frontend), powered by the **LLaMA 2** model via **Ollama**. This project features real-time streaming responses, session-based memory, and options to export conversations as Markdown or PDF.

---

## 🚀 Features

| Feature | Description |
|--------|-------------|
| 💬 LLM Chat | Uses LLaMA 2 model with Ollama for intelligent responses |
| 🔁 Streaming | Real-time chat updates via SSE |
| 🧠 Memory | Tracks session history across messages |
| 📤 Export | Save chat history as `.md` or `.pdf` |
| 🌐 CORS-enabled | Ready for cross-origin access by frontend |
| 🎙️ Voice Input | Handled in frontend via browser API (JavaScript) |

---

## 📁 Project Structure

```
NeuraChat/
├── backend/               # FastAPI server
│   └── main.py            # Core chat, memory, and export logic
├── frontend/              # React app
│   ├── public/
│   ├── src/
│   └── package.json       # Scripts & dependencies
├── requirements.txt       # Python backend dependencies
└── README.md              # This file
```

---

## ⚙️ Backend Setup

**Requirements:**
- Python 3.8+
- [Ollama](https://ollama.ai/) with LLaMA 2 model

**Steps:**
```bash
# Clone the repo and navigate to backend
cd NeuraChat/backend

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r ../requirements.txt

# Pull the model
ollama pull llama2

# Start server
uvicorn main:app --host 0.0.0.0 --port 8000
```

---

## 💻 Frontend Setup

**Requirements:**
- Node.js 18+

**Steps:**
```bash
# Navigate to frontend directory
cd NeuraChat/frontend

# Install dependencies
npm install

# Run development server
npm start
```

Open your browser at [http://localhost:3000](http://localhost:3000)

---

## 🗣️ Voice Interaction

The **speak** feature is implemented on the **frontend** using the Web Speech API (JavaScript), not Python.

---

## 📦 Notable Scripts (`frontend/package.json`)

```json
{
  "start": "react-scripts start",
  "build": "react-scripts build",
  "test": "react-scripts test",
  "eject": "react-scripts eject"
}
```

---

## 🧪 Dependencies

**Backend (`requirements.txt`)**:
```
fastapi==0.115.12
uvicorn==0.22.0
python-dotenv==1.0.0
httpx==0.24.1
pydantic==2.11.3
```



---

