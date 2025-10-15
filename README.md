Absolutely 👍 — here’s your **copy-paste-ready README.md** (you can drop this directly into your GitHub repo).
Everything is formatted with Markdown headings, emojis, and spacing tuned for GitHub rendering.

---

````markdown
# 🌍 AI Trip Planner — Agentic Travel Assistant

### ✨ Overview  
The **AI Trip Planner** is an intelligent, agent-based travel planning assistant that generates personalized itineraries based on user preferences, duration, and budget.  
Built with **FastAPI** (backend), **Streamlit** (frontend), and **Groq/OpenAI LLMs**, it demonstrates the full pipeline of a **Generative AI application** — from user prompt → reasoning agent → data tools → real-time itinerary response.

---

## 🚀 Features
✅ **Conversational AI Interface:** Users can ask natural-language questions like *“Plan a 5-day trip to Goa under $1000”*.  
✅ **Dynamic Itinerary Generation:** The agent constructs daily schedules with destinations, activities, and estimated costs.  
✅ **Tool Integration:** Connects with external APIs (e.g., Maps, Weather, Places) to enrich trip data.  
✅ **Dual-Mode System:** Runs as both a **FastAPI backend** and an interactive **Streamlit web app**.  
✅ **Agentic Architecture:** Modular LLM + tools + prompt libraries for reasoning, context, and execution.  
✅ **Environment-Based Secrets:** `.env` file used for API keys and configuration isolation.  

---

## 🧠 Architecture

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

## ⚙️ Tech Stack

| Layer            | Tools / Libraries                          | Description                     |
| ---------------- | ------------------------------------------ | ------------------------------- |
| **Frontend**     | Streamlit                                  | Interactive chat-like web UI    |
| **Backend**      | FastAPI, Uvicorn                           | REST API serving the AI agent   |
| **LLMs**         | Groq (LLaMA-3.3), OpenAI (GPT-4o optional) | Generative reasoning engine     |
| **Environment**  | Python 3.9+ with `.env`                    | Local secrets and configuration |
| **Dependencies** | LangChain, Requests, dotenv                | AI orchestration and API access |

---

## 🧩 Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/<yourusername>/AI_Trip_Planner.git
cd AI_Trip_Planner
```

### 2️⃣ Create and activate a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate       # macOS / Linux
# .venv\Scripts\activate        # Windows
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Configure environment variables

Create a file named `.env` in the root directory:

```bash
OPENAI_API_KEY=your_openai_api_key_here
GROQ_API_KEY=your_groq_api_key_here
GROQ_MODEL=llama-3.3-70b-versatile
GOOGLE_MAPS_API_KEY=your_google_maps_api_key_here
```

> ⚠️ Never commit `.env` to GitHub. Your API keys must remain private.

---

### 5️⃣ Run the backend (FastAPI)

```bash
uvicorn main:app --reload --port 8000
```

This starts the API at **[http://127.0.0.1:8000](http://127.0.0.1:8000)**

### 6️⃣ Run the frontend (Streamlit)

Open a new terminal window (keep backend running):

```bash
streamlit run streamlit_app.py
```

Then visit [http://localhost:8501](http://localhost:8501)

---

## 🧭 Example Prompt

```
Plan a 5-day trip to Switzerland focused on scenic train routes and mountain hiking.
```

### 🧾 Example Output

> **Day 1:** Zurich arrival — explore Old Town & Rhine Falls
> **Day 2:** GoldenPass train to Interlaken — lake cruise & Harder Kulm sunset
> **Day 3:** Jungfrau region hiking — Grindelwald, First Cliff Walk
> **Day 4:** Zermatt — Gornergrat cogwheel, Matterhorn view
> **Day 5:** Glacier Express to St. Moritz, spa evening

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

## 🧑‍💻 For Recruiters / Interviewers

This project demonstrates:

* **End-to-end GenAI product development**
* **Agentic architecture design** with modular reasoning
* **Integration of external APIs** and dynamic prompt engineering
* **Frontend-backend orchestration** using Streamlit and FastAPI
* **Environment management, reproducibility, and security best practices**

It can serve as both a **portfolio project** and a **baseline for real travel-tech prototypes** (e.g., integrating live bookings, hotel APIs, or AR/VR previews).

---

## 🛠️ Troubleshooting

| Problem                       | Cause                                     | Solution                                             |
| ----------------------------- | ----------------------------------------- | ---------------------------------------------------- |
| `Model decommissioned`        | Old Groq model deprecated                 | Update `.env` → `GROQ_MODEL=llama-3.3-70b-versatile` |
| `Bot failed to respond (400)` | Invalid key or API mismatch               | Check your `.env` keys                               |
| `CORS error`                  | Streamlit & FastAPI running on diff ports | Allow origins in FastAPI middleware                  |
| `No module named 'streamlit'` | Dependencies missing                      | Run `pip install -r requirements.txt`                |

---

## 📜 License

This repository is released under the **MIT License**.
Feel free to fork, modify, or extend for learning and showcase purposes.

---

## 💡 Author

**Abhinav Sanjay Yellina**
🎓 Master’s in Business Analytics | University at Albany, SUNY
💼 Focus: Generative AI • Agentic Systems • AI Infrastructure
🔗 [LinkedIn](https://linkedin.com/in/abhinav-yellina) | [GitHub](https://github.com/yourusername)

```

---

Would you like me to add a **short “Project Story” paragraph** next (2-3 lines that make it sound more personal and impactful for hiring managers — e.g., why you built it, what problem it solves, and what you learned)?  
It helps your README stand out in your portfolio.
```
