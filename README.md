# 💵💱💶 Currency Agent (ADK + MCP)

## Overview

This project demonstrates how to use **ADK Web** and **MCP** to build a currency conversion agent. It allows users to convert between different currencies using a modular and standardized architecture.

The MCP server in this example exposes a `get_exchange_rate` tool, which uses the [Frankfurter](https://www.frankfurter.dev/) API to fetch currency exchange rates. The agent uses an MCP client to invoke this tool as needed.

> **ADK** (Agent Development Kit) is a flexible and modular framework for developing and deploying AI agents. While optimized for Gemini and the Google ecosystem, ADK is model-agnostic, deployment-agnostic, and designed for compatibility with other frameworks. — [ADK](https://github.com/google/adk-python)

In this example, **ADK Web** is used as the orchestration framework for creating the currency agent. It handles user conversations and invokes the MCP tool when required.

---

## Getting Started

### Prerequisites

- Python 3.10+
- Git

### Installation

1. Clone the repository:

```bash
git clone https://github.com/aymen20002005/currency-agent.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Configure environment variables (via `.env` file):

Gemini API Key

1. Get an API key: [Google AI Studio](https://aistudio.google.com/apikey)
2. Create a `.env` file:

```bash
echo "GOOGLE_API_KEY=<your_api_key_here>" >> .env
echo "GOOGLE_GENAI_USE_VERTEXAI=FALSE" >> .env
```

## Local Deployment

### MCP Server

In a terminal, start the MCP server (runs on port 8080):

```bash
python mcp-server/server.py
```

### ADK Web Agent

In another terminal, start the ADK web agent and chose the currency-agent:

```bash
adk web
```
