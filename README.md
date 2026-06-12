# Dive Into LangChain

Hands-on exploration repo for learning how to build with LLMs using LangChain and related AI tooling.

This project is a practical notebook-first sandbox where I experiment with:
- chat models
- agents
- tools and tool calling
- message abstractions
- streaming and batch patterns
- local models with Ollama
- multiple providers through a common LangChain interface

## What This Repo Is

This is a learning and experimentation workspace, not a production application.

The goal is to understand concepts by building small, focused examples and keeping notes in notebooks.

## Tech Stack

- Python 3.14 (see `.python-version`)
- LangChain ecosystem:
  - `langchain`
  - `langchain-community`
  - `langchain-openai`
  - `langchain-groq`
  - `langchain-google-genai`
  - `langchain-ollama`
- `python-dotenv` for environment variables
- Jupyter (`ipykernel`) for notebook workflows

## Project Structure

```text
.
├── main.py
├── pyproject.toml
├── requirements.txt
├── uv.lock
└── notebooks
	 ├── _how _to_setup
	 │   └── 001_python_and_env_setup.ipynb
	 └── langchain
		  ├── 01_langchain_takeaways_summary.ipynb
		  └── practise dump
				├── 1_langchain_agent.ipynb
				├── 2_langchain_chat_model.ipynb
				├── 3_streaming_and_batch.ipynb
				├── 4_tools_creation.ipynb
				├── 5_tools_with_ollama.ipynb
				└── 6_messages.ipynb
```

## Notebook Roadmap

1. `notebooks/_how _to_setup/001_python_and_env_setup.ipynb`
	Environment setup and initial Python/Jupyter workflow.
2. `notebooks/langchain/01_langchain_takeaways_summary.ipynb`
	Consolidated notes and key learnings.
3. `notebooks/langchain/practise dump/1_langchain_agent.ipynb`
	Agent basics and orchestration flow.
4. `notebooks/langchain/practise dump/2_langchain_chat_model.ipynb`
	Chat model usage patterns.
5. `notebooks/langchain/practise dump/3_streaming_and_batch.ipynb`
	Streaming responses and batch invocation.
6. `notebooks/langchain/practise dump/4_tools_creation.ipynb`
	Creating custom tools for agent/tool-calling workflows.
7. `notebooks/langchain/practise dump/5_tools_with_ollama.ipynb`
	Using tools with local LLMs via Ollama.
8. `notebooks/langchain/practise dump/6_messages.ipynb`
	Message abstractions and conversation structuring.

## Setup

### Option A: Using `uv` (recommended)

```bash
uv sync
source .venv/bin/activate
```

### Option B: Using `pip`

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pip install ipykernel
```

## Environment Variables

Create a `.env` file in the repo root (already gitignored).

Add only the keys you need for the provider(s) you are testing:

```env
OPENAI_API_KEY=...
GROQ_API_KEY=...
GOOGLE_API_KEY=...
```

For local models, ensure Ollama is installed and running, then pull a model:

```bash
ollama pull llama3
```

## Running Notebooks

```bash
jupyter notebook
```

Then open the notebooks in the order above, or directly in VS Code with the Python/Jupyter extensions.

## Running Python Script

`main.py` is currently a minimal placeholder script.

```bash
python main.py
```

## Learning Goals

- Build intuition for LangChain primitives (models, prompts, messages, tools, agents).
- Compare hosted and local model workflows.
- Practice reproducible LLM experiments using notebooks.
- Capture practical takeaways after each experiment.

## Notes

- This repo is intentionally notebook-heavy.
- Naming in some folders/files (for example, `practise dump`) is kept as-is to preserve learning history.
- `pyproject.toml` currently uses project name `tpb-rag-course-followup`; it can be renamed later if you want full alignment with this repo name.
