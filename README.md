# ❤️ General Health Query Chatbot (Agent SDK + Gemini + Docker)

## 📌 Overview
The General Health Query Chatbot is an AI-powered assistant that provides safe, friendly, and general health-related information using Gemini LLM (gemini-2.5-flash) via OpenAI Agents SDK.  

It includes a Streamlit-based web UI (chat bubbles, chat history) and a CLI interface, with a safety filter to prevent harmful advice.

It is also Docker-ready for containerized deployment and easy sharing.

## 🔍 What Makes This Project Special

This chatbot demonstrates modern AI engineering practices by combining:

- **Intelligent Agent Architecture**: Built using OpenAI Agents SDK for structured, maintainable AI workflows
- **Safety-First Design**: Implements keyword-based safety filtering to detect emergency situations and redirect users to professional medical help
- **Production-Ready**: Includes Docker containerization, health checks, and environment-based configuration
- **User-Friendly Interface**: Clean Streamlit UI with persistent chat history and real-time responses
- **Responsible AI**: Clear boundaries on what the chatbot can and cannot do - no diagnosis, no prescriptions, only general information

## 🏗️ Architecture & Design

### Agent System
The chatbot uses a single-agent architecture with carefully crafted instructions:
- **Agent Name**: Medical_Assistant
- **Model**: Gemini 2.5 Flash (via OpenAI-compatible API)
- **Behavior**: Provides general health information while maintaining safety boundaries

### Safety Layer
Before any query reaches the LLM, it passes through a safety filter that checks for:
- Suicide-related keywords
- Self-harm indicators
- Overdose mentions
- Emergency situations

If detected, the system immediately returns a warning to seek professional help.

### Response Flow
1. User submits a health question
2. Safety filter validates the query
3. If safe, the Agent processes the question using Gemini LLM
4. Response is displayed with chat history maintained in session state
5. All interactions are logged for the current session

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
git clone https://github.com/moizahmedx/General-Health-Assistant

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

### Safe Queries (Will Get Helpful Responses)
- "What causes a sore throat?"
- "What are symptoms of flu?"
- "How to improve immunity?"
- "Is headache caused by dehydration?"
- "What is common cold?"
- "How much water should I drink daily?"
- "What foods boost immune system?"
- "How to prevent seasonal allergies?"

### Filtered Queries (Will Trigger Safety Warning)
- Questions containing emergency keywords
- Self-harm related queries
- Requests for specific medication dosages
- Diagnostic requests for serious conditions

## 🧪 Technical Implementation Details

### Dependencies
- **streamlit**: Web UI framework for interactive chat interface
- **openai-agents**: Agent SDK for structured LLM interactions
- **python-dotenv**: Secure environment variable management
- **dotenv**: Additional environment configuration support

### API Integration
The project uses Gemini's OpenAI-compatible endpoint:
```python
base_url="https://generativelanguage.googleapis.com/v1beta/openai/"
model="gemini-2.5-flash"
```

### Error Handling
- Try-catch blocks around Agent execution
- Graceful error messages for API failures
- Environment variable validation
- Connection timeout handling

### Session Management
Streamlit's `session_state` maintains:
- Complete chat history
- User and assistant messages
- Conversation context across interactions

---

## ⚠️ Safety & Limitations

### What This Chatbot Does
✅ Provides general health information  
✅ Explains common symptoms and causes  
✅ Suggests preventive care tips  
✅ Recommends healthy lifestyle habits  
✅ Answers questions about nutrition and wellness  

### What This Chatbot Does NOT Do
❌ Diagnose medical conditions  
❌ Prescribe medications or dosages  
❌ Replace professional medical advice  
❌ Handle emergency situations  
❌ Provide treatment plans  

### Safety Mechanisms
- **Keyword Filtering**: Detects dangerous queries before LLM processing
- **Clear Disclaimers**: Agent instructions explicitly prevent diagnosis/prescription
- **Emergency Redirection**: Harmful queries return: "⚠️ This may require immediate medical attention. Please contact a doctor."
- **Scope Limitation**: Responses focus on general information only

## 🚀 Future Enhancements

Potential improvements for this project:
- Add multi-language support
- Implement conversation memory across sessions (database integration)
- Add source citations for health information
- Integrate with health APIs for real-time data
- Implement user authentication
- Add analytics dashboard for query patterns
- Enhanced safety filter using ML-based classification
- Voice input/output capabilities

---

## 👩‍💻 Author
Moiz Ahmed  
AI Engineer | Agentic AI Developer | Python Developer
