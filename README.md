
````markdown
#  AI Trip Planner — Agentic Travel Assistant

###  Overview  
The **AI Trip Planner** is an intelligent, agent-based travel planning assistant that generates personalized itineraries based on user preferences, duration, and budget.  
Built with **FastAPI** (backend), **Streamlit** (frontend), and **Groq/OpenAI LLMs**, it demonstrates the full pipeline of a **Generative AI application** — from user prompt → reasoning agent → data tools → real-time itinerary response.

### project 
This project was built to showcase how Generative AI and agentic systems can transform real-world problem-solving — in this case, travel planning. I wanted to demonstrate how a reasoning LLM can analyze user intent (“Plan a 5-day trip to Goa”) and dynamically generate a detailed, data-driven itinerary.
The goal was to design a complete AI product pipeline — from frontend user interaction (Streamlit), to backend orchestration (FastAPI), to LLM reasoning (Groq / OpenAI), and external API integrations (Maps, Weather).
Through this project, I focused on multi-agent design thinking, prompt engineering, and AI tool integration, aiming to prove that AI systems can move beyond text — towards building personalized, context-aware experiences that feel human and practical.
---

##  Features
 **Conversational AI Interface:** Users can ask natural-language questions like *“Plan a 5-day trip to Goa under $1000”*.  
 **Dynamic Itinerary Generation:** The agent constructs daily schedules with destinations, activities, and estimated costs.  
 **Tool Integration:** Connects with external APIs (e.g., Maps, Weather, Places) to enrich trip data.  
 **Dual-Mode System:** Runs as both a **FastAPI backend** and an interactive **Streamlit web app**.  
 **Agentic Architecture:** Modular LLM + tools + prompt libraries for reasoning, context, and execution.  
 **Environment-Based Secrets:** `.env` file used for API keys and configuration isolation.  

---

##  Architecture

```text
 ┌──────────────────────────────┐
 │         Streamlit UI         │  ← User enters destination, duration, budget
 └──────────────┬───────────────┘
                │
                ▼
       ┌────────────────────┐
       │     FastAPI API     │  ← Receives request, invokes AI agent
       └────────┬────────────┘
                │
                ▼
 ┌────────────────────────────────────────┐
 │    AI Agent (LLM + Tools + Prompts)    │  ← Core reasoning engine
 │  • LLM: Groq / OpenAI / Gemini         │
 │  • Tools: Maps, Weather, Cost Estimator│
 │  • Prompt Library: Travel Contexts     │
 └────────────────────────────────────────┘
                │
                ▼
      Returns structured itinerary
````

---

##  Tech Stack

| Layer            | Tools / Libraries                          | Description                     |
| ---------------- | ------------------------------------------ | ------------------------------- |
| **Frontend**     | Streamlit                                  | Interactive chat-like web UI    |
| **Backend**      | FastAPI, Uvicorn                           | REST API serving the AI agent   |
| **LLMs**         | Groq (LLaMA-3.3), OpenAI (GPT-4o optional) | Generative reasoning engine     |
| **Environment**  | Python 3.9+ with `.env`                    | Local secrets and configuration |
| **Dependencies** | LangChain, Requests, dotenv                | AI orchestration and API access |

---

##  Setup Instructions

### 1️ Clone the repository

```bash
git clone https://github.com/<yourusername>/AI_Trip_Planner.git
cd AI_Trip_Planner
```

### 2️ Create and activate a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate       # macOS / Linux
# .venv\Scripts\activate        # Windows
```

### 3️ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️ Configure environment variables

Create a file named `.env` in the root directory:

```bash
OPENAI_API_KEY=your_openai_api_key_here
GROQ_API_KEY=your_groq_api_key_here
GROQ_MODEL=llama-3.3-70b-versatile
GOOGLE_MAPS_API_KEY=your_google_maps_api_key_here
```

>  Never commit `.env` to GitHub. Your API keys must remain private.

---

### 5️ Run the backend (FastAPI)

```bash
uvicorn main:app --reload --port 8000
```

This starts the API at **[http://127.0.0.1:8000](http://127.0.0.1:8000)**

### 6️ Run the frontend (Streamlit)

Open a new terminal window (keep backend running):

```bash
streamlit run streamlit_app.py
```

Then visit [http://localhost:8501](http://localhost:8501)

---

##  Example Prompt

```
Plan a 5-day trip to new york .
```

### 🧾 Example Output


https://github.com/user-attachments/assets/e5a51d26-abd5-4c83-a0d1-0f1586e39435



---

## 🧱 Project Structure

```bash
AI_Trip_Planner/
│
├── main.py                 # FastAPI backend
├── streamlit_app.py        # Streamlit web UI
│
├── agent/                  # AI agent logic
│   ├── agent_executor.py
│   ├── tools/
│   └── prompt_library/
│
├── utils/                  # Helper utilities
├── logger/                 # Logging config
├── requirements.txt
├── pyproject.toml
├── .env.example
└── README.md
```

---



# This project demonstrates:

* **End-to-end GenAI product development**
* **Agentic architecture design** with modular reasoning
* **Integration of external APIs** and dynamic prompt engineering
* **Frontend-backend orchestration** using Streamlit and FastAPI
* **Environment management, reproducibility, and security best practices**

It can serve as both a **portfolio project** and a **baseline for real travel-tech prototypes** (e.g., integrating live bookings, hotel APIs, or AR/VR previews).

---





## � Author

**Abhinav Sanjay Yellina**
 Master’s in Business Analytics | University at Albany, SUNY
 Focus: Generative AI • Agentic Systems • AI Infrastructure
 [LinkedIn](https://linkedin.com/in/abhinav-yellina) | [GitHub](https://github.com/yourusername)




