# Tour Guide AI 🌍🤖

An intelligent, interactive AI-powered tour guide application designed to help users explore destinations, discover local attractions, plan itineraries, and ask travel-related questions in real time.

Powered by **FastAPI**, **Google Gemini AI**, and **React (Vite)**.

---

## ✨ Features

- 🗺️ **Personalized Itineraries:** Generate tailored travel itineraries based on interest, budget, and destination.
- 💬 **Interactive AI Chat:** Real-time travel Q&A powered by Google Gemini LLM.
- 📍 **Local Recommendations:** Discover hidden gems, restaurants, landmarks, and cultural insights.
- 💾 **Conversation History:** Persistence for chat sessions stored locally using SQLite.
- ⚡ **Fast & Responsive UI:** Built with Vite and React for a modern frontend experience.

---

## 🏗️ Project Architecture

```text
tour-guide-ai/
├── backend/               # FastAPI backend service
│   ├── .env.example       # Example environment variables setup
│   └── tour_guide.db      # SQLite database (local application state)
├── frontend/              # React + Vite frontend application
└── README.md              # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:
- [Python 3.10+](https://www.python.org/)
- [Node.js 18+](https://nodejs.org/)
- [Google Gemini API Key](https://aistudio.google.com/apikey)

---

### 1. Backend Setup

1. **Navigate to the backend directory:**
   ```bash
   cd backend
   ```

2. **Create and activate a virtual environment:**
   - **Windows (PowerShell):**
     ```powershell
     python -m venv venv
     .\venv\Scripts\Activate.ps1
     ```
   - **Linux / macOS:**
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```

3. **Install backend dependencies:**
   ```bash
   pip install fastapi uvicorn google-genai sqlalchemy aiosqlite python-dotenv pytest
   ```

4. **Configure Environment Variables:**
   Create a `.env` file in the `backend/` directory based on the configuration below:

   ```env
   # API Keys
   GEMINI_API_KEY=your_gemini_api_key_here
   LLM_PROVIDER=gemini
   LLM_MODEL=gemini-flash-lite-latest

   # Database
   DATABASE_URL=sqlite+aiosqlite:///./tour_guide.db

   # Application Settings
   APP_NAME=Tour Guide AI
   APP_VERSION=0.1.0
   DEBUG=false
   LOG_LEVEL=INFO

   # Server Settings
   HOST=0.0.0.0
   PORT=8000
   CORS_ORIGINS=http://localhost:5173,http://localhost:3000
   ```

5. **Run the Backend Server:**
   ```bash
   uvicorn main:app --reload --host 0.0.0.0 --port 8000
   ```
   The backend API will be available at `http://localhost:8000` (API Docs at `http://localhost:8000/docs`).

---

### 2. Frontend Setup

1. **Navigate to the frontend directory:**
   ```bash
   cd frontend
   ```

2. **Install frontend dependencies:**
   ```bash
   npm install
   ```

3. **Run the Frontend Development Server:**
   ```bash
   npm run dev
   ```
   The app will run locally at `http://localhost:5173`.

---

## 🛠️ Tech Stack

- **Backend:** Python, FastAPI, SQLAlchemy (Async), SQLite
- **AI Model:** Google Gemini API (`gemini-flash-lite-latest`)
- **Frontend:** React, Vite, JavaScript / TypeScript
- **Styling:** Modern CSS

---

## 📄 License

This project is licensed under the MIT License.
