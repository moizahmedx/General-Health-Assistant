# ❤️ General Health Query Chatbot (Agent SDK + Gemini + Docker)

## 📌 Overview
The General Health Query Chatbot is an AI-powered assistant that provides safe, friendly, and general health-related information using Gemini LLM (gemini-2.5-flash) via OpenAI Agents SDK.  

It includes a Streamlit-based web UI (chat bubbles, chat history) and a CLI interface, with a safety filter to prevent harmful advice.

It is also Docker-ready for containerized deployment and easy sharing.

---

## 🎯 Objective
- Provide general health information
- Explain symptoms and common causes  
- Suggest preventive care & healthy habits 
- Avoid diagnosis or prescription  
- Safety filtering for emergencies  

---

## 🛠 Tools & Technologies
- Python 3.10+  
- OpenAI Agents SDK  
- Gemini LLM (`gemini-2.5-flash`)  
- dotenv, os (for secure API key access)
- Streamlit (Web UI)  
- AsyncOpenAI client
- Docker (for deployment)

---

## 📂 Project Structure
General_Health_Query_Chatbot/
│
├── chatbot.py          # Streamlit UI + CLI version
├── requirements.txt
├── .env
├── Dockerfile          # Docker setup for deployment
└── README.md


---

## ✨ Features
- Gemini-powered intelligent responses 
- Safety filter for harmful queries
- Friendly & clear explanations  
- CLI & Streamlit interfaces  
- Modular, expandable architecture  
- Exception handling & secure API key management
- Docker-ready for easy deployment

---

## ⚙️ Installation

### Step 1: Clone repository
git clone https://github.com/yourusername/general-health-query-chatbot.git

cd general-health-query-chatbot

### Step 2: Create virtual environment
Windows:
python -m venv .venv
.venv\Scripts\activate
Linux / Mac / WSL:
python -m venv .venv
source .venv/bin/activate

### Step 3: Install dependencies
pip install -r requirements.txt

### Step 4: Setup environment variables
Create `.env` file:
GEMINI_API_KEY=your_api_key_here

---

## ▶️ How to Run

### Streamlit UI (Local)
streamlit run chatbot.py

### CLI (optional, if implemented)
python chatbot.py

### Docker Deployment

Build Docker image:
docker build -t health-chatbot .

Run Docker container:
docker run -d -p 8501:8501 --env-file .env health-chatbot

Open browser:

---

## 💬 Example Queries
What causes a sore throat?
What are symptoms of flu?
How to improve immunity?
Is headache caused by dehydration?
What is common cold?

---

## ⚠️ Safety
- Does NOT diagnose or prescribe medicine  
- Emergency or dangerous questions will return:
⚠️ Please contact a doctor immediately.

---

## 👩‍💻 Author
Sehrish Shafiq  
AI Engineer | Agentic AI Developer | Python Developer
LinkedIn: https://www.linkedin.com/in/sehrish-shafiq
