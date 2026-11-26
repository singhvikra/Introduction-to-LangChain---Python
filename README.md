# Introduction to LangChain - Python

Coursework and experiments for the free [LangChain Academy](https://academy.langchain.com/) course
[Introduction to LangChain - Python](https://academy.langchain.com/courses/foundation-introduction-to-langchain-python).

This is weeks 1-2 of my 2-month AI engineering plan. The mini-project at the end becomes the
starting point for the capstone.

## Focus areas

- Structured outputs with Pydantic schemas
- Tool calling and the agent loop
- Memory and conversation state
- Middleware and human-in-the-loop
- Error handling for failed tools and bad model output
- Tracing every run in LangSmith

## Setup

Requires [uv](https://docs.astral.sh/uv/).

```powershell
uv sync                      # create .venv and install dependencies
.venv\Scripts\Activate.ps1   # optional: activate the virtual environment
```

Add packages with uv instead of pip:

```powershell
uv add langchain langgraph python-dotenv
uv add langchain-openai      # or the package for your model provider
```

Create a `.env` file (ignored by git) for API keys:

```
OPENAI_API_KEY=...
LANGSMITH_API_KEY=...
LANGSMITH_TRACING=true
LANGSMITH_PROJECT=intro-to-langchain
```

Run code with `uv run`:

```powershell
uv run python path\to\script.py
```

## Mini-project

A FastAPI endpoint backed by an agent with two tools (for example, a calculator and a mock
ticket lookup). It returns a structured response, and every run is traced in LangSmith.

## Notes

After each module, record two sentences on what problem the feature solves.
