# 🚀 First AI Agent: From Prompt to Action

This repository contains my **first AI Agent built using Google’s Agent Development Kit (ADK)**

The project walks through the full journey from **setting up the environment**, to **authenticating with Gemini**, to **building and running an agent that can take actions** (like Google Search) instead of only returning text.

---

## 🧠 What This Project Demonstrates

Traditional LLM usage looks like this:

```
Prompt → LLM → Text
```

An **AI Agent** goes further:

```
Prompt → Agent → Thought → Action → Observation → Final Answer
```

In this notebook, the agent:

* Uses **Gemini** as its reasoning model
* Decides **when it needs external information**
* Calls **Google Search** as a tool
* Uses the result to generate a better answer

---

## ✅ What’s Included

* ✅ Environment setup in **Kaggle Notebooks**
* ✅ Secure **Gemini API key configuration** using Kaggle Secrets
* ✅ A **simple ADK agent** powered by `gemini-2.5-flash-lite`
* ✅ Tool usage with **Google Search**
* ✅ Running and debugging the agent with an **InMemoryRunner**
* ✅ Launching and exploring the **ADK Web UI**

---

## ⚙️ Setup & Requirements

### Environment

This project is designed to run inside **Kaggle Notebooks**.

> The Kaggle environment already includes:

* `google-adk`
* Required Gemini dependencies
  So **no additional installations are required**.

---

## 🔑 Gemini API Key Configuration

To authenticate with Gemini:

1. **Create an API key**

   * Get one from **Google AI Studio**

2. **Add it to Kaggle Secrets**

   * Open your notebook
   * Go to **Add-ons → Secrets**
   * Create a secret named:

     ```
     GOOGLE_API_KEY
     ```
   * Paste your API key and save
   * Make sure the secret is **enabled for the notebook**

3. **Authenticate in the notebook**

   * The notebook retrieves the secret and sets it as an environment variable
   * Gemini will automatically read it from `GOOGLE_API_KEY`

---

## 📦 Key Components Used

### Agent Development Kit (ADK)

* `Agent` – defines behavior, instructions, tools, and model
* `InMemoryRunner` – runs the agent locally in memory (great for prototyping)
* `google_search` – built-in tool for real-time information retrieval

### Gemini Model

* **Model:** `gemini-2.5-flash-lite`
* Used for fast, cost-efficient reasoning

---

## 🤖 Defining the Agent

The agent is configured with:

* A name and description
* A guiding instruction
* Access to the Google Search tool

Example behavior:

> *“Use Google Search for current information or if unsure.”*

This allows the agent to **decide when to act**, not just respond.

---

## ▶️ Running the Agent

The agent is executed using:

* `InMemoryRunner` for quick experimentation
* `run_debug()` to see responses without managing sessions manually

Example queries:

* *What is Agent Development Kit from Google?*
* *What’s the weather in London?*
* *Who won the last soccer World Cup?*

---

## 🌐 ADK Web UI

ADK also provides a **built-in web interface** for:

* Interactive chatting
* Debugging agent behavior
* Inspecting thoughts, actions, and tool calls

In this project:

* A sample agent is generated using `adk create`
* The web UI is launched inside Kaggle using a **secure proxy URL**

---

## 🏁 Final Note

This project marks the transition from **prompting models** to **building agents that think, act, and observe**.
