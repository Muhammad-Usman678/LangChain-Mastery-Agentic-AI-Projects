# LangChain Mastery: A Comprehensive Learning Journey

![Python](https://img.shields.io/badge/Python-3.12+-blue.svg)
![LangChain](https://img.shields.io/badge/LangChain-v0.3-green.svg)
![OpenAI](https://img.shields.io/badge/Provider-OpenAI-412991.svg)
![Gemini](https://img.shields.io/badge/Provider-Google%20Gemini-8E75B2.svg)
![Groq](https://img.shields.io/badge/Provider-Groq-F55036.svg)

## Overview

Welcome to the **LangChain Learning** repository! This project serves as a hands-on guide to mastering [LangChain](https://python.langchain.com/), the framework for building context-aware reasoning applications. 

Through a series of progressive notebooks, we explore everything from basic model invocation to complex agentic architectures with human-in-the-loop capabilities.

## Notebooks Breakdown

### 1. [LangChain Introduction](./1-langchainintro.ipynb)
**Start Here!** A primer on setting up your environment and building your first Agent.
*   **Key Concepts**: Environment setup (`dotenv`), Version checks, Basic Agent creation using `create_agent`.
*   **Highlight**: Creating a weather assistant that knows it's sunny in New York! ☀️

### 2. [Model Integration](./2-modelintegration.ipynb)
Unlock the power of choice by integrating multiple LLM providers.
*   **Models Covered**: 
    *   **OpenAI**: `gpt-4.1-mini`
    *   **Google**: `gemini-2.5-flash-lite`
    *   **Groq**: `qwen/qwen3-32b`
*   **Learnings**: Unified API for invoking models from different vendors.

### 3. [Custom Tools](./3-tools.ipynb)
Empower your agents to interact with the real world.
*   **Key Concepts**: Using the `@tool` decorator, binding tools to models, and parsing tool calls.
*   **Demo**: A custom `get_weather` tool that the model learns to call when asked about the forecast.

### 4. [Message Management](./4-messages.ipynb)
Deep dive into the conversational state.
*   **Components**: `SystemMessage`, `HumanMessage`, `AIMessage`, `ToolMessage`.
*   **Learnings**: How to manually construct conversation history and handle sophisticated multi-turn dialogues.

### 5. [Structured Output](./5-structuredoutput.ipynb)
Tame output indeterminacy with strict schemas.
*   **Tech Stack**: Pydantic, TypedDict, Dataclasses.
*   **Feature**: `with_structured_output` ensures your LLM replies with valid JSON/Objects every time—perfect for data extraction tasks like pulling Movie details! 🎬

### 6. [Middleware & Advanced Control](./6-middleware.ipynb)
Take total control of your Agent's lifecycle.
*   **SummarizationMiddleware**: Automatically summarize old messages to manage context window limits and save tokens.
*   **HumanInTheLoopMiddleware**: The ultimate safety net. Intercept, review, approve, edit, or reject tool calls before they execute.

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

