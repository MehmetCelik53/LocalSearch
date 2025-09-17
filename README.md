# LocalSearch

A local search implementation with graph-based indexing and LM Studio integration for AI-powered research assistance.

## Features

- **Multiple Search APIs**: Support for Tavily, DuckDuckGo, SearXNG, and Perplexity
- **LM Studio Integration**: Local LLM support via LM Studio's OpenAI-compatible API
- **Ollama Support**: Alternative local LLM provider
- **Graph-based Processing**: Uses LangGraph for structured research workflows
- **Configurable Research Depth**: Adjustable research iteration loops
- **Full Page Content**: Optional full page content fetching for comprehensive research

## Requirements

- Python 3.11+
- LM Studio or Ollama for local LLM inference
- API keys for external search services (optional)

## Configuration

The system supports multiple configuration options through environment variables:

- `MAX_WEB_RESEARCH_LOOPS`: Number of research iterations (default: 3)
- `LOCAL_LLM`: LLM model name (default: "llama3.2")
- `LLM_PROVIDER`: "ollama" or "lmstudio" (default: "ollama")
- `SEARCH_API`: "perplexity", "tavily", "duckduckgo", or "searxng" (default: "duckduckgo")
- `FETCH_FULL_PAGE`: Include full page content (default: True)
- `OLLAMA_BASE_URL`: Ollama API endpoint (default: "http://localhost:11434/")
- `LMSTUDIO_BASE_URL`: LM Studio API endpoint (default: "http://localhost:1234/v1")

## Installation

1. Clone this repository
2. Install dependencies (requirements.txt coming soon)
3. Set up your preferred LLM provider (LM Studio or Ollama)
4. Configure environment variables as needed
5. Run the main application

## Usage

```python
from main import main

# Run the application
main()
```

## Architecture

- `configuration.py`: Configuration management and settings
- `graph.py`: LangGraph state management and workflow definition
- `lmstudio.py`: LM Studio integration and API handling
- `utils.py`: Search utilities and helper functions
- `prompts.py`: Prompt templates and instructions
- `main.py`: Main application entry point

## License

This project is open source. Please check the license file for details.
