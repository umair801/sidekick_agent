---
title: Sidekick Agent
emoji: 🤖
colorFrom: green
colorTo: blue
sdk: gradio
sdk_version: "4.44.0"
app_file: app.py
pinned: false
python_version: "3.11"
---

# 🤖 Sidekick: Autonomous AI Agent

**An intelligent AI co-worker that autonomously completes tasks using web browsing, code execution, and self-evaluation loops.**

🚀 **Live Demo:** [huggingface.co/spaces/umair801/sidekick-agent](https://huggingface.co/spaces/umair801/sidekick-agent)

---

## 🎯 Key Features

- **Autonomous Task Completion** with built-in self-evaluation loop
- **Web Automation** via Playwright browser control
- **Code Execution** in sandboxed Python environment
- **Smart Retry Logic** based on user-defined success criteria
- **Multi-Tool Integration:** Web search, Wikipedia, File I/O, Push notifications

---

## 🏗️ Architecture

Built with **LangGraph + LangChain + GPT-4o-mini** using a Worker-Evaluator pattern:

```
User Input
    ↓
[Worker Agent] → uses tools → produces response
    ↓
[Evaluator Agent] → checks against success criteria
    ↓
Pass → Return to user
Fail → Feedback loop back to Worker
```

- Stateful conversation with memory persistence (MemorySaver)
- Conditional edge routing in LangGraph
- Async Playwright browser for live web interaction

---

## 💡 Use Cases

- Automated research and data collection from the web
- Multi-step workflow automation
- Report generation from live web sources
- Code execution and analysis tasks

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Orchestration | LangGraph |
| LLM | GPT-4o-mini (OpenAI) |
| Web Automation | Playwright (Chromium) |
| Search | Google Serper API |
| UI | Gradio |
| Language | Python 3.11 |

---

## ⚙️ Environment Variables

To run locally, create a `.env` file with:

```
OPENAI_API_KEY=your_key
SERPER_API_KEY=your_key
PUSHOVER_USER_KEY=your_key
PUSHOVER_API_TOKEN=your_key
```

---

## 🚀 Run Locally

```bash
git clone https://github.com/umair801/sidekick_agent.git
cd sidekick_agent
pip install -r requirements.txt
playwright install chromium
python app.py
```

---

*Built by [Muhammad Umair](https://datawebify.com) — Agentic AI Consultant*
