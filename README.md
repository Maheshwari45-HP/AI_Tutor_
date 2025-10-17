# AI Tutor 

A **minimal local implementation** of an AI Tutor Orchestrator combining **FastAPI backend**, **Streamlit frontend**, and a **mock MCP server**. Ideal for hackathons, prototyping, or personal learning projects.

This project allows students and educational platforms to generate **notes, flashcards, and concept explanations** using an autonomous multi-tool AI orchestration.

---

## Project Structure



## 📂 Project Structure

```
AI_Tutor-main/
├── backend/
│ ├── app/ # FastAPI application modules
│ ├── requirements.txt # Python dependencies
│ └── run_backend.bat # Start backend + MCP mock server
├── frontend/
│ ├── streamlit_app.py # Streamlit frontend UI
│ ├── requirements.txt # Python dependencies
│ └── .env # Environment variables
├── run_local.bat # Run backend + frontend together
└── README.md # Project description
```



---

## Quick Start (Windows)

### 1️⃣ Set up Virtual Environments
```cmd
cd AI_Tutor-main
python -m venv venv_backend
python -m venv venv_frontend

Activate the environment before installing dependencies.

---

# Backend
venv_backend\Scripts\activate

# Frontend
venv_frontend\Scripts\activate

2️⃣ Install Dependencies

pip install -r backend/requirements.txt
pip install -r frontend/requirements.txt


3️⃣ Run the Project

Option 1: Run both backend + frontend together

```bat
run_local.bat
```

* **Or individually:**

```bat
backend\run_backend.bat   # Starts MCP mock + FastAPI backend
frontend\run_frontend.bat # Starts Streamlit frontend
```

---

### 4️⃣ Access the Frontend

cd frontend
..\venv_frontend\Scripts\activate
streamlit run streamlit_app.py


Open your browser at:
[http://localhost:8501](http://localhost:8501)

---

## Frontend Preview
![frontend_screenshot](https://github.com/user-attachments/assets/3dcae1a3-81c7-4b5c-a944-69c6faeb6ca9)



## ⚙️ Configuration

* **Environment Variables:**
  `.env` files contain placeholders like:

  ```
  OPENAI_API_KEY=your_key_here
  ```

  Replace with your actual keys for real service integration.

* **MCP (Model Context Protocol):**

  * Local mock server URL: `http://localhost:8001/mcp/process`
  * Backend automatically falls back to a **local simple plan** if MCP is unreachable.

* **LangGraph:**
  Calls are currently mocked in `langgraph_wrapper.py`. Replace with real API calls for full functionality.

---

Usage

Enter your prompt (e.g., "Explain what is a neural network?")

Select Teaching Style, Emotional State, Mastery Level

Choose a Tool: note_maker, flashcard_generator, concept_explainer

Fill Topic, Subject, and optionally Note Taking Style


---

Features

Generate structured notes for any topic

Create flashcards for learning reinforcement

Explain concepts with adaptive teaching style and mastery level

Lightweight, local, hackathon-ready demo

## ✅ Notes

* **MVP-ready**: Ideal for hackathon demos and local prototyping.
* **Extensible**: Easily integrate real AI agents, LangGraph workflows, and multiple educational tools.
* **Lightweight & Deployable**: Runs on local machines or cloud servers.
* **Designed for Education**: Personalizes learning by orchestrating multiple AI-powered tools seamlessly.

---

Future Improvements

Real LangGraph integration for dynamic multi-agent workflows

Advanced personalization based on student engagement and mastery

Support for multiple AI tool APIs


---

🤖Tech Stack

Python

FastAPI (Backend)

Streamlit (Frontend)

MCP Mock Server (Tool orchestration)

Optional: OpenAI API or other LLMs

Copyright (c) 2025 Maheshwari Khobare
All rights reserved.

This project is shared for educational and portfolio demonstration purposes only.
Commercial use, redistribution, or modification of this code is strictly prohibited
without prior written permission from the author.




