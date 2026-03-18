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

An intelligent AI co-worker that autonomously completes tasks using web browsing, code execution, and self-evaluation loops.

## 🎯 Key Features
- **Autonomous Task Completion** with self-evaluation
- **Web Automation** via Playwright browser control
- **Code Execution** in sandboxed Python environment
- **Smart Retry Logic** based on success criteria
- **Multi-Tool Integration** (Search, Wikipedia, File Ops)

## 🏗️ Architecture
Built with LangGraph + LangChain + GPT-4o-mini
- Worker-Evaluator pattern with feedback loops
- Stateful conversation with memory persistence
- Tool routing with conditional edges

## 💡 Use Cases
- Automated research & data collection
- Web scraping with validation
- Multi-step workflow automation
- Report generation from web sources

## 🚀 Demo
[Live Demo Link]

## 🛠️ Tech Stack
`Python` `LangGraph` `LangChain` `Gradio` `Playwright` `OpenAI`
