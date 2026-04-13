# # AI Agent Routing System

## 📌 Description

This project implements an AI-based routing assistant that processes user input, determines intent, and routes requests to appropriate tools.

The system demonstrates key concepts in LLM-based architecture, including:

* Intent recognition
* Tool routing
* Structured data handling
* Persistent conversation memory

---

## ⚙️ Features

### 🔹 Tools

* **Weather API** – get real-time weather data
* **Currency Exchange API** – retrieve exchange rates
* **Math Calculator** – deterministic calculation (no LLM)
* **General Chat** – fallback LLM conversation

### 🔹 Smart Routing

The system uses a dedicated system prompt to decide:

* which tool to use
* what parameters to extract

### 🔹 Memory (Persistence)

* Conversation is stored in `history.json`
* Automatically loaded on startup
* Supports `/reset` command

---

## 🧠 Architecture

User Input → Router (LLM) → Tool Selection → Tool Execution → Response

---

## 🚀 Setup

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file:

```
OPENAI_API_KEY=your_key
WEATHERAPI_KEY=your_key
EXCHANGE_RATE_API_KEY=your_key
```

---

## ▶️ Run

Open the notebook:

```
first_project.ipynb
```

Run all cells and start interacting with the system.

---

## 💬 Example Queries

* "What's the weather in Tel Aviv?"
* "How much is USD in ILS?"
* "Calculate 150 + 20"
* "How many euros can I buy with 100 dollars?"

---

## 🗂 Project Structure

```
AI_Agent_task/
│
├── first_project.ipynb
├── history.json
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🧪 Persistence Test

* Restart program → history is loaded
* Use `/reset` → history is cleared

---

## 📚 Technologies

* Python
* OpenAI API
* REST APIs
* JSON storage



