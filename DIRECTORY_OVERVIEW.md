# Repository Directory Overview

Quick map of the codebase and the kinds of skills you can practice in each area.

## Root
- `README.md` – course summary and learning goals for the Agentic AI hands-on material.
- `requirements.txt` – consolidated Python dependencies covering the demonstrations (FastAPI, CrewAI, smolagents, Streamlit, Google Gemini SDKs, etc.).
- `Agentic AI_Consolidated PPT.pdf` – slide deck that accompanies the repository.
- `LICENSE` – distribution terms for the materials.

## Section 3 - Foundation of Agentic AI
- `weather_agent.py` – bare-bones Gemini + OpenWeatherMap agent that extracts a city from free text and replies conversationally. Good for learning LLM prompting, simple tool use, and request/response loops.
- `aws-agent/` – Flask UI that uses Gemini to decide on EC2 creation and executes it with Boto3. Teaches intent parsing, JSON hand-off between model and code, and basic AWS automation wiring.
- `README.md` – project briefs and flow diagrams for the foundation exercises.

## Section 4 - Developing Agentic AI Systems
- `calculate.py` – minimal Smolagents example that runs a CodeAgent for a simple computation.
- `weather_smolagent.py` – Smolagents demo using `WebSearchTool` to answer weather questions, illustrating agent tool use and streaming outputs.
- `sql_agent.ipynb` – notebook for a text-to-SQL agent with custom tool design and self-correction.
- `n8n-low-code-agent.md` – walkthrough for building a chat-style news agent in the n8n low-code platform.
- `README.md` – descriptions and diagrams tying together the Smolagents and low-code exercises.

## Section 5 - Getting started with MCP
- `mcp_weather_server.py` – FastAPI-based minimal MCP-style JSON-RPC server exposing discovery and `get_weather` tools with in-memory data. Useful for understanding protocol shape and server scaffolding.
- `mcp_client_ui.py` – lightweight client script that discovers tools and calls the MCP server for weather data.
- `agent_client_app.py` – FastAPI app that uses Gemini to extract a city, calls the MCP weather tool, and renders responses via an HTML form. Highlights coupling an LLM agent to MCP backends.
- `README.md` – conceptual overview and diagrams for the MCP projects.

## Section 6 - Introduction to Multi-Agent Systems
- `Multi-Agent-1/` – two-agent CrewAI demo (research + writer) with SerperDevTool for web search; produces a markdown report. Good entry point for agent roles and task handoff.
- `Multi-Agent-2/` – sequential CrewAI flow for customer support analysis with custom data-fetch tool; shows modular separation of agents, tasks, and tools.
- `Multi-Agent-3/` – AWS monitoring crew where one agent gathers EC2 status via a custom tool and another produces a strict cost report. Focus on deterministic outputs and guardrails.
- `Multi-Agent-4/` – multi-cloud crew combining AWS and GCP collectors, an analyst generating HTML, and an email sender. Demonstrates multi-agent A2A context passing and cross-cloud tooling.
- `n8n-multi-agent.md` – notes on orchestrating similar flows in n8n.
- `README.md` – section-level summaries and diagrams for the multi-agent projects.

## Section 7 - RAG-Enhanced Agents
- `RAG_agent.py` – Streamlit file-Q&A chatbot using Gemini; lets you upload text/markdown and ask grounded questions. Practice building simple RAG UIs.
- `AgenticRAG/` – CrewAI-based RAG pipeline with a custom text tool and two agents (retriever/responder) over a local knowledge file; shows agent collaboration on retrieval and answer synthesis.
- `AgenticRAG-2/` – feasibility analyzer that uploads company PDFs to Gemini, scrapes client URLs, and uses an agent to decide project viability. Includes Streamlit frontend (`app.py`) and backend helpers.
- `Course_Agent_RAG.py` – terminal agent that ingests course PDFs into Gemini and answers with citations (file + page). Good for experimenting with Gemini file API and interactive loops.
- `README.md` – narratives and diagrams for the RAG-focused projects.
