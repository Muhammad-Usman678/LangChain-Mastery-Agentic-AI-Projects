# LangChain Mastery: Agentic AI Projects

![Python](https://img.shields.io/badge/Python-3.12+-blue.svg)
![LangChain](https://img.shields.io/badge/LangChain-v0.3-green.svg)
![OpenAI](https://img.shields.io/badge/Provider-OpenAI-412991.svg)
![Gemini](https://img.shields.io/badge/Provider-Google%20Gemini-8E75B2.svg)
![Groq](https://img.shields.io/badge/Provider-Groq-F55036.svg)

## Overview

This repository is a hands-on journey into **Agentic AI** using LangChain.

Instead of focusing only on theory, this project is designed around **practical, progressive notebooks** that demonstrate how real-world AI agents are built, from simple model invocation to advanced agentic systems with tools, structured outputs, and human-in-the-loop control.

If you’re moving from *prompting LLMs* to *building reliable and controllable AI agents*, this repository is built for you.

---

## Notebook Walkthrough

### 1. LangChain Introduction
**Start here.**

Learn the fundamentals of LangChain and build your first AI agent.
- Environment setup using `dotenv`
- Version checks and configuration
- Basic agent creation
- Mini demo: a simple weather assistant ☀️

---

### 2. Model Integration
Work with multiple LLM providers through a single, consistent interface.
- OpenAI: `gpt-4.1-mini`
- Google Gemini: `gemini-2.5-flash-lite`
- Groq: `qwen/qwen3-32b`

**Focus:** Vendor-agnostic agent design.

---

### 3. Custom Tools
Give your agents the ability to interact with external systems.
- Creating tools using the `@tool` decorator
- Binding tools to models
- Allowing the model to decide when to invoke tools
- Example: a custom `get_weather` tool

---

### 4. Message Management
Understand how agent conversations are structured and maintained.
- `SystemMessage`, `HumanMessage`, `AIMessage`, `ToolMessage`
- Manual construction of conversation history
- Handling complex multi-turn interactions

---

### 5. Structured Output
Turn unpredictable text into reliable, machine-readable data.
- Enforcing schemas with Pydantic, TypedDict, and Dataclasses
- Using `with_structured_output` for deterministic outputs
- Example: extracting structured movie data 🎬

---

### 6. Middleware & Advanced Control
Explore production-inspired agent patterns.
- **Summarization Middleware**  
  Automatically condense old messages to manage context size and token usage
- **Human-in-the-Loop Middleware**  
  Review, approve, edit, or reject tool calls before execution

---

## Quick Start

This project manages dependencies using `uv` for speed and reliability.

1.  **Clone the repo**
2.  **Install Dependencies**
    ```bash
    uv sync
    # Or strict pip:
    # pip install -r requirements.txt
    ```
3.  **Configure Environment**
    Create a `.env` file with your API keys:
    ```env
    OPENAI_API_KEY=sk-...
    GOOGLE_API_KEY=AIza...
    GROQ_API_KEY=gsk_...
    ```
4.  **Explore!**
    Launch Jupyter Lab or Notebook to run the tutorials:
    ```bash
    jupyter lab
    ```

##  Features

*   **Multi-Provider Support**: Switch between models instantly.
*   **Robust Typing**: Heavy use of Python type hints and Pydantic.
*   **Stateful Agents**: Examples using LangGraph checkpoints (`InMemorySaver`).
*   **Production Ready Patterns**: Middleware for token management and human review.

---



